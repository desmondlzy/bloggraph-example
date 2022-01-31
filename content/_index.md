---
title: Bloggraph Example Website
---

The introduction section resides in `content/_profile.md`

The best way to get started is get a copy of the source code of this example website and change it as per you need. Simply clone the [github repo](https://github.com/desmondlzy/bloggraph-example).
```
git clone --recursive https://github.com/desmondlzy/bloggraph-example
```

Then try `hugo serve` you shall see the example website running at `localhost:1313/`. Make sure you've [installed Hugo](https://gohugo.io/getting-started/installing/).

## Recommended Directory Layout

If you're working with the example website, you're already set. If you are migrating an existing Hugo project, it's highly recommended to organize files as the following:

```
content/
├─ publications/
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

## Home Page

Home page (the page shown at the root of your website) is generated from the `content/_index.md`. As usual, use [markdown syntax](https://www.markdownguide.org/) to write things on your home page.

### Change Photo/Social Media Links

Change the corresponding field in the [front matter](https://gohugo.io/content-management/front-matter) of `content/_profile.md`. 
Currently, only links to Github, LinkedIn and email are supported. 
Want more? Change `themes/layout/index.html` and file a [pull request](https://github.com/desmondlzy/bloggraph/pulls) to let everyone benefit from it!

### Change the Tabs in the Navigation Bar

Change the corresponding field in `config.toml`. See [official documentation on menus](https://gohugo.io/content-management/menus) for more info.

## Publication

The theme has a special focus on "project page" in contrast to the general themes that usually focus on blogging.
A `publication` layout is provided to ease the process of writing authors and affiliations.


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

It's always good to have some deserts...

### Number the Sections/Figures

Use shortcode:

<pre><code>{{&lt; numbering >}}</code></pre>

Pass different arguments to control items to be numbered:

<pre><code>{{&lt; numbering figure=false h2=true h3=false >}}</code></pre>