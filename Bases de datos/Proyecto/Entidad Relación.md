Empleado(**dniEmpleado**, nombre, teléfono, antigüedad, apellidos, dirección, salario)

PUESTO(***dniEmpleado***, puesto)

factura(***dniEmpleado***, ***dniFamiliar***, fecha, cantidad)

FAMILIAR(**dniFamiliar**, nombre)

TUMBA(**numeroTumba**)

NICHO(***numeroTumba***, altura, inscripción)

FOSA(***numeroTumba***, capacidad)

PANTEON(***numeroTumba***, capacidad, inscripción)

posee(***dniFamiliar***, ***numeroTumba***)

contiene(***numeroSector***, ***numeroTumba***)

SECTOR(***numeroSector***, capacidad, extensión)

encarga(***dniEmpleado***, ***numeroSector***)

entierra(***dniEmpleado***, ***codigo***)

FALLECIDO(**codigo**, dniMuerto, nombre, apellidos, fechaNacimiento, fechaDefuncion)

ocupa(***codigo***, ***numeroTumba***)

tiene(***dniFamiliar***, ***codigo***)