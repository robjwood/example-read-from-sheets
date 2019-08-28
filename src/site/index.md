---
title: Google Sheets data feed example.
layout: default
---


## Content from an external data source

The lists below showing the top scored in the Premier League and Cahmpionship 2018/2019. They're sourced from [a Google Sheet](https://docs.google.com/spreadsheets/d/1KriXplIJ4If3peS_XlEJD2shm6WdPlZOXftJWtcUjYo/edit#gid=0) as [JSON](https://spreadsheets.google.com/feeds/list/1KriXplIJ4If3peS_XlEJD2shm6WdPlZOXftJWtcUjYo/od6/public/values?alt=json) at site build time.


### Premier League Top 5 Scorers

<ul class="listing">
{%- for item in sheet.Prem -%}
  <li>{{ item.name }} - {{ item.team }} - <b>{{ item.goals }}</b></li>
{%- endfor -%}
</ul>

### Championship Top 5 Scorers

<ul class="listing">
{%- for item in sheet.Championship -%}
  <li>{{ item.name }} - {{ item.team }} - <b>{{ item.goals }}</b></li>
{%- endfor -%}
</ul>



## About

- The [code is available to inspect on GitHub]({{ pkg.repository.url}}).




