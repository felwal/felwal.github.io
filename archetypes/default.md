---
title: {{ replace .File.ContentBaseName "-" " " | title }}
created: {{ .Date | time.Format "2006-01-02" }}
modified:
draft: true
summary:
---
