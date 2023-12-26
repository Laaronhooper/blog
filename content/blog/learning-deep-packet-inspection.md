+++
author = "Luke"
title = "My journey in learning DPI"
date = "2023-12-26"
description = "My journey in learning DPI"
draft = true
tags = [
    "DPI",
    "Deep Packet Inspection",
    "Network Profiling",
]
+++

## Intro to Wireshark (Duh-Dun)

Starting out my career at Canopus I had no clue what a "packet" was. I was fresh
out of a coding bootcamp and my web fundamentals were definitely somewhat
limited. There was no further deep I could've been thrown than starting my
journey with them.

On my very first day, I was instructed to download Wireshark. A tool I had never
used, let alone ever heard of. I very quickly found myself staring at a
gobbledygook of text and colours with no discernable way to unscramble what lay
before me. So I did what I thought was the only thing I could do without ensuing
death by a thousand questions on my colleagues. I googled. What does this frame
mean? How is the frame constructed? How is this hexadecimal value calculated?
And the questions went on. Eventually, I got myself to a point where I had a
pretty clear understanding of network architecture. And it was from here that
my DPI began.

## DP-why?

As a part of Canopus' network detection, some Deep Packet Inspection is used.
DPI is essentially the catch-all for looking through the packets of a particular
internet session. What I was able to do with these particular sessions, or flows
if you will, was find the most identifiable flow, and build out logic to catch
cases in which this identifiable flow presents itself.

This was a challenging task to begin with, especially based off where I'd come
from. But by the end of my tenure at Canopus, my understanding of nuance for
finding patterns, increments, dynamic and static constants was well established.
