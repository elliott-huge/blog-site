---
layout: post
title: Idea; LLM + Search engine for high-confidence answers
excerpt: ChatGPT, BingChat and Bard have all integrated web search to their LLMs, but it seems imperfectly implemented. That is, imperfect in terms of answer and search quality; the chosen method may suffice for majority of queries and may be cost-effective for each provider. I am admittedly clueless on the implementation details, mind...
---

# LLM + Search engine for high-confidence answers

`Hu`

ChatGPT, BingChat and Bard have all integrated web search to their LLMs, but it seems imperfectly implemented. That is, imperfect in terms of answer and search quality: the chosen method may suffice for majority of queries and may be cost-effective for each provider. I am admittedly clueless on the implementation details, mind...

This came about because ChatGPT 4 couldn't answer to my below query (this was chat only mode, it may admittedly have succeeded with Bing search enabled):

`EL: Word for observing river boaters especially at a lock`

`GPT4: As of my last training data in January 2022, there isn't a specific single word in the English language that exclusively describes the act of observing river boaters [...]`

*For those curious, the correct answer is '[Gongoozler](https://en.wikipedia.org/wiki/Gongoozler)'*

Anyway, here's the concept:
**An app, web-app, extension - whatever - for automatically performing a *rigorous* search for a query.**  
* User inputs a search, e.g. 'Word for [example activity]'
* LLM is first prompted to describe the nature of the search, in this case 'seeking a word to match a definition'
* LLM is prompted to list the most likely sites where such a term may be answered
  * [Wikipedia](https://www.wikipedia.org/)
  * [WordReference Forums](https://forum.wordreference.com/)
  * [Stack Exchange](https://english.stackexchange.com/)
  * [Merriam-Webster](https://www.merriam-webster.com/)
* LLM is prompted to list alternative search criteria that may plausibly answer the original query:
  * "Terminology for watching boats at a lock"
  * "Lock spectating word"
  * "Term for viewing river boats at lock"
  * "Lock canal boat observation term"
  * "Word for spectators at river locks"
* LLM makes calls for site-constrained searches N:M with the original and the alternative query:
  * "site:wikipedia.org Terminology for watching boats at a lock"
  * "site:wikipedia.org Lock spectating word"
  * "site:wikipedia.org Term for viewing river boats at lock"
  * [...]