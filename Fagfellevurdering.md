# Sjekkliste for fagfellevurdering

- Gjennomfør gjerne fagfellevurdering parvis 
- Dersom feilen du ser er en gjenganger burde den inn som sjekkliste-punkt i denne listen
- _Husk_ : Når du godkjenner Pull Requesten går koden til produksjon

## Generelt

- Gjør en gjennomgang av akseptansekriterier og verifiser at de er dekket i koden
- Kjør opp appen lokalt og gjør en teknisk verifikasjon av brukerhistorien
- Sjekk eventuelle feature-toggles. Sjekk at det fungerer å skru disse av og på, og at funksjonaliteten skjules/vises som forventet
- Clean code. Sjekk kodekvalitet, lesbarhet og forståelse, og at ting forstås funksjonelt
- Sjekk kodeanalyse i Sonar, se etter violations
- Sjekk at policies er fulgt. Ref https://github.com/navikt/fo-policy
- Sjekk at evt. endringer i APIer og migreringsscript er bakoverkompatible
- Sjekk testkvalitet. Verifiser at relevant kode er testet 
- Sjekk at exceptions som fanges faktisk logges 
- Sjekk logger. Se etter warnings og errors
- Sjekk at brukerhistorie er tagget med nødvendig metadata

## Sikkerhet
- Autorisering. Sjekk at det gjøres ABAC-autorisering ved endring av/innføring av nye endepunkter
- Sjekk logger og se etter persondata som f.eks fnr. Abac-loggene skal i egne logger og ikke ligge tilgjengelig i Kibana
- Sjekk at URL-parametre ikke brukes direkte uten validering / sanitering	

## Database
- Ved opprettelse av tabeller eller nye kolonner, se etter potensielle behov for indekser
- Se etter manglende parametrisering av SQL. (SQL-injection)

## Universell utforming
- Se etter semantisk korrekt bruk av h1, h2, h3? Korrekt rekkefølge h1,h2,h3 i stedet for h6,h7,h8.
- Alle input, links, images, buttons og andre synlige elementer bør ha alt tekst.
- Input felter må ha placeholder og label.
  
