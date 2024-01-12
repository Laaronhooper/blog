---
title: "Leetcode puzzle 49 - Group Anagrams"
date: "2024-01-12"
description: "Given an array of strings strs, group the anagrams together. You can return the answer in any order. An Anagram is a word or phrase formed by rearranging the letters of a different word or phrase, typically using all the original letters exactly once."
tags: [
    "Easy",
    "Arrays",
    "Hashing",
]
---

# Group Anagram
This is my first attempt, which was fast, but not in the top 1%
<!-- markdownlint-disable MD033 -->
<pre class="line-numbers language-javascript" data-start="1">
  <code>
    var groupAnagrams = function (strs) {
        sorted = {}
        processed = []
        if (strs.length === 0) return [['']]
        if (strs.length === 1) return [[strs[0]]]
        for (let i = 0; i < strs.length; i++) {
            let key = strs[i].split('').sort().join('');
            if (sorted[key]) {
                sorted[key].push(strs[i]);
            } else {
                sorted[key] = [strs[i]];
            }
        }
        for (let val of Object.values(sorted)) {
            processed.push(val)
        }
        return processed
    };
  </code>
</pre>
<!-- markdownlint-disable MD033 -->

Something more elegant and also the fastest I found:

<!-- markdownlint-disable MD033 -->
<pre class="line-numbers language-javascript" data-start="1">
  <code>
    var groupAnagrams = function(strs) {
        let solutionMap = {}

        for(let str of strs){
            let s = str.split('').sort().join('')
            if(!solutionMap[s]) solutionMap[s] = []
            solutionMap[s].push(str)
        }
        return Object.values(solutionMap)

    };
  </code>
</pre>
<!-- markdownlint-disable MD033 -->
