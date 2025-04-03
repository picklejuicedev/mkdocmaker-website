+++
date = '2025-03-20T12:49:08Z'
draft = false
title = 'Using AI to review selected text or chapters'
+++

## The `//review` command

![Demo](/img/features/reviewmess.gif)


MkDoc Maker offers several ways to review and refine your chapter content, leveraging its AI-powered capabilities to improve clarity, grammar, and overall quality.

**Using MkDoc Maker to Review Content:**

1.  **Reviewing a Section:**

    *   You can ask MkDoc Maker to make a suggestion to improve a part of text. You can use 2 ways to trigger this feature:
        *   As with other commands you can use `//review` to review a whole chapter.
        *   Alternatively you can select a section and right-click to use Review from the context menu.
        *   Additional instructions can be added as notes, i.e. `// shorten this paragraph` or similar.

    Here is an example how you could use the review prompt:

    ```
    ai can review text. will fix typos and have better gramma. also can make examples. Just hightlight and rightclick. mkdoc maker will do the rest.
    ```

    Will change to:

    ```
    MkDoc Maker can help you review your text. It can fix typos, improve grammar, and even generate examples. To use this feature, simply highlight the text you want to review and right-click. MkDoc Maker will handle the rest.
    ```

2.  **Using the `//review` Prompt:**

    *   Place the `//review` prompt within the chapter you want to review. MkDoc Maker will analyze the entire chapter and provide suggestions for improvement.
    *   You can add notes to the prompt to guide the review process. For example, `//review Focus on improving the clarity of the introduction.`

3.  **Using the Context Menu:**

    *   Select the specific text you want to review.
    *   Right-click on the selected text and choose "MkDocMaker: Review Selected Text" from the context menu.
    *   MkDoc Maker will analyze the selected text and provide suggestions for improvement.

4.  **Accepting or Rejecting Suggestions:**

    *   After MkDoc Maker generates suggestions, you'll have the option to "Accept" or "Reject" each suggestion.
    *   Accepting a suggestion will automatically incorporate the changes into your document.
    *   Rejecting a suggestion will discard the changes.

**Example Workflow:**

1.  Write a draft of your chapter content.
2.  Use the `//review` prompt or the context menu to initiate the review process.
3.  Carefully review the suggestions provided by MkDoc Maker.
4.  Accept the suggestions that improve your content and reject the ones that don't.
5.  Make any additional manual edits as needed.

**Using review to change formatting and layout**

The review feature can be used to alter layout and formatting. Use a `// note` to describe the required changes and select the text block to review.

Here an example where a codeblock was pasted into the document and then reformatted:

![review formatting](/img/features/reviewreformat.gif)


**Tips for Effective Reviewing:**

*   **Be specific with your notes:** The more specific you are with your notes, the better MkDoc Maker can understand your goals and provide relevant suggestions.
*   **Focus on one aspect at a time:** Instead of trying to review everything at once, focus on one aspect of your content at a time, such as grammar, clarity, or style.
*   **Don't be afraid to reject suggestions:** MkDoc Maker is a tool to assist you, not replace you. If you don't agree with a suggestion, don't be afraid to reject it.
*   **Always proofread your final content:** Even after using MkDoc Maker, it's important to proofread your final content to catch any errors that may have been missed.

By following these steps, you can use MkDoc Maker to effectively review and refine your chapter content, ensuring that it is clear, concise, and error-free.


