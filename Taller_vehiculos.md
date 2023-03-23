@startuml
class Taller {
    String nombre
    void setNombre(String nombre)
    String getNombre()
}
class Vehiculo {
    String tipo
    Int km
    String color
    Int numero_ruedas
    Int presion_ruedas
    String tamano_ruedas
    Int precio
    Int numero_puertas
    Int peso
    Int getPesoPotencia()
}
class Motor {
    Int hp
    String numero_bastidor
    String combustible
}

class Pais {
    String nombre
}

Vehiculo "0..n" -- "1..n" Pais : montado
Motor "1..n" -- "1" Pais : fabricado
Taller "1" -- "0..n" Vehiculo : tiene
Vehiculo "1" -- "1..n" Motor : tiene
@enduml

