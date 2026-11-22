---
layout: default
title: Stormcast Eternals - Ruination Chamber
parent: Additional Fighters
---

# Fighters

Add the following fighters to the Stormcast Eternals: Ruination Chamber faction.

## Fighters

{% assign warband_fighters = site.data.fighters | where: "warband", "Stormcast Eternals Ruination Chamber" | sort: "points" | reverse %}

{% for fighter in warband_fighters %}
  {% unless fighter.runemarks contains "hero" %}
    {% include fighter-card.html fighter=fighter %}
  {% endunless %}
{% endfor %}