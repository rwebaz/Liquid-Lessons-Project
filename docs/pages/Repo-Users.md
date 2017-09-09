---
title: Repo Users
layout: default
navigation_weight: 9
---
# Repo Users

A List of Git Hub Users

{% include toc-flammarion.md %}

## Combo Snippet

This little combo snippet will render a list of GitHub users associated with your repo, as follows:

### The Code

```liquid
{% raw %}
<ul>
{% for member in site.data.members %}
  <li>
    <a href="https://github.com/{{ member.github }}">
      {{ member.name }}
    </a>
  </li>
{% endfor %}
</ul>
{% endraw %}
```

### Live

**Por ejemplo en vivo**. Need `members` data file in _data to render ...

{% include sources-and-uses.md %}

### External Sources

- The [Project Source Links](https://mminail.github.io/Liquid/Source-Liquid-Links.htm){:title="Click to Visit the Source Links page of the Liquid Lessons Project at GitHub pages"}{:target="_blank"} page of the Liquid Lessons Project. Published by © 2017 [Mminail.github.io](https://mminail.github.io/){:title="Click to Visit the Concept Library of the Medical Marijuana Initiative of North America - International Limited, an Arizona Benefit Corporation"}{:target="_blank"}.