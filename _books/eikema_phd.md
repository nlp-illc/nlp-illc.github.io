---
layout: book-review
title: A sampling-based exploration of neural text generation models 
author: Bryan Eikema
cover: /assets/img/book_covers/eikema-phd.jpg
#olid: OL43499941M # use Open Library ID to fetch cover (if no `cover` is provided)
isbn: 9789465360126 # use ISBN to fetch cover (if no `olid` is provided, dashes are optional)
categories: PhD 
tags: sampling decoding
buy_link: https://dare.uva.nl/id/9cd9d44e-f091-4135-9dc3-5e33f232d9d9
url: https://dare.uva.nl/id/9cd9d44e-f091-4135-9dc3-5e33f232d9d9
date: 2026-02-10
started: 
finished: 
released: 
stars: 
goodreads_review: 
#status: 
---
Neural text generation models form the foundation of modern natural language processing systems. Despite major advances in neural network architectures and training paradigms, their underlying probabilistic formulation has remained unchanged.
In practice, however, this probabilistic nature is often largely ignored at inference time. For many generation tasks, deterministic decoding algorithms are used to extract a single highest-probability sequence from the model. This implicitly assumes that the modes of the model distribution correspond to fluent, data-like text, an assumption that is frequently violated in practice. Across many text generation tasks, the most probable sequences produced by neural text generation models are often too short, repetitive, or otherwise unnatural.
A principled understanding of the full sequence distributions predicted by neural models is therefore crucial for informed decoding decisions. Sampling provides a natural tool for exploring these distributions: by analysing generated samples, we gain insight into the structure, biases, and pathologies of the underlying model distribution. Beyond analysis, samples can also serve as inputs to decoding algorithms or as final outputs in their own right.
In this dissertation, we explore sampling-based approaches to both analyse neural text generation models and improve decoding strategies. We reinterpret well-known generation pathologies through the lens of probabilistic exploration and provide a new perspective on potential underlying causes. Building on these insights, we propose and iteratively refine a sampling-based decoding algorithm inspired by risk minimisation principles, and introduce novel sampling methods for distributions that do not admit an autoregressive, per-token factorisation.
