# PATRONES DE DISEÑO

## Definición
### Cada patron describe un problema que ocurre en nuestro entorno regularmente y la solución a ese problema, de tal modo que se pueda aplicar esta solución un millón de veces
#### Al encontrar una buena solución busca reutilizarla eficientement
### Es un plantilla que puede aplicarse en muchas situaciones diferentes
### No hay que resolver cada problema partiendo de cero

## Patrones de diseño orientado a objetos
### Intervienen clases y objetos relacionados que están particularizados para resolver un problema de diseño general en un determinado contexto
### Nómina,abstrae e identifica los aspectos clave de una estructura de diseño y aquellas características que los volverán un diseño orientado a objetos reutilizable

## Elementos
### Nombre del Patrón
#### Leve idea de la problemática y su solución
### Problema
#### Plantear la problemática de una forma general
### Solución
### Consecuencias
#### Precio a pagar tras usar el patrón de diseño

## Descripción de los patrones
### Nombre y clasificación del patrón
### Proposito
### Motivación
### Aplicabilidad
### Estructura
### Participantes
### Colaboraciones
### Consecuencias
### Implementación
### Código ejemplo
### Usos conocidos
### Patrones relacionados

## Antipatrones de diseño
### Es una guía para un mal diseño de software
#### Da malas soluciones a problemas
### Lava flow
#### Da grandes cantidades de código de forma desordenada y con poca onuladocumentación
### The god
#### Una sola clase realiza todo
### Golder Hammer
#### Usa un solo paradigma para resolver cualquier problema
### Spaguetti code
#### Programas con estructuras de control de flujo compleja
### Fantasmas
#### Varias clases con mínimas o nulas responsabilidades
### Reinventar la rueda
#### Trata de resolver problemas que ya tienen solución

## Estructurales
### Usan la herencia para formar interfaces
#### Permite la colaboración entre objetos con interfaces incompatibles
### Describen formas de agrupar objetos para crear nuevas funcionalidades
#### Los objetos delegan responsabilidades a otros objetos
#### Divide una clase grande en dos jerarquías (abstracción e implementación) para desarrollarlas de forma indendiente
#### Permite añadir funcionalidades a objetos colocando estos dentro de objetos encapsuladores especiales que contienen estas funcionalidades
### Permite mantener mas objetos dentro de la cantidad disponible de memoria ram
### Puede ser estático o dínamico

## De comportamiento
### Describe los patrones de como las clases y los objetos se comunican

## Decorator
### Es usado para extender la funcionalidad de un objeto de manera dinámica sin cambiar el código fuente de la clase original o hacer uso de la herencia de implementación
### Con el fin de implementar su funcionalidad o abstraer servicios mas complejos de acceso
### Caracteristicas
#### Diseñado para tener la misma interfaz que el objeto real
##### Permite que el objeto cliente interactlúa con este de la misma forma en que lo haría con el objeto decorado
#### Tiene una referencia al objeto decorado, tiene todas las solicitudes del cliente y agrega alguna funcionalidad adicional antes o después de enviar los llamados al objeto decorado

## Adaptador
### Transforma una interfaz de una clase en otra
#### Si una clase no pudo utilizar la primera pueda hacer uso de ella a través de la segunda
#### Preserva la utilidad de la primera interfaz
### Se define una clase alrededor del objeto incompatible, a este objeto contenedor se le llama adaptador y se le llama adaptado al objeto al que envuelve
#### Adaptador
##### Proporciona la interfaz esperada por elcliente
##### Convierte las solicitudes del cliente en llamadas a la interfaz de la clase adaptada
#### Adaptado
##### Objeto al que envuelve
### Cuando se usa
#### Si se desea usar una clase existente y su interfaz no concuerda con la necesitada
#### Si se desea crear una clase reusable que copera con las clases no relacionadas
### Adaptador de clase
#### Diseñados por una subclase de la clase adaptada
#### Implementa la interfaz esperada por el objeto cliente
### Adaptador de objeto
#### Contiene una referencia a un objeto de adaptador
#### Implementa una interfaz de lo que el cliente espera
#### Llama a un método de objeto de adaptador y este invoca un método apropiado. Para la instancia adaptada quien referencia su contenido

## Facade
### Permite interactuar en forma centralizada con un subsistema de clases
### Subsistema
#### Conjunto de clases que trabajan juntas para generar un conjunto de servicios relacionados
#### Las clases clientes pueden necesitar interactuar con algunos de sus clases violándose el principio de ocultamiento de la información, esto puede provocar que le afecte al cliente cualquier cambio al sistema
### Provee un alto agrupamiento de interfaces reducidas
#### Hace que el subsistema sea mas fácil para el cliente
#### Con un objeto fachada los clientes pueden interactuar con el sistema evitando hacerlo con las instancias del subsistema

## Proxy
### Permite proporcionar un substituto o marcador de posición para otro objeto
### Controla el acceso al objeto original permitiéndole hacer algo antes o después de que la solicitud llegue al objeto original
### Un cliente puede llamar al proxy por medio de su interfaz y el objeto proxy
#### A su vez envía las llamadas al objeto destino
### El proxy oculta el hecho de que un objeto cliente esta negociando con un objeto remoto
### El proxy oculta el hecho de que un objeto cliente esta negociando con un objeto remoto o que no esta instanciado o necesita una especial autentificación
#### Es un intermediario entre el origen y el destino
##### tiene muchas responsabilidades

## Bridge
### En una jerarquía de clases con diferentes posibilidades de implementación
#### Desacopla la abstracción de esa jerarquía de su implementación de forma que ambos pueden ser modificados de forma independiente
### Una abstracción puede tener una o mas implementaciones de sus métodos, puede ser diseñada como un interfaz con una o mas implementaciones concretas
### Cuando se necesita una nueva subclase de la jerarquía establecida, se podría dar lugar a un numero exponencial de subclases
### Se puede lograr un diseño mucho más flexible y eficiente
### Separa las interfaces de las implementaciones colocando sus abstracciones e implementaciones en jerarquías separadas

## Aggregate Enfocer
### Las clases se diseñan para manejar datos y una funcionalidad
### Objetos agregados
#### Son la unión de otros objetos cuando algunos objetos contienen a otros como sus partes
### Cuando un objeto agregado es construido debe ser creado completamente
### Cuando una clase agregada es instanciada todas sus variables miembro deben ser inicializadas

## Object caché
### Se aplica cuando la construcción de un nuevo objeto es costoso en términos de procesamiento
### El objeto en la memoria no se almacena para siempre
### Define un número óptimo de objetos que se almacenarán en memoria y define por cuanto tiempo

## Clasificación
### Diseño
#### Son de un alto nivel pero a un nivel de granularidad mas fino
##### Grano grueso cuando un problema se parte en pedazos grandes
##### Grano fino un problema se parte en muchos pedazos
### Arquitectura
#### Son los esquemas primarios en la organizacion de un sietema de software
### Elementals
#### Estan directamente involucrados en la codificación por lo que son mas simples y específicos al lenguaje

## Patron Factory
### Interfaz abstracta para crear un método
### Delega a su subclase la responsabilidad de decidir a partir de cual clase se instancia un objeto
#### Todas las subclases son los métodos implementados de la clase padre
### Recomienda encapsular dentro de un método determinado
### La selección de una clase depende
#### Configuración de la apliacion
#### La expansión de requisitos y mejoras

## Abstract Factory
### Es una clase abstracta que suministra una interfaz para producir una familia de objetos
### Busca definir una interfaz abastarte para almacenar una familia de objetos relaionados
#### Definir una capa de servicios abstractos que defina la interfaz hacia un modulo de nivel superior
### Util cuando un objeto necesita crear clases relacionadas y dependientes sin tener que saber cuales clases son instancidas
### Para la modificación y mantenimiento de un software se utiliza los principios de desarrollo abierto y cerrrado

## Patron Builder
### Busca encapsular los detalles de la construcción de objetos
#### Sugiere mover la construcción logica fuera del objeto hacia una clase builder
#### Puede haber más de una clase builder con distinta implementacion
#### Usando este patron el objeto puede ser diseño ocultando la complejidad de la construcción
### Los detalles de la construcción de un objeto (estanciacion e inicializacion) se hacen como parte de un constructor
#### Ata el constructor a las componentes que constituyen al objeto
###  Es adecuado si el objeto de construcción es simple y el proceso de construcción este bien definido y estatico
### Debido a las diferentes implementaciones de los procesos de construcción el objeto se puede volver voluminoso y menos modular
### El objeto cliente crea instancias del metodo builder y del director
#### El cliente asocia el builder con el director
#### El cliente invoca el metodo builder sobre la instancia del objeto para comenzar la creación del objeto
#### Cuando la creación del objeto está completada el cliente invoca el método getobject sobre la instancia builder para obtener el nuevo objeto creado
### Permite crear otros objetos haciendo una copia del objeto prototipo haciendo las modificaciones respectivas

## Prototype
### Permite crear otros objetos haciendo una copia del objeto prototipo haciendo las modificaciones respectivas

## Singleton
### Asegura que exista una sola instancia de una clase y los objetos serán capaces de acceder a esta única instancia
#### Los objetos no podrán crear otras instancias de la clase
### Algunas veces se requiere una sola instancia de una clase durante el tiempo de vida de una aplicación

## Virtual Proxy
### Al ejecutar una aplicación no siempre se requieren todos los objetos de inmediato
### Virtual proxy pospone la creación del objeto hasta que la necesite
### Un objeto independiente referido como virtual proxy puede ser diseñado con su interfaz de igual manera que el objeto real
### Objetos cliente diferentes pueden crear una instancia del virtual proxy y utilizarse en lugar del objeto real
### El objeto proxy virtual mantiene una referencia al objeto real como uno de sus atributos

## Flyweight
### Se usa para crear un gran número de objetos que son solamente únicos en términos de pocos parametros
### Se aplica para diseñar de manera más eficiente la creación de objetos
#### El grupo de objetos creados puede compartir el objeto flyweight ya que representa su estado común
### Elimina la necesidad de almacenar la misma información invariante en todos los objetos de manera que se guarda una sola vez en forma de un objeto único

## Counting Proxy
### Usado para un conjunto de operaciones de conteo y registro para ejecutarse al momento de su invocación
### Sugiere encapsular la funcionalidad adicional en un objeto aparte referenciado como counting proxy
### Se diseña para tener la misma interfaz que el objeto proveedor de servicios al que el cliente accede
### En lugar de acceder al objeto proveedor de servicios directamente los cliente invocan los métodos de un counting proxy

## Iterator
### Permite a los cliente acceder al contenido de una colección de forma que esta se pueda iterar 
#### Sin conocer la estructura interna en que dichas colecciones están estructuradas
### El contenedor se debe desarrollar como una interfaz en la forma de un objeto iterador
#### Diferentes clientes puedan acceder a su contenido
### Un iterador puede ser diseñado como un iterador interno o externo
### Iterador interno
#### La coleccion ofrece métodos para visitar diferentes elementos de la colección
### Iterador externo
#### La función de la iteración es separada de la colección y se mantiene en el interior de otro objeto llamado iterador

## Visitor
### Es una forma de separar el algoritmo de la estructura del objeto
### Define la operación en una clase separada denominada visitar
#### Separa la operación de la colección de objetos
#### Por cada nueva operación definida una nueva clase visitar debe ser creada

## Command
### Se permite encapsular ordenes
#### Se independiza la clase cliente de quien reciba la solicitud
### Independiza a traves de un invocador el cual emite una solicitud en representación al cliente
### El conjunto de servicios de los objetos receptores pueden ser desacopladas
### Crea una abstracción por el procesamiento de acción a ejecutar en respuesta a la solicitud del cliente
#### Las acciones pueden ser almacenadas para facilitar acciones como deshacer

## Mediator
### Usado para diseñar una comunicación controlada y coordinada entre los grupos de objetos eliminando la necesidad de comunicación directa entre ellos
### Abstrae la interacción de todos los objetos en una clase separada llamada mediatriz
### Cada objeto es responsable de ofrecer los servicios pero los objetos no interactúan unos con otro directamente para esto
### Es mas fácil alterar el comportamiento de las relaciones entre los objetos reemplazando

## Cadena de responsabilidad
### Para cuando hay mas de un objeto que puede administrar o atenderían solicitud
### Da a cada objeto una oportunidad para procesar las solicitudes de manera secuencial
### Cada objeto puede ser organizados en forma de una cadena con cada objeto mediante un puntero al próximo objeto de la cadena
#### El primer objeto recibe la solicitud y decide si debe administrar la solicitud o pasarla al próximo objeto

## Observer
### Diseñar un modelo de comunicación entre un conjunto de objetos independientes en un objeto del que dichos objetos dependen
### Al conjunto de objetos dependientes se les llama observadores y al conjunto del que ellos dependen se les llama sujeto
### El objeto debe suministrar una interfaz para registrar los cambios y notificaciones

## Interpreter
### Para interpretar una combinación de reglas gramaticales de un lenguaje
### Aplicar una jerarquía de clases donde cada clase una regla gramatical separada

## NULL object
### Elimina la necesidad que tiene un cliente de verificar si el objeto devuelto es nulo
### Encapsular el comportamiento en una clase que provee los métodos de las demas subclases pro con la implementación por defecto para sus metodos

## Strategy
### Util cuando hay un conjunto de algoritmos relacionados
### Un cliente necesita elegir uno de estos algoritmos e intercambiarlos según las necesidades
### Encapsula los algoritmos en una jerarquía y que el cliente trabaje con un intermediario llamado contexto

## State
### Para el diseño eficiente de una clase
### Cada instancia puede tener muchos estados y exhibir diferentes comportamientos
### Es utilizado cuando el parón de comportamiento de un objeto cambia dependiendo del estado del mismo
### La clase que recibe diferentes comportamientos se llama contexto de la clase
### El contexto resuelve distintos comportamientos según su estado