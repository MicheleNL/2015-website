---
title: 'Nog even over CSS Columns: mogelijkheden en beperkingen'
author: Michèle
layout: post
image:
  feature: post-image-columns.jpg
  thumbnail: post-thumbnail-columns.jpg
permalink: /web-development/nog-even-css-columns-mogelijkheden-en-beperkingen/
categories:
  - Web Development
---
## CSS columns

Kolommen zijn fijn. Als je je content in kolommen plaatst, kun je deze makkelijk onder elkaar laten plaatsen wanneer je je scherm kleiner maakt.

Je kunt gebruik maken van een framework met een gridsysteem, zoals bijvoorbeeld [Bootstrap][1] of [Foundation][2]. Of je maakt een grid, al dan niet met een tool als [Susy][3]. Keuzes te over. Maar sinds CSS beschikt over column properties, kun je content op een vrij makkelijke manier in kolommen verdelen. CSS columns werken zo&#8217;n beetje in elke browser, behalve in Internet Explorer lager dan versie 10.

### Hoe werkt het?

Door een paar simpele instellingen op het parent element geef je aan dat de onderliggende HTML-elementen zich moeten gedragen als een column.

  * **column-count** geeft aan hoeveel kolommen naast elkaar geplaatst moeten worden
  * **column-width** geeft aan hoe breed een afzonderlijke kolom moet zijn
  * **column-gap** is de ruimte tussen de kolommen
  * **column-rule** is een in te stellen lijn tussen de kolommen, zoals je vaak ook in kranten tegenkomt

<pre>main {
    @include column-count(1);
    @include column-width(100%);
    @include column-gap(3em);
    @include column-rule(0.5em solid $accent-color);

    @media screen and (min-width: 43em) {	
        @include column-count(2);
        @include column-width(50%);
    }
}
</pre>

<small><em>In deze voorbeelden maak ik gebruik van Sass en Bourbon syntax. </em></small>

CSS columns en media queries gaan goed samen, zo kun je al het genoemde per breakpoint instellen. Op een klein scherm 1 kolom, en op hele brede schermen wel 6 kolommen naast elkaar, is een fluitje van een cent.

Maar het schrijven van media queries maakt je CSS per definitie minder flexibel. Je kunt ook de column-count niet opgeven, maar wel een column-width. Zo zal de browser zelf bepalen hoeveel kolommen er naast elkaar komen te staan. Je kunt hier elke unit voor gebruiken behalve percentages.

<img class="border" src="/assets/images/post-image-columns-01.jpg" alt="css-columns-rule">
  
<span class="caption">
  De column rule zie je hier terug als gele lijn
</span>

### Elementen uit de column flow halen

Dit doet een beetje denken aan het tabellen-tijdperk, column-span werkt eigenlijk als de colspan. Heb je een twee kolomsverdeling gemaakt maar je wilt toch een heading of ander element over de hele breedte laten lopen? Dan kun je column-span gebruiken.

<pre>h1 {
    @include column-span(all);
}
</pre>

## Beperkingen

### Eventueel nadeel: volgorde

Natuurlijk zijn er ook aspecten om rekening mee te houden. Houd er rekening mee dat de volgorde van de items in kolommen misschien niet altijd logisch lijkt. De chronologische volgorde is namelijk verticaal gerangschikt. Als je CSS columns gebruikt om je tekst in kolommen weer te geven, is het precies wat je wilt. Maar wil je bijvoorbeeld een overzicht van artikelen met een datum in kolommen verdelen, dan is het misschien minder geschikt.

<img class="border" src="/assets/images/post-image-columns-02.jpg" alt="column-order">

<span class="caption">
  Misschien had je op de plek van artikel 4, artikel 2 willen hebben. Dat gaat niet.
</span>

### Ongelijke kolom-hoogte

De browser rekent zelf uit welke content in welke kolom thuishoort, om zo een mooi gelijke verdeling te maken. Stel dat het niet precies goed uitkomt, dan krijgt de laatste kolom de meeste content toebedeeld. Dit ziet er wat gek uit, in print is dit eigenlijk nooit het geval.

Er is een column-fill property die precies dit probleem op zou moeten lossen, maar helaas heb ik deze nog niet aan de praat kunnen krijgen.

<pre>column-fill: auto | balance | inherit | initial;
</pre>

<img class="border" src="/assets/images/post-image-columns-03.jpg" alt="css-columns-overflowing">  
<span class="caption">
  Hier zie je een klein stukje van de afbeelding uit de volgende kolom
</span>


### Overvloeiende columns

Soms begrijpt de browser niet waar de ene kolom eindigt en de nieuwe begint, en zul je soms een stukje van een element in de verkeerde kolom tegenkomen. Dit gebeurt dan met elementen in een kolom die of de eerste of de laatste waren. Gelukkig kun je hier wel wat aan doen:

<pre>.article-column {
    column-break-inside: avoid;
    page-break-inside: avoid;
    break-inside: avoid;	
}
</pre>

Je kunt er ook voor kiezen om **display: inline-block;** te gebruiken. Als je voor een van deze instellingen kiest om de kolommen niet te laten overlopen, heb je kans dat je in Chrome onvoorspelbare stukken witruimte tegenkomt. Hier is nog geen oplossing voor, maar zal vanaf Chrome 35 geen issue meer zijn.

Ook wanneer je content inlaadt met JavaScript kan het zijn dat je uitlijning niet meer helemaal klopt, omdat de kolommen qua hoogteberekening maar moeilijk met deze dynamische content om kunnen gaan.

### Clipping

<img class="border" src="/assets/images/post-image-columns-04.jpg" alt="css-column-clipped">

Box shadows zijn niet zomaar toe te passen zijn op deze CSS kolommen. Zoals je ziet wordt de schaduw afgesneden, omdat deze nu eenmaal buiten de kolom valt. Hier valt wel wat aan te doen door te spelen met margins en widths, maar zo out of the box werkt het nog niet helemaal.

## Conclusie

Wil je de lopende tekst in kolommen verdelen dan is CSS columns hier een mooie manier voor. Ga je echter wat ingewikkeldere layouts met kolommen maken, dan ben je beter af met bijvoorbeeld flexbox. Voor mijn eigen site wilde ik op de homepage een masonry-achtige blokken, en daar kwamen CSS kolommen dan weer goed van pas.

 [1]: http://getbootstrap.com
 [2]: http://foundation.zurb.com/
 [3]: http://susy.oddbird.net/