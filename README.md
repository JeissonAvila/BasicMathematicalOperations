# BasicMathematicalOperations

Se encontrarán con un API que resuelve las cuatro operaciones básicas de las matemáticas con dos valores, por lo que se pueden hacer operaciones de sumas, 
restas, multiplicación y división, consumiendo con un servicio REST de método GET pasando los valores como parámetros dentro de la misma URL.

### Pre-requisitos 📋
Para la instalación de esta aplicación debes contar con lo siguiente:

* [mvn](https://maven.apache.org/install.html) - mvn
* [Intellij](https://www.jetbrains.com/es-es/idea/download/) - Intellij (no obligatorio)

### Instalación 🔧

Para poder realizar la instalación de esta aplicación basta con descargar este repositorio y ejecutar en la ruta donde se descargo lo siguiente: 

```
mvn install
``` 
Si solo estas utilizando maven sin el IDE, debes realizar la ejecución del siguiente comando correr la aplicación:
```
mvn clean package
``` 

Una vez genere los paquetes de despliegue, puede ejecutar la aplicación de la siguiente manera:
```
java -jar target/basic-mathematical-operations-0.0.1-SNAPSHOT.jar
```
Ya con estos pasos aplicados podrá consumir los servicios por la url http://localhost:8080/{operation}?number1={value}&number2={value}.

Otra forma para instalar la aplicación es usar el IDE Intellij y realizar la instalación de las dependencias maven y ejecutarla desde allí, lo que resulta 
realmente útil en caso de ser necesario realizar algún debug sobre el código fuente descargado.

## Ejecutando los servicios 🔩

_Para realizar el consumo de los cuatro servicios por favor tener en cuenta lo siguiente:_

* El servicio es un rest con metodo get /{operation} recibe los dos valores como parametros en el endpoint, de la siguiente manera:
```
http://localhost:8080/{operation}?number1={value}&number2={value}
```
* En {operation} solo están permitidas las operaciones matematicas basicas y en {value} debe ir el valor númerico con el que se quiere realizar la operación, 
de la siguiente manera:
```
http://localhost:8080/addition?number1=15&number2=5
http://localhost:8080/subtraction?number1=15&number2=5
http://localhost:8080/multiplication?number1=15&number2=5
http://localhost:8080/division?number1=15&number2=5
