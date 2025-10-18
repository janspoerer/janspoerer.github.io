---
layout: post
title: "2025-03-27: How to Configure Python MCPs on Claude Desktop on Windows 10 WSL (and WSL2)"
date: 2025-03-27
categories: post
tags: business
is_series: true
series_title: "AI & Natural Language Processing"
image: "/assets/images/2025-03-27-mcp_claude_desktop_windows_10_wsl.png"
image2: "/assets/images/2025-03-27-claude-error-no-wsl-server.png"
imageClaudeDesktopMcPHammer: "/assets/images/2025-03-27-claude-desktop-hammer-mcp.png"
imageSuccess: "/assets/images/2025-03-27-success.png"


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

In this short technical MCP setup tutorial, you find instructions for configuring Python MCPs on Claude Desktop on Windows 10 WSL (and WSL2).

The goal is to allow your Claude Desktop client to access locally running MCP servers on your WSL, even if you are running Claude Desktop as a native Windows application. Claude Desktop is *not* available on Linux, meaning that it also is not available in WSL. So we have to tunnel from Windows to WSL to access the Python MCP servers running on WSL.

## First, the Claude MCP Configuration File

Open your Windows File Explorer and navigate to this folder:

```
C:\Users\insert-your-user-name-here\AppData\Roaming\Claude
```

You find two interesting bits here:

* the `logs/` folder, where Claude Desktop MCP logs are stored, and
* the `claude_desktop_config.json` file, where you can specify which MCP servers to use with Claude Desktop.

First, it might be a good idea to open the files in `logs/` to get a sense for what Claude Desktop is logging when trying to open an MCP server. If you have already struggled a bit with getting MCPs to run, these logs will not be empty. There is an aggregated `logs/mcp.log` file that contains logs for all MCPs, and there is a separate log file for each MCP server. You can savely delete all of the files inside the `logs/` folder. I often find it useful to purge the `logs/` folder as the logs fill up quickly.

Second, you can configure an MCP. Remember the following rules for configuring an MCP with Claude Desktop on Windows:

1) The first level of the JSON configuration will be `mcpServers`, no matter what.
2) Then comes a dictionary/map of MCP servers, and you can give them arbitrary names, as long as they do not repeat. I named my MCP "selenium."
3) The third level contains the keys `command` and `args`. `command` will always be `wsl.exe`. `args` is a list and will always be the Python executable as a first argument and the path to the MCP executable as a second argument. If you can pass arguments to the Python MCP, you can pass them as third, fourth, and so on arguments.

Here is how the configuration is passed to Linux. Linux sees the configuration like so in its shell:
```
/home/insert-your-user-name-here/code/mcp_browser_use/.venv/bin/python /home/insert-your-user-name-here/code/mcp_browser_use/mcp_browser_use
```

![As most people, I fell in love with ChatGPT's Ghibli image generation. But it refused to put a Claude logo in for me, so here you have a makeshift Ghibli Claude user.]({{ page.image }})
<sup>As most people, I fell in love with ChatGPT's Ghibli image generation. But it refused to put a Claude logo in for me, so here you have a makeshift Ghibli Claude user.</sup>

**Note how this is  a plain and simple `python main.py` call, but in our MCP case with the full path to the Python executable and the Python script.** You could also use `python` or `python3` as a Python executable, but one will usually not just want to use that global Python installation.

Long story short, here is the entire JSON config to copy-paste into `claude_desktop_config.json`:

```
{
    "mcpServers": {
        "selenium": {
            "command": "wsl.exe",
            "args": [
                "/home/insert-your-user-name-here/code/mcp-minimal/.venv/bin/python",
                "/home/insert-your-user-name-here/code/mcp-minimal/mcp-minimal"
            ]
        }
    }
}
```

(The full path to the file is: `C:\Users\insert-your-user-name-here\AppData\Roaming\Claude\claude_desktop_config.json`.)

## Second, the Actual MCP Server

So this configuration probably points into nothingness now on your computer. Please go to your Task Manager, kill all running Claude processes, and restart Claude.

After Claude has restarted, you should see this error message on the top right:

<div style="text-align: center; margin: 20px 0;">
  <img src="{{ page.image2 }}" alt="Claude Desktop error message" style="max-width: 80%; height: auto;">
  <p><sup>Do not despair if you see this error in Claude Desktop. You are on the right track.</sup></p>
</div>


Now, we make a very minimal MCP server in Python on our WSL. If you have little time, clone the MCP server from here [https://github.com/janspoerer/mcp-minimal#][https://github.com/janspoerer/mcp-minimal#]:

```
git clone git@github.com:janspoerer/mcp-minimal.git
```

Make sure to install the `fastmcp` Python library either globally or in the repository's `.venv` (or `venv`) file. For example, do the following (you might have to replace `python` with `python3`):

```
cd /home/insert-your-user-name-here/code/mcp-minimal
python -m venv .venv
source .venv/bin/activate
pip install fastmcp
```

I hope nothing fails. If something does fail, copy-paste the content of this blog post into your favorite language model along with your error. It will probably be easy to resolve.

## Verify the MCP Server and the Config

If you restart Claude Desktop on Windows 10 (do not forget to use the Task Manager so that the config JSON reloads), you will hopefully see a number in the bottom-right corner of the Claude chat window. This number shows you how many functions Claude has at its disposal. If you add another function to the MCP, this number will go up to two. Likewise, if you add a server, the hammer number will reflect the sum of all available functions across all available MCP servers.

<div style="text-align: center; margin: 20px 0;">
  <img src="{{ page.imageClaudeDesktopMcPHammer }}" alt="Claude Desktop MCP hammer indicator" style="max-width: 80%; height: auto;">
  <p><sup>The Claude Desktop Client detected one function. If you add more servers or more functions, this number will go up.</sup></p>
</div>

Now, ask Claude for something that it does not know without querying the MCP. In our case, ask about the current datetime. I hope that by now, the setup will be correct, and Claude will be able to infer from the MCP function's docstring that the function is indeed the right tool for the job. If so, you will see a permission prompt asking you to give Claude the permission to use the tool.

<div style="text-align: center; margin: 20px 0;">
  <img src="{{ page.imageSuccess }}" alt="Claude permission prompt" style="max-width: 80%; height: auto;">
  <p><sup>Yay, Claude detected the correct tool to use (not that hard) and is asking you for permission.</sup></p>
</div>

## Conclusion

You are now ready to use Claude Desktop as your own AI agent. Add superpowers (MCPs) to it as you go. Have fun!

## Contact

Contact me on X at [@janspoerer](https://x.com/JanSpoerer) or email me at jan.spoerer@whu.edu if you want to discuss your thoughts about the future of agentic AI and OS integrations.
