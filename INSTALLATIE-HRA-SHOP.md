# HRA Shop refresh — versie 1

Dit pakket is gemaakt voor de huidige live combinatie van **Astra 4.13**, **Elementor**, **WooCommerce 11** en **WooLentor** op hrashop.nl.

## Wat versie 1 verandert

- De zwarte mededelingenbalk beweegt vloeiender en pauzeert bij hover.
- De meldingen staan in losse afgeronde chips en zijn voortaan vanuit één klein HTML-bestand aan te passen.
- De gradient-header blijft subtiel bovenaan staan en krijgt meer rust.
- Producten staan in afgeronde kaarten met een consistente afbeelding, titel en prijs.
- De prijs staat dichter bij de productnaam en sale-prijzen zijn duidelijker.
- De homepage-banner, productgalerij, producttabs en koopknop voelen moderner.
- De productpagina heeft nu één rustig koopblok met zichtbare productnaam, prijs, voorraad en CTA.
- De fotothumbnails gebruiken een afgeronde blauwe selectie in plaats van het oude zwarte kader/driehoekje.
- Variaties zoals maat en kleur krijgen consistente keuzeknoppen.
- Winkelwagen, checkout, meldingen, formulieren en Mijn account krijgen één consistente stijl.
- Op mobiel blijft de productgrid compact in twee kolommen.
- Bezoekers die minder animatie hebben ingesteld krijgen een rustige, niet-bewegende versie.

## Zo installeer je het

1. Maak voor de zekerheid een recente backup van de site.
2. Open in WordPress: **Weergave → Customizer → Extra CSS**.
3. Open `hra-shop.css`, kopieer alles en plak het onderaan in Extra CSS.
4. Klik nog niet direct op **Publiceren**. Bekijk eerst in de preview:
   - de homepage;
   - één normale productpagina;
   - één product met opties/maten;
   - winkelwagen en checkout;
   - Mijn account;
   - desktop én mobiel.
5. Als alles goed staat: klik **Publiceren**.
6. Leeg daarna de cache via **Opschonen cache** in de WordPress-balk.

## Nieuwe, makkelijk aanpasbare bovenbalk

Voor de mooiste versie gebruik je naast de CSS ook `hra-shop-announcement-bar.html`:

1. Open de Elementor-template van de header.
2. Verwijder de oude **Heading** met class `marquee` en de oude HTML-widget met het `setInterval`-script.
3. Voeg op dezelfde plek één **HTML-widget** toe.
4. Plak daar de volledige inhoud van `hra-shop-announcement-bar.html` in.
5. Werk de preview bij en controleer desktop en mobiel voordat je publiceert.

De vier meldingen staan bovenaan het bestand als losse `hra-announcement__item`-blokken. De animatie maakt zelf een tweede kopie; je hoeft een tekst dus maar één keer te wijzigen.

Je kunt voortaan ook simpelweg hier zeggen: **“vervang de melding over Claim Circles door …”**. Dan kan dit projectbestand worden bijgewerkt zonder opnieuw alle styling uit te zoeken.

## Belangrijk voor de bewegende bovenbalk

In de Elementor-header staat nu een HTML-widget met een script dat elke `0` milliseconden de marge van de tekst verandert. De vernieuwde HTML-widget gebruikt JavaScript nog maar één keer om een kopie van de meldingen te maken; de beweging zelf wordt volledig door CSS gedaan.

Als je de nieuwe HTML-widget nog niet installeert, blijft de CSS ook als compactere fallback met de bestaande balk werken.

## Snel kleuren of rondingen aanpassen

Bovenaan het CSS-bestand staan de belangrijkste waarden:

- `--hra-blue` en `--hra-green`: de gradientkleuren;
- `--hra-ink`: bijna-zwarte tekst;
- `--hra-soft`: achtergrondkleur;
- `--hra-radius`: ronding van kaarten;
- `--hra-radius-lg`: ronding van grote onderdelen.

Daarmee kun je later het grootste deel van de uitstraling veranderen zonder alle CSS door te hoeven zoeken.

## Waarom dit veilig is opgezet

De styling richt zich vooral op de classes die de live site nu echt gebruikt. Er zijn geen bestanden van Astra, Elementor of WooCommerce aangepast. Daardoor worden de veranderingen niet verwijderd wanneer het hoofdthema wordt geüpdatet. Bewaar dit CSS-bestand wel als bronbestand voor volgende versies.

## Voorstel voor versie 2

CSS maakt de winkel direct frisser, maar de grootste volgende winst komt uit inhoud en structuur:

1. hero met één duidelijke CTA, bijvoorbeeld **Shop de nieuwste drop**;
2. drie korte vertrouwenspunten onder de hero: gratis verzending vanaf €45, limited drops en support henRYANand;
3. duidelijke badges zoals **Nieuw**, **Limited: 1 van 50** en **Bijna uitverkocht**;
4. compactere productteksten met de koopknop eerder in beeld;
5. betere mobiele productgalerij en eventueel een sticky koopknop;
6. Nederlandse cookietekst en een rustigere footer.

Deze onderdelen vragen kleine Elementor- of WooCommerce-aanpassingen naast CSS. Ze kunnen daarna stap voor stap worden toegevoegd.
