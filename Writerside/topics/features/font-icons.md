# Font Icons

[JekyllFaces](https://jekyllfaces.com/) provides support for several popular font icon sets. The majority of which support loading the icons from a local copy that's stored on your site, or a copy that's served from one of several content delivery networks (CDNs).

Supported font icon sets include:

| Font Icon                                                                  | Allowed Values       
|----------------------------------------------------------------------------|----------------------|
| [boxicons](https://boxicons.com/)                                          | false / local / cdn  |
| [codicons](https://microsoft.github.io/vscode-codicons/)                   | false / local        |
| [devicons](https://vorillaz.github.io/devicons/#/main)                     | false / local / cdn  |
| [drip](http://demo.amitjakhu.com/dripicons/)                               | false / local / cdn  |
| [elegant](https://www.elegantthemes.com/blog/resources/elegant-icon-font)  | false / local        |
| [fontawesome](https://fontawesome.com/search?m=free&o=r)                   | false / local / cdn  |
| [foundation](https://zurb.com/playground/foundation-icon-fonts-3)          | false / local / cdn  |
| [glyphicons](https://www.glyphicons.com/)                                  | false / local        |
| [helium](https://tympanus.net/codrops/2014/10/10/freebie-helium-icon-set/) | false / local        |
| [icomoon](https://icomoon.io/#icons)                                       | false / local / cdn  |
| [ionicons](https://ionic.io/ionicons)                                      | false / local / cdn  |
| [linear](https://linearicons.com/free)                                     | false / local        |
| [lineawesome](https://icons8.com/line-awesome/howto)                       | false / local / cdn  |
| [lineicons](https://lineicons.com/download/)                               | false / local / cdn  |
| [material](https://fonts.google.com/icons)                                 | false / local / cdn  |
| [octicons](https://primer.style/foundations/icons/)                        | false / local / cdn  |
| [themify](https://themify.me/themify-icons)                                | false / local / cdn  |
| [tonicons](https://www.tonicons.com/font-tonicons/)                        | false / local        |
| [zondicons](https://www.zondicons.com/)                                    | false / local        |



## Usage

In your site configuration, there is an entry for every supported font icon set. You enable the icons (zero, one, or more) by setting the value next to the name to one of `false`, `local`, or `cdn`.

For example, to include the Font Awesome icons from a CDN, you would edit your configuration to resemble the following.

<tabs>
<tab title="Jekyll">

In the `_jekyllfaces/config.md` file, update the `fontawesome` entry in the page metadata.
<br/><br/>

```
customize:
  fonticons:
    fontawesome: 
      include: cdn
      website: https://fontawesome.com/search?m=free&o=r
    ...
```
</tab>
<tab title="Eleventy">

In the `_data/site.js` file, update the `fontawesome` entry in the `module.exports`.
<br/><br/>

```
module.exports = {
  customize: {
    fonticons: {
      fontawesome: {
        include: "cdn",
        website: "https://fontawesome.com/search?m=free&o=r",
      },
      ...
    },
  }
};
```
</tab>
</tabs>

