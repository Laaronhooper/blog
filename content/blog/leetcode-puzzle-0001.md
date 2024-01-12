---
title: "Leetcode puzzle 1 - Two Sum"
date: "2024-01-12"
description: "Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target. You may assume that each input would have exactly one solution, and you may not use the same element twice. You can return the answer in any order."
tags: [
    "Easy",
    "Arrays",
    "Hashing",
]
---

# Two Sum
This is my first attempt, which was fast, but not in the top 1%
<!-- markdownlint-disable MD033 -->
<pre class="line-numbers language-javascript" data-start="1">
  <code>
    var twoSum = function(nums, target) {
        compliment = {}
        for (let i = 0; i < nums.length; i++){
            if (nums[i] in compliment) {
                return [compliment[nums[i]],i]
            }
            compliment[target - nums[i]] = i
        }
        return []
    }
  </code>
</pre>
<!-- markdownlint-disable MD033 -->

And this was the fastest:

<!-- markdownlint-disable MD033 -->
<pre class="line-numbers language-javascript" data-start="1">
  <code>
    var twoSum = function(nums, target) {
        let i = 0; do {
            let j = 0; do {
                if (j == i){
                    j++
                }
                if (nums[i] + nums[j] === target){
                    return [i , j]
                }
            } while (j++ < nums.length)
        }while (i++ < nums.length)  
    }
  </code>
</pre>
<!-- markdownlint-disable MD033 -->

But this one resonated with me most:

<!-- markdownlint-disable MD033 -->
<pre class="line-numbers language-javascript" data-start="1">
  <code>
    var twoSum = function(nums, target) {
        let i = 0; do {
            let j = 0; do {
                if (j == i){
                    j++
                }
                if (nums[i] + nums[j] === target){
                    return [i , j]
                }
            } while (j++ < nums.length)
        }while (i++ < nums.length)  
    }
  </code>
</pre>
<!-- markdownlint-disable MD033 -->

