---
title: "Wan Lab - Publications"
layout: gridlay
excerpt: "Wan Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

## Group highlights

**At the end of this page, you can find the [full list of publications](#full-list-of-publications). All papers are also available on [Google Scholar](https://scholar.google.com.hk/citations?user=xvnWY9wAAAAJ&hl=en).**


<style>
  .card {
    height: 100%; 
  }

  .row {
    margin-bottom: 20px;
  }
</style>
<div id="publications">
  {{ content }}
  <div class="row row-cols-1 row-cols-xl-2">
    {% for publi in site.data.publist %}
    {% if publi.highlight == 1 %}

    <div class="col mb-4">

      <div class="card h-100 d-flex flex-column justify-content-between bg-light">
        <div class="card-body clearfix">
          <pubtit class="card-title">{{ publi.title }}</pubtit>
          <p>
            <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-fluid float-start w-33" />
          </p>
          <p class="card-text">{{ publi.description }}</p>
          <p class="card-text"><em>{{ publi.authors }}</em></p>
          <p class="card-text text-danger"><strong> {{ publi.news1 }}</strong></p>
          <p class="card-text"> {{ publi.news2 }}</p>
        </div>
        <div class="card-footer px-0 mx-auto text-center w-100">
          <p class="card-link text-nowrap overflow-x-auto"><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong>
          </p>
        </div>
      </div>
    </div>

    {% endif %}
    {% endfor %}
  </div>

  <p> &nbsp; </p>
</div>




## Full List of publications
### Journal Articles

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
### Conference Abstracts
{% for publi_ in site.data.publist_ %}

  {{ publi_.title }} <br />
  <em>{{ publi_.authors }} </em><br /><a href="{{ publi_.link.url }}">{{ publi_.link.display }}</a>

{% endfor %}

### Books
{% for publi_book in site.data.publist_book %}

  {{ publi_book.title }} <br />
  <em>{{ publi_book.authors }} </em><br /><a href="{{ publi_book.link.url }}">{{ publi_book.link.display }}</a>

{% endfor %}
