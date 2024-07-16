# [jrgn.me](https://jrgn.me)
My personal website created with [Hugo](https://gohugo.io/getting-started/quick-start/) 
and the [risotto theme](https://risotto.joeroe.io/).

## Using Hugo

This is just a section for myself to remember how to use Hugo.

### Installing themes with Hugo
To install a theme, just find a fitting theme repository, download it and put it into the themes folder of your Hugo 
project. Then, you can set the theme in the .toml config file.

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

The content of the file is written in markdown under the front matter. Draft needs to be set to false to publish the 
post.

### Running the server
To run the server, use the following command:

```shell
hugo server -D
```

The -D flag is used to show drafts.

### Publish the site
To publish the site, use the following command:

`hugo`

The site is then generated in the public directory. It then deploys with GitHub Actions.

## Attribution
[Sloth favicon by iconixarPro](https://www.flaticon.com/free-icons/sloth)