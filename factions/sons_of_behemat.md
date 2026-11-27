---
layout: default
title: Sons of Behemat Stomp-Bands
parent: Homebrew Factions
---

The warband was designed so you generally have three Gargants, with a single four-fighter configuration available if you’re willing to go with 50% Beasts (2 Maneaters + 2 Ghyrochs).

The Uninspiring Presence rule is aimed at preventing players from taking two Gargants and filling up the roster with cheap bladeborn. It also feels vaguely thematic and prevents Gargants being taken as allies – you’ll have to stick with the Aleguzzler as a monster.

Why is the Aleguzzler still a monster when these guys are normal fighters? I guess because he’s drunk.

# Sons of Behemat Stomp-Bands

*Gargants are the epitome of strength and brutality. An ancient, monstrous race that has stepped straight out of myth, these titans scorn the puny works of those smaller than them, demolishing civilisation and its defenders with each swing of fist and club.*

{% include warband-abilities.html grand_alliance="destruction" warband="Sons of Behemat" %}

## Fighters

{% assign warband_fighters = site.data.fighters | where: "warband", "Sons of Behemat" | sort: "points" | reverse %}

{% for fighter in warband_fighters %}
  {% unless fighter.runemarks contains "hero" %}
    {% include fighter-card.html fighter=fighter %}
  {% endunless %}
{% endfor %}
