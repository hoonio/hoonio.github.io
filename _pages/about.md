---
permalink: /about/
title: "About"
author_profile: false
sidebar: 
  - title: Hoon Kim
    image: http://placehold.it/350x250
    image_alt: "image"
  - text: "104 Gifford Street, London N1 0DF"
  - text: "+44 73 6161 5539"
  - text: "recruit@hoonio.com"
  - text: "github.com/hoonio"
---

<article class="resume-wrapper text-center position-relative">
  <div class="resume-wrapper-inner mx-auto text-left bg-white shadow-lg">
    <div class="resume-body p-5">
      <section class="resume-section summary-section mb-5">
        <h2 class="resume-section-title text-uppercase font-weight-bold pb-3 mb-3">Career Summary</h2>
        <div class="resume-section-content">
          <p class="mb-0">{{ site.data.resume.summary }}</p>
        </div>
      </section><!--//summary-section-->
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
                    <h4 class="resume-timeline-item-desc-heading font-weight-bold">Tech stacks</h4>
                    <ul>
                      {% for stack in post.stacks %}
                      <li>{{ stack }}</li>
                      {% endfor %}
                    </ul>
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
</article>