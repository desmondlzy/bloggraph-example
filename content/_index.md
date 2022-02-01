---
title: Bloggraph Example Website
---

## Start with the Example Source Code

The best way to get started is get a copy of the source code of this example website and change it as per your need. 
Simply clone the [github repo](https://github.com/desmondlzy/bloggraph-example).
```
git clone --recursive https://github.com/desmondlzy/bloggraph-example yourwebsite
```

Then try `cd yourwebsite; hugo serve` you shall see the example website running at `localhost:1313/`. Make sure you've [installed Hugo](https://gohugo.io/getting-started/installing/) before this.

### Recommended Directory Layout

If you're working with the example website, you're already set. If you are migrating an existing Hugo project, it's highly recommended to organize files as the following:

```
content/
├─ publications/
│  ├─ _index.md (if you want to customize the publication list page)
│  ├─ pequalsnp.md
│  ├─ other-projects.md
├─ _profile.md (bio and social media links; see notes below)
├─ _index.md (home page)
static/
├─ sass/
│  ├─ _custom.sass (recommended place to override the default sass)
themes/
├─ bloggraph/
├─ otherthemes/
config.toml
```

## Site Configuration

Change the corresponding fields in your [site configuration](https://gohugo.io/getting-started/configuration/#configuration-file) at `config.toml` to customize the following.

### Site Owner Name

Change `name` in `[params.author]`. It will be used to highlight your name in the author list.

### Social Media Links

Change the fields in `[params.author]`. Currently, only `linkedin`, `github` and `email` are supported.
Want more? Tweak `themes/bloggraph/layout/index.html` and file a [pull request](https://github.com/desmondlzy/bloggraph/pulls) to let everyone benefit from it!

### Tabs in the Navigation Bar

Change `[menus.main]`. See [official documentation on menus](https://gohugo.io/content-management/menus) for more info.

## Home Page

Home page (the page shown at the root of your website) is generated from the `content/_index.md`. As usual, use [markdown syntax](https://www.markdownguide.org/) to write things on your home page.


## Publication

Bloggraph has a special focus on "project page".
See below for all the tools that may come in handy.

### Add a Publication/Project Page

Simple! Run the following command which creates all the boilerplate and front matters.
```
hugo new publications/p-equals-np.md
```

The authors and affiliations information will be parsed from the front matters and displayed on the page automatically.

### Show the Overview of a Publication from Markdown

A [shortcode](https://gohugo.io/content-management/shortcodes) is bundled so that you can refer a publication page in the website by 

<pre><code>{{&lt; publication/single title="Realtime Rendering on a Single Thread" >}}</code></pre> 

{{< publication/single title="Realtime Rendering on a Single Thread" >}}

### Publication List

A list of publication is automatically generated at `baseURL/publications`. You can add customized content before the list at `content/publications/_index.md`.

## Extras

I like snacks...

### Number the Sections/Figures

Use __shortcode__ in the markdown file you want to number:

<pre><code>{{&lt; numbering >}}</code></pre>

Pass in booleans to different arguments to control items to be numbered:

<pre><code>{{&lt; numbering figure=false h2=true h3=false >}}</code></pre>

Use classes `.count-figure` and `.count-h2h3` if you work with HTML.