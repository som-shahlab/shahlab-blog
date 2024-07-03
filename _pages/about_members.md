## Lab Members

{% for team_member in site.data.people.team %}
 - {{ team_member.name }}, {{ team_member.role }}
{% endfor %}

<hr>

## Recent Lab Alumni
{% for team_member in site.data.people.recent_alumni %}
 - {{ team_member.name }}, {{ team_member.role }}
{% endfor %}
