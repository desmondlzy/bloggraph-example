---
title: "Realtime Rendering on a Single Thread"
type: publications
summary: "Real-time rendering on a single CPU thread is no longer a daydream!"
date: 2021-02-20T20:55:17+01:00
thumbnail: eyeroll-wall.jpg
paper: "url-to-your-paper.pdf"
venue: 
  name: International Journal of Graphics 2021
  url: to-publisher-website
  note: conditionally rejected
authors:
  - name: Foo, Bar
    affiliations: [1, 2]
    url: https://desmondlzy.me
  - name: am I, Who
    affiliations: [1, 2]
    url: https://desmondlzy.me

affiliations:
  - name: University of Foo
    url: https://foo.edu
  - name: Institute of Bar
    url: https://bar.org
---
{{< numbering h2=false h3=false >}}

## Intro

This post is generated with the Hugo mechanism ["Page Bundle"](https://gohugo.io/content-management/page-bundles/) that allows the user to organize all the assets used in a post in a directory.
You can find the source for this post at `/content/publications/realtime-rendering-on-a-single-thread/_index.md`.
On the contrary, the [other](../lossless-conversion-from-soup-to-voxels/index.html) sample post in this website is generated as a standalone post from `/content/publications/lossless-conversion-from-soup-to-voxels.md`.
I generally prefer using page bundles for the ease of organizing many media files that I need to put together for a visual-intense post.

## Author/Affiliation Information

You might also have noticed the information about this publication rendered at the beginning of this post, including the venue, authors, and their affiliations.
**If you have set the `type` as `publications` in the frontmatter of the post markdown file** (`/content/publications/realtime-rendering-on-a-single-thread/_index.md`),
these pieces of information are fetched from the frontmatter and rendered as demonstrated. 
The frontmatter of this post is shown as below:
```
---
title: "Realtime Rendering on a Single Thread"
type: publications
summary: "Real-time rendering on a single CPU thread is no longer a daydream!"
date: 2021-02-20T20:55:17+01:00
thumbnail: eyeroll-wall.jpg
paper: "url-to-your-paper.pdf"
venue: 
  name: International Journal of Graphics 2021
  url: to-publisher-website
  note: conditionally rejected
authors:
  - name: Foo, Bar
    affiliations: [1, 2]
    url: https://desmondlzy.me
  - name: am I, Who
    affiliations: [1, 2]
    url: https://desmondlzy.me

affiliations:
  - name: University of Foo
    url: https://foo.edu
  - name: Institute of Bar
    url: https://bar.org
---
```

To change the style, take a look at 
`themes/bloggraph/layouts/publications/single.html`.