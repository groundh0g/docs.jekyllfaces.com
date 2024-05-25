# Countdown

Generate a little buzz for your project by adding a countdown widget to your page. 
The timer will use the current datetime and your specified datetime to determine how much time is left in the countdown.
If the time runs out, the countdown will stop (at '0d 0h 0m 0s').



## Options

The following options are supported by this widget.

launchDate
: Specify the exact time that the countdown should end, as a UTC datetime value.
: ex: "2024-10-09T05:00:00.000Z"

config
: **(OPTIONAL)** A copy of the config hash. See the snippet that follows. This option reduces the number of times the site configuration values are queried, speeding up the process of building the site.

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
    {% include countdown.widget launchDate="2024-01-09T05:00:00.000Z" %}
```
</tab>
<tab title="Eleventy">

```
    {% include 'countdown.widget' launchDate:'2024-01-09T05:00:00.000Z' %}
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

