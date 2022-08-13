---
permalink: /about/
author_profile: false
sidebar:
  - title: Hoon Kim
    # image: http://placehold.it/350x250
    # image_alt: "image"
  - text: 'London N1 0DF'
  - text: 'recruit@hoonio.com'
  - text: 'github.com/hoonio'
---

# Experience

{% for post in site.data.resume.work %}

## {{ post.title }}

<address>{{ post.client }}</address> _{{ post.period }}_

{{ post.summary }} {% for task in post.tasks %}

- {{ task }} {% endfor %}

{% for stack in post.stacks %}[{{ stack }}](#){: .btn .btn--primary .btn--small} {% endfor %} {% endfor %}

<!-- <article class="resume-wrapper text-center position-relative">
  <div class="resume-wrapper-inner mx-auto text-left bg-white shadow-lg">
    <div class="resume-body p-5">
      <section class="resume-section summary-section mb-5">
        <h2 class="resume-section-title text-uppercase font-weight-bold pb-3 mb-3">Career Summary</h2>
        <div class="resume-section-content">
          <p class="mb-0">{{ site.data.resume.summary }}</p>
        </div>
      </section>
      <button class="mdc-button foo-button">
        <div class="mdc-button__ripple"></div>
        <span class="mdc-button__label">Button</span>
      </button>
      <div class="row">
        <div class="col-lg-9">
          <section class="resume-section experience-section mb-5">
            <h2 class="resume-section-title text-uppercase font-weight-bold pb-3 mb-3">Work Experience</h2>
            <div class="resume-section-content">
              <div class="resume-timeline position-relative">
              {% for post in site.data.resume.work %}
                <article class="resume-timeline-item position-relative pb-5">
                  <h3 class="resume-position-title font-weight-bold mb-1">{{ post.title }}</h3>
                      <div class="resume-company-name ml-auto">{{ post.client }}</div>
                    <div class="resume-position-time">{{ post.period }}</div>
                  <div class="resume-timeline-item-desc">
                    <p>{{ post.summary }}</p>
                    <ul>
                      {% for task in post.tasks %}
                      <li>{{ task }}</li>
                      {% endfor %}
                    </ul>
                    <span class="mdc-evolution-chip-set" role="grid">
                      <span class="mdc-evolution-chip-set__chips" role="presentation">
                        [Primary Button Text](#link){: .btn .btn--primary}
                        {% for stack in post.stacks %}
                        <span class="mdc-evolution-chip" role="row" id="c1">
                          <span class="mdc-evolution-chip__cell mdc-evolution-chip__cell--primary" role="gridcell">
                            <button class="mdc-evolution-chip__action mdc-evolution-chip__action--primary" type="button" tabindex="-1">
                              <span class="mdc-evolution-chip__ripple mdc-evolution-chip__ripple--primary"></span>
                              <span class="mdc-evolution-chip__text-label">{{ stack }}</span>
                            </button>
                          </span>
                        </span>
                        {% endfor %}
                      </span>
                    </span>
                  </div><!--//resume-timeline-item-desc-->

               </article>
              {% endfor %}
             </div><!--//resume-timeline-->
            </div>
          </section><!--//experience-section-->
        </div>
        <div class="col-lg-3">
         <section class="resume-section education-section mb-5">
            <h2 class="resume-section-title text-uppercase font-weight-bold pb-3 mb-3">Education</h2>
            <div class="resume-section-content">
              <ul class="list-unstyled">
                {% for degree in site.data.resume.education %}
                <li>
                  <div class="resume-degree font-weight-bold">{{ degree.title }}</div>
                  <div class="resume-degree-org">{{ degree.institution }}</div>
                  <div class="resume-degree-time">{{ degree.year }}</div>
                </li>
                {% endfor %}
              </ul>
            </div>
          </section><!--//education-section-->
        </div>
        <div class="col-lg-3">
         <section class="resume-section education-section mb-5">
            <h2 class="resume-section-title text-uppercase font-weight-bold pb-3 mb-3">Certificates</h2>
            <div class="resume-section-content">
              <ul class="list-unstyled">
                {% for cert in site.data.resume.certificate %}
                <li>
                  <a href="{{cert.link}}">{{ cert.title }}</a>
                </li>
                {% endfor %}
              </ul>
            </div>
          </section><!--//education-section-->
         <section class="resume-section language-section mb-5">
            <h2 class="resume-section-title text-uppercase font-weight-bold pb-3 mb-3">Languages</h2>
            <div class="resume-section-content">
              <ul class="list-unstyled">
                {% for lang in site.data.resume.linguistic %}
                <li class="mb-2"><span class="resume-lang-name font-weight-bold">{{ lang.language }}</span> <small class="text-muted font-weight-normal">({{ lang.fluency }})</small></li>
                {% endfor %}
              </ul>
            </div>
          </section><!--//language-section-->
       </div>
      </div><!--//row-->
    </div><!--//resume-body-->

 </div>
</article> -->
