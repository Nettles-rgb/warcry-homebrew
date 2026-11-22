---
layout: default
title: Stormcast Eternals - Thunderstrike Stormcast
parent: Additional Fighters
---

# Fighters

Add the following fighters to the Stormcast Eternals: Thunderstrike Stormcast faction.

## Heroes

{% assign warband_fighters = site.data.fighters | where: "warband", "Stormcast Eternals Thunderstrike Stormcast" | sort: "points" | reverse %}

{% assign heroes = warband_fighters | where: "runemarks", "hero" %}
{% for fighter in heroes %}
  {% include fighter-card.html fighter=fighter %}
{% endfor %}

## Fighters

{% for fighter in warband_fighters %}
  {% unless fighter.runemarks contains "hero" %}
    {% include fighter-card.html fighter=fighter %}
  {% endunless %}
{% endfor %}

# Abilities

Add the following abilities to the Stormcast Eternals: Thunderstrike Stormcast faction:

{% include warband-abilities.html grand_alliance="order" warband="Stormcast Eternals Thunderstrike Stormcast" %}


