---
title: "Wan Lab - Publications"
layout: gridlay
excerpt: "Wan Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

### Group highlights

**At the end of this page, you can find the [full list of publications](#full-list-of-publications). All papers are also available on [Google Scholar](https://scholar.google.com.hk/citations?user=xvnWY9wAAAAJ&hl=en).**


{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix" style="height: 400px;">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>




## Full List of publications
### Journal Articles <font size=3>（*: corresponding author; underlined names are lab members）</font>

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
### Conference 
#### Papers
{% for publi_ in site.data.publist_ %}

  {{ publi_.title }} <br />
  <em>{{ publi_.authors }} </em><br /><a href="{{ publi_.link.url }}">{{ publi_.link.display }}</a>

{% endfor %}

#### Abstracts
{% for publi_abstracts in site.data.publist_Abstracts %}

  {{ publi_abstracts.title }} <br />
  <em>{{ publi_abstracts.authors }} </em><br /><a href="{{ publi_.link.url }}">{{ publi_.link.display }}</a>

{% endfor %}


### Books
{% for publi_book in site.data.publist_book %}

  {{ publi_book.title }} <br />
  <em>{{ publi_book.authors }} </em><br /><a href="{{ publi_book.link.url }}">{{ publi_book.link.display }}</a>

{% endfor %}
