# 404 Pages

If you're tired of seeing the same old 404 error page for your GitHub Pages, [JekyllFaces](https://jekyllfaces.com/) provides you with a canned selection of humorous(?) alternatives. 

## Usage

In your site configuration, set the variable `http404` to one of the following values.

| Value   |   | Description                                        |
|---------|---|----------------------------------------------------|
| badge   |   | You've unlocked the 404 achievement!               |
| default |   | For those that prefer a more traditional 404 page. |
| dog     |   | Oops. The dog ate your page!                       |
| droids  |   | These aren't the droids you're looking for...      |
| glass   |   | You broke the site!                                |
| link    |   | You have found a dead Link.                        |
| milk    |   | Have you seen my page?                             |
| monster |   | A monster has your page. We're not going near it.  |
| potty   |   | Crap! We ran out of paper.                         |
| shrug   |   | Beats me. ¯\\\_(ツ)_/¯                              |
| sticky  |   | We'll make a note of it.                           |
| tweet   |   | Tell your friend(s).                               |
| zork    |   | Old skool message about choices and decisions.     |



<tabs>
<tab title="Jekyll">

In the `_jekyllfaces/config.md` file, include an `http404` entry in the page metadata.
<br/><br/>

```
customize:
  http404: badge
  ...
```
</tab>
<tab title="Eleventy">

In the `_data/site.js` file, include an `http404` entry in the `module.exports`.
<br/><br/>

```
module.exports = {
  customize: {
    http404: "badge",
    ...
  }
};
```
</tab>
</tabs>
