---
layout: default
title: Transactions
nav_order: 2
---

{% for transaction in site.transactions %}
  <h2>
    <a href="{{ transaction.url | prepend: site.baseurl }}">
      {{ transaction.transaction.id }} - {{ transaction.transaction.name }}
    </a>
  </h2>
{% endfor %}
