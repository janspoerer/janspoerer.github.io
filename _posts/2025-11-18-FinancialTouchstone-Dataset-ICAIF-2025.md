---
layout: post
title: "FinancialTouchstone Dataset - ACM International Conference on AI in Finance (ICAIF) 2025 in Singapore"
date: 2025-11-18
categories: post
tags: finance ai dataset
is_series: false
---

> To the Dataset:
> https://drive.google.com/drive/folders/1RosV3-XQNPNt9DrEl3tMMZec4rtVo5ad?usp=sharing

# FinancialTouchstone Dataset - ACM International Conference on AI in Finance (ICAIF) 2025 in Singapore

## TL;DR

We compared all flagship LLMs from June 2025 to each other using this financial dataset. If you want to evaluate your financial RAG pipelines with an unbiased (unseen) and realistic benchmark, look no further, you can do it here as well. We provide more than 80 tokens from 480 real annual report along with 2800 question-golden contenxt-golden answer triplets for you to access for free.

## Purpose of the Dataset

The dataset contains the PDFs and text files for 480 annual reports, nicely structured with one folder per report. The file structure is:

```
|-labeled_data.xlsx
|-assets/
  |-report_1/
    |-1.pdf
    |-extracted_text.txt
  |-report_2/
    |-2.pdf
    |-extracted_text.txt
```

This allows you to get started with scalable annual report research without having to manually gather those manually reports from numerous websites like I did.

Also, the `labeled_data.xlsx` contains:
1) questions, 
2) the context where the questions were answered in the report, and 
3) the golden answer to the question.

Because we include the golden context, you will be able to evaluate your RAG pipelines not only in terms of accuracy, but also its hallucination rate. 