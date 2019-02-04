---
title: CCE Course Template
weight: 30
disableToc: false
---

The CCE Course Template in Avenue contains all of the neccessary files and Grade settings to begin integrating a course. Copy all componeents from the CCE Course Template into your course master shell before beginning integration.

{{% notice note %}}
If you are not able to access the CCE Course Template in Avenue contact an LST. You are required to have a MacID to access Avenue.
{{% /notice %}}

## Template Files

The following table provides a breakdown of the various files and folders in the Manage Files(Course Admin &gt; Manage Files) area of the CCE Course Template.

<table class="table table-bordered table-striped table-sm">
   <caption class="sr-only">
      The first column lists the Folder Name. The second column provides a summary of what is in each folder.
   </caption>
   <thead>
      <tr class="d-flex">
         <th class="col-4" scope="col">Location</th>
         <th class="col-8" scope="col">Purpose</th>
      </tr>
   </thead>
   <tbody>      
      <tr class="d-flex">
         <td class="col-4">Avenue/code</td>
         <td class="col-8">CSS, javascript and icon code files.</td>
      </tr>
      <tr class="d-flex">
         <td class="col-4">Avenue/code/css</td>
         <td class="col-8">
            CSS and font icon files.
            <br>
            <div class="spacer-xs-6 spacer-sm-7 spacer-md-8"></div>
            All HTML pages refer to the <strong>main.min.css</strong> for styling. You will also find additional main.min.css(program) files. These are not linked to any HTML files. Based on the course that you are working on, rename the file that you need. For example for a business course I would rename "main.min.css(business)" to "main.min.css".
         </td>
      </tr>
      <tr class="d-flex">
         <td class="col-4">Avenue/toc</td>
         <td class="col-8">Module pages that appear directly in the table of contents are stored here.</td>
      </tr>
      <tr class="d-flex">
         <td class="col-4">Avenue/media</td>
         <td class="col-8">Any additional files in the course such as images, documents or html pages that are hyperlinked from a module are stored here. This includes readings and transcripts.</td>
      </tr>
   </tbody>
</table>

Browse through the CCE Course Template content to familiarize yourself with the structure of a page.

## Hyperlinks

Hyperlinks that are pointing to external content, not hosted in Avenue, must open in a new tab. Thet must also include an additional class and text for screen readers.

```
<a href="http://example.com "target="_blank">Example link<span class="sr-only"> (opens in a new tab)</span></a>
```

Hyperlinks that are pointing to internal content, hosted in Avenue, should open in the same tab.

## Evaluations Module

The files in this module should be Word files (.doc or .docx) unless otherwise specified by the ID.        