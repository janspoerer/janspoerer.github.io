---
layout: post
title: "2025-03-17: A Vision for Natural Language-Driven Operating Systems for More Efficient AI Agents"
date: 2025-03-17
categories: post
tags: business
is_series: true
series_title: "AI & Natural Language Processing"
image: "/assets/images/2025-03-17-mcp_browser_use_logo.jpg"
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

On the frontier of AI, we see the proliferation of AI agents. I argue that to let AI agents come to their full potential, natural language interfaces deep into operating systems will greatly improve the speed of agentic advancement.

To understand why, we have to take a step back into the ancient past when ChatGPT was released.

## But First, What Happened Since ChatGPT Was Released?

### 2022: The Year of ChatGPT

ChatGPT was released in November 2022. The chat assistant achieved explosive overnight success as measured by active users.

### 2023: The Competition Catches Up, Prices Go Down

In 2023, other tech companies followed and released their own models. Microsoft started integrating OpenAI's models into their products, Anthropic came out with Claude as a formidable ChatGPT competitor, and Y Combinator seemed to almost exclusively fund AI startups. 2023 was the year of chatbots and "LLM wrappers"

### 2024: The Grassroots of Agentic AI

In 2024, AI agents became more widespread. AI agents can perform tasks on their own, and are not mere assistants that output text. Increasingly, open-source and closed-source software for computer and browser use was created, allowing AI agents to interact with operating systems and browsers. Not many people noticed it yet, but agentic AI was brewing in the background and waiting for a breakthrough.

### 2025: The Year of Agent Proliferation and Self-Reinforcing Improvements

Now, in 2025, agent proliferation is visible everywhere. Anthropic's Model Context Protocol (MCP), released already in November 2024, but noticed by few, allows AI agents to use tools in a standardized format. And the latest LLMs are now able to help developers to create AI agents, as their knowledge cutoff is no longer limited to the time before agentic AI became widespread.

Let me elaborate on what I mean: In 2024, AI agent software was in even more flux than it is today. Standards were evolving and breaking rapidly. They are still annoyingly unstable today, but are significantly better than a year ago. Thus, it is today much easier to develop AI agents than some months ago.

To be even more concrete, let's take the development of browser automation MCPs. I today started working on browser automation using MCP. The MCP controls a Selenium Chrome browser via Claude as an agent. I open the Claude app and tell Claude which actions to perform in the browser. When Claude encounters any errors in my MCP code, I paste the MCP code into the same Claude chat window, and Claude introspects the code and fixes it. You can imagine how powerful this closed-loop workflow is.

**This is what exponential development feels like -- the better AI agents get, the faster developers can develop, making AI agents even better.**

## What the Future of Agentic AI Holds

While any web scraping task seems to be almost trivial with agentic AI today, it is still a challenge to completely automate arbitrary computer workflows with AI agents. There are a few approaches such as Anthropic's Computer Use feature, but open-source software is still in its infancy.

By late 2025 and into 2026, I expect better standards for OS integrations of AI agents, allowing agents to use operating systems such as Windows, MacOS, Ubuntu (Linux), Android, and iOS. Today's automation tools are superficial, -- often reliant on coarse and inefficient screenshot-to-mouse-movement coordination. These tools require many LLM and computer vision model invocations to move the mouse, send keystrokes, and parse the current stat e of the screen. They are often either very slow or expensive.

Direct OS integrations will be much more efficient, faster, and more reliable. We will see natural language integrations directly in operating systems. Similar to how we use tool calling and MCPs today, we could document OS functionalities in a standardized format. In today's tool calling, AI models use docstrings and function signatures to make sense of the tools at their disposal. Likewise, operating systems will present their functionalities in a standardized MCP-like format to AI agents and allow them to call these functionalities directly without unnecessary human-like interaction through mouse movements and keyboard inputs.

## Contact

Contact me on X at [@janspoerer](https://x.com/JanSpoerer) or email me at jan.spoerer@whu.edu if you want to discuss your thoughts about the future of agentic AI and OS integrations.