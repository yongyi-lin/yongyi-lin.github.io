<h2 id="publications" style="font-size:2rem;">articles</h2>
<div class="publications">
  <ol class="bibliography" style="padding-left: 0;">
    {% for link in site.data.publications.main %}
    <li>
      <div class="pub-row" style="margin-bottom: 10px;">
        <!-- Article Image and Badge (commented out as per your _site version) -->
        <!-- <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
          {% if link.image %} 
          <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
          {% if link.conference_short %} 
          <abbr class="badge">{{ link.conference_short }}</abbr>
          {% endif %}
          {% endif %}
        </div> -->
        
        <!-- Article Details -->
        <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 0px;">
          <div class="title" style="font-weight: normal; font-size: 1em;">
            <a href="{{ link.pdf }}" style="font-weight: normal; font-size: 1.1em;">{{ link.title }}</a>
          </div>
          <div class="author">{{ link.authors }}</div>
          <div class="periodical"><em>{{ link.conference }}</em></div>
          
          {% if link.notes %}
          <div class="periodical"><em>{{ link.notes }}</em></div>
          {% endif %}
          
          {% if link.additional_info %}
          <div><em>{{ link.additional_info }}</em></div>
          {% endif %}
        </div>
      </div>
    </li>
    {% endfor %}
  </ol>
</div>

<!-- Work in Progress Section -->
<h2 id="work-in-progress">work in progress</h2>
{% for project in site.data.publications.work_in_progress %}
<div class="pub-row" style="margin-bottom: 0;">
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 0px;">
    <div class="title" style="font-weight: normal; font-size: 1.1em;">
      <strong>{{ project.title }}</strong> {{ project.status }}
    </div>
    <div class="author">{{ project.authors }}</div>
  </div>
</div>
{% endfor %}
