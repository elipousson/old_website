---
layout: post
title: Making the switch from G Suite apps to Markdown
summary: "I have used Markdown and G Suite apps for research, writing, and publishing for a couple years. Here are a few things I've learned along the way!"
date: 2017-02-17
modified: 2017-05-24
categories: opensource
---

You can make the switch from using [G Suite apps](https://gsuite.google.com) ([Google Docs](docs.google.com) + [Google Sheets](sheets.google.com) + [Google Slides](http://slides.google.com/)) to using [Markdown](https://en.wikipedia.org/wiki/Markdown) + [GitHub](https://github.com/) for writing, publishing, data management, presentations, and collaboration. Or you can keep using both—like I do! Either way, you may find this post helpful to navigating how to use Markdown in your own work.  

Learn more about GitHub and Markdown from my [June 2016 workshop presentation](http://elipousson.github.io/presentations/2016-06-02-intro-to-github.html) for the [bLAM Collective](https://blamcollective.wordpress.com). The [awesome-markdown](https://github.com/mundimark/awesome-markdown) and [awesome-markdown-editors](https://github.com/mundimark/awesome-markdown-editors) are also useful resources.

## Alternatives to Google Docs as text editor

Google Docs is excellent at collaboration and offers a wide variety of rich formatting tools. Most Markdown editors (or plain text editors) offer fewer features but other benefits. Here are a few alternatives to Google Docs worth your consideration.  

### Editing Markdown with Atom

Start by taking a look at [Atom](https://atom.io/). Atom can edit Markdown text files but it works even better when you use packages and themes designed to improve your writing and editing experience.

There are many packages [created for working with Markdown](https://atom.io/packages/search?utf8=%E2%9C%93&q=keyword:markdown) but a few favorites include:

- [markdown-deluxe](https://atom.io/packages/markdown-deluxe)
- [markdown-folder](https://atom.io/packages/markdown-folder)
- [markdown-scroll-sync](https://atom.io/packages/markdown-scroll-sync)
- [markdown-toc](https://atom.io/packages/markdown-toc)
- [markdown-writer](https://atom.io/packages/markdown-writer)
- [tool-bar-markdown-writer](https://atom.io/packages/tool-bar-markdown-writer)
- [markdown-preview-plus](https://atom.io/packages/markdown-preview-plus)
- [language-markdown](https://atom.io/packages/language-markdown)

I'd also recommend a few other packages that can improve the overall writing experience in Atom:

- [linter-write-good](https://atom.io/packages/linter-write-good)
- [linter-alex](https://atom.io/packages/linter-alex)
- [zotero-citations](https://atom.io/packages/zotero-citations)
- [status-stats-jbrains](https://atom.io/packages/status-stats-jbrains)

There are also several [Markdown friendly themes](https://atom.io/themes/search?utf8=%E2%9C%93&q=keyword:markdown) for Atom but [Pen Paper Coffee](https://atom.io/themes/pen-paper-coffee-syntax) is the most popular.

### Other Markdown-friendly text editors

In addition to Atom, I regularly use [Ulysses](https://ulyssesapp.com/). I also occasionally use [Pandoc](http://pandoc.org) and [Marked 2](http://marked2app.com/). My experience using Pandoc is limited so, if you're interested in learning more, I recommend reading [Sustainable Authorship in Plain Text using Pandoc and Markdown](http://programminghistorian.org/lessons/sustainable-authorship-in-plain-text-using-pandoc-and-markdown) (a [Programming Historian](http://programminghistorian.org/) tutorial by Dennis Tenen and Grant Wythoff). Again, there are [several Atom packages](https://atom.io/packages/search?q=pandoc) created to work with Pandoc.

**Update:** I'm currently using [Typora](https://typora.io/) to do most of my writing and editing in Markdown. My current favorite but I still use Atom as well!

Wikipedia provides an [extensive comparison of text editors](https://en.wikipedia.org/wiki/Comparison_of_text_editors) (which include several editors designed for use with Markdown). Some tools allow you to edit Markdown files but other tools specialize in converting Markdown files into other formats (e.g. Word Document or PDF).

Some popular free options for Markdown text editors include:

- [StackEdit](https://stackedit.io/) ([Chrome app](https://chrome.google.com/webstore/detail/stackedit/iiooodelglhkcpgbajoejffhijaclcdg))
- [Minimalist Markdown Editor](https://chrome.google.com/webstore/detail/minimalist-markdown-edito/pghodfjepegmciihfhdipmimghiakcjf)
- [MarkRight](https://github.com/dvcrn/markright)
- [HackMD](https://hackmd.io/) ([GitHub repo](https://github.com/hackmdio/hackmd)): "Realtime collaborative markdown notes on all platforms."

Some useful Markdown editors cost money to purchase. These include:

- [Ulysses](https://ulyssesapp.com/)
- [Marked 2](http://marked2app.com/)
- [Mou](http://mouapp.com)

### Publishing Markdown with GitHub Pages

If you are publishing Markdown files with [GitHub Pages](https://pages.github.com/) (or [Jekyll](http://jekyllrb.com/)), you may want a more feature rich experience than a basic text editor. Take a look at these tools:

- [Prose](http://prose.io/) is a content editor for GitHub designed for managing websites.
- [Jekyll Admin](https://github.com/jekyll/jekyll-admin/) ([documentation](https://jekyll.github.io/jekyll-admin/))

## Alternatives to Google Sheets for editing and sharing data

You may need to create tables to insert in your Markdown documents or you may need to routinely work with Excel or CSV files. Google Sheets is a great tool but there are alternatives worth considering.

Atom packages for working with CSV files include:

- [Atom CSV Markdown](https://atom.io/packages/atom-csv-markdown)
- [language-csv](https://atom.io/packages/language-csv)
- [tablr](https://atom.io/packages/tablr)

For working with tables within Markdown files, useful packages include:

- [table-editor](https://atom.io/packages/table-editor)
- [Markdown Table Formatter](https://atom.io/packages/markdown-table-formatter)

Another accessible tool for editing data files (JSON, YAML, or CSV) hosted on GitHub is [EditData](https://editdata.org/) which is also on GitHub [@editdata](https://github.com/editdata/) (created by [@sethvincent](https://github.com/sethvincent)).

## Alternatives to Google Slides for making presentations

There are a variety of presentation frameworks that allow you to create a web-based slideshow from a Markdown file or from HTML:

- [reveal.js](https://github.com/hakimel/reveal.js/) is one popular option (consider pairing it with [reveal-md](https://github.com/webpro/reveal-md)).
- [remark](https://github.com/gnab/remark) (try it out with [Remarkise](https://remarkjs.com/remarkise)) and [impress.js](https://impress.github.io/impress.js/) are other popular options.
- [Beamer](https://en.wikipedia.org/wiki/Beamer_(LaTeX)) presentations are created with LaTex but may be an option if you are converting a Markdown file with [Pandoc](http://pandoc.org).

Find more options in this [Wikipedia article on web-based slideshows](https://en.wikipedia.org/wiki/Web-based_slideshow).

There are even [a few Atom packages](https://atom.io/packages/search?utf8=%E2%9C%93&q=keyword:presentation) designed for working with these frameworks. However, these options can be difficult for people who are not developers to use.

Some tools make it easier to create web-based slideshows using Markdown but may require a paid subscription. These tools include:

- [Slides](https://slides.com/) (based on reveal.js)
- [Swipe](https://www.swipe.to/markdown/)
- [Spectacle](http://formidable.com/open-source/spectacle/) ([GitHub repo](https://github.com/FormidableLabs/spectacle)) + [Spectacle Editor](https://www.formidable.com/open-source/spectacle-editor/)

## Converting Google Docs or Sheets to Markdown

If you need to work with _both_ Google Docs and Markdown text files, here are a couple extensions and scripts that can help make the process easier:

- [Export as Markdown](https://chrome.google.com/webstore/detail/export-as-markdown/hbojhdcnbcondcdfpfocpkjkfkbnbdad?utm_source=permalink)
- [Gabriel](http://thiscouldbejd.github.io/Gabriel/) ([Extension](https://chrome.google.com/webstore/detail/gabriel/okimajjeocnndpifeelaajdebkkbckff?utm_source=permalink); [GitHub repo](https://github.com/thiscouldbejd/Gabriel))
- [gdocs2md](https://github.com/mangini/gdocs2md) (GitHub repo)
- [sheetdown](https://github.com/jlord/sheetdown) (GitHub repo)

If you need to work with both Google Sheets and Markdown text files or CSV files, here are a couple extensions that can help make the process easier:

- [Crop Sheet](https://chrome.google.com/webstore/detail/crop-sheet/aojcceglbipehndciapjedoomockgagl?utm_source=permalink)
- [Markdown Table Maker](https://chrome.google.com/webstore/detail/markdowntablemaker/cofkbgfmijanlcdooemafafokhhaeold?utm_source=permalink) ([GitHub repo](https://github.com/pffy/googledocs-addon-markdowntablefive))

## Questions or suggestions?

I'll try to keep this updated if any of the links break or someone makes a useful new tool. If you have any comments or suggestions for this post, please add an issue to [my GitHub repo](https://github.com/elipousson/elipousson.github.io) or just say hello [on Twitter](https://twitter.com/elipousson).

P.S. Here are some related things that look interesting but I don't know anything about them so can't really recommend them:

- [Jobby](https://github.com/underscoreio/jobby)
- [google-sheets-parser](https://github.com/DUE-Parsons/google-sheets-parser)
- [Cafe Pitch](https://github.com/joe-re/cafe-pitch)
