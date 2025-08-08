---
layout: post
title: "2025-07-29: The Entire World Currently Only Consumes 8 Trillion Daily LLM Inference Tokens"
date: 2025-07-29
categories: post
tags: business
is_series: true
series_title: "AI & Natural Language Processing"
image: "/assets/images/2025-07-29-the-world-only-consumes-8tn-llm-tokens-daily.png"

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


The number of inference tokens produced per day still seems to be almost laughably low today. I asked Google Gemini to research about today's inference situation, and got a reality check of how early we still are in the adoption of AI by consumers and businesses.

## How Many Tokens Do We Consume Per Day?

According to my quick Google Gemini Deep Research, the world consumes between 5-8 trillion LLM inference tokens per day. At a output token price of $2 (which is the output token price per 1m tokens of GPT-4.1), this translates to only $16m in output token revenue per day for all inference providers combined.

This already includes self-hosted token production!

As input tokens are also charged, and as these typically make up about 2x of the output token cost, the total inference revenue would be $16m for output and $32m for input tokens, totaling a meagre **$48m in *global* daily inference revenue** per day.




Let's assume one chat request leads to 1000 generated tokens. I probably use LLMs 20 times per day. That would result in 20'000 tokens per day for me as a heavy user. Then in my professional and academic life as an AI engineer and AI researcher, I probably spend and average of 10 million output tokens.





 [NVIDIA GPU demand]({% post_url 2025-03-02-how-many-nvidia-gpus-does-the-world-need %}).

## Contact

Contact me on X at [@janspoerer](https://x.com/JanSpoerer) or email me at jan.spoerer@whu.edu if you want to discuss your thoughts about the future of agentic AI and OS integrations.
