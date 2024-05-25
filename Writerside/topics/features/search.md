# Search

If you want search for your Jekyll site, you'll have to roll your own. JekyllFaces provides support for searching your site's content out of the box.


## Usage

In your site configuration, there is an entry for every supported searchable content type. You can enable searching across all content with a `scope: all` entry, or use more granular settings.


| Target      | Allowed Values         | Description                                         |
|-------------|------------------------|-----------------------------------------------------|
| scope       | all / none / mixed     | full search, no search, or use granular settings    | 
| posts       | false / full / excerpt | post content (when scope is "mixed" or "all")       | 
| pages       | false / full / excerpt | page content (when scope is "mixed" or "all")       |
| titles      | false / true           | include titles (when scope is "mixed" or "all")     |
| tags        | false / true           | include tags (when scope is "mixed" or "all")       |
| categories  | false / true           | include categories (when scope is "mixed" or "all") |
| filenames   | false / true           | include filenames (when scope is "mixed" or "all")  |
| ignore      | (file list)            | list of extensions to ignore                        |
| groups      | (path list)            | content groups                                      |
| strip_chars | (string)               | list of characters to omit                          |



For example, to include search for only blog posts and page excerpts, edit your configuration to resemble the following.

<tabs>
<tab title="Jekyll">

In the `_jekyllfaces/config.md` file, update the `search` entries in the page metadata.
<br/><br/>

```
search:
  scope: mixed   # <========
  posts: true    # <========
  pages: excerpt # <========
  titles: false
  tags: false
  categories: false
  filenames: false
  ignore: [ ".css", ".js", ".json", ".xml", "/404.html", "/custom.html", "/status.html" ]
  groups: [ "/content/contributors/", "/content/legal/" ]
  strip_chars: "|'.,:;!?├─└…()[]#-/{}’!@#$%^&*=+“”\\<>~`"

```
</tab>
<tab title="Eleventy">

In the `_data/site.js` file, update the `search` entries in the `module.exports`.
<br/><br/>

```
module.exports = {
  search: {
    scope: "mixed",   // <========
    posts: true,      // <========
    pages: "excerpt", // <========
    titles: false,
    tags: false,
    categories: false,
    filenames: false,
    ignore: [ ".css", ".js", ".json", ".xml", "/404.html", "/custom.html", "/status.html" ],
    groups: [ "/content/contributors/", "/content/legal/" ],
    strip_chars: "|'.,:;!?├─└…()[]#-/{}’!@#$%^&*=+\"\\<>~`",
  },
  ...
};
```
</tab>
</tabs>

