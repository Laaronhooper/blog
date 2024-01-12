---
title: "Leetcode puzzle 242 - Valid Anagram"
date: "2024-01-12"
description: "Given an integer array nums, return true if any value appears at least twice in the array, and return false if every element is distinct."
tags: [
    "Easy",
    "Arrays",
    "Hashing",
]
---

# Valid Anagram
This is my first attempt, which was fast, but not in the top 1%
<!-- markdownlint-disable MD033 -->
<pre class="line-numbers language-javascript" data-start="1">
  <code>
    var isAnagram = function (s, t) {
        sN = s.split('').sort()
        tN = t.split('').sort()
        if (sN.length !== tN.length) return false
        for (let i = 0; i < sN.length; i++) {
            if (sN[i] !== tN[i]) return false
        }
        return true
    };
  </code>
</pre>
<!-- markdownlint-disable MD033 -->

Something more elegant I found:

<!-- markdownlint-disable MD033 -->
<pre class="line-numbers language-javascript" data-start="1">
  <code>
var isAnagram = function(s, t) {
    return s.split('').sort().join('') === t.split('').sort().join('');
};
  </code>
</pre>
<!-- markdownlint-disable MD033 -->

This is the fastest:

<!-- markdownlint-disable MD033 -->
<pre class="line-numbers language-javascript" data-start="1">
  <code>
    var isAnagram = function (s, t) {
        const isEqual = s.length === t.length
        if (!isEqual) return false

        return reorder(s) === reorder(t)
    };

    const reorder = (str) => {
        return str.split('').sort((a, b) => a.localeCompare(b)).join('')
    }
  </code>
</pre>
<!-- markdownlint-disable MD033 -->

And lastly the most readable and intuitive to me:

<!-- markdownlint-disable MD033 -->
<pre class="line-numbers language-javascript" data-start="1">
  <code>
    var isAnagram = function (s, t) {
        if (s.length !== t.length) return false
        return reorder(s) === reorder(t)
    };

    const reorder = (str) => {
        return str.split('').sort((a, b) => a.localeCompare(b)).join('')
    }
  </code>
</pre>
<!-- markdownlint-disable MD033 -->

