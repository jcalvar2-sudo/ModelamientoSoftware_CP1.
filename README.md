# ModelamientoSoftware_CP1

Componente Práctico 1 (CP1) · Modelamiento de Software · Unidad 2: Diagramas de comportamiento UML

Universidad Estatal de Milagro (UNEMI) · Facultad de Ciencias e Ingeniería · Carrera de Ingeniería de Software

---

## 1. Nombre del estudiante

**Calva Rea Jeremy Alexis**

## 2. Caso de estudio

**TravelNow: plataforma de reservas y check-in de una cadena hotelera.**

## 3. Descripción breve del sistema

TravelNow es una cadena hotelera que necesita una plataforma para que los huéspedes reserven alojamiento y gestionen su estadía antes de llegar.

El cliente consulta la disponibilidad indicando ciudad y fechas, selecciona una alternativa y realiza su reserva. Para confirmarla, el sistema registra los datos del cliente, comprueba nuevamente la disponibilidad y calcula el valor total. El pago se realiza de forma electrónica mediante una pasarela de pagos externa; cuando es aprobado, el sistema confirma la reserva y envía la notificación al cliente a través de un servicio externo de correo electrónico.

Antes de la fecha de la estadía, el cliente puede modificar o cancelar su reserva dentro de las condiciones definidas y hacer el pre check-in informando su hora estimada de llegada, con la opción de solicitar servicios adicionales como desayuno o traslado al aeropuerto. Del lado institucional, los empleados consultan reservas y actualizan su estado, y el supervisor realiza las mismas funciones y además autoriza las modificaciones que exceden las condiciones normales.

**Actores:** Cliente, Empleado y Supervisor (primarios); Pasarela de Pagos y Servicio de Correo Electrónico (secundarios externos).

## 4. Relación de diagramas

Los tres diagramas pertenecen al mismo caso de estudio. Los dos diagramas de interacción detallan el caso de uso **CU-02 Realizar reserva** del diagrama de casos de uso.

| Trabajo | Diagrama | Descripción |
|---|---|---|
| TPE1 | Diagrama de casos de uso | Delimita el sistema y muestra 5 actores y 14 casos de uso, con relaciones `«include»`, `«extend»` y la generalización de Supervisor hacia Empleado. |
| TPE2 | Diagrama de comunicación (CU-02) | Muestra quién se comunica con quién: el Sistema TravelNow es el centro de la colaboración con el Cliente, la Pasarela de Pagos y el Servicio de Correo. |
| TPE2 | Diagrama de secuencia (CU-02) | Muestra los mismos participantes y mensajes ordenados en el tiempo, desde `solicitarReserva()` hasta `reservaConfirmada`. |

Los diagramas se complementan: la secuencia muestra el *cuándo* y la comunicación el *quién con quién*.

## 5. Organización del repositorio

```
ModelamientoSoftware_CP1/
├── TPE1/
│   ├── editables/        # Archivo editable del diagrama de casos de uso
│   └── exportados/       # Diagrama de casos de uso en PNG/PDF
├── TPE2/
│   ├── editables/        # Archivos editables de comunicación y secuencia
│   └── exportados/       # Diagramas de comunicación y secuencia en PNG/PDF
└── README.md
```

| Carpeta | Contenido |
|---|---|
| `TPE1/editables/` | `TravelNow_CasosDeUso.drawio` |
| `TPE1/exportados/` | `TravelNow_CasosDeUso.png` |
| `TPE2/editables/` | `TravelNow_Comunicacion_CU02.drawio`, `TravelNow_Secuencia_CU02.drawio` |
| `TPE2/exportados/` | `TravelNow_Comunicacion_CU02.png`, `TravelNow_Secuencia_CU02.png` |
