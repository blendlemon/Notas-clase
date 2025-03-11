
**Tabbla de Clases de Equivalencia**

| Condición de Entrada                               | Clases Válidas                   | Clases No Válidas                               |
| :------------------------------------------------- | :------------------------------- | :---------------------------------------------- |
| Número de alumno (3<br>dígitos, sin 000)           | 100, 123, 999                    | 000, 99, 1000, -123                             |
| Nombre del alumno (10<br>caracteres alfanuméricos) | "JuanPerez1"<br>"MariaLuz12"     | "Juan", "NombreExcesivo123","",<br>"1234567890" |
| Nota obtenida (0 a 10)                             | 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 | -1, 11, "A", "5.5"                              |

**Casos de Prueba**


| Caso | Número<br>de <br>Alumno | Nombre del<br>Alumno | Nota<br>Obtenida | Clases Cubiertas                                           | Salida<br>Esperada |
| ---- | ----------------------- | -------------------- | ---------------- | ---------------------------------------------------------- | ------------------ |
| 1    | 123                     | JuanPerez1           | 2                | Válido número, válido nombre, válida nota (Muy deficiente) | Muy<br>deficiente  |
| 2    | 999                     | MariaLuz12           | 4                | Válido número, válido nombre, válida nota (Insuficiente)   | Insuficiente       |
| 3    | 101                     | JoseGarcia           | 6                | Válido número, válido nombre, válida nota (Suficiente)     | Suficiente         |
| 4    | 200                     | AnaMartinez          | 8                | Válido número, válido nombre, válida nota (Notable)        | Notable            |
| 5    | 305                     | PedroRuizX           | 10               | Válido número, válido nombre, válida nota (Sobresaliente)  | Sobresaliente      |
| 6    | 000                     | JuanPerez1           | 5                | Inválido número                                            | Error              |
| 7    | 123                     | 1234567890!          | 7                | Inválido nombre                                            | Error              |
| 8    | 250                     | MariaLuz12           | 11               | Inválida nota                                              | Error              |
| 9    | -123                    | JoseGarcia           | 4                | Inválido número                                            | Error              |
| 10   | 400                     | AnaMartinez          | "A"              | Inválida nota                                              | Error              |
