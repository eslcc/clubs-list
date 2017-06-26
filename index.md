---
---

# European School Luxembourg 1 Clubs

Also see the Parents' Association's [Periscolaires website](https://www.activitesperiscolaires.lu/){:target="_blank"}.

Maintained by the eslcc - email [marks@eslcc.club](mailto:marks@eslcc.club) to be added to the list.

<ul>
{% for club_hash in site.data.clubs %}
{% assign club = club_hash[1] %}
    <li>
        <label for="toggle">
            <h2>{{club.title}}</h2>
            <div class="subtitle">{{ club.subtitle | markdownify }}</div>
        </label>
        <input type="checkbox" name="toggle" id="toggle" class="toggle">
        <label for="toggle" class="label"></label>
        <div class="desc">{{ club.description | markdownify }}</div>
        <div class="join">
            <p class="jointitle">How to join</p>
            {{ club.join | markdownify }}
        </div>
    </li>
{% endfor %}
</ul>