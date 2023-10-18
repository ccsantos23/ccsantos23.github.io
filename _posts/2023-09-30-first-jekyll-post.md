---
title: First Jekyll Post
date: 2023-09-30 19:55 -0500
last_modified_at: 2023-10-02 04:41 -0500
tags: [jekyll]
---

Oh hey, this afternoon I made a blog with Jekyll. **This** blog.
And it only took a few hours.

Okay, this is a pretty short post. The blog right now is essentially
the result from doing the
[Step by Step Tutorial](https://jekyllrb.com/docs/step-by-step/01-setup/)
on the [jekyll docs page](https://jekyllrb.com/docs/).

And then while trying to get a theme installed, I found out I shouldn't
have skipped the part in the Quickstart where you go:

```shell
jekyll new myblog
```

because that would have installed the `minima` theme.  It wasn't part of the
tutorial.  So I did the `jekyll new ...` in a temporary folder and copied
over what I needed for this site.  Also copied over some files from the theme's
folder so I could customize them.

Aaaagh! `Minima` is using floats for the footer.  Whyyyy?!?  Must. Fix.
