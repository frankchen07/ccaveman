
# steps

1. write post using format below, place in `_posts`
2. place images in link below
3. embed videos if necessary
4. apply post-writing conversions

---
layout: blog
title: 
category: blog
tags: []  
summary: 
image: https://raw.githubusercontent.com/frankchen07/ccaveman/gh-pages/images/blog/.jpg
---

<figure>
    <img src="https://raw.githubusercontent.com/frankchen07/ccaveman/gh-pages/images/blog/.jpg"></img>
    <figcaption></figcaption>
</figure>

<iframe></iframe> embed code from youtube itself

---

# post-writing conversions

* include <!--more-->
* after IPython html conversion, sans the <title> tag
* ImageOptim
* ImageMagick `mogrify -resize 1280x960 *.jpg`
* ImageOptim again

---

# misc renaming entities & notes

`sed -i.bu 's/\/images\/blog/https:\/\/raw.githubusercontent.com\/frankchen07\/ccaveman\/gh-pages\/images\/blog/g' *.md`
`sed -i.bu 's/”/"/g' *.markdown`
`find . -exec rename -n -fc {} +`
`find . -exec rename -n 's/, /_/' {} +`
`find . -exec rename -n 's/ - /_/' {} +`
`find . -exec rename -n 's/- /_/' {} +`
`find . -exec rename -n 's/ -/_/' {} +`
`find . -exec rename -n 's/ /_/' {} +`
`find . -exec rename -n 's/__/_/' {} +`

---

# testing 

* make sure local url matches with local server pushes, since {{site.url}} refers to whichever you last set it to, thus, one may have to change the config.yml and regenerate the correct static files.

---

