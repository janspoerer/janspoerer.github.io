---
layout: post
title: "2025-03-28: Can Claude Desktop Access WSL Files on Windows 10 While Retaining Access to the Windows File System? Yes!"
date: 2025-03-28
categories: post
tags: business
is_series: true
series_title: "AI & Natural Language Processing"
image: "/assets/images/2025-03-28-windows-linux-files.png"

# https://shantoroy.com/jekyll/add-latex-math-to-jekyll-blog-minimal-mistakes/
---
<script type="text/javascript" async
    src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.6/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

<script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        extensions: ["tex2jax.js"],
        jax: ["input/TeX", "output/HTML-CSS"],
        tex2jax: {
        inlineMath: [ ['$','$'], ["\\(","\\)"] ],
        displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
        processEscapes: true
        },
        "HTML-CSS": { availableFonts: ["TeX"] }
    });
</script>

Today I scratched my head over whether Claude Desktop can access WSL files on Windows 10 while retaining access to the Windows file system. The answer is yes, and here is how you can do it.

## How NOT to Do It

My initial idea was to configure two MCPs for file access. One for the Windows file access and another one for the WSL file access. As far as I can tell, this does not work. This configuration below starts without problems, but MCP clients seem to be unable to differentiate between MCP server functions if the functions have the same names, even if they are provided by separate servers.

I have chatted back and forth with Claude regarding it, and tried to get Claude to specify which server to call the function `list_allowed_directories`, but Claude kept calling the function from the `filesystem_windows` server, and claimed that it is unable to differentiate.

So this one was a failed attempt:

```
{
    "mcpServers": {
        "filesystem_windows": {
            "command": "npx",
            "args": [
                "-y",
                "@modelcontextprotocol/server-filesystem",
                "C:\\Users\\j.spoerer\\Desktop",
                "C:\\Users\\j.spoerer\\Downloads"
            ]
        },
        "filesystem_wsl_linux": {
            "command": "wsl.exe",
            "args": [
                "npx",
                "-y",
                "@modelcontextprotocol/server-filesystem",
                "\\\\wsl$\\Ubuntu\\home\\janspoerer\\code\\all_repos"
            ]
        }
    }
}
```

## What Does Work:

What does work is simply starting a single `filesystem` server that primarily runs on Windows, but has access to WSL through a nasty wsl path:

```
{
    "mcpServers": {
        "filesystem": {
            "command": "npx",
            "args": [
                "-y",
                "@modelcontextprotocol/server-filesystem",
                "C:\\Users\\j.spoerer\\Desktop",
                "C:\\Users\\j.spoerer\\Downloads",
                "\\\\wsl$\\Ubuntu\\home\\janspoerer\\code\\all_repos"
            ]
        }
    }
}
```

In this config, the functionality of the original configuration retained, while allowing the MCP client (Claude Desktop) to actually access the WSL paths.

Please make sure the install node on **Windows** (NOT on WSL) to use this MCP server. For further setup instructions for the `server-filesystem` MCP server, check out the [Model Context Protocol quickstart](https://modelcontextprotocol.io/quickstart/user).

If you generally struggle to get WSL MCP servers running on your machine, check my [post about it]({% post_url 2025-03-27-claude-desktop-python-mcps-with-windows-10-wsl %}).

## Contact

Contact me on X at [@janspoerer](https://x.com/JanSpoerer) or email me at jan.spoerer@whu.edu if you want to discuss your thoughts about the future of agentic AI and OS integrations.
