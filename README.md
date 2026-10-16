# TravelNow – Modelado de comportamiento con UML

**Plataforma de reservas y check-in de una cadena hotelera**

Repositorio individual de consolidación de los Trabajos Prácticos Experimentales 1 y 2 de la asignatura **Modelamiento de Software**.

| | |
|---|---|
| Universidad | Universidad Estatal de Milagro (UNEMI) |
| Facultad / Carrera | Facultad de Ciencias e Ingeniería – Ingeniería de Software |
| Docente | MSC. Guevara Serrano Jorge Dumar |
| Periodo | Agosto – diciembre 2026 |
| Estudiante | _Completar con tu nombre_ |

## Descripción del proyecto

TravelNow necesita una plataforma que permita a los huéspedes reservar alojamiento en sus hoteles y gestionar su estadía antes de llegar: consultar disponibilidad, reservar, pagar electrónicamente, modificar o cancelar, y realizar el pre check-in con servicios adicionales. El personal (empleados y supervisores) consulta y actualiza el estado de las reservas, y el supervisor autoriza modificaciones excepcionales.

**Actores**

- Primarios: Cliente, Empleado, Supervisor (especialización de Empleado).
- Secundarios (externos): Pasarela de Pagos, Servicio de Correo Electrónico.

## Diagramas

| # | Diagrama | Origen | Fuente editable | Exportados |
|---|----------|--------|-----------------|------------|
| 1 | Casos de uso (14 CU) | TPE1 | [`01-casos-de-uso.puml`](diagramas/fuentes-editables/01-casos-de-uso.puml) | [PNG](diagramas/exportados/01-casos-de-uso.png) · [SVG](diagramas/exportados/01-casos-de-uso.svg) |
| 2 | Comunicación – CU-02 Realizar reserva | TPE2 | [`02-diagrama-comunicacion.dot`](diagramas/fuentes-editables/02-diagrama-comunicacion.dot) | [PNG](diagramas/exportados/02-diagrama-comunicacion.png) · [SVG](diagramas/exportados/02-diagrama-comunicacion.svg) |
| 3 | Secuencia – CU-02 Realizar reserva | TPE2 | [`03-diagrama-secuencia.puml`](diagramas/fuentes-editables/03-diagrama-secuencia.puml) | [PNG](diagramas/exportados/03-diagrama-secuencia.png) · [SVG](diagramas/exportados/03-diagrama-secuencia.svg) |

![Casos de uso](diagramas/exportados/01-casos-de-uso.png)

![Diagrama de comunicación](diagramas/exportados/02-diagrama-comunicacion.png)

![Diagrama de secuencia](diagramas/exportados/03-diagrama-secuencia.png)

## Estructura del repositorio

```
.
├── README.md
├── CORRECCIONES.md              # coherencia revisada y correcciones aplicadas
├── docs/
│   ├── TPE1_casos_de_uso.pdf
│   └── TPE2_comunicacion_secuencia.pdf
└── diagramas/
    ├── fuentes-editables/       # archivos originales editables
    │   ├── 01-casos-de-uso.puml
    │   ├── 02-diagrama-comunicacion.dot
    │   └── 03-diagrama-secuencia.puml
    └── exportados/              # versiones PNG y SVG
```

## Diagramas originales en Lucidchart

Los diagramas de los TPE se elaboraron originalmente en Lucidchart (enlaces en los anexos de cada informe):

- Casos de uso (TPE1): <https://lucid.app/lucidchart/7a407ac3-d907-46d7-b8f0-c58f7601f586/edit>
- Comunicación (TPE2): <https://lucid.app/lucidchart/91c95098-d0cb-4893-ba2e-3c5141896469/edit>
- Secuencia (TPE2): <https://lucid.app/lucidchart/6c4eb327-5a00-4e70-b707-decd62c01609/edit>

## Regenerar las imágenes

Requisitos: Java, [PlantUML](https://plantuml.com/download) y [Graphviz](https://graphviz.org/download/).

```bash
cd diagramas
java -jar plantuml.jar -charset UTF-8 -tpng -o ../exportados fuentes-editables/01-casos-de-uso.puml
java -jar plantuml.jar -charset UTF-8 -tsvg -o ../exportados fuentes-editables/01-casos-de-uso.puml
java -jar plantuml.jar -charset UTF-8 -tpng -o ../exportados fuentes-editables/03-diagrama-secuencia.puml
java -jar plantuml.jar -charset UTF-8 -tsvg -o ../exportados fuentes-editables/03-diagrama-secuencia.puml
dot -Tpng -Gdpi=150 fuentes-editables/02-diagrama-comunicacion.dot -o exportados/02-diagrama-comunicacion.png
dot -Tsvg fuentes-editables/02-diagrama-comunicacion.dot -o exportados/02-diagrama-comunicacion.svg
```

## Coherencia entre diagramas

Los tres diagramas describen el mismo caso de estudio con los mismos actores, nombres de casos de uso y mensajes. El detalle de lo revisado y corregido está en [`CORRECCIONES.md`](CORRECCIONES.md).
