---
title: Repo Users
layout: default
navigation_weight: 7
---
# Repo Users

## List of Git Hub Users

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

***

**Source**: [Instructional Jekyll Tips n Vids by Cloud Cannon](https://learn.cloudcannon.com/){:target="_blank"}