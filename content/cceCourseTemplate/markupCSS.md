---
title: Markup and CSS
weight: 20
disableToc: false
---

## Markup for Embedding YouTube Videos

Copy and modify the following markup when embedding YouTube videos.

```html
<div class="row justify-content-center">
    <div class="col-sm-10">
        <div class="card px-1">

            <!-- Update the following line with the title of the video, the length of the video, and the transcript href -->
            <p class="mb-1"><strong>Module 1: Introduction</strong> (1:18 min) | <a href="../../media/html/m01-transcript-01.html" target="_blank">Transcript<span class="sr-only"> (opens in a new tab)</span></a></p>
            
            <!-- Update the following element with the url to the YouTube hosted video -->
            <div class="embed-responsive embed-responsive-16by9 hidden-print">
                <iframe src="https://www.youtube.com/embed/NpEaa2P7qZI?rel=0&amp;modestbranding=1&amp;wmode=opaque" allowfullscreen=""></iframe>
            </div>

            <!-- Update the following element with the url to the YouTube hosted video -->
            <p class="d-none d-print-block">https://www.youtube.com/embed/NpEaa2P7qZI?rel=0</p>
            <div class="caption">

            <!-- Update the following element with the name of the author and the narrator. Remove narrator if the author is the narrator. -->
                <p class="my-1">
                    <em>By [first and last] for McMaster University CCE.<br>Narrated by [first and last].</em>
                </p>
            </div>
        </div>
    </div>
</div>
```

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

```html
<a href="http://example.com" target="_blank">Example link<span class="sr-only"> (opens in a new tab)</span></a>
```

Hyperlinks that are pointing to internal content, hosted in Avenue, should open in the same tab.

```html
<a href="http://example.com">Example link</a>
```
