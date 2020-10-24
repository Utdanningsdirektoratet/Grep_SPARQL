> Grep er den nasjonale databasen for fag, læreplaner og opplæringstilbud i grunnopplæringen. 
> Alle fastsatte læreplaner i Kunnskapsløftet (LK06 og LK20) ligger i Grep. 
> I tillegg finnes kodeverk og informasjon om fag i grunnskole og videregående opplæring (vgo), 
> inkludert vurderingsordninger, samt fag- og vitnemålsmerknader til bruk i dokumentasjon av opplæringen.
# Utvikling av Greps SPARQL-endepunkt
## Pågående prosjekt høsten 2020
Tirsdag 29. september hadde vi en kick-off med de utvklerne som har fått oppdraget med å utvikle det nye SPARQL-endepunktet for Grep, og som vi håper å kunne sette i produksjon i løpet av november. Prosjektet går som planlagt, og vi kan nå invitere interesserte i å prøve dette i et testmiljø vi har kalt "[Sandkassen](https://sandkasse-data.udir.no:7200/sparql)".
### Virtuoso ut, GrpahDB inn
Prosjektet går i korte trekk ut på å erstatte dagens løsning basert på [Virtuoso](https://virtuoso.openlinksw.com), med [GrpahDB](https://www.ontotext.com/products/graphdb/). Mer om hvorfor og hvordan senere...
### Prøv selv
I tilknytning til den gamle Virtuoso-løsningen vår, lagde vi en samling [sparql-apørringer](http://grepwiki.udir.no/index.php?title=SPARQL-spørringer) som kunne kjøres mot http://data.udir.no/kl06/sparql.
I forbindelse med dette prosjektet, har vi prøvd å konvertere disse spørringene (i samlingen) til noe som fungerer mot det nye endepunktet. Se:
* [Samling av SPARQL-spørringer](https://github.com/Utdanningsdirektoratet/Grep_SPARQL/blob/main/Samling%20av%20SPARQL-sp%C3%B8rringer.md) - Eksempler du kan teste mot:
* https://sandkasse-data.udir.no:7200/sparql - Testversjon (anbefaler for tiden repoet kalt "NavnFiksing")
