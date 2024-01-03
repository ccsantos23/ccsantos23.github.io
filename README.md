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

### Some notes on the dev environment

- Because I moved to a new machine, and realized I hadn't noted down the steps
  to create this site.  These are the steps to get the dev environment recreated.
  There are extra steps if creating the site from scratch.
  See the [jekyll setup tutorial](https://jekyllrb.com/docs/step-by-step/01-setup/).
- Install Ruby for Windows
  - Downloaded and installed the latest `Ruby+Devkit 3.2.X (x64)` installer.
  - Run `ridk install` step of the wizard.
    - Choose `MSYS2 and MINGW development tool chain`
  - On a new Terminal window, run `gem install jekyll bundler`
  - Checked if Jekyll has  been installed properly:  `jekyll -v`
  - Installed update for RubyGems: `gem update --system 3.5.3`
- Run `bundle install` on the top-level of this site's source folder.
- To start the server, do:

  ```powershell
  bundle exec jekyll serve --livereload
  ```

  Then browse to [https://localhost:4000](https://localhost:4000).
- The command also rebuilds the `docs` folder, which is served on [Lint Bucket](https://ccsantos23.github.io/)
  once the changes are pushed by git to the remote repo on GitHub.
