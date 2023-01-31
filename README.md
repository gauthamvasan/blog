# Musings of an Enlightened Idiot

This is my personal blog, hosted on git. I'm using the Jekyll version of the "Editorial" theme by [HTML5 UP](https://html5up.net/).

![Editorial Theme](assets/images/screenshot.jpg "Editorial Theme")

## Local development tips
To host website locally for dev purposes:
```
bundle exec jekyll serve
```

## How to Use

For those unfamiliar with how Jekyll works, check out [https://jekyllrb.com/](https://jekyllrb.com/) for all the details,
or read up on just the basics of [front matter](https://jekyllrb.com/docs/frontmatter/), [writing posts](https://jekyllrb.com/docs/posts/),
and [creating pages](https://jekyllrb.com/docs/pages/).

## Local preview
MacOS can be quite finicky with github pages. This purge process seems to work:
 
1. Remove Gemfile and Gemfile.lock
2. Install gems
```bash 
gem install bundler jekyll webrick jekyll-feed
bundle add jekyll-feed
```
3. Host locally
```bash
bundle exec jekyll serve
```
4. You should see a similar message:
```bash
(base) gautham@Ryuk-MacBook blog % bundle exec jekyll serve             
Configuration file: /Users/gautham/src/blog/_config.yml
            Source: /Users/gautham/src/blog
       Destination: /Users/gautham/src/blog/_site
 Incremental build: disabled. Enable with --incremental
      Generating... 
       Jekyll Feed: Generating feed for posts
                    done in 0.683 seconds.
 Auto-regeneration: enabled for '/Users/gautham/src/blog'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
```
 
