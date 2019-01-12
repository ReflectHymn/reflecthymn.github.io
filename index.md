---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

### ReflectHymn Pieces
<ul>
{% for piece in site.data.rh_piece %}
  <li>
    RH#{{ piece.piece_id }} — {{ piece.piece_release }}
    <h3>{{ piece.piece_name}}</h3>
  </li>
{% endfor %}
</ul>
