---
title: Craft A Link
layout: default
navigation_weight: 9
---
# Craft A Link

## How To Craft A Hyperlink In Markdown With Liquid

Placing strategic **Liquid** statements enveloped with {% raw %}{{ double sets of curly braces }}{% endraw %} will offer a shortcut to the more common long form way of expressing **Markdown** external hyperlinks.

## Table O Contents

![MMI™ Flammarion Logo Badge](../assets/img/MMI-Medmj-Org-Got-Tree-Flammarion-Person-Through-Celestial-Sphere-circle-725-x-725.svg){:height="120px" width="120px"}

**Note**. The above **Live** rendition of the **MMI™ Flammarion Logo Badge** `( .svg )` image file is set to the dimensions of 120.00px x 120.00px.

- TOC
{:toc}

## Long Cut Links

### The Code

In **Markdown**, a *long cut* external hyperlink consists of first the bracketed clickable text, as follows:

```markdown
{% raw %}
[Liquid Lessons Project]
{% endraw %}
```

After establishing the bracketed clickable text, next the developer appends the full *long cut* external Url in a set of single parenthesis, as shown below:

```markdown
{% raw %}
[Liquid Lessons Project](https://rwebaz.github.io/Liquid-Lessons-Project/)
{% endraw %}
```

**Note**. A full *long cut* external Url in **Markdown** is written the same way as an absolute Url in **Html**.

Finally, a **Liquid** statement may be appended to the tail end of the **Markdown** hyperlink chain in order to designate a target of blank.

```markdown
{% raw %}
[Liquid Lessons Project: Ping-back Home Page](https://rwebaz.github.io/Liquid-Lessons-Project/){:target="_blank"}
{% endraw %}
```

### Live Link

Putting it all together yields the following **Live** rendition ...

1. [Liquid Lessons Project](https://rwebaz.github.io/Liquid-Lessons-Project/){:target="_blank"}

## Short Cut Links ( Relative )

**Liquid** *short cut* external hyperlinks replace some of the more static elements of a **Markdown** *long cut* hyperlink with *moustache* statements.

A **Liquid** *moustache* is simply another way to say {% raw %}{{ double sets of curly braces }}{% endraw %} with the double sets of curly braces resembling a sort of caricature moustache, don't you see.

### Break It Down

An analysis of a **Markdown** *long cut* hyperlink consists of the following primary elements:

1. **Link Title**

1. **Link Url Full**

1. **Target Statement**

**Note**. The full Url of a hyperlink may be dissected further to reveal the following sub-elements eligible for consideration as static **Liquid** variables:

1. **Base Url**

1. **Url**

Both the **Base Url** and **Url** may be set in stone as **Liquid** variables via the **Config dot yaml** file stored in the docs folder of your repo.

### baseurl

The **baseurl** is a static variable set inside your `config.yml` file.

This variable can then be placed within your *long* hyperlink locked inside a **Liquid** moustache statement to avoid the repetition of always having to type the same **baseurl** all the time, as follows:

```liquid
{% raw %}
{{ "/" | relative_url }}
{% endraw %}
```

Here, we have established a **Liquid** moustache statement that uses a **Unix** pipe to send the value of your designated path to the built-in site method `relative_url`, a *filter*.

The built-in site method `relative_url` then instructs your development machine to fetch the value of the variable **baseurl** and in effect prepend the **baseurl** to your path entry.

A little backwards, heh?

But, it works!

**Note**. The **baseurl** path `"/"` shown above is the directory from which your index page will be served.

In this case, we are serving our files via Git Hub Pages using the docs directory.

The docs directory, therefore, is the root directory for our index file as well as for our pages subdirectory.

### Finale Relative

Taking the code of our already completed *long cut* external hyperlink from the beginning of this tutorial above ( See: [Long Cut Links]({{ "/pages/Craft-A-Link#Long Cut Links" | relative_url }}){:target="_blank"} ), we may now inject our **Liquid** moustache statement into the mix, as follows:

#### The Code: Short Cut ( Relative )

```liquid
{% raw %}
[Liquid Lessons Project]({{ "/pages/Source-Links" | relative_url }}){:target="_blank"}
{% endraw %}
```

#### Live Link: Short Cut ( Relative )

Putting it all together yields the following **Live** rendition ...

[Liquid Lessons Project]({{ "/pages/Source-Links" | relative_url }}){:target="_blank"}

## Changing The Switch

If we now substitute the `relative_url` method with the built-in `absolute_url` site method, or *filter*, then the program will instruct your development machine to fetch the value of both the variable **baseurl** ( as in the `relative_url` method shown above ) plus the variable **url**, as well.

Let's try that ...

### url

Recall from above, the full Url of a hyperlink may be dissected further to reveal the following sub-elements eligible for consideration as static **Liquid** statements:

1. **Base Url**

1. **Url**

Recall further, that both the **Base Url** and **Url** may be set in stone as **Liquid** variables via the **Config dot yaml** file stored in the docs folder of your repo.

## Short Cut Links ( Absolute )

The **url** is a static variable set inside your `config.yml` file.

This variable can then be placed within your *long* hyperlink locked inside a **Liquid** moustache statement to avoid the repetition of always having to type the same **url** all the time.

### Finale Absolute

Live, this should simply recreate the *long cut* external hyperlink from the beginning of this tutorial above ( See: [Long Cut Links]({{ "/pages/Craft-A-Link#Long Cut Links" | relative_url }}){:target="_blank"} ).

#### The Code: Short Cut ( Absolute )

```liquid
{% raw %}
[Liquid Lessons Project]({{ "/index" | absolute_url }}){:target="_blank"}
{% endraw %}
```

#### Live Link Short Cut ( Absolute )

Putting it all together yields the following **Live** rendition ...

[Liquid Lessons Project]({{ "/index" | absolute_url }}){:target="_blank"}

**Note**. When the "absolute" version of the filter is used, the method instructs your machine to prepend first the value of the **url** variable, then the variable of the **baseurl** to your designated path.

## Anchors ( Relative )

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

## Execution

If we hover over each live rendition shown above, we should see at the bottom of your browser ( if your status bar is enabled ) the pathways of both the above "long" and the "short" Urls as compiled.

### Hover Over

Simply hover over each of the above "long" and the "short" links, and then spy the **Status Bar** at the bottom of your browser.

### Status Bar

The **Status Bar** will show each link as compiled, when hovered over.

## Bonus: Flammarion SVG

The **Flammarion** is an ancient portrait of a medieval man poking his head into the ether beyond the then given celestial sphere upon which all planets traversed guided and pulled by Apollo's all powerful Sun Chariot.

The engraving could have been mastered by the 19h century expounder of science, French astronomer Camille Flammarion.

But, more than likely was created by an unknown designer from the 16th century.

Christopher Columbus knew of the value of understanding "the sphere" and put his knowledge of celestial beings to work when unfortunately on his last voyage to the New World he found himself and his crew marooned after battling a late season hurricane.

The ancient Meso-Americans considered an eclipse to be a "bad omen" such that Columbus while shipwrecked used his knowledge of the occurrences of solar eclipses to extract concessions from the natives.

**Note**. The last full eclipse of the sun across America occurred in the year #1979 prior to the ascent of Ronald Reagan's conservative movement and administration.

"If you don't give me and my crew some food, I will cause the sun to stop shining!"~ Christopher Columbus, circa 1500

As if by a miracle, the eclipse came at the exact time Columbus ( and, his star charts ) said it would!

Quite a display of astronomical prowess, heh?

The natives were quite impressed by this feat, and scared, too!

As a result, Columbus and his crew were able to stave off starvation, rebuild their ships, and continue on to the Isthmus of Panama.

### How To Render SVG In Markup

From the tagline of the **[Inline Images][1]** article at our **[Markdown Lessons Project][2]** ...

**Inline Images** may be displayed in **Markdown** using the exclamation point `!` followed by a bracketed `[Alt Text]` followed by a relative `URL` enclosed in a single set of parenthesis `(...)`.

That includes SVG images, as follows:

#### The Code: SVG In Markup

```liquid
{% raw %}
![MMI™ Flammarion Logo Badge](../assets/img/MMI-Medmj-Org-Got-Tree-Flammarion-Person-Through-Celestial-Sphere-circle-725-x-725.svg){:height="500px" width="500px"}
{% endraw %}
```

Here, we are using an original `( .xcf )` file that has been exported from **GIMP** as a `( .psd )` of dimensions 725px x 725px x 96dpi and then imported via **Adobe Illustrator**, or **AI**.

Once inside **AI**, the `( .psd )` file is then "save as" an `( .svg )`.

Out comes an `( .svg )` file of dimensions 543.75px x 543.75px.

Now, an **SVG** file is both expandable and responsive.

To render a smaller version of the `( .svg )`, simply append an appropriate height and width, as follows:

```liquid
{% raw %}
{:height="120px" width="120px"}
{% endraw %}
```

#### Live Image: SVG In Markup

The following **Live** rendition of the **MMI™ Flammarion Logo Badge** `( .svg )` image file is set to the dimensions of 500.00px x 500.00px.

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
