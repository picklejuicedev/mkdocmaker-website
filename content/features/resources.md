+++
date = '2025-03-20T12:49:08Z'
draft = false
title = 'Resources'
+++

# Using Resources

For many projects we have useful information embedded in code, pdfs, screen shots, manuals etc. All those files acan be used to generate our documentation by including those files when generating chapters.


![resources](/img/features/resources.gif)

MkDoc Maker automatically creates two folders next to your markdown document: `images` and `resources`. The `images` folder is for screenshots you want to include in your document. `resources` can contain subfolders with images or text files that are useful references for the AI, but are not shown to the reader.

In the example above, the `resources/install` folder contains images of how to install and register the MkDocMaker extension. This folder is then referenced with a `//use install/*.*` and used with the `//generate` command.

  ```markdown
 # MkDoc Maker

 ## Install and Register

  //use install/*.*
  //generate

  
  ```



## Using Glob Wildcards

At times you may include multiple files or images as resources. You can add multiple files as semicolon separated values, however you can also use wildcards.

This is an example syntax after moving the file `package.json.txt` into a folder called `commands` (note the "/" after the folder name):

  ```markdown

  ## Commands and Shortcuts

  //use commands/*.*
  // list all available commands, menue items and shortcuts, don't list internal command names such as mkdocmaker.review
  //generate

  ```

Here some more examples using wildcards:

- `//use myfolder/*.png` - will include all png images
- `//use **/*.png` - will include all folders and subfolders in the search for png images
- `//use *.{png,jgp}` - will include png and jpg images in the resources folder
- `//use a_folder/*.*; b_folder/*.*` - will include all files in a_folder and b_folder

You can also reference files outside the resource folder:
- `//use ../source/mylib/*.ts` - will include all files from the source folder inthe project root and then include all typescript files in the mylib folder
- `//use c:/code/myproject/README.md` - will include the README file from the absolute path


> NOTE:
> More files will increase the time and load on the Large Language Model and it may pick information that isn't directly relevant to your chapter. It is recommended to have fewer, but more relevant files. Maybe create more chapters if too much information is needed for a single query.

Glob wildcards are very versitile and powerful, for more detailed information, check out this [glob primer](https://github.com/isaacs/node-glob?tab=readme-ov-file#glob-primer).


### Supported file formats


We are continually adding more formats that can be used as resources. At the time of writing the following formats are supported:

| Format                    | Example     | Description                                                  |
| ------------------------- | ----------- | ------------------------------------------------------------ |
| Text files (.txt)         | myFile.txt  | Can ingest any plain text file.  |
| Images (.png, .jpg, jpeg) | myImage.png | Images can be screengrabs or any other useful resource.      |
| Markdown (.md)            | myDoc.md    | A markdown file, i.e. technical documentation of some other technology. |
| PDF (.pdf)                | myDoc.pdf   | Any pdf file as resource or reference |
| Video (.mp4)              | myVideo.mp4 | Any mp4 video file as resource or reference |
| Audio (.m4a, .mp3)        | myAudio.m4a     | Any m4a or mp3 audio file as resource or reference | 

-----
  
Additionally, MkDoc Maker can process any file format that can be decoded as text, including but not limited to:

* HTML (.html, .htm)
* XML (.xml)
* JSON (.json)
* CSV (.csv)
* TSV (.tsv)
* YAML (.yaml, .yml)
* RTF (.rtf)
* Log files (.log)
* Configuration files (.ini, .cfg, .conf)
* Source code files (.c, .h, .cpp, .hpp, .java, .py, .js, .ts, .dart, .go, .rs, .php, .sh, .bash, .css, .sql, .lua, .rb, .swift, .kt, .pl, .asm, .vb, .dat, .inf, .lst, .dic, .text, .properties, .env)

> If you encounter a file format that is not supported, please submit a feature request.

