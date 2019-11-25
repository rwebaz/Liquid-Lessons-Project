---
title: Relative Anchors
layout: default
excerpt: How to craft an internal Anchor Link in Markdown with Liquid ...
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

## Targeting SubTitles

If you wish to target a certain heading or sub-heading within a page at landing time, simply append the designated pathway with a sharp symbol `#` followed by the **Location ID** of the selected heading or sub-heading, as follows:

### Finale Anchor

#### The Code: Short Cut ( Relative ) Anchor

```liquid
{% raw %}
[Liquid Lessons Project]({{ "/pages/Craft-A-Link#Long Cut Links" | relative_url }}){:target="_blank"}
{% endraw %}
```

#### Live Link: Short Cut ( Relative ) Anchor

Putting it all together yields the following **Live** rendition ...

[Liquid Lessons Project]({{ "/pages/Craft-A-Link#Long Cut Links" | relative_url }}){:target="_blank"}

## Subtitle

Place the introducing line of text ie.) the 'tagline' here ...

### Another Example

Taking the code of our already completed *long-cut* external hyperlink from the beginning of this tutorial ...

See: [Long Cut Links]({{ "/pages/Craft-A-Link#Long Cut Links" | relative_url }}){:target="_blank"} ), we may now inject our **Liquid** moustache statement into the mix, as follows:

## Last Subtitle

More to come ...

***

**Note**. The above synopsis was derived from an article written by Jekyll RB [[1](#JEKYLLRB){:.red}].

1. {:#JEKYLLRB}[How To Convert an Html Site To Jekyll](http://jekyllrb.com/tutorials/convert-site-to-jekyll/){:title="Click to Visit How To Convert an Html Site To Jekyll"}{:target="_blank"}. Published by © 2017 [Jekyllrb.com](http://jekyllrb.com){:title="Click to Visit Jekyllrb dot com"}{:target="_blank"}.

***

{% include patreon-link.md %}
