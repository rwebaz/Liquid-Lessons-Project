---
title: Relative Anchors
layout: default
navigation_weight: 9
---
# Relative Anchors

How To Craft An Internal Hyperlink In Markdown With Liquid

{% include toc-flammarion.md %}

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

{% include sources-and-uses.md %}

### External Sources

- The [Project Source Links](https://mminail.github.io/Liquid/Source-Liquid-Links.htm){:title="Click to Visit the Source Links page of the Liquid Lessons Project at GitHub pages"}{:target="_blank"} page of the Liquid Lessons Project. Published by © 2017 [Mminail.github.io](https://mminail.github.io/){:title="Click to Visit the Concept Library of the Medical Marijuana Initiative of North America - International Limited, an Arizona Benefit Corporation"}{:target="_blank"}.

- [How To Convert an Html Site To Jekyll](http://jekyllrb.com/tutorials/convert-site-to-jekyll/){:title="Click to Visit How To Convert an Html Site To Jekyll"}{:target="_blank"}. Published by © 2017 [Jekyllrb.com](http://jekyllrb.com){:title="Click to Visit Jekyllrb dot com"}{:target="_blank"}.
