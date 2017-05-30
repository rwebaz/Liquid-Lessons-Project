---
title: Roll Call
layout: default
navigation_weight: 2
---
# Issue: Roll Call

## How to Render Data From a Data Store In Jekyll

## Solution

For the purposes of accessing data ...

The Jekyll engine will allow access to the following types of files in the hidden `_data` subdirectory:

- Comma separated values, or `(.csv)` files that contain a header line ...

- Javascript Object Notation name-value pairs, or `(.json)` files ..., and

- Yaml data file entries, or `(.yml)` files.

## How to Call a Data set in Jekyll

First, create your data set and place the file in the `_data` subdirectory of your repo.

**Note.** Be sure to place the `_data` folder in either the root `/` directory of your repo ... Or, under the `/docs` subdirectory  of your repo.

Dependent upon which directory ( `root or docs` ) is being used by GitHub pages.

## The Code

For this example, we will create a `(.json)` file named 'tabs' and place the file in the `_data` folder under the `/docs` subdirectory, as follows:

```Javascript
{"reps":[
  { "lastName" : "Allen", "vote" : true },
  { "lastName" : "Alston", "vote" : false },
  { "lastName" : "Andrade", "vote" : null },
  { "lastName" : "Barton", "vote" : true }
]}
```

**Note.** Notice the new `(.json)` file named 'tabs' has a section named 'reps' that can be assessed via dot notation.

## Accessing The Data Store

Next, we will use a liquid `for loop` statement to access the above data store, as follows:

```liquid
{% raw %}
{% for tab in site.data.tabs.reps %}{% endfor %}
{% endraw %}
```

**Note.** Because we are using the Jekyll engine to render the highlighted example code on this page, and because Jekyll processes liquid statements by default ...

When we attempt to render a highlighted block of code that includes liquid code statements ...

If we place an escape `\` character before the liquid statement characters of `{` and `%` and `}`, the effect of the liquid statements will be neutralized.

## Escape Characters v Raw

But, this is cumbersome ...

Plus, the escape `\` characters must eventually be removed from the liquid `example` statements when rendered "live".

There must be a better way.

Simply enveloping the liquid `example` statements in Triple back-ticks {% raw %}```{% endraw %} does not work because the Jekyll engine automatically parses liquid statements as the engine iterates through the repo in a sort of logical progressions.

## Shopify Liquid

If we could only find a way to [temporarily disable liquid tag processing](https://shopify.github.io/liquid/tags/raw/){:target="_blank"} we would be set.

After checking with our friends over at Shopify ...

Who also use liquid statements to render their output ...

If we envelope the liquid `example` statements with the keyword `raw`, itself a liquid statement, and then envelope all with Triple-backticks {% raw %}```{% endraw %}, then

We should see a highlighted, yet disabled liquid `example` statement, as follows:

```liquid
{% raw %}```liquid
{% raw %}
{% for tab in site.data.tabs.reps %}{% endfor %}
\{\% endraw \%\}
{% endraw %}
```

**Hint.** Don't forget the Triple-backticks {% raw %}```{% endraw %}, at the end of a highlighted block of code.

## The Roll Call Vote

Inside the liquid `for loop` statement we will call ...

- a `string`, followed by ...

- the `lastName` value from each record within the data store, followed by ...

- a colon `:`

As follows,

```liquid
{% raw %}
- {{ 'Arizona State Representative' }} {{ tab.lastName }}:
{% endraw %}
```

**Hint.** A traditional Html unordered `line item`, or `<li></li>` may be produced in GitHub Flavored Markdown, or **GFM** by prepending the line with a simple `-` hyphen character as shown above.

## Alt If Else If Loop

After the colon `:`

We could place a liquid `If Else If Loop` statement that would iterate over the data store for the purpose of discovering a boolean state of either `true` or `false`, or a json state of `null` from the `vote` value of each record within the data store.

However, the truthy - falsy outcomes of values placed in json data stores do become delicately upset when confronted with the strict `==` operator.

If the boolean state of either `true` or `false`, or the json state of `null` is discovered in the `vote` value, then the Jekyll engine is instructed to render a piece of descriptive text in the type of a string for each respective discovery.

**Exception.** The json state of `null` may represent a "Non-vote" or abstention within the data store.

## Task Summation

In this case, we shall ask the Jekyll engine to:

- Render the string 'Yea' when encountering the boolean state of `true`,

- Render the string 'Abstain' when encountering the json state of `null`, and to

- Render the string 'Nay' when encountering the boolean state of `false`.

## Case When Switch

We could also try a liquid `Case - When` switch to render each output WITHOUT the added baggage of using the strict `==` operator.

When the author first attempted to utilize the liquid `If Else If Loop` for this model, the strict `==` operator behaved ... Well, ... STRICTLY at times.

Especially when accessing the data store!

## The Strict Operator

The strict `==` operator will return its evaluation of truthiness or falsyness when iterating over the data store using the liquid `If Else If Loop` statement.

Rather than simply identifying the values, in this case the booleans `true` and `false`, and the json state of `null` ...

The strict `==` operator returned its evaluation of whether or not the value was `truthy` or `falsy`.

Needless to say, the strict `==` operator considered the `null` value to be of the `falsy` flavor and, therefore returned `false` while subsequently rendering the string `Nay`!

Not accurate! Not good!

The json state of `null` should return simply `null` and then the Jekyll engine should render the string 'Abstain`.

## Enter the Case

To implement a liquid `Case - When` switch, we will use the same initial liquid `for loop` statement as before in order to access the data store, as follows:

## The Code Redux

```liquid
{% raw %}
{% for tab in site.data.tabs.reps %}{% endfor %}
{% endraw %}
```

We will also use the same two (2) prefix liquid statements followed by the colon `:` and preceded by the hyphen `-`

As before,

```liquid
{% raw %}
- {{ 'Arizona State Representative' }} {{ tab.lastName }}:
{% endraw %}
```

However, instead of appending a liquid `If Else If Loop` statement to the extra space following the colon `:`, we shall invoke the liquid `case` keyword to operate upon each iteration of the vote in tabs, or `tab.vote`, as follows:

```liquid
{% raw %}
{% case tab.vote %}
{% endraw %}
```

Each subsequent `when` switch will test for and find ...

One (1) of three (3) potential values ...

- `true`, `null`, `false`

In addition to the discovery of the values from the data store ...

During each iteration of `tab.vote` the Jekyll engine is instructed to render the appropriate, respective given string, as follows:

```liquid
{% raw %}
{% when true %}{{'Yea'}}{% when null %}{{'Abstain'}}{% when false %}{{'Nay'}}
{% endraw %}
```

Finally, prior to ending the `case` switch, we will inject an `else` statement into the liquid `case` statement ...

In order to test for those rare occasions where the operator may have failed to enter a value into the data store.

As follows,

```liquid
{% raw %}
{% else %}{{ 'There are no items to report!' }}
{% endraw %}
```

**Note.** Upon finding no such `blank` values, the liquid `case-when` switch is ended, and the preceding liquid `for loop` statement is ended, as well.

As follows,

```liquid
{% raw %}
{% endcase %}
{% endfor %}
{% endraw %}
```

## The Sequence of Events

Still befuddled as to how to stitch the above components together in order to render a coherent display?

Well, it goes a-like this ...

- Remember to remove the escape `\` characters from the liquid statements, if any, before going "Live" ...

```liquid
{% raw %}
{% for tab in site.data.tabs.reps %}

- {{ 'Arizona State Representative' }} {{ tab.lastName }}: {% case tab.vote %} {% when true %}{{'Yea'}}{% when null %}{{'Abstain'}}{% when false %}{{'Nay'}}

{% else %}{{ 'There are no items to report!' }}

{% endcase %}

{% endfor %}
```

## Live Rendition

{% for tab in site.data.tabs.reps %}

- {{ 'Arizona State Representative' }} {{ tab.lastName }}: {% case tab.vote %} {% when true %}{{'Yea'}}{% when null %}{{'Abstain'}}{% when false %}{{'Nay'}}

{% else %}{{ 'There are no items to report!' }}

{% endcase %}

{% endfor %}

{% comment %}Finito!{% endcomment %}

Source: [Arizona House of Representatives](http://www.azleg.gov/MemberRoster/?body=H)

## Extra Bonus

Would you like to view the failed `If Else If Loop` ( Example ) from the start of the lesson?

If you do, here it is!

## The Alt Code

```liquid
{% raw %}
{% for tab in site.data.tabs.reps %}
- {{ 'Arizona State Representative' }} {{ tab.lastName }}:
{% if tab.vote == true %}{{'Yea'}}{% else if tab.vote == null %}{{'Abstain'}}{% else if tab.vote == false %}{{'Nay'}}
{% else %}{{ 'There are no items to report!' }}
{% endif %}
{% endfor %}
{% endraw %}
```