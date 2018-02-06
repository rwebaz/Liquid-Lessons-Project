---
title: Liquid Variables
layout: default
excerpt: Variables in Liquid are declared at the Yaml front matter section of the page ...
navigation_weight: 8
version: Markdown Page Template md Dtd 02-05-18 am
categories: frontmatter
---
# {{ page.title }}

{{ page.excerpt }}

{% include toc.md %}

## Importing Variables

By placing a variable in the `yaml` *front matter* of your page ...

That variable can then be used multiple times throughout the content of your page.

### Liquid Comments

How to craft a Liquid comment statement in Jekyll ...

#### Simple Comment

In a *simple* **Liquid Comment** statement in Jekyll place your text between the `comment` and the `endcomment` tags, as follows:

```liquid
{% raw %}
{% comment %}
Developer notes go inside ...
{% endcomment %}
{% endraw %}
```

For example, here is a Liquid comment tag that takes advantage of the now available variable placement.

As follows,

```liquid
{% raw %}
{% comment %}version{% endcomment %}
{% endraw %}
```

**Note**. When the page is rendered, the `value` stored inside the variable `version`, in this case a `String` ...

Becomes *applied* within the enclosing Liquid tag.

The variable namespace `version` is actually pointing to the location within the page memory stack where the data of the `String` type `value` is stored.

The `value` of the namespace `version` is then output to the screen.

As follows *live* ...

[{% comment %}version{% endcomment %}]

What happened?

Where is the comment?

**Answer**: When using a Liquid comment tag to define a page comment ...

The comment tag is placed on the page for the benefit of the developer.

Not the end-user.

You can see this in the source view of the page by clicking `view`, `developer`, `view source` from the main menu of your Chrome browser window.

Zip, zero, nada.

The program pulls the contents of the `String` value from the declared `yaml` front matter variable, places the value within the Liquid comment statement, and displays nothing.

Not even in the source of the page!

#### Complex Comment

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
{:hello ... this is an example of a Liquid tag.
But, you cannot execute me ...
Because I am enveloped within a set of {% raw - endraw %} liquid tags.}
{% endcomment %}
{% endraw %}
```

**Note**. The set of `comment - endcomment` Liquid tags will hide the text from the end-user as a comment, but any code statements will not be hidden from the Liquid compiler in Jekyll.

Hence, when rendering a *complex* **Liquid Comment** statement in Jekyll, wrap your set of `comment - endcomment` Liquid tags inside a set of `raw - endraw` Liquid tags, too.

## Import Code

More to come ...

## Last Subtitle

Place the introducing line of text ie.) the 'tagline' here ...

### Raw Code Block

```liquid
{% raw %}
Enjoy the successful output!
{% endraw %}
```

{% include sources-and-uses.md %}

### External Sources

- The [Project Source Links](https://mminail.github.io/Liquid/Source-Liquid-Links.htm){:title="Click to Visit the Source Links page of the Liquid Lessons Project at GitHub pages"}{:target="_blank"} page of the Liquid Lessons Project. Published by © 2017 - 2018 [Mminail.github.io](https://mminail.github.io/){:title="Click to Visit the Concept Library of the Medical Marijuana Initiative of North America - International Limited, an Arizona Benefit Corporation"}{:target="_blank"}.
