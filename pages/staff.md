---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
{% include landing_small.html title='About Us' %}

<div id="about" class="offset" style="margin-top: 5px;">
  <div class="bg-light py-4">
    <div class="container py-4">
      <div class="col-12 text-center">

        <p class="lead text-left">{{ site.data.staff.about }}</p>
      </div>

      <div class="row mb-4">
        <div class="col-lg-5">
          <h2 class="display-5 font-weight-light">Instructors</h2>
        </div>
      </div>
      <div class="row text-center">
        {% include staff_cards.html role='prof' %}
      </div>

      <div class="row mb-4">
        <div class="col">
          <h2 class="display-5 font-weight-light">Student Educators</h2>
        </div>
      </div>
      <div class="row text-center">
        {% include staff_cards.html role='se' %}
      </div>

    </div>
  </div>
</div>
