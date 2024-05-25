# Horizontal Rule

To separate sections of text, you can inject an HR widget.



## Options

The following options are supported by this widget.

size
: Specify the size in pixels of the horizontal rule.
: ex: 3px

color
: Specify the color of the horizontal rule.
: ex: cornflowerblue

opacity
: Specify the opacity of the horizontal rule.
: ex: 75%

config
: **(OPTIONAL)** A copy of the config hash. See the snippet that follows. This option reduces the number of times the site configuration values are queried, speding up the process of building the site.

<tabs>
<tab title="Jekyll">

```
    {% include read-config.liquid %}
    {% include countdown.widget config=config launchDate="2024-01-09T05:00:00.000Z" %}}
```
</tab>
<tab title="Eleventy">

```
    {% include 'countdown.widget' config=site.config launchDate:'2024-01-09T05:00:00.000Z' %}
```
</tab>
</tabs>



## Usage

There are several ways to incorporate this widget into your pages.

### Inline

If you have more than one countdown target datetime, you can specify each directly on the widget.

<tabs>
<tab title="Jekyll">

```
    {% include hr.widget size="3px" %}
```
</tab>
<tab title="Eleventy">

```
    {% include 'hr.widget' size:'3px' %}
```
</tab>
</tabs>



### Page Metadata

If you want to have multiple hr widgets on the same page, you can set the style values in the page's metadata.

<tabs>
<tab title="Jekyll">

```
---
hr:
  color:   white
  size:    2px
  opacity: 75%
---
{% include hr.widget %}
```
</tab>
<tab title="Eleventy">

```
---
hr:
  color:   white
  size:    2px
  opacity: 75%
---
{% include 'hr.widget' %}
```
</tab>
</tabs>



### Site Config

If you want to have multiple hr widgets on the same page, you can set the style values in the page's metadata.
If the countdown widget is used across the site in multiple places, you can store the target datetime in the site config.

<tabs>
<tab title="Jekyll">

<p>In the 'config.yml' file:</p><br/>

```
    launchDate: "2024-01-09T05:00:00.000Z"
```

<p>In the 'my-page.md' file:</p><br/>

```
    {% include countdown.widget %}
```
</tab>
<tab title="Eleventy">

<p>In the 'config.yml' file:</p><br/>

```
    launchDate: "2024-01-09T05:00:00.000Z"
```

<p>In the 'my-page.md' file:</p><br/>

```
    {% include 'countdown.widget' %}
```
</tab>
</tabs>



<seealso>
    <!--Provide links to related how-to guides, overviews, and tutorials.-->
</seealso>

