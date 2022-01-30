---
---

The introduction section resides in `content/_profile.md`

## Get Started with Home Page

The best way to get started is get a copy of the source code of this example website and change it as per you need. Clone the [github repo](https://github.com/desmondlzy/bloggraph) of bloggraph and copy everything inside of `exampleSite/` might be the simplest thing to do.

### Change Photo/Social Media Links

Change the corresponding field in the front matter of `content/_profile.md`. Only links to Github, LinkedIn and email are supported. Want more? Change `themes/layout/index.html` and file a pull request to let everyone benefit from it!

### Change the Tabs in the Navigation Bar

Change the corresponding field in `config.toml`. See [official documentation on menus](https://gohugo.io/content-management/menus) for more info.

## Publication

Simple! Run the following command which creates all the boilerplate and front matters.
```
hugo new publications/p-equals-np.md
```