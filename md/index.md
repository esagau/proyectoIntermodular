## Introducció
Les aplicacions informàtiques utilitzades en l’actualitat per a la gestió de qualsevol organització mouen una quantitat considerable de dades que s’emmagatzemen en bases de dades gestionades per sistemes gestors de bases de dades (SGBD).

Hi ha bases de dades ofimàtiques, com ara Ms-Access o Base de l’OpenOffice, que donen prou prestacions per emmagatzemar informació que podríem anomenar *domèstica*. En podem trobar molts exemples: base de dades per organitzar els nostres volums musicals (discos, CD...), base de dades per portar la comptabilitat domèstica, base de dades per gestionar les fotos que tenim a casa, base de dades per gestionar els llibres de la nostra biblioteca... I, també, per què no, gestionar les dades de petites organitzacions empresarials (botigues, tallers...). Però les bases de dades ofimàtiques acostumen a no tenir prou recursos quan es tracta de gestionar grans volums d’informació a la qual han de poder accedir molts usuaris simultàniament des de la xarxa local i també des de llocs de treball remots i, per aquest motiu, apareixen les bases de dades corporatives.

Tots els SGBD (ofimàtics i corporatius) incorporen el llenguatge SQL (*structured query language*) per poder donar instruccions al sistema gestor i així poder efectuar altes, baixes, consultes i modificacions, i crear les estructures de dades (taules i índexs), i als usuaris perquè puguin accedir a les bases de dades, concedirlos i revocar-los permisos d’accés... El treball en SGBD ofimàtics s’acostuma a efectuar sense utilitzar aquest llenguatge, ja que la interfície gràfica que aporta l’entorn acostuma a permetre qualsevol tipus d’operació. Els SGBD corporatius també aporten (cada vegada més) interfícies gràfiques potents que permeten efectuar moltes operacions però, tot i així, es fa necessari el coneixement del llenguatge SQL per efectuar múltiples tasques.

En aquesta unitat, “Llenguatge SQL. Consultes”, farem els primers passos en el coneixement del llenguatge SQL, i ens introduirem en els tipus de dades que pot gestionar i en el disseny de consultes senzilles a la base de dades, per passar a ampliar el nostre coneixement sobre el llenguatge SQL per tal d’aprofitar tota la potència que dóna en l’àmbit de la consulta d’informació. Així, per exemple, aprendrem a ordenar la informació, a agrupar-la efectuant-hi filtratges per reduir el nombre de resultats, a combinar resultats de diferents consultes... És a dir, que aquest llenguatge és una meravella que possibilita efectuar qualsevol tipus de consulta sobre una base de dades per obtenir la informació volguda.

Concretament, en l’apartat “Consultes de selecció simples” es fa una breu introducció als diferents tipus de sentències SQL per a passar a veure els tipus de dades que suporta MySQL (SGBD amb el que es treballa en aquests materials) i per acabar veient l’estructura bàsica de la sentència de selecció SELECT.

En l’apartat “Consultes de selecció complexes” es donaran a conèixer les funcions més importants que incorpora MySQL, així com algunes clàusules opcionals de la sentència de selecció SELECT que permeten ordenar o agrupar files o combinar diverses taules.

També trobareu un “Annex 1. MySQL” que us guiarà durant la instal·lació de MySQL i dóna unes indicacions per a donar els primers passos en aquest entorn on es treballarà al llarg de tota la unitat.

Per adquirir un bon coneixement del llenguatge SQL, és necessari que aneu reproduint en el vostre ordinador tots els exemples incorporats en el text, i també les activitats i els exercicis d’autoavaluació. I per a això, utilitzarem l’SGBD MySQL i les eines adequades seguint les instruccions del material web d’aquest mòdul.

## Resultats d'aprenentatge
En finalitzar aquesta unitat l’alumne/a:

1. Consulta la informació emmagatzemada en una base de dades emprant assistents, eines gràfiques i el llenguatge de manipulació de dades.

    + Identifica les funcions, la sintaxi i les ordres bàsiques del llenguatge SQL per consultar i modificar les dades de la base de dades de manera interactiva.
  
    + Empra assistents, eines gràfiques i el llenguatge de manipulació de dades sobre un SGBDR corporatiu de manera interactiva i tenint en compte les regles sintàctiques.
   
    + Fa consultes simples de selecció sobre una taula (amb restricció i ordenació) per consultar les dades d’una base de dades.
   
    + Fa consultes utilitzant funcions afegides i valors nuls.
  
    + Fa consultes amb diverses taules mitjançant composicions internes.
  
    + Fa consultes amb diverses taules mitjançant composicions externes.
   
    + Fa consultes amb subconsultes.