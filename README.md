# canvas-demos
This repository features several demos of how to display, render, or execute code in Canvas pages.

Security settings in the Canvas pages HTML editor prevent inserting <script> tags. Using iFrames, however, provides a way to execute javascript in a Canvas page. This feature allows us to:
  - Display code stored on github with syntax highlighting
  - Execute or render code stored on github, stored in the Canvas files section, or stored elsewhere on the web
  
The following demos provide some minimum working examples of how to replicate this functionality. The code in these demos can be copied and pasted into a Canvas page via the HTML editor. Where specified, you'll also need to add files to your Canvas file repository.

_Note: Files stored in Canvas must be accessed through the following URL construction._

`[course_root_url]/file_contents/course%20files/[file_path_in_canvas_files]`

For example, assuming you've saved a file at `test/my_example.html` in a course with a url of `https://lms.au.af.edu/courses/99999999/`, the URL of this file is:
`https://lms.au.af.edu/courses/99999999/file_contents/course%20files/test/my_example.html`

## Render HTML fragments with iFrame
Canvas provides the ability to embed iFrames in a Canvas page. This allows the creation of an interactive HTML file which can then be embedded with an iFrame. The HTML file can be stored in the Canvas file repository or elsewhere on the web. The only caveat is that the location from which the HTML file is being served must not prevent the file from being included as an iFrame (the easiest way to know what the hosting server has prevented the use of their content from being used an iFrame is to try). Here are three examples:
- [iFrame with simple js example stored in Canvas files](https://github.com/wbwatkinson/canvas-demos/blob/main/execute-arbitrary-code.html)
- [iFrame with more complex example stored in Canvas files](https://github.com/wbwatkinson/canvas-demos/blob/main/render-html-from-files.html)
- [iFrame source stored elsewhere](https://github.com/wbwatkinson/canvas-demos/blob/main/render-html-from-www.html)

## [Display Code with Syntax Highlighting](https://github.com/wbwatkinson/canvas-demos/blob/main/display-code.html)
Though Canvas provides the &lt;pre&gt; tag, code displayed with this tag does not have syntax highlighting. gist.github provides a js for every gist to display the gist code with line numbers and syntax highlighting. Though Canvas pages do not allow the use of &lt;script&gt; tags on a page, we use iFrames as a workaround in this example. Note that changes made to the gist are automatically reflected in Canvas.

## [Render/reuse code stored on github](https://github.com/wbwatkinson/canvas-demos/blob/main/render-code-from-github.html)
Github prevents code stored on their site from being used in an iFrame. Thus, the previous examples do not work for github repositories or for gist snippets. This example uses a third-party API which pulls the data from Github using the github API and then provides the code with the appropriate `Content-Type` so that the code can be interpreted correctly as HTML, JS, etc, within Canvas. 
