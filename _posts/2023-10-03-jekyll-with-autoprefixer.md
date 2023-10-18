---
title: Jekyll with Autoprefixer
date: 2023-10-03 06:32 -0500
tags: [jekyll, sass, autoprefixer, vscode]
---

Getting `autoprefixer` included in the jekyll workflow.

Finally got `autoprefixer` going for this blog's CSS files (using [octopress-autoprefixer](https://github.com/octopress/autoprefixer)),
but ended up losing the `livereload` option when running `bundle exec jekyll serve`
(because it errors out), and losing meaningful sourcemapping for the SCSS files.

An option would be to use an [autoprefixer plugin in VSCode](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-autoprefixer)
and remember to do it every time I save a stylesheet.  Or also try out
a [VSCode extension that runs commands on save](https://marketplace.visualstudio.com/items?itemName=emeraldwalk.RunOnSave).

Another option is to bypass jekyll and do the other workflow tasks
with gulp like in [this discussion](https://talk.jekyllrb.com/t/autoprefixer-sourcemaps-for-sass/884).
I could probably do it with node scripts too (done it before).
But it takes away from the whole convenience that jekyll provides.

p.s. Also learned that I'd better use the `github-pages` gem to make sure the jekyll
output on my local is going to work when it's hosted on github.io.
So I made that change.
