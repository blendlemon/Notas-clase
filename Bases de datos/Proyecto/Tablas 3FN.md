EMPLEADO

| DNIEMPLEADO | nombre | telefono | antigüedad | apellidos | direccion | salario |
| :---------: | :----: | -------- | ---------- | --------- | --------- | ------- |
|             |        |          |            |           |           |         |

TipoEmpleado

| DNIEMPLEADO | PUESTO |
| ----------- | ------ |
|             |        |
factura

| DNIEMPLEADO | DNIFAMILIAR | fecha | cantidad |
| ----------- | ----------- | ----- | -------- |
|             |             |       |          |
FAMILIAR

| DNIFAMILIAR | nombre |
| ----------- | ------ |
|             |        |
TUMBA

| NUMEROTUMBA | NUMEROSECTOR |
| ----------- | ------------ |
|             |              |
NICHO

| NUMEROTUMBA | altura | inscripcion |
| ----------- | ------ | ----------- |
|             |        |             |
FOSA

| NUMEROTUMBA | capacidad |
| ----------- | --------- |
|             |           |

PANTEON

| NUMEROTUMBA | capacidad | inscripcion | DNIFAMILIAR |
| ----------- | --------- | ----------- | ----------- |
|             |           |             |             |

SECTOR

| NUMEROSECTOR | CAPACIDAD | EXTENSION |
| ------------ | --------- | --------- |
|              |           |           |
SECTOR-EMPLEADO

| NUMEROSECTOR | DNIEMPLEADO |
| ------------ | ----------- |
|              |             |

FALLECIDO-EMPLEADO

| DNIEMPLEADO | CODIGO |
| ----------- | ------ |
|             |        |

FALLECIDO

| CODIGO | dniMuerto | nombre | apellidos | fechaNacimiento | fechaDefuncion |
| ------ | --------- | ------ | --------- | --------------- | -------------- |
|        |           |        |           |                 |                |
FALLECIDO-TUMBA

| NUMEROTUMBA | CODIGO |
| ----------- | ------ |
|             |        |
