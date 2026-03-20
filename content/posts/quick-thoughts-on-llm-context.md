---
title: "Quick Thoughts on Context Windows"
date: 2026-03-16T10:00:00-04:00
draft: false
categories: ["Notes"]
tags: ["LLMs", "Thoughts"]
---

> "In the age of infinite context, retrieval is still king."

Even as LLM context windows get larger, efficient RAG is still necessary. Dumping the whole codebase into a prompt technically works, but it is slow and degrades the model's focus. Feeding it exact snippets is much better.
