---
title: Liquid TOC
layout: default
excerpt: Only one Table of Contents code block is allowed per page in Markdown ...
navigation_weight: 8
categories: 
---
# Liquid TOC

{{ page.excerpt }}

{% comment %}Markdown Page Template md Dtd 02-04-18{% endcomment %}

{% include toc.md %}

## Table O Contents

To illustrate ...

```liquid
{% raw %}
- TOC
{:toc}
{% endraw %}
```

**Note**. In the above example, when placed below another similar *TOC* code block, the secondary code block is rendered mute, as follows:

```liquid
{% raw %}
Original *TOC* code block ...
- TOC
{:toc}
===========
- TOC
{:toc}
Secondary *TOC* code block ...
{% endraw %}
```

**Note**. Though separated by a line of text `===`, the secondary *TOC* code block will not render.

## Last Subtitle

{{ site.description }}

### Raw Code Block

```liquid
{% raw %}
Enjoy the successful output!
{% endraw %}
```

{% include sources-and-uses.md %}

### External Sources

- The [Project Source Links](https://mminail.github.io/Liquid/Source-Liquid-Links.htm){:title='Click to Visit the Source Links page of the Liquid Lessons Project at GitHub pages'}{:target='_blank'} page of the Liquid Lessons Project. Published by © 2017 - 2018 [Mminail.github.io](https://mminail.github.io/){:title='Click to Visit the Home Page of the Concept Library at the Medical Marijuana Initiative of North America - International Limited, an Arizona Benefit Corporation'}{:target='_blank'}.
