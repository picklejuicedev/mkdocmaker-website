+++
date = '2025-03-20T12:49:08Z'
draft = false
title = 'summarise'
+++

# Auto-Summary

Let's say you want to add an overview or summary to a document. You can use the `//sum` or `//summary` prompt. It will use any selected text so you can control what part of the document you want to summaries. If no text is selected it will use the current chapter where the command is located and include all sub-chapters.

Here and example:

**Input:**

```markdown
# Welcome to MkDoc Maker

 //summary

## Installing the Extension

```

**Output:**

```markdown
# Welcome to MkDoc Maker

 //ignore

MkDoc Maker is a powerful extension for Visual Studio Code that helps you create high-quality documentation from Markdown files. It provides a range of features to streamline your documentation workflow, including prompts for generating different types of content, a review system for improving your writing, and shortcuts for common tasks. 
```

In this instance, nothing was selected so it will use all sub-chapters which in this case is the whole document as "# Welcome to MkDoc Maker" is the root or top-level chapter.

