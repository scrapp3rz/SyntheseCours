# I - Les structures de Données


# II - Encapsulation


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


	{
	"date" : 1.5274348196831222E9,
	"text" : " lorem ipsum",
	"user" : "eaIHGKF6EVUPIVICHbMgL8serC23"	
	}


Le scope est délimité par les { … } et les paires sont séparées par une virgule.



# IV - Instructions Conditionnelles / Boucles


# V - Opérateurs


