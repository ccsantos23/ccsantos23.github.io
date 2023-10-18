# Lint Bucket

A blog for random things learned. And a playground to try out some web dev stuff.

## Note to Self

After the recent change to make this
[skip Jekyll processing](https://github.blog/2009-12-29-bypassing-jekyll-on-github-pages/)
on Github Pages, and generating the site in the `docs/` folder
while on my dev environment, all posts should now be created
in the dev environment.  Don't add files to the `_posts/` folder
on Github, because it won't re-build the site anymore.

Did this because Github Pages was not generating the preview cards
with the `jekyll-url-metadata` plugin like Jekyll does on my
dev environment.

## Change Log

### 2023-10-09

- Set destination folder to `docs/` instead of the default `_site/`,
  and add a `.nojekyll` file to skip Jekyll processing on Github Pages.
- Add link preview cards using `jekyll-url-metadata` plugin.
- Adjust post meta markup so comment count icon is part of link,
  otherwise it just sits there.
- Set `comments:true` as default. Adjust styles for comment section.
- Enable Disqus. Remove check for `jekyll.environment == "production"`
  for Disqus sections.
- Add thumbnail to home page front matter.
- Add link to RSS feed.
