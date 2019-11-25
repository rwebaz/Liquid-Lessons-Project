---
title: Liquid TOC
layout: default
excerpt: Only one Table of Contents code block is allowed per page in Markdown ...
hint: Place the intro paragraph ie.) the 'hypothesis' here ...
repo: Liquid-Lessons-Project
ver_date: 11-20-19
navigation_weight: 8
categories: page 
---
{% include toc.md %}

## First Subtitle

> **Hint**. {{ page.hint }}

More to come ...

## Table O Contents Section

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

More to come ...

***

**Note**. The above synopsis was derived from an article written by Blank Author [[1](#BLANKAUTHOR){:.red}].

1. {:#BLANKAUTHOR}[A Narrative of Psychology by Blank Author, Jan #1999](http://cowles.yale.edu/sites/default/files/files/pub/d20/d2069.pdf){:target="_blank"}

***

{% include patreon-link.md %}
