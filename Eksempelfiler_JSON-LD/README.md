# Eksempelfiler JSON-LD
Databasen i GraphDB, også kalt "triple store", er direkte generert fra en dump av .jsonld-filer som igjen er generert av "vanlig" .json fra Greps REST-API.

Vi skal dokumentere dette mer nøye senere, men vi kan ta med noen punkter allerede nå, for det er verdt å merke seg noen forskjeller mellom en .json-representasjon av et objekt og en .jsonld-representasjon av det samme.

## @Context
Alle .jsonld-filer hos oss, starter med en @context-blokk.
Kort fortalt blir context brukt til å mappe termer til IRI-er.
I [JSON-LD-dokumentasjonen til W3C](https://w3c.github.io/json-ld-syntax/#the-context), forklarees det slik:
> *Når to personer kommuniserer med hverandre, foregår samtalen i et delt miljø, vanligvis kalt "konversasjonens kontekst". Denne delte konteksten gjør det mulig for enkeltpersoner å bruke snarveiuttrykk, som f.eks fornavnet til en felles venn, for å kommunisere raskere, men uten å miste nøyaktighet. En kontekst i JSON-LD fungerer på samme måte. Det tillater to applikasjoner å bruke snarveiuttrykk for å kommunisere med hverandre mer effektivt, men uten å miste nøyaktighet.*

### Eksempel på @context hos oss:
```
"@context": {
    "@vocab": "http://psi.udir.no/ontologi/kl06/",
    "uriId": "@id",
    "uri": {
      "@type": "@id"
    },
    "url-data": {
      "@type": "@id"
    },
    "grepType": "@type",
    "grep-type": {
      "@type": "@id"
    },
    "verdi": "@value",
    "spraak": "@language",
    "status": {
      "@type": "@id"
    }
```
#### Angående uriID og grepType i @context-sammenheng:
Noen vil kanskje reagere på at @context-elementene "uriID" og "grepType" avviker fra det man kunne forvente som "uri" og "grep-type" slik vi kjenner det fra .json.
Dette er en endring vi har gjort i .jsonld for at GraphDB skal kunne vise grep-type og uri, og at vi videre kan kjøre sparql-spørringer på dem.

Vi endret uri til uriId, og grep-type til grepType.

Videre la vi tilbake uri og grep-type som en "@type".
Dette gjør at GraphDB heller lager koblinger på grepType og uriId, slik at vi får beholde grep-type og uri som attributter på typene.

Husk at våre .jsonld-fileer er laget spesifikt for at de skal fungere som direkte kilde til GraphDBs triple store.

## Forflatning og løfting
Et annet avvik (eller skulle vi si, en serie med avvik) fra .json-filene våre er hvordan objektene ({}) er bygd opp.
### eksempel
Siden formålet med .jsonld er å forsyne GraphDB-repoet med tripler, trenger vi ikke å brodere ut mer enn bare referansen til de relaterte objektene. Se forskjellen på "fagtype" og "tilgjengelige-spraak" i filene vist nedenfor:
[bilde]
