```mermaid
classDiagram
    class Hotel {
        -String nombre
	    -vector habitaciones
	    -vector clientes 
        
     
     +Hotel(string)
     +~Hotel()
     +void agregarHabitacion(int, string)
     +void registrarCliente(Cliente* cliente)
     +void mostrarInfo()
    }

    class Habitaciones {
       -Numero
       -Tipo
       -Ocupada
       +Habitacion(int, string)
       +~Habitacion()
       +int getNumero() const
       +string getTipo() const
       +bool estaOcupada() const
       +void ocupar()
       +void desocupar
    }

    class Cliente {
        -int id
        -string nombre 
        +Cliente(int i, string n)
        +~Cliente()
        +int getId() const
    }

    Hotel *-- Habitaciones
    Hotel o-- Cliente
