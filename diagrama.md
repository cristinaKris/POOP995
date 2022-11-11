@startuml
class Animal{
    - nombre: String
    - lugarOrigen: String
    - color: String
    + sonidos(String): void 
    + comer(): void
}

class AnimalAcuatico{
    - numeroAletas: int
    + nadar(): void
    + comer(): void
}

class AnimalTerrestre{
    - numeroPatas: int
    + correr(): void
    + comer(): void
}

class AnimalAereo{
    - numeroAlas: int
    + volar(): void
    + comer(): void
}

class Ballena{
    - largo: int
    + pelearConPinocho(): void
}

class Perro{
    - colorCollar: String
    + hacerTrucos(): void
}

class Pajaro{
    - tipoPico: String
    + recolectarRamas(): void
}

Animal <|-- AnimalAcuatico : herencia
Animal <|-- AnimalTerrestre : herencia
Animal <|-- AnimalAereo : herencia
AnimalAcuatico <|-- Ballena : herencia
AnimalTerrestre <|-- Perro : herencia
AnimalAereo <|-- Pajaro : herencia
@enduml