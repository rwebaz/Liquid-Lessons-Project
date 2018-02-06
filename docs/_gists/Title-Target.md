---
title: Title Target
layout: default
navigation_weight: 8
---
# Title Target

How To Force a New Target Blank When Clicking A GFM Hyperlink

{% include toc.md %}

## Solution

To route an external link to a new tabbed page within your browser ...

From your GitHub Flavored Markdown, or **GFM** `(.md)` page ...

Append your `(.md)` external link with the `{:target="_blank"}` kramdown statement, as follows:

## The Code

```liquid
{% raw %}
[temporarily disable liquid tag processing](https://shopify.github.io/liquid/tags/raw/){:target="_blank"}
{% endraw %}
```

## Summation

The components of a successful external link in markdown are, as follows:

- First, clickable text enveloped in a single set of bracket characters `[...]`
- Followed by, the complete URI for the targeted destination enveloped in a single set of parenthesis characters `(...)`, and
- Thirdly, the given kramdown statement

{% include sources-and-uses.md %}

### External Sources

- The [Project Source Links](https://mminail.github.io/Liquid/Source-Liquid-Links.htm){:title="Click to Visit the Source Links page of the Liquid Lessons Project at GitHub pages"}{:target="_blank"} page of the Liquid Lessons Project. Published by © 2017 [Mminail.github.io](https://mminail.github.io/){:title="Click to Visit the Concept Library of the Medical Marijuana Initiative of North America - International Limited, an Arizona Benefit Corporation"}{:target="_blank"}.

- [Temporarily disable liquid tag processing](https://shopify.github.io/liquid/tags/raw/){:title="Click to Visit ..."}{:target="_blank"}
