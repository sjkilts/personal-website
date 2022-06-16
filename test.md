---
layout: default
section: post
published: true
---



<div class='listing col6 pad4h margin3' style='padding-bottom:6em;'>
  {% for item in site.categories.post limit:1000 %}
    {% capture date %}{{ item.date | date: '%B %Y' }}{% endcapture %}
  	{% capture url %}{{ item.url }}{% endcapture %}
  
    <details class='splash' style='padding-bottom:.42em;'>
      <summary>
        <h4 class='item'></h4>
        <span class='date fl'>{{ item.title }}</span>
        <span class='date fr'>{{item.date | date:"%b %d %Y"}}</span>
      </summary>
      <p>
        <a href="{{site.baseurl}}{{item.url}}">{{ item.excerpt }}</a>
      </p>
    </details>
      
  {% endfor %}
</div>





<!--
show list by default
boolean first one open
click on list to open
separate link to post
summary is post name and date
<p> is {{ post.excerpt }}
-->