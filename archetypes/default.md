---
title: '{{ replace .File.ContentBaseName "-" " " | title }}'
date: {{ .Date }}
draft: true
tags: ["some", "tags", "here"]
author: "Jørgen Skontorp"
description: "A description here"
#summary: "Summary here"
#canonicalURL: "https://jrgn.me/weird/<canon>
#CanonicalLinkText: "some text"
hidemeta: false
cover:
    image: "/images/<name>.png" # image path/url
    alt: "An alt text here"  
    caption: "caption" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
---
