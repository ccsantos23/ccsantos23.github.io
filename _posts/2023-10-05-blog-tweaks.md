---
title: Blog Tweaks
date: 2023-10-05 03:44 -0500
tags: [jekyll, autoprefixer, css, vscode]
---

Removing `pure.css` and getting sourcemapping back.

Realized that the version of `jekyll` that the `github-pages` gem was using
was messing up sourcemapping even before `autoprefixer`.  That and the loss
of `livereload` made me switch out of `github-pages` and just went back to
my original config and Gemfile that had the latest versions.

When I looked at the HTML of the site, it had all these "pure-*" classes on
the markup.  And realized that was `pure.css`, a CSS framework.  It reminded
me too much of Tailwind, which I didn't really like from first time I saw it
(see Jeff Sandberg's [Tailwind, and the death of web craftsmanship](https://pdx.su/blog/2023-07-26-tailwind-and-the-death-of-craftsmanship/)
for a lot of reasons).  Also saw [this article](https://medium.com/codex/pure-css-more-like-pure-junk-1ec2d26a1122)
while I was researching `pure.css` (sadly requiring a login to read the whole thing).
So I ripped-out pure from the HTML and the SASS.  Turned out it was hardly used,
and it was easy enough to drop in the necessary styles to take its place.

For a while I contemplated switching to a simpler theme, like [contrast](https://jekyllthemes.io/theme/contrast).
But I'd have to put in features like tags, and taxonomy index pages.

About `autoprefixer`--that was still messing up the sourcemapping.  I decided to
take it off the `jekyll` workflow and just use an [autoprefixer extension for VSCode](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-autoprefixer),
with the `formatOnSave` option turned on.  And did a
save on all the *.scss files.  I just have to remember to delete the related prefixed
lines if I needed to change something that got prefixed, so they'd get
regenerated on save.

Also tweaked some styles.

My "built a jekyll website in just a few hours" isn't accurate anymore.
Needed a few more days to have one I'm happier with as far as rendered
output and development environment.

And thank goodness for [git](https://git-scm.com/).
And [Git Extensions](https://gitextensions.github.io/).
