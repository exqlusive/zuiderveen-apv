# Transportroutes Gids Zonder XP En Geld

Deze gids beschrijft alle routes die momenteel in `zv_trucking_tycoon` zijn geconfigureerd, zonder zichtbare XP-, geld- of kosteninformatie.

## Algemene werking

- Start bij het `Transporthoofdkwartier` of rij direct naar een laadlocatie.
- Voor `laden` en `verkopen` krijg je een batchkeuze:
    - `1 batch`
    - `3 batches`
    - `10 batches`
- Elke laad- of verkoopbatch duurt `3 seconden`.
- Een batch stopt automatisch eerder als:
    - je laadruimte vol is
    - je niet genoeg items meer hebt voor een volledige verkoopbatch
- `Process`-acties draaien altijd per enkele actie en niet in batches.

## Korte routekaart

| Route | Min. level | Eindproduct |
| --- | ---: | --- |
| Gereedschap | 1 | Gereedschap |
| Gummen | 2 | Gummen |
| Houtkap | 6 | Planken of zaagsel |
| Recycling | 9 | Plastic schroot / verfijnd aluminium / verfijnd tin |
| Gekoeld | 10 | Vliegtuigmaaltijden |
| Petrochemisch / Militair | 10 | Explosieven |
| Sieraden | 15 | Sieraden |
| Batterijen | 15 | Batterijen |
| Illegale pillen | 17 | Pillen |
| Beton | 20 | Beton |
| Wapeningsstaal | 20 | Wapeningsstaal |
| Huiskit | 100 | Huiskit |

## Basisroutes

### Gereedschap

- Min. level: `1`
- Type: basisroute
- Uitleg: laad een startersbatch gereedschap en lever die direct af.

| Stap | Locatie | Actie | Benodigd | Resultaat |
| --- | --- | --- | --- | --- |
| 1 | Gereedschapsdepot | Laad gereedschap | - | `15x Gereedschap` |
| 2 | Ladingkoper: Gereedschap | Verkoop gereedschap | `15x Gereedschap` | - |

### Gummen

- Min. level: `2`
- Type: basisroute
- Uitleg: een iets betere starterroute met een andere ophaal- en afleverkant.

| Stap | Locatie | Actie | Benodigd | Resultaat |
| --- | --- | --- | --- | --- |
| 1 | Kantooroverschot | Laad gummen | - | `8x Gummen` |
| 2 | Ladingkoper: Gummen | Verkoop gummen | `8x Gummen` | - |

### Houtkap

- Min. level: `6`
- Type: verzamel + verwerk + verkoop
- Uitleg: laad boomstammen en kies daarna of je planken of zaagsel wilt maken.

| Stap | Locatie | Actie | Benodigd | Resultaat |
| --- | --- | --- | --- | --- |
| 1 | Houthakkerskamp | Laad boomstammen | - | `2x Boomstammen` |
| 2A | Zagerij | Zaag boomstammen tot planken | `2x Boomstammen` | `6x Planken` |
| 3A | LS Havenexport | Verkoop planken | `6x Planken` | - |
| 2B | Zagerij | Maal boomstammen tot zaagsel | `2x Boomstammen` | `8x Zaagsel` |
| 3B | LS Havenexport | Verkoop zaagsel | `8x Zaagsel` | - |

### Recycling

- Min. level: `9`
- Type: verzamel + sorteer + verfijn + verkoop
- Uitleg: deze route splitst zich na het sorteren in drie verkooprichtingen.

| Stap | Locatie | Actie | Benodigd | Resultaat |
| --- | --- | --- | --- | --- |
| 1 | Recyclingcentrum | Laad recyclebaar afval | - | `1x Recyclebaar afval` |
| 2 | Sorteercentrum | Sorteer recyclebaar afval | `1x Recyclebaar afval` | `3x Plastic schroot`, `2x Aluminium schroot`, `2x Blikschroot` |
| 3A | McKenzie Export | Verkoop plastic schroot | `3x Plastic schroot` | - |
| 3B | LS Gieterij | Verfijn aluminium schroot | `2x Aluminium schroot` | `2x Verfijnd aluminium` |
| 4B | LS Havenexport | Verkoop verfijnd aluminium | `2x Verfijnd aluminium` | - |
| 3C | LS Gieterij | Verfijn blikschroot | `2x Blikschroot` | `2x Verfijnd tin` |
| 4C | LS Havenexport | Verkoop verfijnd tin | `2x Verfijnd tin` | - |

## Grondstoffen voor geavanceerde routes

Deze pickups zijn op zichzelf nog geen volledige verkooproute, maar ze voeden de geavanceerde en premium ketens.

| Cargo | Min. level | Locatie | Resultaat per batch | Gebruikt voor |
| --- | ---: | --- | --- | --- |
| Giftig afval | 11 | Elysian afvaldepot | `1x Giftig afval` | Batterijen, beton |
| Gerecyclede elektronica | 13 | Elektronicawinkel | `1x Gerecyclede elektronica` | Sieraden |
| Steengroevepuin | 15 | Steengroeve | `1x Steengroevepuin` | Sieraden, batterijen, beton |

## Geavanceerde routes

### Sieraden

- Min. level: `15`
- Type: geavanceerde craft-route
- Uitleg: combineer puin en elektronica bij de juwelier en verkoop het eindproduct daar ook.

| Stap | Locatie | Actie | Benodigd | Resultaat |
| --- | --- | --- | --- | --- |
| 1 | Steengroeve | Laad steengroevepuin | - | `1x Steengroevepuin` |
| 2 | Elektronicawinkel | Laad gerecyclede elektronica | - | `1x Gerecyclede elektronica` |
| 3 | Juwelier | Maak sieraden | `1x Steengroevepuin`, `1x Gerecyclede elektronica` | `2x Sieraden` |
| 4 | Juwelier | Verkoop sieraden | `2x Sieraden` | - |

### Batterijen

- Min. level: `15`
- Type: geavanceerde multi-input route
- Uitleg: deze keten gebruikt steengroevepuin, recyclebaar afval en giftig afval.

| Stap | Locatie | Actie | Benodigd | Resultaat |
| --- | --- | --- | --- | --- |
| 1 | Steengroeve | Laad steengroevepuin | - | `1x Steengroevepuin` |
| 2 | Recyclingcentrum | Laad recyclebaar afval | - | `1x Recyclebaar afval` |
| 3 | Elysian afvaldepot | Laad giftig afval | - | `1x Giftig afval` |
| 4 | Batterijfabriek | Maak batterijen | `1x Steengroevepuin`, `1x Recyclebaar afval`, `1x Giftig afval` | `2x Batterijen` |
| 5 | Batterijexport | Verkoop batterijen | `2x Batterijen` | - |

## Premiumroutes

### Beton

- Min. level: `20`
- Type: premium route
- Uitleg: combineert vier grondstoffen tot beton.

| Stap | Locatie | Actie | Benodigd | Resultaat |
| --- | --- | --- | --- | --- |
| 1 | Steengroeve | Laad steengroevepuin | - | `1x Steengroevepuin` |
| 2 | Houthakkerskamp | Laad boomstammen | - | `2x Boomstammen` |
| 3 | Land Act Reservoir | Laad ongefilterd water | - | `2x Ongefilterd water` |
| 4 | Elysian afvaldepot | Laad giftig afval | - | `1x Giftig afval` |
| 5 | Betoncentrale | Meng beton | `1x Steengroevepuin`, `2x Boomstammen`, `2x Ongefilterd water`, `1x Giftig afval` | `2x Beton` |
| 6 | Alta bouwplaats | Verkoop beton | `2x Beton` | - |

### Wapeningsstaal

- Min. level: `20`
- Type: premium verwerkingsroute
- Uitleg: gebruikt metalen uit recycling plus beton.

| Stap | Locatie | Actie | Benodigd | Resultaat |
| --- | --- | --- | --- | --- |
| 1 | Recyclingketen afronden | Verzamel verfijnd aluminium en verfijnd tin | `2x Verfijnd aluminium`, `2x Verfijnd tin` | grondstoffen klaar |
| 2 | Betonroute afronden | Verzamel beton | `1x Beton` | grondstof klaar |
| 3 | Staalfabriek | Smeed wapeningsstaal | `2x Verfijnd tin`, `2x Verfijnd aluminium`, `1x Beton` | `2x Wapeningsstaal` |
| 4 | Alta bouwplaats | Verkoop wapeningsstaal | `2x Wapeningsstaal` | - |

### Huiskit

- Min. level: `100`
- Type: eindspelroute
- Uitleg: gebruikt meerdere eindproducten uit andere ketens.

| Stap | Locatie | Actie | Benodigd | Resultaat |
| --- | --- | --- | --- | --- |
| 1 | Verzamel alle eindproducten | Neem mee naar de woningbouwplaats | `2x Beton`, `2x Wapeningsstaal`, `1x Sieraden`, `1x Batterijen` | grondstoffen klaar |
| 2 | Woningbouwplaats | Bouw huiskit | `2x Beton`, `2x Wapeningsstaal`, `1x Sieraden`, `1x Batterijen` | `1x Huiskit` |
| 3 | Woningbouwplaats | Lever huiskit af | `1x Huiskit` | - |

## Transportsubtypes

### Gekoeld

- Min. level: `10`
- Type: voedselketen
- Uitleg: laad drie soorten gekoelde cargo en verwerk ze tot vliegtuigmaaltijden.

| Stap | Locatie | Actie | Benodigd | Resultaat |
| --- | --- | --- | --- | --- |
| 1 | Great Chaparral-boerderij | Laad groenten | - | `4x Groenten` |
| 2 | Grapeseed-boerderijen | Laad zuivelproducten | - | `4x Zuivelproducten` |
| 3 | Vleesverwerking | Laad vleeskratten | - | `3x Vleeskratten` |
| 4 | Luchtvaartcatering | Stel vliegtuigmaaltijden samen | `4x Groenten`, `4x Zuivelproducten`, `3x Vleeskratten` | `4x Vliegtuigmaaltijden` |
| 5 | Luchtvaartcatering | Lever vliegtuigmaaltijden af | `4x Vliegtuigmaaltijden` | - |

### Petrochemisch / Militair

- Min. level: `10`
- Type: grondstof + productie
- Uitleg: laad olie en gas en verwerk die in het militair depot tot explosieven.

| Stap | Locatie | Actie | Benodigd | Resultaat |
| --- | --- | --- | --- | --- |
| 1 | LS Oliepompstation | Pomp ruwe olie op | - | `2x Ruwe olie` |
| 2 | GSD Gaspompstation | Pomp ruw gas op | - | `2x Ruw gas` |
| 3 | Militair depot | Produceer explosieven | `2x Ruwe olie`, `2x Ruw gas` | `2x Explosieven` |
| 4 | Militair depot | Lever explosieven af | `2x Explosieven` | - |

### Illegale pillen

- Min. level: `17`
- Type: illegale keten
- Uitleg: haal capsules en methamfetamine op, pers pillen en lever die af aan de koper.

| Stap | Locatie | Actie | Benodigd | Resultaat |
| --- | --- | --- | --- | --- |
| 1 | Capsulelab | Laad pilcapsules | - | `4x Pilcapsules` |
| 2 | Liquor Ace | Laad methamfetamine | - | `2x Methamfetamine` |
| 3 | Illegale pillenpers | Pers pillen | `4x Pilcapsules`, `2x Methamfetamine` | `4x Gevulde pillen` |
| 4 | Zwarte markt koper | Verkoop pillen | `4x Gevulde pillen` | - |

## Locaties

| Locatie | Gebruik |
| --- | --- |
| Transporthoofdkwartier | Hoofdmenu, route-overzicht, huurvoertuigen |
| Gereedschapsdepot | Start gereedschapsroute |
| Ladingkoper: Gereedschap | Verkoop gereedschap |
| Kantooroverschot | Start gummenroute |
| Ladingkoper: Gummen | Verkoop gummen |
| Houthakkerskamp | Boomstammen laden |
| Zagerij | Boomstammen verwerken |
| LS Havenexport | Planken, zaagsel, verfijnd aluminium, verfijnd tin verkopen |
| Recyclingcentrum | Recyclebaar afval laden |
| Sorteercentrum | Recyclebaar afval sorteren |
| McKenzie Export | Plastic schroot verkopen |
| LS Gieterij | Aluminium/tin verfijnen |
| Elysian afvaldepot | Giftig afval laden |
| Elektronicawinkel | Gerecyclede elektronica laden |
| Steengroeve | Steengroevepuin laden |
| Juwelier | Sieraden maken en verkopen |
| Batterijfabriek | Batterijen maken |
| Batterijexport | Batterijen verkopen |
| Land Act Reservoir | Ongefilterd water laden |
| Betoncentrale | Beton mengen |
| Alta bouwplaats | Beton en wapeningsstaal verkopen |
| Staalfabriek | Wapeningsstaal smeden |
| Woningbouwplaats | Huiskit bouwen en leveren |
| Great Chaparral-boerderij | Groenten laden |
| Grapeseed-boerderijen | Zuivelproducten laden |
| Vleesverwerking | Vleeskratten laden |
| Luchtvaartcatering | Vliegtuigmaaltijden maken en verkopen |
| LS Oliepompstation | Ruwe olie laden |
| GSD Gaspompstation | Ruw gas laden |
| Militair depot | Explosieven maken en verkopen |
| Capsulelab | Pilcapsules laden |
| Liquor Ace | Methamfetamine laden |
| Illegale pillenpers | Pillen persen |
| Zwarte markt koper | Pillen verkopen |

## Praktische notities

- Laad- en verkoopacties gebruiken batchkeuzes van `1`, `3` of `10`.
- Zwaardere cargo betekent dat grotere trucks en trailers merkbaar beter uitkomen.
- De `pounder` wordt gebruikt als een vaste midden/bovensectie-benchmark voor laadruimte.
