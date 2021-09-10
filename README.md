> *Greps SPARQL-endepunkt er en RDF-representasjon av innholdet i [Grep](https://www.udir.no/om-udir/data/kl06-grep/), som er den nasjonale databasen for fag, læreplaner og opplæringstilbud i grunnopplæringen. 
> Alle fastsatte læreplaner i Kunnskapsløftet (LK06 og LK20) ligger i Grep. 
> I tillegg finnes kodeverk og informasjon om fag i grunnskole og videregående opplæring (vgo), 
> inkludert vurderingsordninger, samt fag- og vitnemålsmerknader til bruk i dokumentasjon av opplæringen.*
# Om Greps nye SPARQL-endepunkt
## I produksjon fra 7. desember 2020
> NB: Det meste av informasjonen om Greps SPARQL-tjeneste finner du i "<a href="/Utdanningsdirektoratet/Grep_SPARQL/wiki">Wiki</a>" i toppmenyen

Tirsdag 29. september 2020, hadde vi en kick-off med de utvklerne som har fått oppdraget med å utvikle det nye SPARQL-endepunktet for Grep. Resultatet satte  vi i produksjon 07.12.2020. Prosjektet gikk som planlagt, og vi mener vi nå har en mer robust tjeneste enn tidligere som i tillegg er enklere og billigere å forvalte i framtida.
### Virtuoso ut, GrpahDB inn
Prosjektet gikk i korte trekk ut på å erstatte den forrige løsningen basert på [Virtuoso](https://virtuoso.openlinksw.com), med [GrpahDB](https://www.ontotext.com/products/graphdb/).

Den forrige løsningen var basert på oppdatering av data via en protokoll, kalt [SDShare Protocol](https://www.sdshare.org/), men det viste seg relativt dyrt og tungvinnt å skrive om denne hver gang vi gjorde små eller store endringer i datagrunnlaget. Da vi startet arbeidet med å gå over til GraphDB, valgte vi å ikke ta hensyn til endringer. Vi sletter databasen for SPARQL-tjenesten, og deretter og importerer nye data hver natt. Dette er en relativt rask prosess, som skjer litt over midnatt hver natt (typisk rundt ca 00:30). Enddringshistorikk ivaretar vi i forbindelse med det vi har "under panseret" for REST-tjenestene, i SPARQL-sammenheng, har vi valgt å kun tilby "dagens bilde".
### Prøv selv
<a href="/Utdanningsdirektoratet/Grep_SPARQL/wiki/Hvordan-bruke-Greps-SPARQL-tjeneste">Les her om hvordan du kan bruke Greps SPARQL-tjeneste</a> (en side fra wikien)

> Dette og mere til, finner du under "<a href="/Utdanningsdirektoratet/Grep_SPARQL/wiki">Wiki</a>" i toppmenyen
