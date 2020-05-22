# Welcome to your new Leafcutter site

Create .md files in the content directory to begin adding content. The provided sample content contains comments explaining some handy features.

<!-- page output is parsed with Twig, so you can use a lot of provided variables -->
<ul>
{% for p in page.children %}
<li>{{p|link}}
{% endfor %}
<ul>
<!-- Markdown is applied before Twig, so generally constructing HTML with Twig is safer -->


<!--@meta 
name: Home
 -->
