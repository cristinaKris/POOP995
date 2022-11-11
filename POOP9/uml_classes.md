@startuml
class Event {
    +startTime: DataTime
    +nombre: String
    +RegistrationClosed: boolean
    +execute()
}

interface Hola{
    +perro: int
    -gato: String
}

+class Foo{
    +estado: boolean
}

Hola <|-- Foo : herencia
@enduml