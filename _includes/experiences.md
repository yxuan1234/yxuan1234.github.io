## Internships

<div class="publications">
<ol class="bibliography">

{% for experience in site.data.experiences.main %}

<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    {% if experience.logo %} 
    <img src="{{ experience.logo }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
    {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title"><strong>{{ experience.company }}</strong></div>
      <div class="author"><strong>Location:</strong> {{ experience.location }}</div>
      <div class="periodical"><strong>Duration:</strong> <em>{{ experience.start_date }} - {{ experience.end_date }}</em></div>
      <div class="description"><strong>Description:</strong> {{ experience.description }}</div>
      {% if experience.skills %}
      <div class="skills"><strong>Skills:</strong> {{ experience.skills | join: ", " }}</div>
      {% endif %}
      {% if experience.supervisor %}
      <div class="supervisor"><strong>Supervisor:</strong> {{ experience.supervisor }}
        {% if experience.supervisor_email %}
        (<a href="mailto:{{ experience.supervisor_email }}">{{ experience.supervisor_email }}</a>)
        {% endif %}
      </div>
      {% endif %}
  </div>
</div>
</li>
<br>

{% endfor %}

</ol>
</div>