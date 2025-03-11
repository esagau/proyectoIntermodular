## 1. Consultes de selecció simples
La millor manera d’iniciar l’estudi del llenguatge SQL és executar consultes senzilles en la base de dades. Abans, però, ens convé conèixer els orígens i evolució que ha tingut aquest llenguatge, els diferents tipus de sentències SQL existents (subdivisió del llenguatge SQL), com també els diferents tipus de dades (nombres, dates, cadenes...) que ens podem trobar emmagatzemades en les bases de dades. I, llavors, ja ens podrem iniciar en l’execució de consultes simples.

### 1.1. Orígens i evolució del llenguatge SQL sota el guiatge dels SGBD
El model relacional en què es basen els SGBD actuals va ser presentat el 1970 pel matemàtic Edgar Frank Codd, que treballava en els laboratoris d’investigació de l’empresa d’informàtica IBM. Un dels primers SGBD relacionals a aparèixer va ser el System R d’IBM, que es va desenvolupar com a prototip per provar la funcionalitat del model relacional i que anava acompanyat del llenguatge SEQUEL (acrònim de *Structured English Query Language*) per manipular i accedir a les dades emmagatzemades en el System R. Posteriorment, el mot SEQUEL es va condensar en SQL (acrònim de *Structured Query Language*).

Una vegada comprovada l’eficiència del model relacional i del llenguatge SQL, es va iniciar una dura cursa entre diferents marques comercials. Així, tenim el següent:

+ IBM comercialitza diversos productes relacionals amb el llenguatge SQL: System/38 el 1979, SQL/DS el 1981, i DB2 el 1983.

+ Relational Software, Inc. (actualment, *Oracle* Corporation) crea la seva pròpia versió de SGBD relacional per a la Marina dels EUA, la CIA i d’altres, i l’estiu del 1979 allibera *Oracle* V2 (versió 2) per a les computadores VAX (les grans competidores de l’època amb les computadores d’IBM).

El llenguatge SQL va evolucionar (cada marca comercial seguia el seu propi criteri) fins que els principals organismes d’estandardització hi van intervenir per obligar els diferents SGBD relacionals a implementar una versió comuna del llenguatge i, així, el 1986 l’ANSI (American National Standards Institute) publica l’estàndard SQL-86, que el 1987 és ratificat per l’ISO (Organització Internacional per a la Normalització, o International Organization for Standardization en anglès).

La taula [1.1](#taula) presenta les diferents revisions de l’estàndard SQL que han aparegut des de 1986. No ens cal saber què ha aportat cada revisió, sinó que aquestes revisions han existit.

###### Taula 1.1 Revisions de l'ensàndard SQL { #taula }

|  Any | Revisió | Àlies | Comentaris |
| :--- |   :---  | :---  |    :---    | 
| 1986 | SQL-86 | SQL-87 / SQL1 | Publicat per l'ANSI el 1986, i ratificat per l'ISO el 1987.|
| 1989 | SQL-89 |        | Petita revisió.|
| 1992 | SQL-92 | SQL2 | Gran revisió.|
| 1999 | SQL:1999 | SQL3 | Introdueix consultes recursives, disparadors...|
| 2003 | SQL:2003 |      | Introdueix temes d'XML, funcions Windows...|
| 2006 | SQL:2006 |      |        |

### 1.2. Tipus de sentències SQL
Els SGBD relacionals incorporen el llenguatge SQL per executar diferents tipus de tasques en les bases de dades: definició de dades, consulta de dades, actualització de dades, definició d’usuaris, concessió de privilegis... Per aquest motiu, les sentències que aporta el llenguatge SQL s’acostumen a agrupar en les següents:

1. Sentències destinades a la definició de les dades (LDD), que permeten definir els objectes (taules, camps, valors possibles, regles d’integritat referencial, restriccions...).

2. Sentències destinades al control sobre les dades (LCD), que permeten concedir i retirar permisos sobre els diferents objectes de la base de dades.

3. Sentències destinades a la consulta de les dades (LC), que permeten accedir a les dades en mode consulta.

4. Sentències destinades a la manipulació de les dades (LMD), que permeten actualitzar la base de dades (altes, baixes i modificacions).

En alguns SGBD no hi ha distinció entre LC i LMD, i únicament es parla d’LMD per a les consultes i actualitzacions. De la mateixa manera, a vegades s’inclouen les sentències de control (LCD) juntament amb les de definició de dades (LDD). No té cap importància que s’incloguin en un grup o que siguin un grup propi: és una simple classificació.

Tots aquests llenguatges acostumen a tenir una sintaxi senzilla, similar a les ordres de consola per a un sistema operatiu, anomenada **sintaxi auto-suficient**.

**SQL allotjat**
Les sentències SQL poden presentar, però, una segona sintaxi, sintaxi allotjada, consistent en un conjunt de sentències que són admeses dins d’un llenguatge de  programació anomenat *llenguatge amfitrió*.

Així, podem trobar LC i LMD que es poden allotjar en llenguatges de tercera generació com C, Cobol, Fortran..., i en llenguatges de quarta generació.

Els SGBD acostumen a incloure un llenguatge de tercera generació que permet allotjar sentències SQL en petites unitats de programació (funcions o procediments). Així, l’SGBD Oracle incorpora el llenguatge PL/SQL, l’SGBD SQLServer incorpora el llenguatge Transact-SQL, l’SGBD MySQL 5.x segueix la sintaxi SQL 2003 per a la definició de rutines de la mateixa manera que l’SGBD DB2 d’IBM.