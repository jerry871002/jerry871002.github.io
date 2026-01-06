---
date: '{{ .Date | time.Format "2006-01-02" }}'
draft: true
title: '{{ replace .File.ContentBaseName "-" " " | title }}'
summary: ''
toc: true
readTime: true
autonumber: true
tags: []
showTags: true
---