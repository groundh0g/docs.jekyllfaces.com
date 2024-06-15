# Writing Compatible Markdown

Eleventy is based heavily on Jekyll. But there are some differences that have to be accounted or when writing markdown that works in both static site generators.

## Shortcodes Example - Highlight

For one example, Jekyll has a built-in liquid statement for syntax highlighting code snippets.

```
{% highlight css %}
body {
  font-size: 1.2em;
}
{% endhighlight %}
```

In this Jekyll shortcode, `css` is the target language, and it is specified as shown (without quotes). There is no equivalent shortcode in Eleventy, but it does allow me to add my own shortcodes. So, I created a `highlight` shortcode for Eleventy.

The Eleventy version of the above code snippet is as follows. Note the quotes around "css".

```
{% highlight "css" %}
body {
  font-size: 1.2em;
}
{% endhighlight %}
```

Shortcodes accept parameters. In Jekyll's shortcodes, string values are passed without the quotes, but in Eleventy's shortcodes, the quotes are expected. Luckily, both types of shortcodes accept variables. So, by adding the parameter as a variable, both shortcode variants will behave as expected.

```
{% assign css = "css" %}
{% highlight css %}
body {
  font-size: 1.2em;
}
{% endhighlight %}
```

Note the subtle difference. We just added a line to assign the string value to a variable, and passed that variable into the shortcode. This way, both Jekyll and Eleventy are satisfied.

> **NOTE:** If you don't care about writing markdown that works in both site generators, use the syntax that suits your choice. You need not add the extra line of logic.
