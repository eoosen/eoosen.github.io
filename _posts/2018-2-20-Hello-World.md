---
layout: post
title: This is a test
category: test
tags: [test, text, practice]
---
test2

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed sed fringilla elit, mattis rutrum augue. Ut euismod elementum massa, nec eleifend lacus eleifend ut. Nunc ullamcorper tellus et quam blandit, in egestas mauris fringilla. Morbi consequat eget arcu ac semper. Cras feugiat id massa id porta. Donec vehicula nisi ac libero laoreet fringilla. Vivamus non finibus est, sit amet fringilla lectus. Ut euismod magna pellentesque rhoncus hendrerit. Phasellus feugiat eleifend blandit. Vivamus pretium id lorem id ornare. Proin aliquet ultrices enim in egestas. Aenean ac nulla vitae orci cursus hendrerit vitae a lacus. Praesent a lorem consequat, aliquet purus non, consequat lorem. Fusce vel nisi tellus. Proin tincidunt rhoncus mollis. Vivamus sit amet mi tellus.

{% comment %}
=======================
The purpose of this snippet is to list all the tags you have in your site.
=======================
{% endcomment %}
{% for tag in tags %}
	<a href="#{{ tag | slugify }}"> {{ tag }} </a>
{% endfor %}

Sed rhoncus metus sem, vitae pretium dui cursus vitae. Ut sit amet aliquet dui, gravida lobortis mi. Pellentesque non nisl id est hendrerit aliquet. Integer eu fringilla felis. Nam dolor tellus, blandit ut viverra eu, feugiat ut lectus. Quisque vehicula mauris id vestibulum tempus. Maecenas convallis massa id tristique venenatis. Curabitur non erat eget lacus dapibus laoreet. Curabitur quis euismod orci. Pellentesque vel elit ultricies sem egestas tristique. Nulla malesuada porttitor ante commodo commodo. Cras id massa non justo interdum euismod. Phasellus id volutpat sapien. Donec ut ligula et felis venenatis pellentesque et ut magna.


{% comment %}
=======================
The purpose of this snippet is to list all your posts posted with a certain tag.
=======================
{% endcomment %}
{% for tag in tags %}
	<h2 id="{{ tag | slugify }}">{{ tag }}</h2>
	<ul>
	 {% for post in site.posts %}
		 {% if post.tags contains tag %}
		 <li>
		 <h3>
		 <a href="{{ post.url }}">
		 {{ post.title }}
		 <small>{{ post.date | date_to_string }}</small>
		 </a>
		 {% for tag in post.tags %}
			 <a class="tag" href="/blog/tag/#{{ tag | slugify }}">{{ tag }}</a>
		 {% endfor %}
		 </h3>
		 </li>
		 {% endif %}
	 {% endfor %}
	</ul>
{% endfor %}

Sed consectetur justo tellus, eu cursus purus cursus eget. Vivamus in urna posuere, accumsan massa eget, consequat velit. Integer eu sollicitudin ligula. Ut sed lacinia mi. Nunc mattis arcu quis risus congue tincidunt. Integer eget finibus velit, condimentum consectetur massa. Integer elementum volutpat felis et vestibulum. Aenean vel urna vitae nibh fermentum volutpat ac a felis. Praesent interdum, libero et facilisis varius, ligula diam pulvinar felis, sit amet gravida sem arcu tempor mauris. Etiam a tortor turpis. Sed pulvinar lorem id justo malesuada malesuada. Sed sit amet enim quam. Phasellus varius non diam id vulputate. Suspendisse potenti. Suspendisse potenti. Phasellus in tincidunt orci, at tincidunt arcu.

Vestibulum a felis diam. Maecenas tristique leo elit, vel porttitor metus eleifend at. Nulla vel nisi ultricies, feugiat quam et, efficitur erat. Fusce tempor, urna eget tempor sodales, nibh nisi convallis nibh, quis lobortis velit turpis quis lorem. Aenean accumsan ex eget malesuada pellentesque. Ut mattis magna in nisi tempor, ac accumsan justo auctor. Nam ac commodo dolor. Aenean sodales, dui a feugiat luctus, quam sem pharetra purus, sit amet vehicula lacus massa sit amet libero. Nullam mollis magna ac ligula ultricies, eu consequat elit pharetra.

Vestibulum enim arcu, varius non enim ac, accumsan bibendum magna. Fusce auctor
dolor ut aliquam tincidunt. Donec eget odio sem. Ut est neque, auctor quis
auctor sit amet, ullamcorper in lorem. Curabitur at condimentum nunc. Maecenas
feugiat tellus magna. Nullam ultrices porttitor commodo. Suspendisse quis libero
sodales, placerat velit eu, feugiat ex. Maecenas in semper metus. Mauris eget
tellus sapien. Maecenas dignissim vestibulum nulla, at ullamcorper arcu ornare
sed. Duis eget lacinia eros.

![_config.yml]({{ site.baseurl }}/images/config.png)
