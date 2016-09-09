---
layout: default
title: Differentiable benchmark functions
---
<div class="home">

  <h2>Differentiable Functions</h2>

  <ol >
    {% for post in site.pages %}
	{% if post.resource == true %}
	{% unless post.tags contains 'non-differentiable' %}
		 <li>
        <h3>
          <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
		  <br />
		{% assign tags = post.tags | split:&nbsp; %}
		<ul>
			{% for tag in tags %}
			<code><a class="fcntag" href="{{ tag | prepend:'/' | prepend: site.baseurl }}">{{ tag}}</a></code>
			{% endfor %}
		</ul>
        </h3>
      </li>
	{% endunless %}
     
    {% endif %}
	{% endfor %}
  </ol>

</div>