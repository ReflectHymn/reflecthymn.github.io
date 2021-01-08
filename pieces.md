---
layout: page
title: Pieces
permalink: /pieces/
---
### ReflectHymn Pieces
<!-- <ul> -->
{% for piece in site.data.rh_piece %}
<hr>
  <!-- <li> -->
<h3>{{ piece.piece_name}} <small>({{ piece.tune_name }})</small></h3><img src="/assets/img/rh{{ piece.piece_id}}-page.png" alt="[Artwork for: {{ piece.piece_name }}]" /><br />
    RH#{{ piece.piece_id }} — {{ piece.piece_release }} 
    <a href="/assets/rh/rh{{ piece.piece_id}}/{{ piece.asset }}.mp3">mp3</a> |
    <a href="/assets/rh/rh{{ piece.piece_id}}/{{ piece.asset }}.pdf">pdf</a>    <br/>

- <tt>{{ piece.tune_meter }}</tt>, {{ piece.piece_key }}, {{ piece.tune_timesignature }} Time
- Copyright: [{{ piece.tune_copyright }}]({{ piece.tune_copyright_link }})

<i>{{piece.tune_comment}}</i>

{% for tune in site.data.rh_tune %}
{% if tune.tune_id == piece.tune_id and tune.tune_story  %}
<details><summary>Story: <i>{{ tune.tune_name }}</i></summary>
<blockquote>
{{ tune.tune_story | markdownify }}
</blockquote>
</details>
{% endif %}
{% endfor %}


{% for words in site.data.rh_words %}
{% if words.words_id == piece.words_id %}
<details><summary>Lyrics: <i>{{ words.words_name }}</i></summary>
- Author: {{ words.words_author }} {{ words.words_date }}
<blockquote>
{{ words.words_text | markdownify }}
</blockquote>
</details>
{% endif %}
{% endfor %}


{% endfor %}
<!-- </ul> -->
