---
title: Page Path
layout: default
navigation_weight: 9
---
# Page Path

Couple two *moustache* or **Liquid Variable Statements** ...

{% include toc-flammarion.md %}

## Site baseurl

One the `site.baseurl` and the other the `page.path` to illustrate the absolute path of a page, as follows:

## The Code

```liquid
{% raw %}
{{ site.baseurl }}{{ page.path }}
{% endraw %}
```

### Live

**Por ejemplo en vivo**. {{ site.baseurl }}{{ page.path }}

{% include sources-and-uses.md %}

### External Sources

- The [Project Source Links](https://mminail.github.io/Liquid/Source-Liquid-Links.htm){:title="Click to Visit the Source Links page of the Liquid Lessons Project at GitHub pages"}{:target="_blank"} page of the Liquid Lessons Project. Published by © 2017 [Mminail.github.io](https://mminail.github.io/){:title="Click to Visit the Concept Library of the Medical Marijuana Initiative of North America - International Limited, an Arizona Benefit Corporation"}{:target="_blank"}.