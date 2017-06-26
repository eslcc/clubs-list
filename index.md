---
---

# European School Luxembourg 1 Clubs

Also see the Parents' Association's [Periscolaires website](https://www.activitesperiscolaires.lu/){:target="_blank"}.

Maintained by the eslcc - email `marks@eslcc.club` to be added to the list

<ul>
{% for club_hash in site.data.clubs %}
{% assign club = club_hash[1] %}
    <li>
        <h2>{{club.title}}</h2>
        {{ club.description | markdownify }}
        <div class="join">
            <small class="label">How to join</small>
            {{ club.join | markdownify }}
        </div>
    </li>
{% endfor %}
</ul>
