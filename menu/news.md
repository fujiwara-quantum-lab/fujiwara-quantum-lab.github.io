---

layout: default

title: Blog

---



<h1>{{ page.title }}</h1>



<ul>

&nbsp; {% for post in site.posts %}

&nbsp;   <li>

&nbsp;     <a href="{{ post.url | relative\_url }}">{{ post.title }}</a>

&nbsp;     <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

&nbsp;   </li>

&nbsp; {% endfor %}

</ul>

