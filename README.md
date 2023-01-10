# Mijn oba
Ontwerp en maak voor een opdrachtgever een component of website op basis van een bestaande huisstijl.

## User Story
> Als oba-lid wil ik op de website persoonlijke boekentips krijgen, zodat ik gestimuleerd wordt meer te lezen.

## Beschrijving
In deze sprint staat de huisstijl van de opdrachtgever centraal. Het is natuurlijk belangrijk dat gebruikers weten op welke website ze zitten en dat de website herkenbaar is. De oba maakt gebruik van drie verschillende kleuren die je steeds terug ziet op de website. Dit zijn rood, zwart en grijs. Deze kleuren heb ik ook toegevoegd binnen mijn project. Ik heb rood gebruikt voor knoppen met een interactie en die het meest belangrijk zijn op de website. Zoals het navigeren en het toevoegen van boekentips aan je leeslijst.

Mijn user story gaat over de persoonlijke boekentips, dus ik vond het belangrijk dat dit centraal stond. Om een onderscheid te maken, heb ik ervoor gezorgt dat de boeken in een kader worden laten zien met een lichtgrijze achtergrond. De heading en tekst zijn zwart wat goed te lezen is met een witte achtergrond. Ik heb dit gescant met de Colour Contrast Analyser en hier kwam een heel goed resultaat uit. De boekentips hebben een slider, dus je kan door al je tips heen sliden met de pijlen, of het automatisch laten sliden.

De overige knoppen zijn voorzien van een zwarte kleur. Dit gaat dan om je profiel, uitloggen, meer informatie, darkmode en social media. Dit zijn dus overige zaken die te maken hebben met je profiel en je voorkeuren. Wil je de website bekijken, dan kan dat door de volgende linkt te volgen: [Mijn OBA omgeving](https://amberhva.github.io/look-and-feel-corporate-identity/). Hieronder zal ik een voorbeeld laten zien van de website op de desktop en op de mobiel:

![boekentips](https://user-images.githubusercontent.com/112861033/195666128-cb4fe13c-f935-4171-8d29-0acb5a9a5fa2.jpg)
![responsive-oba (2)](https://user-images.githubusercontent.com/112861033/195671724-c123c54f-2385-455e-bf5c-fd35beeccc04.png)


## Kenmerken
<!-- Bij Kenmerken staat welke technieken zijn gebruikt en hoe. Wat is de HTML structuur? Wat zijn de belangrijkste dingen in CSS? Wat is er met JS gedaan en hoe? -->
Ik heb zoals boven vermeld, gebruik gemaakt van de Colour Contrast Analyser om te zorgen dat de website meer toegankelijk is voor mensen die slechtziend zijn. Ik heb ook geprobeerd meer gebruik te maken van iconen zodat bijvoorbeeld oudere mensen gemakkelijker door de webpagina kunnen navigeren. Dit zie je het beste wanneer de website te zien is op de mobiel. 

Ik heb voor de automatische swiper een externe library gebruikt en toegevoegd aan mijn website. Ik heb alle delen van de website onderverdeeld door middel van nav, header, sections en footers maar ook met divs. Ik heb een section genaamd featured waar ik de boekentips laat zien. Door middel van JavaScript heb ik een slideshow gemaakt waardoor je kan swipen met de pijlen maar ook een automatisch swiped. Voorbeeld code van de html en JavaScript zal ik hieronder laten zien:

### HTML
```html
<section class="featured">

    <h1 class="heading"> <span>Bekijk uw persoonlijke boekentips</span> </h1>

    <div class="swiper featured-slider">
        <div class="swiper-wrapper">

            <div class="swiper-slide box">
                <div class="image">
                    <img src="image/book1.jpg" alt="">
                </div>
                <div class="content">
                    <h3>Titel</h3>
                    <a href="#" class="btn">Voeg toe aan leeslijst</a>
                </div>
            </div>
```
### JavaScript
```javascript
var swiper = new Swiper(".featured-slider", {
  spaceBetween: 10,
  loop:true,
  centeredSlides: true,
  autoplay: {
    delay: 9500,
    disableOnInteraction: false,
  },
  navigation: {
    nextEl: ".swiper-button-next",
    prevEl: ".swiper-button-prev",
  },
  breakpoints: {
    0: {
      slidesPerView: 1,
    },
    450: {
      slidesPerView: 2,
    },
    768: {
      slidesPerView: 3,
    },
    1024: {
      slidesPerView: 4,
    },
  },
});
```
## Licentie

![GNU GPL V3](https://www.gnu.org/graphics/gplv3-127x51.png)

This work is licensed under [GNU GPLv3](./LICENSE).
