<section id="research">
  <div class="wrap measure">
    <p class="eyebrow reveal"><span class="num">02</span> &nbsp;/&nbsp; Research</p>
    <h2 class="section-title reveal">Research</h2>

    {% assign _pubs = site.data.publications %}

    {% if _pubs.job_market_paper.size > 0 %}
      <p class="group-label reveal">Job Market Paper</p>
      {% for p in _pubs.job_market_paper %}{% include paper.html p=p %}{% endfor %}
    {% endif %}

    {% if _pubs.working_papers.size > 0 %}
      <p class="group-label reveal">Working Papers</p>
      {% for p in _pubs.working_papers %}{% include paper.html p=p %}{% endfor %}
    {% endif %}

    {% if _pubs.publications.size > 0 %}
      <p class="group-label reveal">Publications</p>
      {% for p in _pubs.publications %}{% include paper.html p=p %}{% endfor %}
    {% endif %}

    {% if _pubs.work_in_progress.size > 0 %}
      <p class="group-label reveal">Selected Works in Progress</p>
      {% for p in _pubs.work_in_progress %}{% include paper.html p=p %}{% endfor %}
    {% endif %}
  </div>
</section>
