---
title: Instructor Guides
weight: 30
disableToc: false
---

The instructor guides need to be modified for each course.

As of July 2019 instructor guides for all new courses are generated from content saved in a database on GitHub: <a href="https://github.com/McMastercce/avenue-content-library-database/blob/master/database.json" target="_blank">McMastercce / avenue-content-library-database</a>.

Each content topic in Avenue (before.html, during.html, after.html etc.) uses a javascript application to pull the necessary items for that specific page from the database.

## Content Item Properties

Each content item in the database has the following properties:

* id
* name
* markup

The id property is a unique identifier for each content item. The application uses this value to get content objects to display.

The name property does not currently get displayed in Avenue. It's for organizational purposes.

The markup property is a string with all of the HTML for the content item. It cannot inclide line breaks, and quotes need to be escaped.

## Example Topic in Avenue

The following is a breakdown of a before.html page in Avenue.

### Head Element

The head element must include a global variable, "sections", with an array of content item id's in the order that they should to appear on the page.

```html
<head>
  <title>Before Your Course Begins</title>
  <script type="text/javascript">
    
    var content = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13];
    
    window.sections = content;
    </script>
    <meta content="width=device-width,initial-scale=1" name="viewport">
</head>
```

### Body Element

The body element must include the following items:

* A div element with the id of "content-library". When the javascript application pulls the content items from the database, they will appear within this div element.
* A reference to the javascript application.
* The jQuery file from Manage Files.
* A javascript function to notify users if the application does not work.

```html
<body>

<div id="content-library"></div>

<script src="https://mcmastercce.github.io/avenue-content-library-app/index.js" type="text/javascript"></script>

<script src="/content/enforced/195193-harorr_sandbox/toc/instructor-guide/../../code/js/jquery.min.js"></script>

<script>
    window.onload = function() {
        var element = document.getElementById('content-library');
        if (element.innerHTML === '' || element.innerHTML === '<app-root></app-root>') {
            document.getElementById('content-library').innerHTML =
                '<p>The content for this page failed to load. This may be due to an extension you have installed in your browser.<\/p><p>If you continue to experience issues after testing in other browsers please report this issue to <a href="mailto:ccecrsdv@mcmaster.ca">ccecrsdv@mcmaster.ca</a>.</p>';
        }
    };
</script>

</body>
```

### Complete example

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <title>Before Your Course Begins</title>
  <script type="text/javascript">
    
    var content = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13];
    
    window.sections = content;
    </script>
    <meta content="width=device-width,initial-scale=1" name="viewport">
</head>

<body>
<div id="content-library"></div>
<script src="https://mcmastercce.github.io/avenue-content-library-app/index.js" type="text/javascript"></script>
<script src="/content/enforced/195193-harorr_sandbox/toc/instructor-guide/../../code/js/jquery.min.js"></script>
<script>
    window.onload = function() {
        var element = document.getElementById('content-library');
        if (element.innerHTML === '' || element.innerHTML === '<app-root></app-root>') {
            document.getElementById('content-library').innerHTML =
                '<p>The content for this page failed to load. This may be due to an extension you have installed in your browser.<\/p><p>If you continue to experience issues after testing in other browsers please report this issue to <a href="mailto:ccecrsdv@mcmaster.ca">ccecrsdv@mcmaster.ca</a>.</p>';
        }
    };
</script>
</body>
</html>
```

## Adding Items That Are Not in the Database

If the content item that you want to add is not in the database and it applies to several courses, contact ccecrsdv@mcmaster.ca to have these items added.

If the content that you want to add is not in the database and it only applies to the course that you are working on you can add the HTML directly in the topic page.

### Before and/or After Content Items

If the additional HTML needs to appear before or after the ```<div id="content-library"></div>``` element, simply add that markup before or after this element.

### Between Content Items

If you need to add HTML between content items, you can include it as an item in single quotations.

{{% notice note %}}
Markup in the content variable cannot include line breaks.
{{% /notice %}}

Example:

```html
<head>
  <title>Before Your Course Begins</title>
  <script type="text/javascript">
    
    var content = [0, 1, 2, 3, 4, '<h2>PebblePage</h2><p>Update PebblePad settings for this term</p>', 5, 6, 7, 8, 9, 10, 11, 12, 13];
    
    window.sections = content;
    </script>
    <meta content="width=device-width,initial-scale=1" name="viewport">
</head>
```


