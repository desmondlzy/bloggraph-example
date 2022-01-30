---
title: Bloggraph Example Website
---

The introduction section resides in `content/_profile.md`

## Get Started with Home Page

The best way to get started is get a copy of the source code of this example website and change it as per you need. Clone the [github repo](https://github.com/desmondlzy/bloggraph-example) of this site might be the simplest thing to do.
```
git clone --recursive https://github.com/desmondlzy/bloggraph-example
```

### Change Photo/Social Media Links

Change the corresponding field in the [front matter](https://gohugo.io/content-management/front-matter) of `content/_profile.md`. Only links to Github, LinkedIn and email are supported. Want more? Change `themes/layout/index.html` and file a pull request to let everyone benefit from it!

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

### Show Overview of a Publication from Markdown

A [shortcode](https://gohugo.io/content-management/shortcodes) is bundled so that you can refer a publication page in the website by 

<code>
{{&lt; publication/single title="Realtime Rendering on a Single Thread" >}}
</code>

{{< publication/single title="Realtime Rendering on a Single Thread" >}}

### Publication List

A list of publication is automatically generated at `baseURL/publications`. You can add customized content before the list at `content/publications/_index.md`.

## Extras

It's always good to have some deserts...

### Number the Sections/Figures

Use shortcode:

<code>
{{&lt; numbering >}}
</code>
</br> </br>

Pass different arguments to control items to be numbered:

<code>
{{&lt; numbering figure=false h2=true h3=false >}}
</code>