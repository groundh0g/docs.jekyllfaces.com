# Image

The image widget allows you to easily add an image (and its alt text) to your markdown without dropping to HTML.


## Options

The following options are supported by this widget.

file
: Specify the relative path of the image file.
: ex: "/assets/images/foo.png"

id
: **(OPTIONAL)** Specify the DOM element ID.
: ex: "MyImageFoo"

alt
: **(OPTIONAL)** Specify the alt text for the image, used by screen readers.
: ex: "An image of the infamous 'Foo'."

collapsible
: **(OPTIONAL)** Specify whether this image should be toggled between hidden and shown.
: one of: true | false

config
: **(OPTIONAL)** A copy of the config hash. See the snippet that follows. This option reduces the number of times the site configuration values are queried, speding up the process of building the site.

<tabs>
<tab title="Jekyll">

```
    {% include read-config.liquid %}
    {% include image.widget config=config file="fooBar.png" %}}
```
</tab>
<tab title="Eleventy">

```
    {% include 'image.widget' config=site.config file:'fooBar.png' %}
```
</tab>
</tabs>



> **NOTE:** The site configuration defaults to strict mode, where many optional parameters become required. To disable this behavior (and make those parameters truly optional), add the following to your config.
> ```
> widgets:
>   strict: false
> ```



## Usage

There are several ways to incorporate this widget into your pages.

### Inline

If you have more than one countdown target datetime, you can specify each directly on the widget.

<tabs>
<tab title="Jekyll">

```
    {% include image.widget file="fooBar.png" %}
```
</tab>
<tab title="Eleventy">

```
    {% include 'image.widget' file:'fooBar.png' %}
```
</tab>
</tabs>



### Page Metadata

If you want to have multiple countdown widgets on the same page, you can set the target datetime in the page's metadata.

<tabs>
<tab title="Jekyll">

```
---
launchDate: 2024-01-09T05:00:00.000Z
---
{% include countdown.widget %}
```
</tab>
<tab title="Eleventy">

```
---
launchDate: 2024-01-09T05:00:00.000Z
---
{% include 'countdown.widget' %}
```
</tab>
</tabs>



### Site Config

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

