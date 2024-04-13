---
title: {{ replace .File.ContentBaseName "-" " " | title }}
taken:
published: {{ .Date | time.Format "2006-01-02" }}
image: images/TODO.jpg
---
