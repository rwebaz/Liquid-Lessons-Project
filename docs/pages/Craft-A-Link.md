---
title: Craft A Link
layout: default
navigation_weight: 9
---
# Craft A Link

## How To Craft A Hyperlink In Markdown With Liquid

Placing strategic **Liquid** statements enveloped with {% raw %}{{ double sets of curly braces }}{% endraw %} will offer a shortcut to the more common long form way of expressing **Markdown** external hyperlinks.

## Table O Contents

![MMI™ Flammarion Logo Badge](../assets/img/MMI-Medmj-Org-Got-Tree-Flammarion-Person-Through-Celestial-Sphere-circle-100-x-100.png)

- TOC
{:toc}

### Long Cut Links ( Full )

- Commonly, in **Markdown**, a *long cut* external hyperlink consists of first the bracketed clickable text, as follows:

```liquid
{% raw %}
[Medcoin™ Crypto Currency Project: Ping-back Home Page]
{% endraw %}
```

- After establishing the bracketed clickable text, next the developer places the full *long cut* external Url in a set of single parenthesis, as shown below:

```liquid
{% raw %}
[Medcoin™ Crypto Currency Project: Ping-back Home Page](https://rwebaz.github.io/Medcoin-Crypto-Currency-Project/)
{% endraw %}
```

**Note**. A full *long cut* external Url in **Markdown** is written the same way as an absolute Url in **Html**.

- Finally, a **Liquid** statement is appended to the tail end of the **Markdown** hyperlink chain to designate a target of blank, as presented in the following complete *long cut* external hyperlink:

#### Long Cut: The Code

```liquid
{% raw %}
[Medcoin™ Crypto Currency Project: Ping-back Home Page](https://rwebaz.github.io/Medcoin-Crypto-Currency-Project/){:target="_blank"}
{% endraw %}
```

#### Long Cut: Live Link

Putting it all together yields the following **Live** rendition ...

1. [Medcoin™ Crypto Currency Project: Ping-back Home Page](https://rwebaz.github.io/Medcoin-Crypto-Currency-Project/){:target="_blank"}

### Short Cut Links ( Relative )

**Liquid** *short cut* external hyperlinks replace some of the more static elements of the above **Markdown** *long cut* hyperlink with *moustache* statements.

**Note**. A **Liquid** *moustache* is simply another way to say {% raw %}{{ double sets of curly braces }}{% endraw %} with the double sets of curly braces resembling a sort of caricature moustache, don't you see.

#### Break It Down

An analysis of the above **Markdown** *long cut* hyperlink consists of the following primary elements:

1. **Link Title**
1. **Link Url Full**
1. **Target Statement**

**Note**. The full Url of a hyperlink may be dissected further to reveal the following sub-elements eligible for consideration as static **Liquid** statements:

1. **Base Url**
1. **Url**

Both the **Base Url** and **Url** may be set in stone as **Liquid** variables via the **Config dot yaml** file stored in the docs folder of your repo.

##### baseurl

The **baseurl** is a static variable set inside your `config.yml` file.

This variable can then be placed within your *long* hyperlink locked inside a **Liquid** moustache statement to avoid the repetition of always having to type the same **baseurl** all the time, as follows:

```liquid
{% raw %}
{{ "/Medcoin-Crypto-Currency-Project/" | relative_url }}
{% endraw %}
```

Here, we have established a **Liquid** moustache statement that uses a **Unix** pipe to send the value of your designated path to the automatic site method `relative_url`, or *filter*.

The automatic site method `relative_url` then instructs your development machine to fetch the value of the variable **baseurl** and in effect prepend the **baseurl** to your path entry.

A little backwards, heh?

But, it works!

#### Finale Relative

Taking the code of our already completed *long cut* external hyperlink from the beginning of this tutorial above ( See: [Long Cut Links] ), we now inject our **Liquid** moustache statement into the mix, as follows:

##### Short Cut: The Code ( Relative )

```liquid
{% raw %}
[Medcoin™ Crypto Currency Project: Ping-back Home Page]({{ "/Medcoin-Crypto-Currency-Project/" | relative_url }}){:target="_blank"}
{% endraw %}
```

##### Short Cut: Live Link ( Relative )

Putting it all together yields the following **Live** rendition ...

[Medcoin™ Crypto Currency Project: Ping-back Home Page]({{ "/Medcoin-Crypto-Currency-Project/" | relative_url }}){:target="_blank"}

### Short Cut Links ( Absolute )

#### Changing The Switch

If we now substitute the `relative_url` method with the `absolute_url` automatic site method, or *filter*, then the program instructs your development machine to fetch the value of both the variable **baseurl** ( as in the `relative_url` method shown above ) plus the variable **url**, as well.

Let's try that ...

##### url

Recall from above, the full Url of a hyperlink may be dissected further to reveal the following sub-elements eligible for consideration as static **Liquid** statements:

1. **Base Url**
1. **Url**

Recall further, that both the **Base Url** and **Url** may be set in stone as **Liquid** variables via the **Config dot yaml** file stored in the docs folder of your repo.

The **url** is a static variable set inside your `config.yml` file.

This variable can then be placed within your *long* hyperlink locked inside a **Liquid** moustache statement to avoid the repetition of always having to type the same **url** all the time.

#### Finale Absolute

Live, this should simply recreate the *long cut* external hyperlink from the beginning of this tutorial above ( See: [Long Cut Links] ).

##### Short Cut: The Code ( Absolute )

```liquid
{% raw %}
[Medcoin™ Crypto Currency Project: Ping-back Home Page]({{ "/Medcoin-Crypto-Currency-Project/" | absolute_url }}){:target="_blank"}
{% endraw %}
```

##### Short Cut: Live Link ( Absolute )

Putting it all together yields the following **Live** rendition ...

[Medcoin™ Crypto Currency Project: Ping-back Home Page]({{ "/Medcoin-Crypto-Currency-Project/" | absolute_url }}){:target="_blank"}

**Note**. When the "absolute" version of the filter is used, the method instructs your machine to prepend first the value the **url** then the variable of the **baseurl** to your designated path.

If we hover over each live rendition, we should see at the bottom of your browser ( if your status bar is enabled ) the pathway of the full Url as compiled.

## Raw Code

```liquid
{% raw %}
`...`
{% endraw %}
```

## Raw External Hyperlink Full

Place the introducing line of text ie.) the 'tagline' here ...

### Raw External Hyperlink Full: The Code

```liquid
{% raw %}
[New Title by Author](http://mminail.github.io). Published by © 2017 [Mminail.github.io](http://mminail.github.io){:target="_blank"}.
{% endraw %}
```

### Raw External Hyperlink Full: Live Link

Putting it all together yields the following **Live** rendition ...

[New Title by Author](http://mminail.github.io). Published by © 2017 [Mminail.github.io](http://mminail.github.io){:target="_blank"}.

***

## The Flammarion

The **Flammarion** is an ancient portrait of a medieval man poking his head into the ether beyond the then given celestial sphere upon which all planets traversed.

Guided and pulled by Apollo's all powerful Sun Chariot, the engraving could have been mastered by its 19h century expounder of science French astronomer Camille Flammarion, but more than likely was created by an unknown designer from the 16th century.

Christopher Columbus knew of the value of understanding "the sphere" and put his knowledge of celestial beings to work when unfortunately on his last voyage to the New World he found he and his crew marooned after battling a late season hurricane.

The ancient Meso-Americans considered an eclipse to be a "bad omen" such that Columbus while shipwrecked used his knowledge of the occurrences of solar eclipses to extract concessions from the natives.

**Note**. The last full eclipse of the sun across America occurred in the year #1979 prior to the ascent of Ronald Reagan's conservative movement and administration.

"If you don't give me and my crew some food, I will cause the sun to stop shining!"~ Christopher Columbus, circa 1500

As if by a miracle, the eclipse came at the exact time Columbus ( and, his star charts ) said it would!

Quite a display of astronomical prowess, heh?

The natives were quite impressed by this feat, and scared, too!

As a result, Columbus and his crew were able to stave off starvation, rebuild their ships, and continue on to the Isthmus of Panama.

![MMI™ Flammarion Logo Badge](../assets/img/MMI-Medmj-Org-Got-Tree-Flammarion-Person-Through-Celestial-Sphere-circle-725-x-725.svg)

## Sources

- [Instructional Jekyll Tips n Vids by Cloud Cannon](https://learn.cloudcannon.com/){:target="_blank"}. Published by © 2017 [Cloudcannon.com](https://www.cloudcannon.com){:target="_blank"}.

- [How To Convert an Html Site To Jekyll](http://jekyllrb.com/tutorials/convert-site-to-jekyll/). Published by © 2017 [Jekyllrb.com](http://jekyllrb.com){:target="_blank"}.
