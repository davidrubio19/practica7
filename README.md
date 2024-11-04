
# ACTIVIDAD 1

PASOS A SEGUIR:
## Levantar un clúster de Hadoop + YARN + Hive. Hacer pruebas con consultas básicas SQL.





 - Clonar repositorio donde esta el docker compose que tiene los contenedores con las imagenes de hadoop, de yarn y de hive
 
 git clone https://github.com/davidrubio19/practica7.git
 - Levantar contenedores

docker-compose up -d
 - Ejecutar hive
docker-compose exec hive-server bash
 - Usar hive para usar bases de datos con hadoop
 hive
 - Crear tabla

    CREATE TABLE Empleados (
    nombre VARCHAR(50),
    apellidos VARCHAR(50)
    );
- Insertar datos
INSERT INTO Empleados (nombre, apellidos) VALUES ('Mario', 'Martin');
INSERT INTO Empleados (nombre, apellidos) VALUES ('Pablo', 'Herrera');
INSERT INTO Empleados (nombre, apellidos) VALUES ('Samuel', 'Barahona');
- Consultas basicas

  - SELECT * FROM Empleados WHERE apellidos = 'Herrera';
  - SELECT COUNT(*) AS TotalEmpleados FROM Empleados;
  - SELECT * FROM Empleados ORDER BY apellidos ASC;


