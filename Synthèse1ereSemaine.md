
# I - Les structures de Données

Une structure de données est une manière d'organiser les données.
Les principales structures de données sont :

- les variables :	var	
- les constantes :	const	
- les tableaux :	tab[]
	

Elles peuvent être de plusieurs types qui sont :

- charactère: 			char	
- chaine de caractères :	string
- entier :			int	
- flottant :			float
- booléen :			bool
	
	
JavaScript s'occupe de definir le type, il n'y a donc pas besoin de le definir.


# II - Encapsulation

Définition de l'encapsulation : 
- Coupe  une classe / un contexte du reste du code grace aux { }. 
- Les class (attributs) ont des fonctions (méthodes) qui lui sont spécifiquement associés. 
- Le champ d'action des attributs et des méthodes est par défaut l'objet lui-même et non les autres objets.  
- Une méthode communique avec son attribut mais également avec les attributs de son attribut. L'inverse n'est pas possible (voir exemple let blop='blop')

Quand on intègre un objet dans une classe / un contexte, on dit qu'on INSTANCIE un objet à une classe. 



// Exemple d'utilisation: 

let blop = "blop"



    class Point {                                                              |
    constructor(x, y) {                         |                              | 
    this.x = x;                                 |   constructor                |
    this.y = y;                                 |   est un objet               |
    blop = "test"	//valable car il peut             	                     |
                     communiquer avec blop                                     |
    }                                                                          |
                                                                               |
                                                                               |  Classe Point est le contexte
    static distance(a, b) {                     |                              |
    const dx = a.x - b.x;                       |   static distance            |
    const dy = a.y - b.y;                       |    est un objet              |
    }                                                                          |
     dx = 3 //non valable car il ne peut pas                                   |
           communiquer avec static distance                                    |
           car il est en dehors des {}                                         |
  }                                                                            |
                                                                               |
dx = 3 //non valable car il ne peut pas                                        |
         communiquer avec static distance
         car il est en dehors des {}

 ==> class Point et ses fonctions peuvent communiquer avec let blop MAIS let blop = 'blop'  ne peut pas communiquer avec class Point 
 ====> COMMUNICATION À SENS UNIQUE 



## Définition de l'encapsulation :

Coupe une classe / un contexte du reste du code grace aux { }.
Les class (attributs) ont des fonctions (méthodes) qui lui sont spécifiquement associés.
Le champ d'action des attributs et des méthodes est par défaut l'objet lui-même et non les autres objets.
Une méthode communique avec son attribut mais également avec les **attributs** de son **attribut**. L'inverse n'est pas possible (voir exemple let blop='blop')
Quand l'on intègre un objet dans une classe / un contexte l'on dit que l'on **INSTANCIE** un objet à une classe.

// Exemple d'utilisation:

let blop = "blop"

class Point {                   |
 constructor(x, y) {            |                   | this.x = x; | constructor | this.y = y; | est un objet | blop = "test"	//valable car il peut | communiquer avec blop | } | | | Classe Point est le contexte static distance(a, b) { | | const dx = a.x - b.x; | static distance | const dy = a.y - b.y; | est un objet | } | dx = 3 //non valable car il ne peut pas | communiquer avec static distance | car il est en dehors des {} | } | | dx = 3 //non valable car il ne peut pas | communiquer avec static distance car il est en dehors des {}



==> class Point et ses fonctions peuvent communiquer avec let blop MAIS let blop = 'blop' ne peut pas communiquer avec class Point ====> COMMUNICATION À SENS UNIQUE




# III - JSON/Objets

## Qu’est ce que l’Objet?

L’objet, et par extension la POO (Programmation Orientée Objet) est une méthode de programmation qui se base sur la formation de modèles de données regroupées en une unité, l’objet.
Ainsi, lorsque l’on veut **instancier** un objet, il faut commencer par définir ce que seront ses **propriétés**. Afin de les définir, il est nécessaire de se rappeler que ces propriétés sont des variables qui seront accessibles pour **l’instanciation** de l’objet. 

Par exemple, un être humain peut être défini comme un objet et aura plusieurs propriétés, comme : 

Prénom
Surnom
Âge
Sexe
Couleur des yeux

On peut en imaginer bien d’autres, qui peuvent permettre de compléter les fonctionnalités de l’objet, mais aussi créer un second objet qui héritera du premier et en reprendra les propriétés en les modifiant et/ou en ajoutant d’autres pour le rendre plus spécifique.

Un **objet** a donc des **propriétés** (caractéristique d'un objet, sa couleur par exemple), mais a également des **méthodes** (capacité d'un objet, changer de couleur par exemple), c’est à dire ce que l’objet peut faire. 


Afin de construire un objet, il faut d’abord le définir via un **constructeur**, puis ensuite, une fois défini, on va **l'instancier**. Chaque **instanciation** est unique, et lorsque l’on a besoin d’utiliser un objet, on l’instance (on en crée une copie).

### Le constructeur : 

Il contient la structure de base de l’objet, sa **classe**, et la syntaxe est la même que pour une fonction, par exemple pour un humain générique : 

Function Human(forname, name, age, sex, eyes)  {
	this.forname = forname;
	this.surname = surname;
	this.age = age;
	this.sex = sex;
	this.eyes = eyes;
}

### L’instanciation et la modification de l’objet : 

Lorsque l’on instancie un objet, on utilise le constructeur pour attribuer à un nouvel objet les propriétés et les méthodes du constructeur.
Par exemple, pour la classe Human, on peut instancier un nouvel objet que l'on va appeler "ted" : 

Var ted = new Human(‘ted’, ‘teddy’, ’30’, ‘male’, ‘blue’)


Une fois l’objet instancié, on peut alors modifier ses propriétés ainsi.

ted.age = 20; 


## Le JSON

Le **JSON** est un format de données structurées que l’on retrouve en JS, mais également dans bien d’autres langages. 
Il repose sur une structure de paires **CLEF : VALEUR** et se structure ainsi : 

`{
        "date" : 1.5274348196831222E9,
        "text" : " lorem ipsum",
        "user" : "eaIHGKF6EVUPIVICHbMgL8serC23"
}`

Le scope est délimité par les { … } et les paires sont séparées par une virgule.



# IV - Instructions Conditionnelles / Boucles

Il existe deux types d'instructions :

-les instructions alternatives (condition,action)
-les instructions iteratives (répétition)

Les instructions alternatives sont de deux types :

- si-sinon : 		if-else
- switch :		switch
Les instructions itératives sont de deux types :

-nombre répétition connue :		for(initialisation ; condition de continuation ; incrément)
-nombre de reépétition inconnue :	while()

Pour le while() la condition d'arrêt peut être :
- au début :				while(condition d'arrêt)
- à la fin :				do ... while(condition d'arrêt)

# V - Opérateurs

Un opérateur est un caractère ou une chaine de caractère qui permet de réaliser une opération entre 2 *(et seulement 2)* opérandes !

## Les opérateurs arithmétiques

* `+` : l'opérateur d'addition et de concaténation
	ex : `1 + 3 => 4`
	ex : `'ab' + 'bc' => 'abbc'`
* `-` : l'opérateur de soustraction
	ex : `4 - 3 => 1`
* `/` : l'opérateur de division
	ex : `5 / 2 => 2.5`
* `\*` : l'opérateur de multiplication
	ex: `3 \* 2 => 6`
* `%` : l'opérateur "modulo"
	Renvoie le reste de la division euclidienne entière
	`ex: 10 % 2 => 0`
	`ex: 10 % 3 => 1`
* `\*\*` : l'opérateur d'exponentiation
	Permet d'effectuer la puissance d'un chiffre
	`ex: 3 ** 2 => 9`
* `++` : l'opérateur d'incrément à 1
	`ex: 5++ => 6`
* `--` : l'opérateur de décrément à 1
	`ex: 9-- => 8`

## Les opérateurs de comparaison

* `===` : l'opérateur "Strictement égal à"
	Renvoie `true` si les deux opérandes sont de même types et de valeurs égales
	`ex: 3 === 3 => true`
	`ex: 5 === 4 => false`
	`ex: '2' === 2 => false`
* `==` : l'opérateur "égal à" (à ne pas utiliser)
	Renvoie `true` si les deux opérandes sont de valeurs égales
	`ex: 3 == 3 => true`
	`ex: 5 == 4 => false`
	`ex: '2' == 2 => true`
* `!=` : l'opérateur "différent de"
	Renvoie `true` si les deux opérandes sont de types ou de valeurs différentes
	`ex: 3 != 5 => true`
	`ex: '3' != 3 => true`
	`ex: 'abc' != 'abc' => false`
* `>` : l'opérateur "Strictement supérieur à"
	renvoie `true` si l'opérande de gauche est strictement supérieure à celle de droite
	`ex: 4 > 2 => true`
	`ex: 4 > 8 => false`
	`ex: 4 > 4 => false`
	`ex: '4' > '2' => true`
* `<` : l'opérateur "Strictement inférieur à"
	renvoie `true` si l'opérande de gauche est strictement inférieure à celle de droite
	`ex: 4 < 2 => false`
	`ex: 4 < 8 => true`
	`ex: 4 < 4 => false`
	`ex: '2' < '4' => true`
* `>=` : l'opérateur "supérieur ou égal à"
	renvoie `true` si l'opérande de gauche est supérieure ou égale à celle de droite
	`ex: 4 >= 2 => true`
	`ex: 4 >= 4 => true`
* `<=` : l'opérateur "inférieur ou égal à"
	renvoie `true` si l'opérande de gauche est inférieure ou égale à celle de droite
	`ex: 4 <= 8 => true`
	`ex: 4 <= 4 => true`

##Les opérateurs logiques

* `&&` : l'opérateur ET Logique
	renvoie true si les deux opérandes renvoie true
* `||` : l'opératuer OU Logique
	renvoie true si une des deux opérande (ou les deux) renvoie true

## Les opérateurs particuliers

* `=` : l'opérateur d'affectation
	permet d'affecter une "valeur" à une variable
	ex: `a = "blop"`
* `!` : l'opérateur de négation
	permet d'utiliser l'état inverse
	ex: `!false => true`
* `+=` : l'opérateur d'affectation après addition
	ajoute une valeur à la valeur de la variable et stock le resultat dans cette variable
	ex: `a = 3; a += 2 => a: 5`
* `-=` : l'opérateur d'affectation après soustraction (déclinable avec tous les opérateurs arythmétiques classiques et les opérateurs logiques)
	soustrait une valeur à la valeur de la variable et stock le resultat dans cette variable
	ex: `a = 3; a -= 2 => a: 1`
* `.` : l'opérateur d'accession (voir JSON & Objects)
	permet d'accéder à une propriété d'un objet JSON
	NE FONCTIONNE PAS POUR LES TABLEAUX
	ex: `t = {"a" : 3} ; t.a => 3`
* `[]` : l'opérateur d'accession (JSON (Objets et tableaux))
	permet d'accéder à une propriété d'un objet JSON (méthode pour les tableaux)
	ex: `t = {3, 5 ,8} ; t[a] => 3`
	ex: `t = {"a" : 3, "b" : 5 ,"c" : 8} ; t[a] => 3`
* `()` : l'opérateur d'appel et d'instanciation (voir Objets)
	permet d'appeler une fonction par son nom et lui passer des paramètres
	ex: `fnct("blop")`
* `:` : l'opérateur d'assignation d'une valeur à une clé (voir JSON)
	permet d'assigner une valeur à une clé dans un objet JSON
	ex: `t = { key : "value` }`




