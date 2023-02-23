---
layout: default
---
<h1>{{ page.name }}</h1>
<div class="soc">
<div class="content">
{{ content }}
</div>

<div>
<h2>Supported PMICs</h2>
{% assign pmics = page.pmic | split: ", "  %}
{% for pmic in pmics %}
{% if forloop.first %}
<ul>
{% endif %}
<li><a href="{{site.url}}{{site.baseurl}}/pmic/{{pmic}}">{{pmic}}</a></li>
{% if forloop.last %}
</ul>
{% endif %}
{% else %}
<p>No PMICs defined in database</p>
{% endfor %}
</div>

<a href="{{site.url}}{{site.baseurl}}/">Return to Home Page</a>

<div class="soc-status">
<h2>Platform status</h2>
<table>
{% include layout_soc.liquid %}
</table>
</div>

</div>
