---
title: Craft A Link
layout: default
navigation_weight: 9
---
# Craft A Link

## How To Craft An External Hyperlink In Markdown With Liquid

Placing strategic **Liquid** statements enveloped with {% raw %}{{ double sets of curly braces }}{% endraw %} will offer a shortcut to the more common long form way of expressing **Markdown** external hyperlinks.

{% include toc.htm %}

## Long Cut Links

In **Markdown**, a *long-cut* external hyperlink is crafted with a train of connected statements consisting of first the bracketed clickable text, as follows:

### The Code

```markdown
{% raw %}
[Liquid Lessons Project]
{% endraw %}
```

After establishing the bracketed clickable text, next the developer appends the full *long-cut* external Url within a set of single parenthesis `(...)`, as shown below:

```markdown
{% raw %}
[Liquid Lessons Project](https://rwebaz.github.io/Liquid-Lessons-Project/)
{% endraw %}
```

**Note**. A full *long-cut* external Url in **Markdown** is written the same way as an absolute Url in **Html**.

### Finale Liquid

Finally, a **Liquid** statement may be appended to the tail end of the **Markdown** hyperlink chain in order to designate a target of self or blank.

```markdown
{% raw %}
[Liquid Lessons Project](https://rwebaz.github.io/Liquid-Lessons-Project/){:target="_blank"}
{% endraw %}
```

### Live Link

Putting it all together yields the following **Live** rendition ...

- [Liquid Lessons Project](https://rwebaz.github.io/Liquid-Lessons-Project/){:target="_blank"}

## Short Cut Links

**Liquid** *short-cut* external hyperlinks can replace some of the more static elements of a **Markdown** *long-cut* hyperlink with *moustache* statements.

**Note**. A **Liquid** *moustache* is simply another way to say {% raw %}{{ double sets of curly braces }}{% endraw %} with the double sets of curly braces resembling a sort of caricature moustache, don't you see.

### Break It Down Relatively

An analysis of a **Markdown** *long-cut* hyperlink consists of the following primary elements:

1. **Link Title**
- The Title of The Destination
1. **Link Url Full**
- The Full Url
1. **Target Statement**
- The Landing Page ( Self or Blank )

### Dissect Further

The full Url of a hyperlink may be dissected further to reveal the following sub-elements eligible for consideration as static **Liquid** variables:

#### baseurl

1. **Base Url**
- The Directory From Which The Files Are Served
1. **Url**
- The Parental Web Address of Your Designated Project

**Note**. Both the **Base Url** and **Url** may be set in stone as **Liquid** variables via the **Config dot yaml** file.

The `config.yml` file is stored in the docs folder of your repo.

### Base Url Example #1

The **Base Url** represents a static variable named `baseurl` that can be set inside your `config.yml` file representing the subpath of your designated project, e.g. /blog, as follows:

```liquid
{% raw %}
# The 'baseurl' is the subpath of your designated project
baseurl: "/Liquid-Lessons-Project"
{% endraw %}
```

The `baseurl` may then be placed within the *long-cut* hyperlink if locked inside a **Liquid** moustache statement.

An application of this code avoids the repetition of always having to type the same repo subpath when crafting an external hyperlink.

#### Unix Pipe

Let's establish a **Liquid** moustache statement that uses a **Unix** pipe to send the value of your designated path to the built-in site method `relative_url`, also known as a *filter*.

```liquid
{% raw %}
{{ "/" | relative_url }}
{% endraw %}
```

The built-in site method `relative_url` instructs your development machine to fetch the value of the variable **baseurl** from the **Config dot yaml** file and then prepend the **baseurl** variable to your path entry as shown above in order to create a valid relative link programmatically.

A little backwards, heh?

But, it works!

In effect, we have crafted programmatically the following **long-cut** Url:

```liquid
{% raw %}
[Liquid Lessons Project](../Liquid-Lessons-Project/){:target="_blank"}
{% endraw %}
```

From the following **short-cut** Url statement ...

#### The Code: Short Cut ( Relative ) #1

```liquid
{% raw %}
[Liquid Lessons Project](../{{ "/" | relative_url }}){:target="_blank"}
{% endraw %}
```

**Note**. By setting the path with simply the slash key `"/"` we have invoked the index page of the project.

The path `"/"` shown above is the directory from which your 'index dot md' page will be served, as well as the md files located in the `docs` subdirectory named `pages`.

In this case, we are serving our files via **Git Hub Pages** using the `docs` directory.

The `docs` directory, therefore, becomes the root directory `"/"` for our 'index dot md' file as well as for our 'pages' subdirectory.

Prepending the **baseurl** onto the `"/"` produces, in **long-cut**, the following relative Url statement ...

#### The Code: Long Cut ( Relative ) #1

```liquid
{% raw %}
[Liquid Lessons Project](../Liquid-Lessons-Project/){:target="_blank"}
{% endraw %}
```

Where, the 'Liquid-Lessons-Project' is the variable **baseurl**.

### Base Url Example #2

Here, we are prepending via the **Unix Pipe** the **baseurl** variable from our `config.yml` file onto the pathway shown to create a relative link, as follows:

#### The Code: Long Cut ( Relative ) #2

```liquid
{% raw %}
[Liquid Lessons Project](../Liquid-Lessons-Project/pages/Source-Links){:target="_blank"}
{% endraw %}
```

**Note**. It is not required to place a suffix after the title of the targeted page in this relative instance.

**Markdown** will infer the type of page from the code inside and **Kramdown** the file into a standard **Html** file with a ( .html ) suffix.

#### From Afar

However, when crafting an external absolute hyperlink from an external html source page ...

When you do target a file that has been **Kramdown**, be sure to reference the standard ( .html ) suffix.

#### Live Link: Short Cut ( Relative ) #2

Putting it all together yields the following **Live** rendition ...

- [Liquid Lessons Project]({{ "/pages/Source-Links" | relative_url }}){:target="_blank"}

### Flipping The Switch

If we now substitute the `relative_url` method with the built-in `absolute_url` site method, or *filter*, then the program will instruct your development machine to fetch the value of BOTH the variable **baseurl** ( as in the `relative_url` method shown above ) plus the variable **url**, as well.

Let's try that ...

#### url

Recall from above, the full Url of a hyperlink may be dissected further to reveal the following sub-elements eligible for consideration as static **Liquid** statements:

1. **Base Url**
- The Directory From Which The Files Are Served
1. **Url**
- The Parental Web Address of Your Designated Project

Recall further, that BOTH the **Base Url** and the **Url** may be set in stone as **Liquid** variables via the **Config dot yaml** file stored in the `docs` folder of your repo.

### Absolute Short Cut Links

The **url** is a static variable set inside your `config.yml` file representing the parental web address of your designated project.

This variable can be placed within the code statement of your *short-cut* hyperlink locked inside a **Liquid** moustache statement to avoid the repetition of always having to type the same **url**, or parental web address of your designated project ... all the time, as follows:

#### The Code: Short Cut ( Absolute )

```liquid
{% raw %}
[Liquid Lessons Project]({{ "/index" | absolute_url }}){:target="_blank"}
{% endraw %}
```

#### Live Link: Short Cut ( Absolute )

Putting it all together yields the following **Live** rendition ...

[Liquid Lessons Project]({{ "/index" | absolute_url }}){:target="_blank"}

**Note**. When the "absolute" version of the filter is used, the method instructs your machine to prepend first the value of the **url** variable, then the variable of the **baseurl** to your designated path.

Locally, when rendering the page over your local Jekyll server, **localhost** is substituted for BOTH of the variables.

However, when rendering the page over the remote Jekyll server at the Git Hub Pages server farm, we have transformed the code from the above **short-cut** link to the following code more conducive to the rendering of a **long-cut** link, as follows:

[Liquid Lessons Project](https://rwebaz.github.io/Liquid-Lessons-Project/index){:target="_blank"}

Where, 'rwebaz.github.io' is the parental web address of your designated project, or **url** variable and **baseurl** is the subpath of your designated project, in this case '/Liquid-Lessons-Project`.

Another way to put it is ...

Your designated `path` ( in this case "/index" ) is prepended by the **url** variable appended by the **baseurl** variable!

## Execution

If we hover over each live rendition shown above, we should see at the bottom of your browser ( if your status bar is enabled ) the pathways of both the **long-cut** and **short-cut** Urls as compiled.

### Hover Over

Simply hover over each of the above "long" and the "short" links, and then spy the **Status Bar** at the bottom of your browser.

### Status Bar

The **Status Bar** will show each link as compiled, when hovered over.

{% include flammarion-text.htm %}

{% include flammarion-svg.htm %}

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

- [How To Convert an Html Site To Jekyll](https://jekyllrb.com/tutorials/convert-site-to-jekyll/). Published by © 2017 [Jekyllrb.com](https://jekyllrb.com){:target="_blank"}.
