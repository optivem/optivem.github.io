---
layout: page
title: Optivem
description: Building high-quality high-ROI Software
---

<header class="masthead text-white text-center">
  <div class="overlay"></div>
  <div class="container">
	<div class="row">
	  <div class="col-xl-9 mx-auto">
		<h1 class="mb-5">Build a landing page for your business or project and generate more leads!</h1>
	  </div>
	  <div class="col-md-10 col-lg-8 col-xl-7 mx-auto">
		<form>
		  <div class="form-row">
			<div class="col-12 col-md-9 mb-2 mb-md-0">
			  <input type="email" class="form-control form-control-lg" placeholder="Enter your email...">
			</div>
			<div class="col-12 col-md-3">
			  <button type="submit" class="btn btn-block btn-lg btn-primary">Sign up!</button>
			</div>
		  </div>
		</form>
	  </div>
	</div>
  </div>
</header>


Welcome to Vemcodex, your central source of high quality information to build great software and improve your team productivity.






{% for post in site.posts reversed %}
<h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
{% assign author = site.data.authors[post.author] %}

  <div class="date">
    Written by <a href="{{ author.web }}" target="_blank">{{ author.name }}</a> on {{ post.created | date: "%B %e, %Y" }}, last modified {{ post.modified | date: "%B %e, %Y" }}
  </div>
  
<hr/>
{{ post.excerpt }}
{% endfor %}
