> *Greps SPARQL-endepunkt er en RDF-representasjon av innholdet i [Grep](https://www.udir.no/om-udir/data/kl06-grep/), som er den nasjonale databasen for fag, læreplaner og opplæringstilbud i grunnopplæringen. 
> Alle fastsatte læreplaner i Kunnskapsløftet (LK06 og LK20) ligger i Grep. 
> I tillegg finnes kodeverk og informasjon om fag i grunnskole og videregående opplæring (vgo), 
> inkludert vurderingsordninger, samt fag- og vitnemålsmerknader til bruk i dokumentasjon av opplæringen.*
# Om Greps nye SPARQL-endepunkt
## I produksjon fra 7. desember 2020
Tirsdag 29. september hadde vi en kick-off med de utvklerne som har fått oppdraget med å utvikle det nye SPARQL-endepunktet for Grep. Resultatet satte  vi i produksjon 07.12.2020. Prosjektet gikk som planlagt, og vi mener vi nå har en mer robust tjeneste enn tidligere som i tillegg er enklere og billigere å forvalte i framtida.
### Virtuoso ut, GrpahDB inn
Prosjektet gikk i korte trekk ut på å erstatte den forrige løsningen basert på [Virtuoso](https://virtuoso.openlinksw.com), med [GrpahDB](https://www.ontotext.com/products/graphdb/). Mer om hvorfor og hvordan senere...
### Prøv selv
Her er en [samling av SPARQL-spørringer](https://github.com/Utdanningsdirektoratet/Grep_SPARQL/wiki/Samling-av-SPARQL-sp%C3%B8rringer) du selv kan kjøre mot følgende testmiljøer hos oss (vi håper dere kan bruke testmiljøene til test og utforsking, og at produksjonsmijøet kun brukes til produksjonsformål for å spare serverbelastning):
* https://sandkasse-data.udir.no:7200/sparql - Testversjon, kalt Sandkassen, med GraphDB sitt workbench-grensesnitt. Bruk repoet KL06_201906. (data oppdateres manuelt ca ukentlig)
* https://beta-data.udir.no/kl06/sparql - Betaversjon som er mer likt produksjonsmiljøet, men der formålet er å teste eventuelle modellendringer i Grep (data oppdateres hver natt)