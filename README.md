# HRA Shop CSS

De onderhoudbare designlaag voor [hrashop.nl](https://hrashop.nl), gebouwd voor de huidige combinatie van Astra, Elementor, WooCommerce en WooLentor.

## Bestanden

- `hra-shop.css` — de volledige actuele styling voor de webshop.
- `hra-shop-announcement-bar.html` — de makkelijk aanpasbare mededelingenbalk bovenaan.
- `INSTALLATIE-HRA-SHOP.md` — installatie, testen en aanpassen.
- `PRODUCTPAGINA-OPBOUW.md` — vaste structuur voor nieuwe productteksten en foto’s.

## CSS installeren

1. Open WordPress.
2. Ga naar **Weergave → Customizer → Extra CSS**.
3. Vervang de bestaande HRA Shop CSS door de volledige inhoud van `hra-shop.css`.
4. Controleer homepage, productpagina, winkelwagen, checkout en account op desktop en mobiel.
5. Publiceer pas wanneer de preview klopt en leeg daarna de WordPress-cache.

## Bovenbalk aanpassen

De tekst van de bovenbalk staat in `hra-shop-announcement-bar.html`. Iedere melding is één `hra-announcement__item`. De animatie maakt automatisch een tweede kopie, dus iedere melding hoeft maar één keer in de HTML te staan.

## Werkwijze voor volgende wijzigingen

Deze repository is de bronversie. Pas eerst de bestanden hier aan en vervang daarna de CSS/HTML in WordPress. Zo blijft de volledige historie bewaard en kan iedere eerdere versie via GitHub worden teruggevonden.

## Status

De huidige CSS staat als ongepubliceerde preview in de WordPress Customizer. Publiceren gebeurt bewust pas na een laatste visuele controle.
