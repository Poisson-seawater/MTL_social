#coding/SQL 

**Obligatoire:**
SELECT  <liste des résultats>
FROM   <liste des tables touchées par la question>

**Optionnel**
WHERE  <liste des critères de restriction>
GROUP BY  <liste des expressions d'agrégation>
HAVING  <liste des critères de restriction sur les agrégats>
ORDER BY  <liste des expressions de tri du résultat

#### Clés primaires (PK)
La clé primaire (primary key, PK) est une contrainte qu’on ajoute sur un attribut d’une table, et qui fait en sorte que cet attribut serve à identifier chaque ligne de façon unique pour une table donnée. La PK est souvent appliqué sur un attribut d’identification (ID).  

La clé primaire peut être :
- Clé primaire simple, i.e. composée d’un seul attribut
- Clé primaire composée, i.e. composée de plusieurs attributs

La PK est généralement appliquée sur le premier attribute de la table.
Symbole d'une clée noir. 


#### Clés lointaines (FK)
Utilisées afin de relier les tables entres elles lors de l’écriture de requêtes. La FK d’une table ira généralement lier la PK d’une autre table (ou autre valeur unique).
Représenter par une clé blanche.

Intégrité référentielle : L’intégrité référentielle signifie que la clé lointaine de la table doit (si NOT NULL) renvoyer à une ligne valide de la table référencée.  
*Par exemple : Dans une table Commande, une clé lointaine ClientID doit renvoyer vers les détails d’un ClientID existant dans la table Clients.*

La clé lointaine peut être :
- Clé lointaine simple, i.e. composée d’un seul attribut
- Clé loinataine composée, i.e. composée de plusieurs attributs


### Les jointures
Quatre types de jointures :
- INNER JOIN- LEFT  JOIN
- RIGHT JOIN
- FULL  JOIN


#### Jointure INTERNE (INNER) :
- Joint les entités de la table gauche avec les entités de la table droite
- Contient seulement les lignes pour lesquelles la condition de jointure est satisfaite.

Select *
From *owner*
	INNER JOIN *Pets* ON *FK = JF*

#### Jointure GAUCHE (LEFT) :
- Joint les entités de la table gauche avec les entités de la table droite
- Contient toutes les lignes de la table gauche ainsi que toutes les lignes de la table droite pour lesquelles la condition de jointure est satisfaite.

#### Jointure DROITE (RIGHT) :  
- Joint les entités de la table gauche et les entités de la table droite
- Contient toutes les entités de la table droite ainsi que toutes les entités de la table gauche pour lesquelles la condition de jointure est satisfaite.

#### Jointure PLEINE (FULL):  
- Joint les entités de la table gauche et les entités de la table droite
- Contient toutes les entités des deux tables.
- *ATTENTION* Ce type de jointure est très peu utilisé dans la réalité sauf si absolument nécessaire (peu efficace

![[jointureSQL.png]]




### Requêtes, Ordre d’exécution: 
L'ordre d'exécution des requêtes SQL est le suivant :  
1. FROM
2. JOINTURE(S)
3. WHERE
4. GROUP BY
5. AGRÉGATION(S)
6. HAVING
7. SELECT
8. ORDER BY
9. LIMIT ou TOP


 #### La clause GROUP BY
- Regrouper les données selon une ou plusieurs colonnes
- Lorsqu’on regroupe les données, il faut utiliser une ou plusieurs méthodes d’agrégation pour synthétiser l’information.
- Les fonctions d’agrégation sont utilisées pour accomplir ceci
- fonctions d’agrégation :
	- SUM, AVG, MIN, MAX, COUNT

##### Fonctions d’agrégation
- SUM : La somme des valeurs d’une colonne
- AVG : La moyenne des valeurs d’une colonne
- MIN : Le minimum des valeurs d’une colonne
- MAX : Le maximum des valeurs d’une colonne
- COUNT : Le nombre d’éléments pas NULL dans une colonne
	- COUNT(étoile): Retourne le nombre de lignes dans une table


#### WHERE VS HAVIN
WHERE
- liste des critères de restriction sur les enregistrements individuels
- Nécessite aucune clause supplémentaire

vs.

HAVING
- liste des critères de restriction sur les agrégats
- Nécessite l’utilisation de la clause GROUP BY
- Éléments communs:
	- Sert à filtrer les données!
	- Si la clause donne un résultat VRAI, l’enregistrement est conservé
	- Si elle donne un résultat FAUX, l’enregistrement n’est pas conservé

#### Union, Union All, Except et Intersect
Les Operateurs Union, Union All, Except et Intersect permettent de rassembler les résultats de différentes instructions SELECT dans une seule table.
- Chaque instruction SELECT dans UNION, UNION ALL ou EXCEPT doit avoir le même nombre de colonnes.
- Les colonnes doivent également avoir des types de données similaires.
- Les colonnes de chaque instruction SELECT doivent également être dans le même ordre.


##### L'opérateur UNION 
sert à combiner 2 ou plusieurs tables en les « superposant » l’une sur l’autre.
UNION ne sélectionne que des valeurs distinctes par défaut.


###### UNION ALL
L'opérateur UNION ALL sert aussi à combiner 2 ou plusieurs tables en les « superposant » l’une sur l’autre.
UNION ALL sélectionne toutes les lignes (incluant les doublons).


##### EXCEPT
L'instruction SQL EXCEPT renvoie les enregistrements de la requête SELECT de gauche, qui ne sont pas présents dans les résultats renvoyés par la requête SELECT sur le côté droit de l'instruction EXCEPT.

Une instruction SQL EXCEPT fonctionne de manière très similaire à celle de l'opérateur moins en mathématiques.

##### INTERSECT
L'instruction INTERSECT renverra uniquement les lignes communes aux deux ensembles de données.

### Les fonctions prédéfinies Built-in functions
 - les fonctions d’agrégation et
 - les fonctions scalaires 
 - (autre pas vue dans se cours)

Les **fonctions d’agrégations** se font sur un ensemble de valeurs et ne retournent qu’une seule valeur. Nous les avons largement couvert lors de l’utilisation de la clause GROUP BY :
- AVG, COUNT, SUM, MAX, MIN

Les **fonctions scalaires** se font sur une seule valeur et retournent une seule valeur qui a été transformée d’une certaine façon. Il y a plusieurs types de fonctions scalaires qui peuvent agir sur différents types de données (INT, CHAR, DATETIME,…), nous étudierons toutefois uniquement celles-ci:
- Les fonctions sur les dates
- Les fonctions mathématiques
- Les fonctions sur les chaînes de caractères "strings"

 
###### Fonctions prédéfinies (dates)
Fonction ([Consultez la documentation](https://msdn.microsoft.com/en-us/library/ms186724.aspx))|Résultat
--|--
GETDATE()| renvoie la date de l’instance de SQL Server
DAY(date)|renvoie un entier (exemple : 31)
MONTH(date)|renvoie un entier (exemple : 12)
YEAR(date)|renvoie un entier (exemple : 2016)
DATEDIFF(interval, start_date, end_date)|renvoie un entier
DATEADD(interval, number, date)|renvoie une date
DATENAME(date_part, date)|renvoie un entier ou une chaîne de caractères


###### Fonctions prédéfinies (math)
 

Fonction ([Consultez la documentation](https://msdn.microsoft.com/en-us/library/ms177516.aspx))|Résultat
--|--
ABS(numeric_expression)|renvoie la valeur absolue
ROUND(numeric_expression, n)|arrondit à la nième décimale
EXP(numeric_expression)|renvoie ex
CEILING(numeric_expression)|arrondit à l’entier supérieur
FLOOR(numeric_expression)|arrondit à l’entier inférieur
POWER(float_expression, y)|X à la puissance y
SQRT(float_expression)|renvoie la racine carrée

###### Fonctions prédéfinies (string)

Fonction ([Consultez la documentation](https://msdn.microsoft.com/en-us/library/ms181984.aspx))|Résultat
--|--
FORMAT( value, format [, culture ] )|Change le format d’affichage pour la culture voulue
LEN( string_expression )|Retourne le nombre de caractères d’une chaîne
CHARINDEX( expressionToFind , expressionToSearch [ , start_location ] )|Recherche une expression et retourne l’index de début de l’expression
CONCAT( string_value1, string_value2, . . . string_valueN)|Concatène deux (ou plus) chaînes de caractères
SUBSTRING( expression, start, length )|Retourne la chaîne de caractère de longueur length débutant en start
LEFT|Retourne la partie de gauche d’une chaîne, d’une longueur donnée
RIGHT|Retourne la partie de droite d’une chaîne, d’une longueur donnée
UPPER|Retourne la chaîne de caractères en majuscule
LOWER|Retourne la chaîne de caractères en minuscule
LTRIM|Retire tous les espaces à gauche d’une chaîne de caractères
RTRIM|Retire tous les espaces à droite d’une chaîne de caractères
TRIM|A l’effet combiné de LTRIM et de RTRIM


#### CONCAT
La concaténation : joindre deux chaînes de caractères bout à bout.
On peut utiliser la fonction CONCAT, ou encore joindre avec +.

SELECT CONCAT('bon matin ', 'classe!’) AS [salutation]
SELECT 'bon matin ' + 'classe!’      AS [salutation]

La concaténation avec CONCAT transforme en chaîne de caractères toutes les valeurs présentes dans son expression.
SELECT DISTINCT CONCAT('Prix: ', ListPrice) AS PriceTag
FROM  Production.Product

L’avantage de CONCAT est qu’il n’est pas nécessaire de modifier les données pour les concaténer car la fonction transforme tous les attributs présents en type caractère (string).

Le + ne transforme pas les attributs présents, et donc il faudra tous les convertir en type caractère (string) pour que cela fonctionne. Sinon le code ne s’exécutera pas et on recevra un message d’erreur.


#### FORMAT
La function FORMAT permet de contrôler la mise en forme d’une valeur numérique.

EN AUCUN CAS, elle ne modifie le contenue de la db!
Elle spécifie seulement sous quel format afficher la valeur dans la table virtuelle résultante de la requête.


SELECT 4.567890;
SELECT FORMAT(4.567890, '00.00’)
SELECT FORMAT(4.567890, '00.0#####’)
SELECT FORMAT(4.567890, '00.000000')
*la db = 4.567890 ; les 3 autres FORMAT change le nombre de chiffre après la virgule dans cette exemple.* 

###### Le séparateur de milliers
SELECT FORMAT(1900000, '#,#’)    --> séparateur de milliers
SELECT FORMAT(1900000, '#,0.00')  --> 2 chiffres après la virgule
SELECT FORMAT(445.89, 'C3’)    --> currency C=>Currency 3=>3 chiffres après la virgule
SELECT FORMAT(0.1234, '0.00%’)    -->  pourcentage


#### CASE
CASE fournit un moyen d’afficher des informations, selon des conditions, comme ceci :

USE OwnersAndPets;
SELECT
PetName, CASE WHEN PetAge > 3 THEN 'Older animal'
ELSE 'Younger animal’ 
END   AS 'message concerning age'
FROM Pets;


#### COALESCE
Coalesce retourne la première valeur non-nulle parmi sa liste d’arguments. Si tous les arguments donnés sont NULLs, la valeur retournée sera NULL.
COALESCE ( expression [ ,...n ] )
Autrement dit, on spécifie quel attribut affiché, si celui-ci est NULL alors quel autre 
attribut affiché, etc.

