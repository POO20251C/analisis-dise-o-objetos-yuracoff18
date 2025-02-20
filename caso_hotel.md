## **Caso hotel**

### Miembros:
**Yura Hernandez**
**Juan José Bolivar**

```mermaid
classDiagram
    Reserva o-- Sistema : Contiene
    Persona o-- Sistema : contiene
    Persona <|-- Reserva : usa
    Habitacion <|-- Reserva : usa
    Sistema : - list Reservas
    Sistema : - list Personas
    Sistema : + checkOut()

    class Reserva{
        - int persona_id
        - int id_habitacion
        - string fecha_in
        - string fecha_out
        - bool already_out
        + hacerReserva()
    }

    class Persona{
      + int id_persona
      + bool is_in_sistem
      + string fecha_actual
      + Resgistrarse()
    }

    class Habitacion{
      - int id_habitacion
      - string tipo_de_habitacion
      - int tarifa_por_noche
    }
```