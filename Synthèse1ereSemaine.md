# I - Les structures de Données


# II - Encapsulation


# III - JSON/Objets


# IV - Instructions Conditionnelles / Boucles


# V - Opérateurs
Un opérateur est un caractère ou une chaine de caractère qui permet de réaliser une opération entre 2 *(et seulement 2)* opérandes !

## Les opérateurs arythmétiques

* `+` : l'opérateur d'addition et de concaténation
	ex : `1 + 3 => 4`
	ex : 'ab' + 'bc' => 'abbc'
* "-" : l'opérateur de soustraction
	ex : 4 - 3 => 1
* "/" : l'opérateur de division
	ex : 5 / 2 => 2.5
* "\*" : l'opérateur de multiplication
	ex: 3 \* 2 => 6
* "%" : l'opérateur "modulo"
	Renvoie le reste de la division euclidienne entière
	ex: 10 % 2 => 0
	ex: 10 % 3 => 1
* "\*\*" : l'opérateur d'exponentiation
	Permet d'effectuer la puissance d'un chiffre
	ex: 3 ** 2 => 9
* "++" : l'opérateur d'incrément à 1
	ex: 5++ => 6
* "--" : l'opérateur de décrément à 1
	ex: 9-- => 8

## Les opérateurs de comparaison

* "===" : l'opérateur "Strictement égal à"
	Renvoie "true" si les deux opérandes sont de même types et de valeurs égales
	ex: 3 === 3 => true
	ex: 5 === 4 => false
	ex: '2' === 2 => false
* "==" : l'opérateur "égal à" (à ne pas utiliser)
	Renvoie "true" si les deux opérandes sont de valeurs égales
	ex: 3 == 3 => true
	ex: 5 == 4 => false
	ex: '2' == 2 => true
* "!=" : l'opérateur "différent de"
	Renvoie "true" si les deux opérandes sont de types ou de valeurs différentes
	ex: 3 != 5 => true
	ex: '3' != 3 => true
	ex: 'abc' != 'abc' => false
* ">" : l'opérateur "Strictement supérieur à"
	renvoie "true" si l'opérande de gauche est strictement supérieure à celle de droite
	ex: 4 > 2 => true
	ex: 4 > 8 => false
	ex: 4 > 4 => false
	ex: '4' > '2' => true
* "<" : l'opérateur "Strictement inférieur à"
	renvoie "true" si l'opérande de gauche est strictement inférieure à celle de droite
	ex: 4 < 2 => false
	ex: 4 < 8 => true
	ex: 4 < 4 => false
	ex: '2' < '4' => true
* ">=" : l'opérateur "supérieur ou égal à"
	renvoie "true" si l'opérande de gauche est supérieure ou égale à celle de droite
	ex: 4 >= 2 => true
	ex: 4 >= 4 => true
* "<=" : l'opérateur "inférieur ou égal à"
	renvoie "true" si l'opérande de gauche est inférieure ou égale à celle de droite
	ex: 4 <= 8 => true
	ex: 4 <= 4 => true

## Les opérateurs logiques

* "&&" : l'opérateur ET Logique
	renvoie true si les deux opérandes renvoie true
* "||" : l'opératuer OU Logique
	renvoie true si une des deux opérande (ou les deux) renvoie true

## Les opérateurs particuliers

* "=" : l'opérateur d'affectation
	permet d'affecter une "valeur" à une variable
	ex: a = "blop"
* "!" : l'opérateur de négation
	permet d'utiliser l'état inverse
	ex: !false => true
* "+=" : l'opérateur d'affectation après addition
	ajoute une valeur à la valeur de la variable et stock le resultat dans cette variable
	ex: a = 3; a += 2 => a: 5
* "-=" : l'opérateur d'affectation après soustraction (déclinable avec tous les opérateurs arythmétiques classiques et les opérateurs logiques)
	soustrait une valeur à la valeur de la variable et stock le resultat dans cette variable
	ex: a = 3; a -= 2 => a: 1
* "." : l'opérateur d'accession (voir JSON & Objects)
	permet d'accéder à une propriété d'un objet JSON
	NE FONCTIONNE PAS POUR LES TABLEAUX
	ex: t = {"a" : 3} ; t.a => 3
* "[]" : l'opérateur d'accession (JSON (Objets et tableaux))
	permet d'accéder à une propriété d'un objet JSON (méthode pour les tableaux)
	ex: t = {3, 5 ,8} ; t[a] => 3
	ex: t = {"a" : 3, "b" : 5 ,"c" : 8} ; t[a] => 3
* "()" : l'opérateur d'appel et d'instanciation (voir Objets)
	permet d'appeler une fonction par son nom et lui passer des paramètres
	ex: fnct("blop")
* ":" : l'opérateur d'assignation d'une valeur à une clé (voir JSON)
	permet d'assigner une valeur à une clé dans un objet JSON
	ex: t = { key : "value" }
