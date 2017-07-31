---
title: Page Path
layout: default
navigation_weight: 9
---
# Page Path

Couple two *moustache* or **Liquid Variable Statements** ...

One the `site.baseurl` and the other the `page.path` to illustrate the absolute path of a page, as follows:

## The Code

```liquid
{% raw %}
{{ site.baseurl }}{{ page.path }}
{% endraw %}
```

### Live

**Por ejemplo en vivo**. {{ site.baseurl }}{{ page.path }}

***

**Source**: [Instructional Jekyll Tips n Vids by Cloud Cannon](https://learn.cloudcannon.com/){:target="_blank"}