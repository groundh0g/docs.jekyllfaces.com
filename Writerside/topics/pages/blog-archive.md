# Blog Archive

The blog archive page lists excerpts from all the blog posts on the site in one place so that the reader can scan the posts in chronological order. This page supports several configuration options to alter the appearance of the archive. Hopefully one of the variants will suit your needs.

If you're not thrilled with the options presented for the blog archive page, you can build your own using several of the available widgets from the site.

## Usage

| Setting  | Values                 | Description                                                                    |
|----------|------------------------|--------------------------------------------------------------------------------|
| recent   | true / false           | Include the most recent N posts at the top of the page in a different style.   |
| featured | true / false           | Include the most recent N featured posts at the top in a different style.      |
| count    | (number)               | How many recent / featured posts should be called out at the top of the list?  |
| style    | list / card / carousel | Show blog summaries as standard text, or as styled cards.                      |

> **NOTES:**
> 
> 1. If both `recent` and `featured` are enabled, `featured` takes precedence.
> 2. The value of `count` determines how many featured posts are listed at the top of the archive page.
> 3. The value of `style` determines how the blog posts are rendered. See their descriptions in the following table.

| Style    | Description                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| list     | Non-featured posts are rendered in a standard style, similar to what you see on most sites.    |
| card     | Non-featured as cards (a block with preview image, title, tag(s), and excerpt.                 |
| carousel | Featured posts are displayed as one card that automatically scrolls between the `count` posts. |

### Example

An example of the supported settings is demonstrated in the following snippet.

<tabs>
<tab title="Jekyll">

In the `_jekyllfaces/config.md` file, include an `archive` entry under the `blog` entry in the page metadata.
<br/><br/>

```
customize:
  blog:
    archive:
      recent: false
      featured: true
      count: 3
      style: list
  ...
```
</tab>
<tab title="Eleventy">

In the `_data/site.js` file, include an `archive` entry under the `blog` entry in the `module.exports`.
<br/><br/>

```
module.exports = {
  customize: {
    blog: {
      archive: {
        recent: false,
        featured: true,
        count: 3,
        style: "list",
      },
    },
    ...
  },
};
```
</tab>
</tabs>
