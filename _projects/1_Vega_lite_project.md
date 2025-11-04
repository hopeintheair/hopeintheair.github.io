---
name: HW5 - Licenses in Illinois
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
description:  HW5.1. Submit Jekyll webpage link !
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


## Plot 1

Example comes from this [great blog post right here](https://blog.4dcu.be/programming/2021/05/03/Interactive-Visualizations.html) that was also used in [our test import script](https://github.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/blob/main/week01/test_imports_week01.ipynb).

We can use a vegachart HTML tag like so:

<vegachart schema-url="{{ site.baseurl }}/assets/json/license.json" style="width: 100%"></vegachart>

In theory, you can also use [Jekyll hooks](https://jekyllrb.com/docs/plugins/hooks/) to do it, but I haven't figured out a way that looks nice yet.



## Plot 2

Below is where we can put some links to both the data and the analysis code as buttons:
<vegachart schema-url="{{ site.baseurl }}/assets/json/Disciplined.json" style="width: 100%"></vegachart>

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/licenses_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/hopeintheair/hopeintheair.github.io/blob/main/python_notebooks/HW5.ipynb" text="The Analysis" %}
</div>

