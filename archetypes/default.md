---
title: {{ replace .File.ContentBaseName "-" " " | title }}
summary:
published: {{ .Date | time.Format "2006-01-02" }}
modified:
draft: true
tags: []
images: []
---
