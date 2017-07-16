---
title: Citrus Table
layout: default
navigation_weight: 9
---
# Citrus ( Kramdown ) Table

## Navigating This Page ( Internal Anchor Links )

- TOC
{:toc}

**Note**. Unordered Lists (ul) should be surrounded by blank lines in GitHub Flavored Markdown (GFM), except in those instances where a Kramdown command is subsequently evoked on the very next line, as follows:

### Table O Contents

```liquid
{% raw %}
- TOC
{:toc}
{% endraw %}
```

## Table (Mesa) O Citrus ( de Citrus )

This rendition of the Kramdown table has a class ( the class holds a border ), an id, and a footer.

**Note**. No Html has been used to construct this table. Only Markdown - Kramdown syntax has been used to compile the table features.

### Classes and IDs

A reference to the class housed at the 'style dot scss file' under the 'assets/css folder' is placed after the final frame of the table, as follows:

```liquid
{% raw %}
|---------+---------+---------|
{: .groove-table #TableCage}
{% endraw %}
```

**Note**. The id for the table is declared after the class reference, as shown above.

### Style dot scss

The style design of the exterior table border is, as follows:

```liquid
{% raw %}
/* Set the Table Border */
.groove-table {
    border: 5px groove green;
}
/* End Setting the Table Border */
{% endraw %}
```

### Header Column Alignment

The header columns are left-aligned, center-aligned, and right aligned respectively, as follows:

```liquid
{% raw %}
|---------+---------+---------|
|English - Citrus|Photo|Spanish - Citrus|
|---------|:---------:|---------:|
{% endraw %}
```

### Optional Footer

The optional footer is rendered by a frame of double-hyphens, or 'equal signs' `=========` placed after the last row of data followed by the text of the footer placed directly above the final frame `|---------+---------+---------|` of the table, as follows:

```liquid
{% raw %}
|=========+=========+=========|
|This is an optional footer row of text ...|
|---------+---------+---------|
{% endraw %}
```

### Table Data

The internal columns of table data have been entered manually row-by-row after the introducing header frame, as follows:

```liquid
{% raw %}
|Blackberries|![Page Banner](../assets/img/raspberry-frambuesa-32-x-32.png)|Zarzamoras|
|Raspberries|![Page Banner](../assets/img/raspberry-frambuesa-32-x-32.png)|Frambuesas|
{% endraw %}
```

**Note**. Placing the table data in a json file under the '_data' subdirectory and calling for each 'bag' in 'bags' may optionally populate the rows of the table programmatically with fruits, vegetables, and meats, as well.

### Putting It All Together

To create a live rendition of the table as described, the individual components of the table must be aggregated, as follows:

```liquid
{% raw %}
|---------+---------+---------|
|English - Citrus|Photo|Spanish - Citrus|
|---------|:---------:|---------:|
|Blackberries|![Page Banner](../assets/img/raspberry-frambuesa-32-x-32.png)|Zarzamoras|
|Raspberries|![Page Banner](../assets/img/raspberry-frambuesa-32-x-32.png)|Frambuesas|
|=========+=========+=========|
|This is an optional footer row of text ...|
|---------+---------+---------|
{: .groove-table #TableCage}
{% endraw %}
```

### Live Rendition

A live rendition of the 'Table (Mesa) O Citrus ( de Citrus )' is reproduced here by your browser ...

|---------+---------+---------|
|English - Citrus|Photo|Spanish - Citrus|
|---------|:---------:|---------:|
|Blackberries|![Page Banner](../assets/img/raspberry-frambuesa-32-x-32.png)|Zarzamoras|
|Raspberries|![Page Banner](../assets/img/raspberry-frambuesa-32-x-32.png)|Frambuesas|
|=========+=========+=========|
|This is an optional footer row of text ...|
|---------+---------+---------|
{: .groove-table #TableCage}

### Ping-back

**Source**: [GitLab Markdown Guide](https://about.gitlab.com/){:target="_blank"}
