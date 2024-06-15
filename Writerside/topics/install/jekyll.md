# Jekyll

[CONTENT NEEDED]

## Deploying Your Site

GitHub Actions can process the build for you in one of two ways:

1. GitHub recognizes the Jekyll content in the `/docs` folder of your repo. This is the classic (aka. legacy) way of processing Jekyll content. The version of Jekyll is determined by the `github-pages` Ruby gem, and it has a strict whitelist of allowed Jekyll plugins.
2. You [write your own workflow](https://jekyllrb.com/docs/continuous-integration/github-actions/) in GitHub Actions (aka. the recommended way) to build you site.
   * This allows you to use an arbitrary Jekyll version, including the latest version.
   * This allows you to use any plugin&mdash;not just the ones approved by GitHub.

## Updating Your Ruby Tools

Jekyll is written in Ruby. So the Ruby ecosystem will need to be installed on your system to perform local builds and preview you site before you commit it to the web.

## Installing Ruby

[[CONTENT NEEDED](ruby-for-jekyll.md)]

## Updating the Gem Tool

It's not a strict requirement, but you might want to make sure that you're running the latest version of the Ruby tools.

```Text
gem update --system 3.5.11
```


## Installing Jekyll

For several reasons, including inconsistent SASS support between Jekyll and Eleventy, I've decided to abandon the `github-pages` gem. Jekyll recommends that you use GitHub Actions to drive your builds and deploys. This also allows us to use the latest version of Jekyll, 4.x.x.

> **NOTE:** Before you install Jekyll, check to see if it's already there. Any version greater than 4.x.x is fine.
>
> ```Text
> > jekyll --version
> jekyll 4.3.3
> > _
> ```

If that command fails to run, you may need to install Jekyll.

```Text
gem install jekyll
```

> **NOTE:** If the command complains about missing gems, like `wdm`, install them.
> ```Text
> > gem install wdm
> ```


