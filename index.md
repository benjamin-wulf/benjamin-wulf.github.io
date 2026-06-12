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
        If you're reading this you, for some reason, didn't get redirected to my GitHub, will return here when I have a chance to update my website properly! If you want to check out my work you can do so <a href="https://github.com/benjamin-wulf">here</a>.
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