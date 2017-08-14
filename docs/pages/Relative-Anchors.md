---
title: Relative Anchors
layout: default
navigation_weight: 9
---
# Relative Anchors

## How To Craft An Internal Hyperlink In Markdown With Liquid

## Table O Contents

![MMI™ Flammarion Logo Badge](../assets/img/MMI-Medmj-Org-Got-Tree-Flammarion-Person-Through-Celestial-Sphere-circle-725-x-725.svg){:height="120px" width="120px"}

**Note**. The above **Live** rendition of the **MMI™ Flammarion Logo Badge** `( .svg )` image file is set to the dimensions of 120.00px x 120.00px.

- TOC
{:toc}

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

## Raw Code

Place the introducing line of text ie.) the 'tagline' here ...

```liquid
{% raw %}
`...`
{% endraw %}
```

## The Flammarion

{% include flammarion-text.htm %}

![MMI™ Flammarion Logo Badge](../assets/img/MMI-Medmj-Org-Got-Tree-Flammarion-Person-Through-Celestial-Sphere-circle-725-x-725.svg){:height="500px" width="500px"}

## Sources and Uses

The source and use of 3rd party materials in the creation of this **Markdown** page is greatly appreciated.

Most authors and publishers will allow for the abbreviated reproduction of their works in part when the case of brief quotations or ideas embodied in critical articles or reviews becomes necessary to further the understanding of the end-user's learning process.

Indeed, ping-backs to the original sources are welcome by the readers, the authors, and the publishers of instructional hard copies.

Therefore, it is the policy of the **[MMINAIL][3]** to always provide a **Ping Back** to the original author, or to the publisher of the original publication when citing 3rd party work.

### Inline References

1. [Inline Images](https://rwebaz.github.io/Markdown-Lessons-Project/pages/Inline-Images.html){:title="Click to Visit the Inline Images Page at GitHub"}{:target="_blank"}. Inline images may be displayed in Markdown using the exclamation point `!` followed by a bracketed `[Alt Text]` followed by a relative `URL` enclosed in a single set of parenthesis `(...)`. Published by © 2017 [Mminail.github.io](https://mminail.github.io/){:title="Click to Visit the current Home Page of the Medical Marijuana Initiative of North America - International Limited, an Arizona Benefit Corporation"}{:target="_blank"}.

1. [Markdown Lessons Project](https://rwebaz.github.io/Markdown-Lessons-Project/){:title="Click to Visit the Markdown Lesson Project Template - Home Page at GitHub"){:target="_blank"}. The Markdown Lessons Project is a Git Hub repo of coding lessons that emphasize both the GFM and Kramdown engines. Published by © 2017 [Mminail.github.io](https://mminail.github.io/){:title="Click to Visit the current Home Page of the Medical Marijuana Initiative of North America - International Limited, an Arizona Benefit Corporation"}{:target="_blank"}.

1. [MMINAIL](https://mminail.github.io/){:title="Click to Visit the current Home Page of the Medical Marijuana Initiative of North America - International Limited, an Arizona Benefit Corporation"}{:target="_blank"}. The MMINAIL is an acronym for the Medical Marijuana Initiative of North America - International Limited, an Arizona Benefit Corporation. Published by © 2017 [Mminail.github.io](https://mminail.github.io/){:title="Click to Visit the current Home Page of the Medical Marijuana Initiative of North America - International Limited, an Arizona Benefit Corporation"}{:target="_blank"}.

### External Sources

- [Instructional Jekyll Tips n Vids by Cloud Cannon](https://learn.cloudcannon.com/){:target="_blank"}. Published by © 2017 [Cloudcannon.com](https://www.cloudcannon.com){:target="_blank"}.

- [How To Convert an Html Site To Jekyll](http://jekyllrb.com/tutorials/convert-site-to-jekyll/). Published by © 2017 [Jekyllrb.com](http://jekyllrb.com){:target="_blank"}.
