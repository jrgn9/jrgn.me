
# [jrgn.me](https://jrgn.me) <img align="left" height="42" src="./static/favicon-32x32.png"> 

My personal website created with [Hugo](https://gohugo.io/getting-started/quick-start/) 
and the [PaperMod theme](https://adityatelange.github.io/hugo-PaperMod/). Deployed to GitHub Pages with Github Actions.

## Using Hugo

This is just a section for myself to remember how to use Hugo.

### Installing themes with Hugo (git submodule)

Inside the folder of your Hugo site MyFreshWebsite, run:
```
git submodule add --depth=1 https://github.com/<dev>/<name>.git themes/<name>
git submodule update --init --recursive # needed when you reclone your repo (submodules may not get cloned automatically)
```

Then set the theme in the .toml/.yaml config file.

#### Updating theme
Inside the folder of your Hugo site MyFreshWebsite, run:
```
git submodule update --remote --merge
```

### Creating content
To create a new post, use the following command:

```shell
hugo new content content/<directory>/<post-name>.md
```

Hugo created the file in the content/posts directory. Open the file with your editor.

By default the file is added as draft and looks like this:

```markdown
+++
title = 'My First Post'
date = 2024-01-14T07:07:07+01:00
draft = true
+++
```

The content of the file is written in markdown under the front matter. Draft needs to be set to false to publish the post.

#### Using archetype for creating posts

Archetypes contains templates. I have used a template for posts [from PaperMod](https://adityatelange.github.io/hugo-PaperMod/posts/papermod/papermod-installation/#sample-pagemd).

Use this template when creating a post by using the following command:
```
hugo new --kind post content/<directory>/<post-name>.md
```

### Running the server
To run the server, use the following command:

```shell
hugo server -D
```

The -D flag is used to show drafts.

The server is by default running in Fast Render Mode. For full rebuilds on change: 
```
hugo server --disableFastRender
```

#### Clear cache

Sometimes the cache needs to be cleared for the server to update:

```
hugo --ignoreCache
```

### Uninstall theme (remove submodule)

This walkthrough is only for themes installed as a git submodule.

1. Remove the submodule entry from .gitmodules:
```
[submodule "themes/<name>"]
    path = themes/<name>
    url = https://github.com/example/name.git
```

2. Remove the submodule from the .git/config:
```
git submodule deinit -f themes/<name>
```

3. Remove the submodule directory:
```
rm -rf .git/modules/themes/<name>
rm -rf themes/<name>
```

4. Remove the submodule entry from the index:
```
git rm -f themes/<name>
```

## Attribution
[Sloth favicon by iconixarPro](https://www.flaticon.com/free-icons/sloth)
