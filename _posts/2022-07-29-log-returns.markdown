---
layout: post
title: "2022-07-29: Log Returns in Portfolio Management"
date: 2022-07-29
categories: post
tags: finance
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

# Log Returns in Financial Economics

Today, I added a note about the usage of log returns in finance to my [second brain](/secondbrain), and thought it might be interesting to some people. The most valuable videos on the topic are referenced below. I suggest watching all three videos as each gives a different angle to the subject.

A log return is calculated by dividing the current price of an asset by the past price of an asset and taking the natural logarithm: $ln(price_{t}/price_{t-1})$.

**We use log returns because** the product of normally-distributed variables is not normal. But the sum of normally-distributed variables follows a normal distribution. A product of simple gross returns will not be normally distributed! A time series of $1\%$ price increases would look like this when aggregated, but the returns will not be normally distributed: $1.01 * 1.01 * 1.01 ...$

Have you ever wondered why, when a portfolio loses $-20\%$ and then gains $20\%$, we do not end up at the value we left off? Log returns solve this issue! **What is also nice is that** log returns are time-additive (time-consistent). But they are not portfolio-additive. See also this video:

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/PtoUlt3V0CI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

When you add log returns, you will have to $exp()$ the result to get the percentage return. See also this video, starting at about 7:30min:

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/47h5VsGahfc?start=448" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

The following video is the most comprehensive one with 25min length. As you can see in this video after 4:30min, the geometric average is another concept related to log returns:

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/sR5foYbymaE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

After studying these videos, I became a bit of a fan of log returns. I hope they make your life easier as well.