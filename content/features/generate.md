+++
date = '2025-03-20T12:49:08Z'
draft = false
title = 'Generate'
+++

## Generate Chapter content

MkDoc Maker offers a variety of prompts to help you generate different types of content. The one that is used the most is the `generate` command (or its aliases `gen` or `generateChapter`). This command instructs MkDoc Maker to generate content for the current chapter based on the available context.

![Using Generate](/img/quickdemo.gif)

**Basic Usage:**

1.  **Place the `//generate` prompt:**  
Insert the `//generate` command (or `//gen` or `//generateChapter`) within the chapter where you want the content to be generated.  It's best to place it after any existing introductory text or headings within that chapter.

2.  **Provide Context (Optional):**  
Before the `//generate` command, you can provide context to guide the content generation. This can include:
    *   Chapter title: The title of the chapter provides a primary focus for the generated content.
    *   Existing text: Any text already written in the chapter will be considered.
    *   Notes: Add notes starting with `// ` (note the space!) to give directives or instructions to the AI model. For example: `// Limit the output to 100 lines and put in a table.`
    *   Images: Embed images using markdown syntax. MkDoc Maker will analyze the images and consider them in its response.
    *   Resources: Reference external files (text files, code snippets, etc.) using the `//use <filename>` command. These files will be used as additional context for content generation. You can use glob wildcards to include multiple files.

3.  **Run the Extension:**  Trigger the content generation process by pressing the "PLAY" button in the top right of your editor or using the shortcut **Ctrl+M, Ctrl+M**.

4.  **Review and Accept/Reject:**  MkDoc Maker will generate content and insert it into the document. Buttons will pop up for you to "Accept" or "Reject" the suggestion. Press "Accept" to keep the generated content or "Reject" to discard it.

5.  **Automatic Ignore:** If you accept the generated text, then the extension will automatically change the prompt to "//ignore" so it isn't accidentally run again.

**Example:**

```markdown
## My New Chapter

This chapter will discuss the benefits of using MkDoc Maker.

 //generate
```

In this example, MkDoc Maker will generate content for the "My New Chapter" section, potentially discussing the features, advantages, and use cases of the tool.

**Using Resources:**

```markdown
## Commands and Shortcuts

 //use package.json
 // list all available commands, menue items and shortcuts, don't list internal command names such as mkdocmaker.review
 //generate
```

This example uses the contents of the `package.json` file as context to generate a list of commands, menu items, and shortcuts, excluding internal command names.

**Important Considerations:**

*   **Context is Key:** The quality of the generated content depends heavily on the context you provide. The more information you give MkDoc Maker, the better it can understand your needs and generate relevant content.
*   **Review and Validate:** Always review and validate the generated content to ensure accuracy and alignment with your project's specific requirements. MkDoc Maker is a tool to assist you, not replace you.
*   **Glob Wildcards:** You can use glob wildcards to include multiple files as resources. For example, `//use myfolder/*.png` will include all PNG images in the `myfolder` directory.
*   **Supported File Formats:** MkDoc Maker supports a variety of file formats, including text files, images, Markdown files, PDFs, videos, and audio files.

