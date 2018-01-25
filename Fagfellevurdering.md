# Sjekkliste for fagfellevurdering

- Gjennomfør gjerne fagfellevurdering parvis 
- Dersom feilen du ser er en gjenganger burde den inn som sjekkliste-punkt i denne listen
- _Husk_ : Når du godkjenner Pull Requesten går koden til produksjon

## Generelt

- Akseptansekriterier
  - Verifiser at de er dekket i koden
  - Kjør opp appen lokalt og gjør en funksjonell verifikasjon av brukerhistorien
- Sjekk eventuelle feature-toggles. Sjekk at det fungerer å skru disse av og på, og at funksjonaliteten skjules/vises som forventet
- Clean code. Sjekk kodekvalitet, lesbarhet og forståelse, og at ting forstås funksjonelt
- Kodeanalyse
  - Sonar, se etter violations
  - Prettier
  - Linter
- Sjekk at policies er fulgt. Ref https://github.com/navikt/fo-policy
- Sjekk at evt. endringer i APIer og migreringsscript er bakoverkompatible
- Sjekk testkvalitet backend. Verifiser at relevant kode er testet. Kjør tester.
- Sjekk testkvalitet frontend. Verifiser at relevant kode er testet. Kjør tester.
- Sjekk at exceptions som fanges faktisk logges 
- Sjekk logger. Se etter warnings og errors
- Gå gjennom commit-meldinger. Disse bør inneholde JIRA-referanse og være forstålige for andre enn utviklere (meldingene brukes til vurdering på go/no-go-møtet).
- Hvis oppgaven er av en veldig teknisk art, pass på at det er kommentert på PK-saken hva som er gjort, evt hvorfor.
- Hvis oppgaven innebærer nytt design, få det godkjent av designer.

## Sikkerhet
- Autorisering. Sjekk at det gjøres ABAC-autorisering ved endring av/innføring av nye endepunkter
- Sjekk logger og se etter persondata som f.eks fnr. Abac-loggene skal i egne logger og ikke ligge tilgjengelig i Kibana
- Sjekk at URL-parametre ikke brukes direkte uten validering / sanitering	

## Database
- Ved opprettelse av tabeller eller nye kolonner, se etter potensielle behov for indekser
- Se etter manglende parametrisering av SQL. (SQL-injection)
- Sjekk at migreringen enten skjer fullstendig eller ikke i det hele tatt. Pass på at migreringen er wrappet inn i en transaction. Delvis migreringer er vanskelig å komme seg ut av.

## Universell utforming
- Se etter semantisk korrekt bruk av h1, h2, h3? Korrekt rekkefølge h1,h2,h3 i stedet for h6,h7,h8.
- Alle input, links, images og andre synlige elementer bør ha alt tekst.
- Input felter må ha placeholder og label.
- Alle elementer nås med tastatur. F.eks.: lenker, knapper, radioknapper, checkboxer, nedtrekksmenyer og funksjoner kan styres ved tastatur. At man kan navigere seg vekk/videre vha tastatur.
- Vurder punktene under "Design av enkeltelementer og koding" : https://confluence.adeo.no/display/INI754/FO+-+Brukskvalitetskrav+-+ekstern+arbeidsflate#expand-Kravtiltastaturnavigasjon

## Til slutt
- Husk å kommentere på PK-saken at man har utført fagfellevurdering.
  
