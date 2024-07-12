---
layout: post
title: "Automating the Sanity Checks for Your Academic Paper's Result Section"
date: 2024-07-12
categories: post
tags: private
is_series: true
series_title: "AI & Natural Language Processing"
image: "/assets/images/2024-07-12-Helsinki-Hotel-Midnight-Oil.jpg"
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

Today, I found a way to solve on of my biggest pains in academic writing.

In the last hours, I proofread a paper that was almost ready for hand in to a conference. When reading a printout, I marked about ten passages with "check" -- indicating that I had to check the empirical results against the results that are buried somewhere in the scripts for our experiments.

What a pain.

The thing is: I did this multiple times already. Some time in between, we made changes to the experiments, or my co-author re-arranged passages. So I wanted to be extra sure to check everything again and again each time a potential source of error was introduced.

**Let’s automate the results checking for numbers mentioned in text and tables in LaTeX papers!**

![Writing from a hotel in Helsinki this time.]({{ page.image }})
<sup>Writing from a hotel in Helsinki this time.</sup>

## What you have to do to build your little academic paper checker

The checker has the following main components:

1) A language model. This is component is, of course, the brain behind the whole checking. The other components are only there to feed the language model with the correct empirical results and with the text in the correct format. In July 2024, as I write these line, one of the best options is probably the Llama 3 model with 8bn parameters (in 4-bit quantization or with a higher quantization). Or you use an API for a language model (e.g., the OpenAI API).

2) The loader of the academic texts and tables. If you are an academic researcher, you likely write your articles in LaTeX. The good thing about LaTeX is that all input text and tables are usually written in, well, LaTeX text, -- which can very simply throw into the language model without an issue. The model will know what to do. Make sure to load and concatenate all the paper content that you want to check. 

3) The loader for the results. Ideally, you have one script that produces your paper's results. Maybe your results are a bit scattered around in your script. Take this moment as an opportunity to structure your script a bit, and to have it concatenate all of your results. For example, if you have four experiments with two metrics per experiment, the end result would be something like: 
```
Experiment 1, metric 1: 50%, metric 2: 20%; Experiment 2, metric 1: 30%, metric 2: 10%; Experiment 3, metric 1: 15%, metric 2: 15%; Experiment 1, metric 1: 90%, metric 2: 80%;
```

4) A prompt that glues the components 2) and 3) together. For example:
```
Please check if the following results fit to the text and tables that were created about the results. Please check all numbers carefully. If the text does not represent the results, this is an error. Please flag all differences for me. Also pay attention to the tables.

Results:
<Insert results from 3) here>

Text to be checked:
<Insert your paper sections from 2) here>
```

You can do the loading of your article fully automatically, or you can paste in the text manually, however you prefer! Reading `.tex` files in Python works as with any other text file:
```
with open('main.tex') as f:
    string_with_text = f.readlines()
```

## Some challenges

My paper only has about 8 pages, but already has about 15'000 tokens. This can exceed the context lengths of some models. You might want to only load in the result section of your paper be selective about what you load into the language model. Of course, you could also chunk the requests by dividing the article text into medium-size (max. 8'000 tokens) pieces.

## Closing remarks

The truth is, I’m much more motivated to automate these types of tasks than to do them myself. In theory, I should at least be 3x faster just doing the checks manually. But that’s not the case: The pure energy that I draw, as opposed to drain, by automating this mind-numbing activity, made the work seem like a breeze. And the code (as well as this article) were all written past midnight! I could have not gotten myself to doing a boring manual check that late at night. Implementing these checks took lees than 2h.*

Needless to say, Llama 3 is much more reliable than me in checking these numbers. Also, I can now check the numbers whenever I want, almost instantly. I can trust my paper much more than I could before I implemented these checks.

Wish me luck, I hope my paper gets accepted!

(*) If you do these checks locally, without the aid of an API such as the OpenAI GPT-4 API, the initial setup may take longer, if you have never done local inference before. — Downloading the model(s) might take hours, depending on your internet connection and on the load that the model source’s hosting servers currently face. Also, these language models do not run on any hardware, so you may need to invest in a new MacBook Pro with high RAM (at least 64GB) or an NVIDA GPU.

