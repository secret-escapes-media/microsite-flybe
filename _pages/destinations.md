---
layout: default
id: destinations
title: Destinations
nav: true
nav-order: 2

destinations:

- id: edinburgh
  title: Edinburgh
  description: Lorem ipsum dolor sit, amet consectetur adipisicing elit. Tenetur, enim impedit. Nihil consequatur sint cum culpa quod libero hic impedit ea alias! Tenetur esse, ipsam ab accusamus facilis quod maiores. Illum fuga excepturi atque est corrupti in ex harum! Ipsa, facilis quas autem dignissimos facere ea recusandae aut ut!
  link: "#Edinburgh-link"

- id: manchester
  title: Manchester
  description: Lorem ipsum dolor sit, amet consectetur adipisicing elit. Tenetur, enim impedit. Nihil consequatur sint cum culpa quod libero hic impedit ea alias! Tenetur esse, ipsam ab accusamus facilis quod maiores. Illum fuga excepturi atque est corrupti in ex harum! Ipsa, facilis quas autem dignissimos facere ea recusandae aut ut!
  link: "#Manchester-link"

- id: jersey
  title: Jersey
  description: Lorem ipsum dolor sit, amet consectetur adipisicing elit. Tenetur, enim impedit. Nihil consequatur sint cum culpa quod libero hic impedit ea alias! Tenetur esse, ipsam ab accusamus facilis quod maiores. Illum fuga excepturi atque est corrupti in ex harum! Ipsa, facilis quas autem dignissimos facere ea recusandae aut ut!
  link: "Jersey-link"

- id: belfast
  title: Belfast
  description: Lorem ipsum dolor sit, amet consectetur adipisicing elit. Tenetur, enim impedit. Nihil consequatur sint cum culpa quod libero hic impedit ea alias! Tenetur esse, ipsam ab accusamus facilis quod maiores. Illum fuga excepturi atque est corrupti in ex harum! Ipsa, facilis quas autem dignissimos facere ea recusandae aut ut!
  link: "#Belfast-link"

- id: glasgow
  title: Glasgow
  description: Lorem ipsum dolor sit, amet consectetur adipisicing elit. Tenetur, enim impedit. Nihil consequatur sint cum culpa quod libero hic impedit ea alias! Tenetur esse, ipsam ab accusamus facilis quod maiores. Illum fuga excepturi atque est corrupti in ex harum! Ipsa, facilis quas autem dignissimos facere ea recusandae aut ut!
  link: "#Glasgow-link"

- id: birmingham
  title: Birmingham
  description: Lorem ipsum dolor sit, amet consectetur adipisicing elit. Tenetur, enim impedit. Nihil consequatur sint cum culpa quod libero hic impedit ea alias! Tenetur esse, ipsam ab accusamus facilis quod maiores. Illum fuga excepturi atque est corrupti in ex harum! Ipsa, facilis quas autem dignissimos facere ea recusandae aut ut!
  link: "#Birmingham-link"

- id: southampton
  title: Southampton
  description: Lorem ipsum dolor sit, amet consectetur adipisicing elit. Tenetur, enim impedit. Nihil consequatur sint cum culpa quod libero hic impedit ea alias! Tenetur esse, ipsam ab accusamus facilis quod maiores. Illum fuga excepturi atque est corrupti in ex harum! Ipsa, facilis quas autem dignissimos facere ea recusandae aut ut!
  link: "#Southampton-link"
---

<div class="container vpad--xxxl">
  {% for item in page.destinations %}
    <div class="bob{% cycle: '', ' bob--swap' %}">
      <div class="bob__img">
          <div class="bg-img bg-img--4-3" style="background-image: url('{{site.img}}/img.jpg');">
            <a class="bg-img__link" href="{{item.link}}"></a>
          </div>
      </div>
      <div class="bob__text">
        <h2 class="title title--lg">{{item.title}}</h2>
        <p>{{item.description}}</p>
        <div class="space--sm"></div>
        <a class="btn btn--orange" href="{{item.link}}">See flights</a>
      </div>
    </div>
    {% unless forloop.last %}
      <div class="space--xxxl"></div>
    {% endunless %}
  {% endfor %}
</div>