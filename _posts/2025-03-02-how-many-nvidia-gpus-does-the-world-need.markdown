---
layout: post
title: "2025-03-02: How Many NVIDIA GPUs Does the World Still Need?"
date: 2025-03-02
categories: post
tags: business
is_series: true
series_title: "AI & Natural Language Processing"
image: "/assets/images/2025-03-02-gpu-city.jpg"
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

I use NVIDIA GPUs directly and indirectly in my everyday work as an AI software developer and NLP Ph.D. student. Also, I hold a meager amount of NVIDIA stock.

Naturally, I wonder: How long will NVIDIA be able to keep prices high, and continue to sell so many GPUs each year?

My main thought about NVIDIA currently is that the market may get saturated with GPUs. Big Tech companies such as Meta (Llama), X/xAI (Grok), Tesla (self driving cars and autonomous robots), Google (Google Cloud), Amazon (AWS Cloud) Microsoft (Azure Cloud), ByteDance, and Tencent have spent billions on NVIDIA GPUs already. Based on the recently published Q4 2024 report, NVIDIA realized USD 62bn in revenue in 2024, and expects USD 130bn in 2025. These are sizable expenditures even for NVIDIA's main buyers. 

As GPUs are durable and expensive, do we maybe already have enough of them and can scale production down?

## TL:DR;

Probably not. It appears that we are still early.

**There is a 10x inference gap between our demand (60tn daily usable tokens) and existing effective GPU supply (6tn daily usable tokens).**

Across the world, we need 60tn daily inference tokens in the near-term future (1--2 years). We can only realistically produce 6tn daily inference tokens per day with the entire existing GPU stock.

Taking NVIDIA's current GPU architecture Blackwell, we would need to add 12 million GPUs to our world-wide GPU stock to satisfy demand.

12 million Blackwell GPUs correspond to USD 23bn in revenue for NVIDIA. This is 2 years of NVIDIA revenues (at 2025 expected levels). The runway would be until the end of 2026. In 2026, new large-scale use cases would have to be exploited to keep pushing AI inference demand.

Caveat: Many assumptions were simplified. No significant growth in AI use cases was assumed in this calculations. I would overall argue that my assumptions are conservative.

Here is the back-of-the-envelope calculation:
[https://docs.google.com/spreadsheets/d/1SkJ14IIECiMzNvivGMS4zPPOw96PN_OMUlJ90fqSQzg/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1SkJ14IIECiMzNvivGMS4zPPOw96PN_OMUlJ90fqSQzg/edit?usp=sharing).

![Everything that happens in our cities will be in some way controlled by GPUs.]({{ page.image }})
<sup>Everything that happens in our cities will be in some way controlled by GPUs.</sup>

## The Assumptions: Future GPU Demand (Hard), Existing GPU Supply (Easy)

### Some Relaxed Assumptions for Estimating GPU Demand:

The NVIDIA GPU architectures that are still remotely usable and relevant for AI workloads are: Hopper (2022), Ada Lovelace (2022), and Blackwell (2024). Prior architectures were neglected -- Volta (2017), Turing (2018), Ampere (2020).

I assume that there 4bn people in the world that can afford to use AI in their daily lives.

The largest possible Claude output for a single request is around 4'000 tokens. Let us assume that each human that can afford inference does 2.5 large requests per day, or 10 small ones with 1'000 tokens each. This would result in 10'000 inference tokens per day per person.

10'000 x 4bn = 40'000'000'000'000. 40tn tokens of demand per day! 

> Important note: This 40tn daily token demand is ad-hoc demand. It cannot be scheduled. People want immediate answers.

5'000 extra tokens per person: Some corporations, governments and militaries also need GPUs. I assume that they spend about 5'000 tokens per person.

**This brings us to 40tn + 20tn tokens per day. The entire world needs 60tn daily inference tokens.**

### And Here are Some Equally Simplified Assumptions for Estimating GPU Supply:

Llama-3.1 70B with 8-bit quantization is somewhat usable for most daily use cases. We thus use this model when calculating how many tokens a GPU can produce per second.

A Hooper GPU can produce about 100 tokens per second. An Ada Lovelace 10 tokens per second. A Blackwell 200 tokens per second.

There exist about:
* 1,000,000 Hoppers GPUs
* 5,000,000 Ada Lovelace GPUs
* 500,000 Blackwell GPUs

Let us assume that only 90% of the GPUs can be utilized for inference. There will be downtime for maintenance and for other reasons.

Let us also assume that we need to have a lot of average GPU capacity slack to deal with peak demand. Let us assume that the total daily token demand must not exceed 30% of installed GPU capacity to deal with demand fluctuations. When I refer to the daily token demand, I refer to **usable token demand**, not the installed theoretical token throughput at 100% 24h full-throttle GPU inference.

> For all other assumptions and calculations, please review the small Google Sheet. Please provide feedback if any assumptions are way off or you would like to do some calculations differently: [https://docs.google.com/spreadsheets/d/1SkJ14IIECiMzNvivGMS4zPPOw96PN_OMUlJ90fqSQzg/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1SkJ14IIECiMzNvivGMS4zPPOw96PN_OMUlJ90fqSQzg/edit?usp=sharing)

## Results

We have 6.5 million AI-viable GPUs installed world-wide, but we need about 67 million. So we need to scale our GPU stock by 10x, given the performance of past GPUs. But the new Blackwell GPUs are much faster than the Ada Lovelace and Hopper GPUs, so we only need **12 million more Blackwell GPUs** to scale to 60tn usable tokens per day.

Given a price of USD 20'000 per Blackwell GPU, this would mean that NVIDIA can expect more than USD 230bn in revenue from the current demand gap.

This number matches with [USD 325bn of self-reported expected overall 2025 CapEx](https://finance.yahoo.com/news/big-tech-set-to-invest-325-billion-this-year-as-hefty-ai-bills-come-under-scrutiny-182329236.html) of Meta, Microsoft, Amazon, and Alphabet. This number includes non-NVIDIA expenditures.

USD 230bn in *GPU gap demand* is a less than 2x of NVIDIA's expected 2025 revenue. 

It is now early 2025, thus NVIDIA's revenue runway with the immediate demand gap will last until the end of 2026. In 2026, new large-scale use cases would have to be exploited to keep pushing AI inference demand in 2027 and beyond.

## Caveats

All assumptions are very vague. 

One the one hand, I assumed that we need 15'000 tokens per person on average. Naturally, this is more than we currently consume, as we do not even have the global capacity to serve 15'000 daily inference tokens to 4bn people. But on the other hand, this does not factor in use cases such as 24/7 AI logging of our daily lives (automated journaling), self-driving cars, massive automation in agriculture, administration, and manufacturing, and hundreds of other realistic near-term use cases. One could easily argue that we need 100'000 tokens per person in the very near future -- which would only correspond to a bit more than one token per second throughout a 24h day.

Also, I simplify the calculation by only using tokens as a unit of demand and supply bridge. There are also AI uses that are not measured in tokens.

We cannot be sure how far software and hardware improvements will bring us. Maybe the assumption of needing a Llama-3.1 70B 8-bit model is too aggressive -- and we can do with smaller models. On the contrary, we may want even larger models. 

Furthermore, competitors may enter the field and direct demand away from NVIDIA. Apple, Google, and Groq are all producing alternative AI inference chips. While NVIDIA likely remains king in AI training, other providers may be commercially more attractive for the inference market.

Check the [Google Sheet](https://docs.google.com/spreadsheets/d/1SkJ14IIECiMzNvivGMS4zPPOw96PN_OMUlJ90fqSQzg/edit?usp=sharing) and you will likely find many other assumptions that one can rightly criticize. If any calculations are too far off, please let me know via email or as a comment in the Google Sheet. I hope, and am somewhat confident, that the broader message still remains valid.

## Closing Thoughts

Will there ever be a limit to our appetite for intelligence? I think not. 

Either competitors will eat NVIDIA's lunch, or NVIDIA will continue to keep its high-margin business. However, GPU demand is not nearly satisfied with the existing GPU stock. 

## Contact

Contact me on X at [@janspoerer](https://x.com/JanSpoerer) or text me at jan.spoerer@whu.edu if you want to discuss your thoughts about the topic.