---
layout: default
title: Home
---

<h1>Benjamin Wulf</h1>
<div class="grid">

  <section>
    <p>
      Cyber Threat Intelligence<br>Malware Analysis | GREM
    </p>
    <p>
        this is probably where I talk about kicking hackers' butts or whatever
    </p>
    
    <a href="/about" role="button" class="outline">Read Full Bio</a>
  </section>

  <section>
    <h2>Latest Intelligence</h2>
    
    {% for post in site.posts limit:3 %}
      <article style="padding: 1rem; margin-bottom: 1rem;">
        <header style="margin-bottom: 0.5rem;">
          <small>{{ post.date | date: "%b %d, %Y" }}</small>
        </header>
        <a href="{{ post.url | relative_url }}"><strong>{{ post.title }}</strong></a>
        <p><small>{{ post.excerpt | strip_html | truncatewords: 15 }}</small></p>
      </article>
    {% endfor %}
    
    <a href="/research">View All Research →</a>
  </section>

</div>