---
title: Liquid-Comments
layout: default
excerpt: How to craft a Liquid comment statement in Jekyll ...
navigation_weight: 8
categories: jekyll liquid
---
# Liquid Comments

{{ page.excerpt }}

{% include toc-flammarion.md %}

## Simple Comment

In a *simple* **Liquid Comment** statement in Jekyll place your text between the `comment` and the `endcomment` tags, as follows:

```liquid
{% raw %}
{% comment %}
Developer notes go inside ...
{% endcomment %}
{% endraw %}
```

## Complex Comment

In a *complex* **Liquid Comment** statement in Jekyll place your text and/or code between the `comment` and the `endcomment` tags, as well.

As follows:

```liquid
{% raw %}
{% comment %}
- TOC
{:toc}
{% endcomment %}
{% endraw %}
```

**Note**. When rendering *complex* comments in Markdown each and every Liquid statement within must be enveloped in a set of `raw` Liquid tags to avoid execution, as follows:

```liquid
{% raw %}
{% comment %}
{:hello ... this is an example of a Liquid tag. But, you cannot execute me because I am enveloped within a set of `raw` liquid tags.}
{% endcomment %}
{% endraw %}
```

**Note**. The set of `comment - endcomment` Liquid tags will hide the text from the end-user as a comment, but any code statements will not be hidden from the Liquid compiler in Jekyll.

Hence, when rendering a *complex* **Liquid Comment** statement in Jekyll, wrap your set of `comment - endcomment` Liquid tags inside a set of `raw - endraw` Liquid tags, too.

## Table O Contents

**Rule**. Only one Table of Contents code block is allowed per page in Markdown.

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
