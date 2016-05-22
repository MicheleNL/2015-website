---
title: De highlights van Fronteers 2014
author: Michèle
layout: post
permalink: /web-development/front-enders-conferentie-de-highlights-van-fronteers-2014/
image:
  feature: post-image-fronteers-14-rachel.jpg
  thumbnail: post-thumbnail-fronteers-14-rachel.jpg
categories:
  - Web Development
---
*Dit artikel verscheen 20 oktober 2014 op [www.occhio.nl][1].*

Ook dit jaar was er weer een delegatie van Occhio van de partij bij de jaarlijkse conferentie van [Fronteers][2], de vakvereniging voor front-end ontwikkelaars. Het congres vond tot ons groot plezier, net als eerdere jaren, plaats in het prachtige [Tuschinski][3].

## Wat is een frontender?

Nog even in het kort voor diegene die niet weet wat een front-end ontwikkelaar is: een front-end ontwikkelaar zet met behulp van de technieken [HTML][4], [CSS][5], en JavaScript/jQuery een (interactie)ontwerp om in een website. Dingen zoals databases, algoritmes en formulieren laat een front-ender aan een back-ender over. Als ik de vergelijking met een auto maak, dan zou je kunnen stellen dat de frontender zorgt voor de lak, het plaatwerk (de vormen), handgrepen, kleine accessoires zoals antenne etc. en de backender is verantwoordelijk voor de motor en overige onderdelen die ervoor zorgen dat de auto rijdt.

<p>
<img class="full-width" src="/assets/images/post-image-fronteers-14-jaffa.jpg" alt="Fronteers 2014 Occhio, foto door Peter Peerdeman" width="1024" height="381" />

<span class="caption">
  Deze editie van Fronteers werd gepresenteerd door Jake Archibald, Google Chrome developer.<br /> <small><em>Foto door Peter Peerdeman</em></small>
</span>
</p>


## Conferentie kick-off: over CSS

De conferentie trapt af met een interessante presentatie over CSS. CSS is de taal die er voor zorgt dat de HTML elementen van een website mooi worden gestyled, denk hierbij aan mooi gekleurde blokken of leuke iconen bij een lijstje. HTML is de interface en CSS is enkel de branding.  
Betoogd wordt dat het is aan te raden om overal de juiste HTML elementen voor te gebruiken, zodat CSS classes eigenlijk overbodig zijn.  
De spreker haalt ook de *ARIA landmark roles* aan, hiermee kun je van een bepaald element aangeven wat nu eigenlijk zijn rol is binnen de website. *role=”navigation”* geeft bijvoorbeeld aan dat het menu ook echt een navigatie-item is, in plaats van alleen maar een simpele lijst. Op deze manier wordt je website een stuk robuuster en ook meteen wat toegankelijker, want de screenreaders begrijpen er opeens veel meer van! Dus belangrijk als je [webrichtlijnen][6] dient te volgen en toegankelijke sites bouwt.

<p class="note">
  Meer over werken met <a href="http://www.occhio.nl/blog/links-openen-een-nieuw-venster-toch-niet/">links vind je in deze blog</a>
</p>

En nu we het toch over toegankelijkheid hebben: ook links kunnen beter maar altijd onderlijnd blijven, dit komt de duidelijkheid en dus usability erg ten goede.

## Animatie &#8211; veelbesproken topic

Een veelbesproken onderwerp dit jaar op Fronteers. Animatie verbetert de acceptatiegraad van nieuwe interfaces. Veranderingen worden d.m.v. animatie veel makkelijker begrepen, zeker wanneer deze *gradueel* zijn. Vooral ouderen en kinderen kunnen hier veel aan hebben. Vandaag de dag wordt animatie eigenlijk steeds meer verwacht binnen een applicatie of website.

Google heeft ook nog een prachtige documentatie waar je hier meer over kunt lezen en ook het verschil kunt zien in de beleving tussen een applicatie met en zonder animatie: [Google Material Design Meaningful Transition videos][7].  
Er worden ook nog enkele animatie librariers besproken zoals [GSAP][8] en [Velocity.js][9].

## Het animeren van SVG

We maken steeds minder gebruik van afbeeldingen om een website op te leuken. We zijn al vaker aan de slag gegaan met [iconfonts][10], maar ook SVG is een erg mooie manier om bijv. iconen of logo’s te tonen. SVG staat voor [Scalable Vector Graphics][11], wat wil zeggen dat de afbeeldingen gemaakt zijn uit vectoren en hierdoor schaalbaar zijn zonder scherpte te verliezen. Erg handig in combinatie met [responsive webdesign][12] en retina schermen!

SVG kun je animeren met CSS en JavaScript. Met deze talen kun je bijvoorbeeld makkelijk transities instellen of de SVG laten infaden.  
Helaas zijn hier wel grenzen aan verbonden, dus echt geavanceerde animatie kun je beter overlaten aan SMIL. SMIL is een opmaaktaal voor allerlei soorten multimedia-weergaves, zoals timing, layout, duur, het embedden van media etc. Ook begrijpt SMIL wanneer er op een link wordt geklikt, wat handig is, want zo kun je hier ook weer visuele feedback voor verzorgen. Helaas begrijpt Internet Explorer nog niet veel van deze hippe SMIL-taal, maar het is zeker iets om in de gaten te houden.

## Real-time web

Het real-time web bestaat uit een set technologieën en methodes die ervoor zorgen dat bezoekers van een website informatie kunnen ontvangen direct wanneer deze is gepubliceerd. Zoals die ene Facebook notificatie die je krijgt zonder dat je de site hebt hoeven herladen.

Er wordt hard gewerkt aan verschillende methodes om dit voor elkaar te krijgen. Helaas blijkt wel dat elke methode weer zijn eigen nadelen heeft waardoor er eigenlijk nog niet één perfecte manier is. Er werden verschillende methoden besproken, zoals AJAX, WebSockets en Server Sent Events (waar ik nu niet verder op inga vanwege de technische aard).

## Web performance

Net als vorig jaar werd er aandacht besteed aan web performance. Deze snelheidsoptimalisatie zorgt ervoor dat de algehele gebruikerservaring positief wordt beïnvloed. De spreker Dave Olsen presenteert een groot scala aan handige, bruikbare tips en best practices. Ook wist hij wat leuke statistieken te vertellen:

  * De gemiddelde website is 1.8mb groot
  * 78% hiervan bestaat uit afbeeldingen en scripts
  * 5 sec is de maximale laadtijd, daarna zie je al snel bezoekers die afhaken

> &#8216;De gemiddelde website is 1.8mb groot&#8217;

Ook noemt Dave Olsen een set diagnostische tools waarmee je snel kunt zien hoe je site er voor staat, o.a. [Page Speed Insights][13], [WebPageTest][14] en [Google Analytics Sitespeed][15].  
De spreker besteedt ook aandacht aan SPOF. SPOF staat voor *Single Point Of Failure* en hiermee wordt bedoeld dat het gehele systeem kan falen wanneer een enkel onderdeel niet meer werkt. Het is dus mogelijk dat een website niet meer naar behoren werkt (bijv. traag wordt), doordat Facebook down is en hierdoor de Facebook like button problemen veroorzaakt.

## Overige onderwerpen

### Gaming in the browser

Met HTML5 kun je tegenwoordig erg coole games maken. Drie sprekers presenteerden hun games, waaronder zelfs een 3d-game, en maakten de hele zaal enthousiast. Ben je zelf ook benieuwd of gewoon even toe aan een leuke game? Kijk dan op [LessMilk.com][16].

### Offline first

Alex Feyerke pleit voor een offline first aanpak, en dan met name voor web en native apps. Aan de hand van commercials demonstreert hij hoe onrealistisch deze eigenlijk zijn: alle technologieën werken altijd foutloos en er is altijd een goedwerkende internetverbinding beschikbaar. Zo zie je iemand bungelen aan een berg, terwijl ze nog snel even een berichtje verstuurt.  
In de echte wereld werkt dit niet zo en daardoor vindt Alex dat we realistisch moeten zijn en de gebruiker een goede gebruikservaring moeten bieden d.m.v. offline first.  
Offline first houdt in dat je webapp altijd moet werken, dus ook wanneer je bovenop een bergtop staat. Het hebben van een verbinding is hierop niets meer dan een verbetering.  
De spreker bespreekt een aantal technische oplossingen hiervoor en laat ook zien dat visuele feedback erg belangrijk is.


 [1]: http://www.occhio.nl/
 [2]: http://www.fronteers.nl
 [3]: http://nl.wikipedia.org/wiki/Theater_Tuschinski
 [4]: http://www.occhio.nl/?s=html
 [5]: http://www.occhio.nl/?s=css
 [6]: http://www.occhio.nl/tag/webrichtlijnen/
 [7]: https://www.google.com/design/spec/animation/meaningful-transitions.html
 [8]: http://greensock.com/gsap
 [9]: http://julian.com/research/velocity/
 [10]: /blog/waarom-iconfonts-cool-zijn/
 [11]: http://nl.wikipedia.org/wiki/Scalable_Vector_Graphics
 [12]: /blog/responsive-webdesign/
 [13]: https://developers.google.com/speed/pagespeed/insights/
 [14]: http://www.webpagetest.com
 [15]: https://support.google.com/analytics/answer/1205784?hl=en
 [16]: http://www.lessmilk.com/12games