---
layout: default
title: Stormcast Eternals - Extremis Chamber
parent: Homebrew Factions
---

# Stormcast Eternals: Extremis Chamber

*Many are the ways that the godbeast Dracothion has contributed to Sigmar’s crusade, but that alliance is embodied most of all in the drake-riding knights of the Chambers Extremis. The combination of the sons of Sigmar and the star-scaled beasts of the Great Drake has proven an unstoppable force upon many a battlefield.*

{% include warband-abilities.html grand_alliance="order" warband="Stormcast Eternals Extremis Chamber" %}

## Fighters

### Heroes

{% assign warband_fighters = site.data.fighters | where: "warband", "Stormcast Eternals Extremis Chamber" | sort: "points" | reverse %}

{% assign heroes = warband_fighters | where: "runemarks", "hero" %}
{% for fighter in heroes %}
  {% include fighter-card.html fighter=fighter %}
{% endfor %}

### Fighters

{% for fighter in warband_fighters %}
  {% unless fighter.runemarks contains "hero" %}
    {% include fighter-card.html fighter=fighter %}
  {% endunless %}
{% endfor %}