---
title: "A deep dive on ZCO"
description: "A deep dive into the preparation for the ZCO"
date: 2025-05-05
draft: true
---
### Author: Samik Goyal
---

This is the second part in a 3-part series:

- _[Indian Computing Olympiad: India's IOI Selection Process](/posts/ico-starter/)_
- _[A deep dive on ZCO](/posts/zco-deepdive/)_
- _[A deep dive on INOI]() (Coming Soon)_

_This part goes in depth about preparation for the ZCO._

---

This article has pretty much everything I know and have learned about ZCO.

## All about the contest

ZCO is a 3 hour, 2 problem contest. Both of the problems are 100 marks each and have different subtasks.

## Contest Analysis

Looking at the previous year's cutoffs, it is easy to see that clearing ZCO just requires basic CP knowledge. Usually just scoring the subtasks which require brute-force are enough to qualify.

## Common mistakes

1) Going for ACs: You should not go for ACs as it almost never will be required to qualify. However, ACing ZCO problems might still be slightly difficult.

2) Not knowing debugging: This is common to all stages but I am mentioning it here. If you do not know how to compile manually or debug your code, you might get some weird bug in your code. There are some people I know that could not clear ZCO just cause they had a simple bug in their code that they could not debug.

## Preparation guide

Preparing for the ZCO is simply going to be learning CPP and learning the basics of CP. Let us cover these 2 separately.

### Learning CPP

This is a part which everyone will do differently. For me, personally, I prefer learning from videos. The channel I learnt CPP from is [The Cherno](https://www.youtube.com/@TheCherno). This youtuber goes into depth about each topic.

Some people might prefer learning in other languages. Some people also might not like the depth that the Cherno goes into. For the latter, however, I would say that avoiding depth is not benefitial in the long run. While not required, CPP knowledge can help find some weird bugs and sometimes speed up or shorten your code.

### Learning the basics of CP

In my opinion, the best way to learn CP is reading the Competitive Programmer's Handbook. This is a book written by Antti Laaksonen. It is completely free and available online.

The book covers a lot of standard algorithms in CP. Another thing to go along with it is the CSES Problem Set. Every topic in the book has a corresponding question in CSES. 

Now please bear in mind that the problems in CSES are _standard problems_. That is, they have standard solutions that have been discovered by other people. You are not expected to be able to solve these from scratch. It is expected that you have to learn the solution to every problem. 

Most OI problems usually work like this:

You find some reductions (simplifications) in the problem statement -> It reduces to a standard problem -> You code them up together

Other times they might be slightly modified versions of standard problems. For example, there are so many problems I can think of which use dijkastra's algorithm alone, with ratings ranging from IOITC level to ZCO level.

A lot of the times, one OI problem might reduce to several standard problems. For example, there are some problems where you need to use a dijkastra on top of a segment tree made inside a graph. (Here, dijkastra and segment trees are both standard algorithms)

