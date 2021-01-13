# canvas-demos
This repository features several demos of how to display, render, or execute code in Canvas pages.

Security settings in the Canvas pages HTML editor prevent inserting <script> tags. Using iFrames, however, provides a way to execute javascript in a Canvas page. This feature allows us to:
  - Display code stored on github with syntax highlighting
  - Execute or render code stored on github, stored in the Canvas files section, or stored elsewhere on the web
  
The following demos provide some minimus working examples of how to replicate this functionality. The code in these demos can be copied and pasted into a Canvas page via the HTML editor. Where specified, you'll also need to add files to your Canvas file repository.

## [Display Code with Syntax Highlighting](https://github.com/wbwatkinson/canvas-demos/blob/main/display-code.html)
Though Canvas provides the <pre> tag, code displayed with this tag does not have syntax highlighting. gist.github provides a js for every gist to display the gist code with line numbers and syntax highlighting. Though Canvas pages do not allow the use of <script> tags on a page, we use iFrames as a workaround in this example.
