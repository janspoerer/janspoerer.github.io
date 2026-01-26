---
layout: post
title: "Living on Dividends - A Simple Portfolio Tracker for Dividend Investors"
date: 2026-01-01
categories: post
tags: finance investing dividends
is_series: false
imageHeader: "/assets/images/2026-01-01-living-on-dividends-portfolio-tracker-header.png"
imageSplit: "/assets/images/2026-01-01-living-on-dividends-portfolio-tracker-split.png"
---

I made a tool that you can use to align your investment portfolio to your monthly expenses. It shows how close you are to covering your monthly expenses with dividends. Dividends and expenses are grouped and matched by expense type, creating an intuitive diversification effect.

**Try it here:** [Living on Dividends Portfolio Tracker](https://consumer-portfolio.spoerico.com/)


![Header of the portoflio tracker.]({{ page.imageHeader }})

## What Is It?

The application lets you enter your total monthly expenses and the applicable capital gains tax rate in your jurisdiction. 

It splits the monthly total into different expense buckets using fixed ratios for each expense bucket.

![Progress per basket category.]({{ page.imageSplit }})


## Features

- Enter the portfolio position sizes of your current portfolio per stock.
- See how far along you are in total and per expense basket.
- Get motivated by seeing how close to 100% you aleady are in certain baskets.

## Why I Built This

I built this because I am trying out how fast I can set up some simple applications using Claude Code. This is just one of many small toy projects that I felt inspired to build with it.

## Tech Stack

This application is built in React and uses a Hetzner server along with a subdomain for hosting. The server exposes the static files via Ngnix.

## Try It Out

The tracker is free to use at [consumer-portfolio.spoerico.com](https://consumer-portfolio.spoerico.com/).

No account needed.

The application is hopefully self-explanatory. Otherwise, please contact me!

## Contact

Contact me on X at [@janspoerer](https://x.com/JanSpoerer) or email me at jan.spoerer@whu.edu if you have feedback or feature requests.
