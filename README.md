# Policies for Forenklet Oppfølging

## Manuelle policies 
- Gjennomgå [sjekkliste for fagfellevurdering](https://github.com/navikt/fo-policy/blob/master/Fagfellevurdering.md) 

## Automatiske policies
- Alle commits tagges med brukerhistorie
  * https://github.com/navikt/pus-policy-validator/blob/master/src/main/java/no/nav/pus/policyvalidator/TaggetMedBrukerhistorie.java
  * https://github.com/navikt/pus-policy-validator/blob/master/src/test/java/no/nav/pus/policyvalidator/TaggetMedBrukerhistorieTest.java

- Alle package.json definerer faste versjoner
  * https://github.com/navikt/pus-policy-validator/blob/master/src/main/java/no/nav/pus/policyvalidator/FasteVersjoner.java
  * https://github.com/navikt/pus-policy-validator/blob/master/src/test/java/no/nav/pus/policyvalidator/FasteVersjonerTest.java