---
layout: project
type: project
image: images/glover/thumb.png
title: Jas. W. Glover, Ltd. website
permalink: projects/gloverltd
date: 2017
labels:
- web development
- php
- markdown
summary: As part of my internship, I developed a new website for Jas. W. Glover, Ltd. 
---

<img class="ui image rounded" src="../images/glover/home.png">

As part of my internship at [Jas. W. Glover, Ltd.](https://www.gloverltd.com), I created a new website for them, incorporating modern web design standards to support both desktop and mobile web experiences.

Taking advantage of their existing PHP hosting, I chose [Pico](http://picocms.org/) for their content management system. Pico uses Markdown files for core content, and a templating engine called [Twig](https://twig.symfony.com/) to generate pages from those Markdown files. The system doesn't require a database, and can generously cache the generated files to approach the performance of a static website, while maintaining the ease of use of a website backed by a scripted language. I thought the easily editable Markdown formatting, in combination with the file-centric content system and seamless updating, would be a good fit for the company.

I also created a custom extension for Pico, which preprocesses the Markdown files using regular expressions. It parses a shorthand into HTML content blocks, like so:

```
[~table.border.alt]
	[~row.cell.title]
		### Title
	[~row]
		[~cell.smaller.half]
			Left column text
		[~cell.smaller.half]
			Right column
[~content]
	Example text
``` 

becomes

```html
<div class="container rounded table border alt">
	<div class="row cell title"><h3>Title</h3></div>
	<div class="row">
		<div class="cell smaller full">
			<p>Left column text</p>
		</div>
		<div class="cell smaller half">
			<p>Right column text</p>
		</div>
	</div>
</div>
<div class="container content">
	<p>Example text</p>
</div>
```


The new website is still pending official approval, following a copy-editing process.
