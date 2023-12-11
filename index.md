---
title: Instruções online hospedadas
permalink: index.html
layout: home
---

# Diretório de conteúdo

Hiperlinks para cada estudo de caso estão listados abaixo.

## Estudos de Caso

{% assign casestudy = site.pages | where_exp:"page", "page.url contains '/Instructions/CaseStudy'" %}
| Módulo | Estudo de caso |
| --- | --- | 
{% for activity in casestudy  %}| {{ activity.casestudy.module }} | [{{ activity.casestudy.title }}{% if activity.casestudy.type %} - {{ activity.casestudy.type }}{% endif %}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}
