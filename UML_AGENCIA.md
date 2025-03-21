
			
```mermaid
classDiagram
    class AgenciaRenta {
	-string nombre
	-vector  <Autos> auto
	-vector <Clientes> clientes 
			
	+AgenciaRenta(string n)
	+~AgenciaRenta()
	+void agregarAuto()
	+void agregarCliente()
	+void mostrarInfo() const
    }

    class Auto {
       -string placa
       -string modelo
       -bool disponible

       +Auto(string p, string m)
       +~Auto()
       +string getPlaca() const
       +string getModelo() const
       +bool estaDisponible() const
       +void rentar()
       +void devolver()
    }

    class Cliente {
        -int id
        -string nombre

        +Cliente(int i, string n)
        +~Cliente()
        +int getId() const
        
    }
        class Contrato {
        -Cliente* cliente
        -Auto* autoRentado
        -int dias
        +Contrato(Cliente* c, Auto* a, int d)
        +~Contrato()
    }


    AgenciaRenta *-- Auto : composicion 
    AgenciaRenta *-- Cliente :composicion 
    Contrato -->  Auto : Asociacion
    Contrato --> Cliente : Asociacion 

