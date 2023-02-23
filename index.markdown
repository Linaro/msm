---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
<div>
<h2>SoC status</h2>
<p>This table contains highlights of the features supported for each SoC.</p>
<p>Click on the SoC link to see the full list.</p>
<table>
<thead>
{% include index_soc_header.liquid %}
</thead>
<tbody>
{% for d in site.soc %}
<tr>
<td><a href="{{d.url | absolute_url}}">{{d.name}}</a></td>
{% include index_soc_status.liquid %}
</tr>
{% endfor %}
</tbody>
</table>
</div>

<div>
<h2>PMIC Status</h2>
<table>
<thead>
{% include index_pmic_header.liquid %}
</thead>
<tbody>
{% for d in site.pmic %}
<tr>
<td><a href="{{d.url | absolute_url}}">{{d.name}}</a></td>
{% include index_pmic_status.liquid %}
</tr>
{% endfor %}
</tbody>
</table>
</div>
