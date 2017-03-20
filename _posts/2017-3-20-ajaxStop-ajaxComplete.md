---
layout: post
categories: tech
tags: jquery ajax
title: "ajaxStop vs ajaxComplete"
---



Stupidest little fix today. I was updating some data via ajax, which on success ran another little bit of ajax. I had a loading spinner attached to the submit button that appeared on click and disappeared on ajaxComplete.

The second ajax call took longer to complete than the first, so the spinner flashed up for a millisecond then there was nothing whilst the second call completed. A quick googling determined the difference between ajaxComplete - which runs when the current ajax call completes - and ajaxStop - which runs when all ajax calls are complete.

Simple solution, but not something I’d come across before today.
