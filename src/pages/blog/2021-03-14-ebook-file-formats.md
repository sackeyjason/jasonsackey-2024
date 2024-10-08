---
title: "Converting Kindle books to EPUB format"
date: "2021-03-14"
categories: 
  - "file-formats"
tags: 
  - "ebooks"
  - "epub"
layout: "./_layout.astro"
---

...is not easy. But it's possible. At least, at the time of writing, and the handful of ebooks I tried so far. There are many such guides online, often incomplete. Or more accurately, out of date, because Amazon subsequently added more stumbling blocks. I shall document what worked for me, a combination of steps from various guides. Some steps may be redundant!

<!--more-->

This guide is for performing the process on Windows PCs. My goal was to get EPUBs I can read on my Kobo device.

Software to install (version numbers are what I have. Not saying these exact version are what's required, but it might help):

- [Kindle Reader](https://www.amazon.com/kindle-dbs/fd/kcp) (I have the latest, version 1.30.0. Some guides say you need an earlier version, but nah, this is fine)
- [Calibre](https://calibre-ebook.com/) (version 5.12)
- [DeDRM plugin for Calibre](https://github.com/apprenticeharper/DeDRM_tools/releases) (7.10)
- Adobe Digital Editions (4.5) - actually I'm not sure if this is required. It's supposed to help the DeDRM plugin do its thing. But I haven't signed into it with my Amazon account, so how does have the necessary keys with which to do the decryption? I don't know if it's doing anything as part of this ritual)

1. Install all of the above
2. Open the Kindle Reader application, be signed in
3. Open the Registry Editor
4. Go to this location in RegEdit: `Computer\HKEY_CURRENT_USER\SOFTWARE\Amazon\Kindle\User Settings`
5. Edit this key: `isKRFDRendererSupported` - change the value from `true` to `false`
6. (For MacOS and and perhaps Linux, the equivalent of this RegEdit stuff is documented [here](https://jacintowilson.medium.com/kfx-converter-convert-kfx-to-pdf-epub-mobi-txt-71843fe9b844))
7. In the Kindle program, download your book (Already downloaded it? Delete it. Download it again.)
8. Find the location of the downloaded file. By default it's in `My Documents/My Kindle Content`
   1. The subfolder will be unhelpfully named something like `B00BUJ2RAG_EBOK`
9. There should be on .azw file in there. Import it into Calibre - drag it onto the main window. This copies the file into your Calibre library folder
10. In Calibre: select and convert the book. Right click on it> Convert books > Convert individually

![](https://jasonsackey.com/wp-content/uploads/2021/03/image.png?w=455)

- In this new window, ensure the top-right corner shows EPUB as the selected format. Click OK.
- The .epub file is now there in your Calibre library.

Done. Hooray!
