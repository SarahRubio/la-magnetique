---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
background-color: aquablue
title: Laboratoire d'expérimentations et de créations sonores sous forme d'ateliers
image: nos-ateliers
---

<div class="columns is-mobile is-multiline is-centered mt-6 pt-6 mb-3 pb-3">
  <div class="column columns is-centered is-8-desktop is-11-mobile has-text-centered my-6 py-6">
    <h1 class="column is-full has-text-centered is-size-1-desktop is-size-4-mobile home-page"><strong>{{ page.title }}</strong></h1>
  </div>
  <div class="column columns is-centered is-8-desktop is-11-mobile has-text-centered">
    <div class="column is-8">
        <h2 class="mb-6 inline-block has-text-centered is-size-4" id="nos-ateliers">Nos ateliers</h2>
    </div>
  </div>
</div>
<div class="columns is-desktop is-mobile is-multiline is-centered is-vcentered {{ page.layout }} mb-6 pb-6">
    <div class="column is-3-desktop is-8-mobile">
        <div><a class="py-2 px-3 m-2" id="bg-azur" href="/pages/atelier-doublage">Doublage</a></div>
        <div><a class="py-2 px-3 m-2" id="bg-yellow" href="/pages/atelier-carte-postale-sonore">Carte postale sonore</a></div>
        <div><a class="py-2 px-3 m-2" id="bg-orange" href="/pages/atelier-boite-a-sons">Boîte à sons</a></div>
        <div><a class="py-2 px-3 m-2" id="bg-blueduck" href="/pages/atelier-lutherie-electronique">Lutherie électronique</a></div>
        <div><a class="py-2 px-3 m-2" id="bg-yellow" href="/pages/atelier-piezo">Piezo</a></div>
        <div><a class="py-2 px-3 m-2" id="bg-orange" href="/pages/atelier-paysage-sonore">Paysage sonore</a></div>
        <div><a class="py-2 px-3 m-2" id="bg-azur" href="/pages/ateliers-sur-mesure">Ateliers sur mesure</a></div>
    </div>
    <div class="column is-4-desktop is-8-mobile">
        <div>
        <div class="image is-1by1">
            <img src="/assets/img/{{page.image}}.png" alt="">
        </div>  
        </div>
    </div>
</div>

