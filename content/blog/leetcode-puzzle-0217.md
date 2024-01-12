---
title: "Leetcode puzzle 217 - Contains Duplicate"
date: "2024-01-12"
description: "Given an integer array nums, return true if any value appears at least twice in the array, and return false if every element is distinct."
tags: [
    "Easy",
    "Arrays",
    "Hashing",
]
---

# Contains Duplicate
This is my first attempt, which was fast, but not in the 
<!-- markdownlint-disable MD033 -->
<pre class="line-numbers language-javascript" data-start="1">
  <code>
 var containsDuplicate = function(nums) {
    if (nums.length <= 1) {
        return false
    }
    sorted = nums.sort((a,b) => a - b)

    dupe = sorted[0]
    for (let i = 1; i < sorted.length; i++) {
        if (sorted[i] > dupe){
            dupe = sorted[i]
        } else {
            return true
        }
    }
    return false
};
  </code>
</pre>
<!-- markdownlint-disable MD033 -->

And this was the fastest:

<!-- markdownlint-disable MD033 -->
<pre class="line-numbers language-javascript" data-start="1">
  <code>
    var containsDuplicate = function(nums) {
        for(let i =0; i < nums.length; i++){
            for(let j = i + 1; j<nums.length; j++){
                if(nums[j] === nums[i]){
                    return true
                }  
            }
        }
        return false;
    };
  </code>
</pre>
<!-- markdownlint-disable MD033 -->
