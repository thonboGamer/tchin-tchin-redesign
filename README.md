# Tchin Tchin — redesign

Konceptredesign af [tchin-tchin.dk](https://tchin-tchin.dk): én `index.html` plus en `images/`-mappe, uden build-trin.

## Se siden

Åbn `index.html` i Chrome, Safari eller Firefox. Der er ingen installation.

## Hvad er der på siden

- **Preloader**: et guldglas tegnes op og fyldes, før siden løfter sig.
- **Hero**: overskriften glider ind ord for ord. Ved siden af ligger en bunke kort med de rigtige produktfotos, som skifter af sig selv. Man kan swipe kortene væk eller trykke på et kort for at hoppe til drinken.
- **Om os**: teksten lyser op ord for ord, mens man scroller, og tallene tæller op. Pris-kortene vipper i 3D.
- **Fire trin, tyve sekunder**: sektionen står fast, mens man scroller vandret gennem de fire trin. Hvert trin har et rigtigt foto, der åbner sig som en cirkel, og en guldring der fyldes. Et ur tæller til 20.
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

- Kontaktformular og nyhedsbrev skal kobles til en server. Lige nu viser de kun en bekræftelse.
- Kurven sendes ikke videre til webshoppen. Knappen åbner den nuværende shop.
- Matchango og Cosmo Kiss findes i webshoppen, men er ikke med i sortimentet. Det er de heller ikke på den nuværende forside.
