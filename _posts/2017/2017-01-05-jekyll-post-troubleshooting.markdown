---
layout: "post"
title: "Jekyll Post Troubleshooting"
date: "2017-01-05 09:29"
description: Simple Jekyll Troubleshooting Steps
share: true
tags: jekyll
---

## Why wont my new post show up???
* The post is not placed in the `_posts` directory.
* The post has incorrect title. Posts should be named `YEAR-MONTH-DAY-title.MARKUP`
* The post's date is in the future. You can make the post visible by setting future: true in `_config.yml` (documentation)
* The post has `published: false` in its front matter. Set it to true.
* The title contains a `:` character. Replace it with `&#58`.
