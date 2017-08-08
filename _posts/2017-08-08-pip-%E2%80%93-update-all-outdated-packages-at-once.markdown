---
layout: post
title: "pip – update all outdated packages at once"
date: "2017-08-08 13:02:53 +0200"
---
A quick one: Ever wanted to update all your outdated pip packages and wondered why there isn't an easy solution built in? Well, try this in your shell:
`pip list -o | cut -d " " -f 1 | tail -n +3 | xargs pip install -U` (thx _Jermic_)

Works on mac and at least with my Python 3.6.
