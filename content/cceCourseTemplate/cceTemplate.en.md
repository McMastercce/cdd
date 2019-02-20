---
title: CCE Course Template
weight: 10
disableToc: false
---

Before beginning integration, copy all componeents from the CCE Course Template in Avenue into your course master shell.

{{% notice note %}}
If you are not able to access the CCE Course Template in Avenue contact an LST. You are required to have a MacID to access Avenue.
{{% /notice %}}

## Manage Files

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

## Custom CSS Classes
Custom CSS classes have been added to the stylesheet.

### List Types
The list type attribute is obsolete. To accomodate custom list types the following classes are available.

#### Ordered
##### lower-alpha
<iframe width="100%" height="175" src="//jsfiddle.net/ccecrsdv/kLo24gxr/embedded/result,html/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

##### upper-alpha
<iframe width="100%" height="175" src="//jsfiddle.net/ccecrsdv/dLwhxv27/embedded/result,html/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

##### lower-roman
<iframe width="100%" height="175" src="//jsfiddle.net/ccecrsdv/kr2fx37q/embedded/result,html/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

##### upper-roman
<iframe width="100%" height="175" src="//jsfiddle.net/ccecrsdv/r6nezstL/embedded/result,html/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

#### Unordered
##### noType
<iframe width="100%" height="175" src="//jsfiddle.net/ccecrsdv/751qomuL/embedded/result,html/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

##### circle
<iframe width="100%" height="175" src="//jsfiddle.net/ccecrsdv/7vhqaz36/embedded/result,html/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

##### square
<iframe width="100%" height="175" src="//jsfiddle.net/ccecrsdv/z0bhv5Ly/embedded/result,html/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>
   

## Hyperlinks

Hyperlinks that are pointing to external content, not hosted in Avenue, must open in a new tab. They must also include an additional class and text for screen readers in a \<span> attribute.

{{% notice info %}}
The \<span> attribute should not be included on any hyperlinks that don't have the cce stylesheet attached. For example, if there is a link in the description of a discussion topic, exclude the \<span> attribute.
{{% /notice %}}

```
<a href="http://example.com" target="_blank">Example link<span class="sr-only"> (opens in a new tab)</span></a>
```

Hyperlinks that are pointing to internal content, hosted in Avenue, should open in the same tab.

```
<a href="http://example.com">Example link</a>
```

## Evaluations Module

The files in this module should be Word files (.doc or .docx) unless otherwise specified by the ID.