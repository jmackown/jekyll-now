---
layout: post
categories: tech
tags: [css, work, tech]
title: "CSS Adjacent Selector"
---

Today we found ourselves wanting to use part of a standard javascript library but hide the rest. Easy enough to add `display:none;` to the icon we want to remove but there was a sneaky `<br />` in there as well. 

So I discovered the CSS adjacent selector, which I have never used before. I was able to add

`.tableclass th a + br {
   display: none;
}`

to the css and solve the problem. 