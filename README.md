# Tchin Tchin — redesign

Konceptredesign af [tchin-tchin.dk](https://tchin-tchin.dk): én `index.html` plus en `images/`-mappe, uden build-trin.

**Se siden live:** https://thonbogamer.github.io/tchin-tchin-redesign/

Siden er mærket "Koncept" i menuen og footeren og er sat til `noindex`, så den ikke dukker op i Google ved siden af den rigtige side.

## Se siden

Åbn `index.html` i Chrome, Safari eller Firefox. Der er ingen installation.

## Hvad er der på siden

- **Preloader**: et guldglas tegnes op og fyldes, før siden løfter sig.
- **Hero**: overskriften glider ind ord for ord. Ved siden af ligger en bunke kort med de rigtige produktfotos, som skifter af sig selv. Man kan swipe kortene væk eller trykke på et kort for at hoppe til drinken.
- **Om os**: teksten lyser op ord for ord, mens man scroller, og tallene tæller op. Pris-kortene vipper i 3D.
- **Fire trin, tyve sekunder**: når sektionen kommer i syne, afspiller den sig selv i rigtige 20 sekunder: hæld (4 sek.), is (3), shake (10) og servér (3). Hvert trin har et rigtigt foto, der åbner sig som en cirkel, og shake-trinnet tæller sine 10 sekunder ned. Uret har en knap til pause og afspil igen, og man kan klikke på et trin i tidslinjen.
- **Sortiment**: produktfotoet står fast i en buet ramme. Ved hver ny drink fejer drinkens farve hen over billedet, og det nye foto følger med. Baggrunden skifter farve, og hver drink har pris, faner med servering, inspiration og cocktail og et link til produktsiden i webshoppen.
- **Erhverv, events, kontakt og footer**: kortet vokser ud til fuld bredde, et kort med et foto følger musen under events, og formularen har labels, der flytter sig. Footeren har de rigtige links, Fødevarestyrelsens smiley og skiltet med aldersgrænse for salg.
- **Kurv**: skuffe med produktfotos, antal og subtotal, og en animation hvor en prik flyver op til kurven. Indholdet gemmes i `localStorage`.

## Billeder

Produktfotos, fotos af serveringstrinnene, smiley og skiltet med aldersgrænse er hentet fra tchin-tchin.dk. De er gemt i `images/`, og fotoene er konverteret til WebP i webstørrelse (ca. 390 KB i alt). Prisen, 161 kr. pr. flaske, står i `PRICE` i scriptet.

## Teknik

- Ren HTML, CSS og JavaScript i én fil.
- Eksterne afhængigheder: Google Fonts (Fraunces og Manrope) og [Lenis](https://github.com/darkroomengineering/lenis) 1.1.13 til blød scroll. Siden virker også uden Lenis.
- Respekterer `prefers-reduced-motion` og kan bruges med tastatur. Piletasterne bladrer i produktkortene.

## Mangler før lancering

- Kontaktformular og nyhedsbrev skal kobles til en server. Lige nu sender de ikke noget. Formularen tilbyder i stedet at åbne beskeden som en e-mail.
- Kurven sendes ikke videre til webshoppen. Knappen åbner den nuværende shop.
- Matchango og Cosmo Kiss findes i webshoppen, men er ikke med i sortimentet. Det er de heller ikke på den nuværende forside.
