---
layout: default
id: destinations
title: Destinations
nav: true
nav-order: 1

banner:
  title: Spring <br>Staycations

destinations:

- id: edinburgh
  title: Edinburgh
  description: The ravishing capital of Scotland is a wonder of grand Georgian boulevards and lofty castles, revelrous nights and loud-mouthed comedy. Strut down the Royal Mile and explore side streets like the colourful Victoria Street, stopping for a dram as you discover hidden gems in the narrow alleys of the Old Town. Get your art fix at the National Gallery of Modern Art and eclectic Summerhall, or peer over the Victorian galleries of the National Museum’s breathtaking exhibition hall. Climb the volcanic heights of Arthur’s Seat for gorgeous sunset panorama, before heading back to town for memorable nights of delicious eats and packed-out pubs.
  link: https://www.flybe.com/cheap-flights/edinburgh

- id: manchester
  title: Manchester
  description: The north’s capital of cool, Manchester is a buzzing hotbed of art, music and style. Get your shopping fix at the Arndale, or head for the renowned boutiques of the Northern Quarter, whilst dipping into trendy roasteries and coffee hangouts for a caffeine fix. Discover street art and grand museums, contemporary galleries and iconic industrial architecture. At night, the red-brick warehouses of the Northern Quarter become home to the city’s best bars and nightspots, with craft breweries and music venues offering revelrous nights that continue into the early hours. Get in on the ‘Madchester scene’ and discover a city that went from industrial to cultural powerhouse.
  link: https://www.flybe.com/cheap-flights/manchester

- id: jersey
  title: Jersey
  description: The largest of the Channel Islands, Jersey is a wild island escape. A windswept coastline is dotted by gorgeous beaches, quaint fishing villages and craggy cliffs, but the treasures don’t stop there. Inland, rambling country lanes criss-cross the island, connecting villages, towns, castles and beguiling scenery. Meet the island’s artisan producers at St Helier food market and feast on fine local fare, stop at a pub for a sunset drink on the coast, and spend your days discovering the island’s remarkable history. Set out to unpick the Jersey wilds, with excellent hiking, cycling and walking routes. Head for your island escape.
  link: https://www.flybe.com/cheap-flights/jersey

- id: belfast
  title: Belfast
  description: The Titanic City is a lively hub that effortlessly mixes Victorian pomp, industrial edge and contemporary cool. A city of characters, its quarters each take on different personalities; the red-brick and cobbles of the Cathedral Quarter, the post-industrial, cultural revival of the Titanic Quarter and the drinks and dining scene of the trendy Linen Quarter – the list goes on. Yet its walkable size and friendly demeanour belies its urban spread; almost like a village, Belfast is good craic as well as multifaceted. It’s also wonderfully affordable; there’s no need for euros, and itineraries can easily be filled with exquisite restaurants, a host of galleries and museums (obviously not missing the Titanic Experience Belfast), buzzing music scene and much, much more.
  link: https://www.flybe.com/cheap-flights/belfast

- id: glasgow
  title: Glasgow
  description: Glasgow is a truly captivating destination. It has an air of grandeur, with its collection of stately Victorian architecture, but you won’t find a single hint of pretension; this city is as down-to-earth as it gets, with a thriving cultural and nightlife scene. Dip-in to a great selection of museums and galleries, where art rubs shoulders with archaeological gems and classic car collections. For a spot of shopping Glasgow offers rich pickings, with a host of treasures to be found in a string of vintage shops and the old Barras Market. Dining is a fuss-free affair, with local produce put together with flair. After dinner,  check out the city’s burgeoning live music scene, as you dip into old-school convivial pubs and put the world to rights with friendly locals. Because above all of the first-rate experiences, Glasgow is best for just that – the warmest welcome on the isles.
  link: https://www.flybe.com/cheap-flights/glasgow

- id: birmingham
  title: Birmingham
  description: More canals than Venice, home of heavy metal, Britain’s curry capital and a hotbed of urban renewal, Birmingham is an enthralling mix of modernity and unique culture. The Bullring might be a modern shopping mecca, but look a little deeper and you’ll find a proud industrial heritage, revitalised by refined canalside dining, buzzing cultural hubs built in old custard factories, and a music and arts scene that thrives in Britain’s second city. From the smart Jewellery Quarter, filled with jazz bars and fine restaurants, to the youthful and creative energy of Digbeth, Birmingham is much more than a second city; it’s a destination in its own right, where a warm Brummie welcome is a given.
  link: https://www.flybe.com/cheap-flights/birmingham

- id: southampton
  title: Southampton
  description: This bustling port town is a hive of activity. A gateway to the Isle of Wight and the ravishing New Forest, Southampton offers an itinerary filled with diverse experiences. Discover a clutch of art galleries showcasing contemporary works from the local area and beyond, or see a show at the Mayflower Theatre for a culturally rich outing. Southampton is also steeped in history; walk the old town walls and under the imposing Bargate, or head back in time at the Tudor House & Garden. Throw in great shopping and buzzing bars, and you have a surprising southern destination.
  link: https://www.flybe.com/cheap-flights/southampton

- id: exeter
  title: Exeter
  description: This bustling university town is packed with old-world charms. Roman foundations and a medieval heart lie along the river Exe, accompanied by waterside pubs and beer gardens perfect for those long summer nights. Marvel at the impressive cathedral, a lofty Norman fortress with an intricate facade, before unpicking the cobbled streets filled with cafes and shops. With its student population informing the arts and music scenes, Exeter also promises a culturally-charged night out. Unwind in a homely pub before heading to one of a few live music venues and annual festivals.
  link: https://www.flybe.com/cheap-flights/exeter
---

<div class="bg--light">
  <div class="container vpad--xxl">
    <div class="width width--lg text--center">
      <p class="text--xxxl">{{site.description}}</p>
      <div class="space--sm"></div>
      <a class="btn btn--outline btn--outline-purple" href="{{site.client.link}}">See flights</a>
    </div>
  </div>
</div>

<div>
  {% for item in page.destinations %}
    <div id="{{item.id}}" class="harvey{% cycle: '', ' harvey--swap' %}">
      <div class="harvey__img" style="background-image: url({{site.img}}/content/{{page.id}}/{{item.id}}.jpg);">
        <a class="harvey__link" href="{{item.link}}" id="track-destination-{{item.id}}-img"></a>
      </div>
      <div class="harvey__text">
        <h2 class="title title--xl">{{item.title}}</h2>
        <p class="text--xl">{{item.description}}</p>
        <div class="space--sm"></div>
        <a class="btn btn--purple" href="{{item.link}}" id="track-destination-{{item.id}}-btn">Book flights</a>
      </div>
    </div>
  {% endfor %}
</div>

{% include page/promo-competition.html %}