Filene i denne mappen er ontologi-filer i TTL-format, samt en ordliste.ttl.
Dato-delen av filnavnet angir når filen er skapt, og det er den nyeste fila som skal importeres til GraphDB-repo, kalt "Ontologi".

Ved wiping av all data fra et GraphDB-miljø, skal det opprettes et nytt repo, kalt "Ontologi", og nyeste ttl-fil skal importeres til dette repoet.
Slik gjør du:

1. Importer til "201906" på vanlig måte, og påse at denne er default graph

2. Gjenopprette ekstra-repoene:
2.1 Opprett et nytt repo, kalt "Ontologi"
    - Oppe i høyre hjørne i workbench, velg repoet "Ontologi", slik at det er der du "står"
    - Importer fila
    - velger du å importere via URL, bruk raw-versjonen av Github-URLen til fila

2.2 Opprett et nytt repo, kalt "ordliste"
    - Oppe i høyre hjørne i workbench, velg repoet "ordliste", slik at det er der du "står"
    - Importer fila "ordliste.ttl"
    - velger du å importere via URL, bruk raw-versjonen av Github-URLen til fila
