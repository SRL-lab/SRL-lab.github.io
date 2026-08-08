---
layout: page
permalink: /publications/
title: Publications
description: #publications by categories in reversed chronological order.
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}



<div class="publications">


<h2>Preprints</h2>
{% bibliography --query @*[preprint=true] %}


---

<h2>Journal Publications</h2>
{% bibliography --query @*[preprint!=true] %}

</div>
