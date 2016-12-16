---
title: Overview
first_published: October 2002
layout: main
---

Ce guide décrit les activités qui vous aideront à intégrer l'accessibilité tout au long du cycle de production Web. Cela s'applique à des projets individuels et à des projets d'entreprises. Ces activités ne sont pas nécessairement réalisées dans un ordre séquentiel, et sont idéalement répétées au fil du temps pour augmenter constamment le niveau d'accessibilité.

{::nomarkdown}<%= link_to "Web Accessibility First Aid: Approaches for Interim Repairs", (w3url '/WAI/impl/improving') %>{:/}, fournit des conseils ou des solutions correctives pour lever obstacles à l'accessibilité. 

{::nomarkdown}
<ul class="grid">
<% cycle = 'even' %>
<% data.structure.each do |tag, section| %>
  <% cycle = (cycle == 'odd' ? 'even' : 'odd') %>
  <li class="<%= cycle %>"><p><%= link_to "<i class='fa fa-#{section.icon}'></i>#{section.label}", "#{tag}.html" %></p>
    <p><%= section.description %></p>
    <ul>
    <% section.activities.each do |activity| %>
      <li><%= link_to title(activity), "#{tag}.html##{activity}" %></li>
    <% end %>
    </ul>
  </li>
<% end %>
</ul>
{:/}
