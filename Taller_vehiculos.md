@startuml
class Taller {
    String nombre
}
class Vehiculo {
    String tipo
    Int km
    String color
    Int numero_ruedas
    Int presion_ruedas
    String tamano_ruedas
}
class Motor {
    Int hp
    String numero_bastidor
}
class Combustible {
    String tipo
    String get_tipo()
    void set_tipo()
}
class Pais {
    String nombre
}

Vehiculo -- Pais : montado
Motor -- Pais : fabricado
Motor -- Combustible : tiene
Taller -- Vehiculo : tiene
@enduml
