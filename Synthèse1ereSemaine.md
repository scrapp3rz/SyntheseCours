I - Les structures de Données


II - Encapsulation

Définition de l'encapsulation : 
- Coupe  une classe / un contexte du reste du code grace aux { }. 
- Les class (attributs) ont des fonctions (méthodes) qui lui sont spécifiquement associés. 
- Le champ d'action des attributs et des méthodes est par défaut l'objet lui-même et non les autres objets.  
- Une méthode communique avec son attribut mais également avec les attribus de son attribu. L'inverse n'est pas possible (voir exemple let blop='blop')

Quand l'on intègre un objet dans une classe / un contexte, on dit que l'on INSTANCIE un objet à une classe. 



// Exemple d'utilisation: 

let blop = "blop"



    class Point {                                                              |
     constructor(x, y) {                        |                              | 
    this.x = x;                                 |   constructor                |
    this.y = y;                                 |   est un objet               |
    blop = "test"	//valable car il peut                                      |
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




III - JSON/Objets


IV - Instructions Conditionnelles / Boucles


V - Opérateurs
