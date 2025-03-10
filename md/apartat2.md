## 2. Consultes de selecció complexes
Una vegada coneixem els tipus de dades que facilita l’SGBD i sabem utilitzar la sentència SELECT per a l’obtenció d’informació de la base de dades amb la utilització de les clàusules select (selecció de columnes i/o expressions), from (selecció de les taules corresponents) i where (filtratge adequat de les files que interessen), estem en condicions d’aprofundir en les possibilitats que té la sentència SELECT, ja que només en coneixem les clàusules bàsiques.
A l’hora d’obtenir informació de la base de dades, ens interessa poder incorporar, en les expressions de les clàusules select i where, càlculs genèrics que els SGBD
faciliten amb funcions incorporades (càlculs com el valor absolut, arrodoniments, truncaments, extracció de subcadenes en cadenes de caràcters, extracció de l’any,
mes o dia en dates...), com també poder efectuar consultes més complexes que permetin classificar la informació, efectuar agrupaments de files, realitzar
combinacions entre diferents taules i incloure els resultats de consultes dins altres consultes.
### 2.1 Funcions incorporades a MySQL
Els SGBD acostumen a incorporar funcions utilitzables des del llenguatge SQL. El llenguatge SQL, en si mateix, no incorpora funcions genèriques, a excepció de les anomenades funcions d’agrupament.