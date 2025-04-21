# torneo-esports-uml
Este repositorio es para realizar la tarea 3 de EEDD UNIR

**IMPORTANTE** Iré actualizando este **README** según vaya trabajando en la tarea, de momento está montado con
la estructura solicitada.

# Sistema de Gestión de Torneos de eSports

## Autor
Stephen Nicholas Jones De Giorgi
Perfil de GitHub: https://github.com/L0cksat

## Descripción del Proyecto

Se puede acceder al repositorio del proyecto a través del siguiente enlace: https://github.com/L0cksat/torneo-esports-uml

Este proyecto se enfoca en realizar e implementar un sistema de gestión de torneos de eSports utilizando UML para el modelado y Java para la implementación.

## Diagramas UML
### Diagrama de Casos de Uso


### Diagrama de Clases


## Estructura del Proyecto
torneo-esports-uml/ <br>
| ├── diagrams/ <br>
|   ├── casos-uso.png <br>
|   ├── clases.png <br>
├── README.md <br>
├── .gitignore


## Instalación y Ejecución
1. Clonar el repositorio:
`git clone https://github.com/L0cksat/torneo-esports-uml`

2. Compliar y ejecutar el proyecto:

## Justificación del diseño
(Tengo que poner aquí todas la justificaciones de la estructura y el cómo y por qué de la organización de las clases.)

**1. Análisis del problema y requisitos del sistema:**
<br>
    **- ¿Quiénes son los actores que interactúan con el sistema?**
    <br>
        _En mi opinion, los actores en este caso serían un Administrador de equipos (sería el jefe de equipo o entrenador) y el Administrador de torneos (que sería el administrador de la organización quienes organizan los torneos). De momento para justificar la presencia del actor Administrador de torneos en el punto 1 del diagrama de caso de uso, es porque luego se va a interactuar con más partes del sistema en el caso de "Crear torneo", "Inscribir equipo en un torneo" y "Generar emparejamiento de partidas" del punto 2 de Gestión de torneos. Mi justifcación del actor de Administrador de equipos es porque yo veo y entiendo que el entrenador tiene la información del equipo y de sus jugadores y para facilitar la gestion de registro, el actor de Administrador de equipos puede directamente interactuar con el sistema para registrar su equipo y sus jugadores, que en mi opinion reduce el factor del error del registro (que no quiere decir que no habrá errores)._
<br>
    **- ¿Cuáles son las acciones que cada actor puede realizar?**
    <br>
        _Como he explicado en la pregunta anterior en este caso el actor de Administrador de equipos se encargaría de registar la información de su equipo y por lo tanto los jugadores que forman parte de ese equipo, por lo cuál realizaría en el punto 1 del diagrama de casos de usos las acciones de "Registrar equipo" y "Añadir jugadores a un equipo" además, en mi opinion, puede interactuar con el sistema para consultar la lista de equipos y jugadores tanto como el suyo como para ver los equipos rivales, por lo tanto puede realizar la acción de "Consultar lista de equipos y jugadores".
        En el caso del actor Administrador de torneos, como he comentado antes, ahora mismo en el punto 1 del diagrama de casos de usos solamente le interesaría consultar la lista de equipos y jugadores para luego posteriormente asñadirlos al torneo correspondiente, por lo tanto puede interactuar con el sistema para realizar la acción de "Consultar lista de equipos y jugadores"._
<br>
    **- ¿Cómo se relacionan entre sí las entidades del sistema?**
    <br>
        _En este caso las entidades se relacionaría entre sí con relaciones mayormente de dependencia ya que por ejemplo la acción de "Añadir jugadores a un equipo" depende de que si; primero el equipo exista en el sistema (el sistema lo tendrá que comprobar a través de la acción "Comprobar si equipo está registrado") y luego posteriormente tiene que hacer la comprobación de si el jugador haya sido añadido anteriormente a través de la acción de "Comprobar si jugador ha sido añadido", la acción principal de "Añadir jugadores a un equipo **depende** de estas dos comprobaciones para poder ejecutarse.



**2. Identificación de los casos de uso y elaboración del diagrama:**
El diagrama de los casos de uso se encuentran en la carpeta "diagrams"

   2.1 Justificación del **punto 1** "Gestión de equipos y jugadores"
   <ul>
    <li>Registrar equipo</li>
    <li>Añadir jugadores a un equipo</li>
    <li>Consultar lista de equipos y jugadores</li>
   </ul>
Todo lo escrito aquí en esta justificación se hace referencia al punto 1 del diagrama de casos de usos.
En primer lugar he añadido dos actores: El administrador de equipos (quien sería el jefe o entrendador del equipo) quién interactuaría con el sistema para poder registar su equipo dentro del sistema y el administrador de torneos (de la organización quienes organizan los torneos donde participarán dichos equipos).

En el caso de uso "Registar equipo" (que desempeña el actor Adiministrador de equipos), el sistema tendría que hacer una comprobación para ver si el equipo que se está registrando ya existe en este caso sería "Registrar equipo" ---<<includes>>-- "Comprobar si equipo está registrado", por lo tanto la acción de "Registrar equipo" depende de la comprobación de "Comprobar si equipo está registrado".

En el caso de uso "Añadir jugadores a un equipo" (que también desempeña el actor Administrador de equipos), el sistema primero tendría que hacer una comprobación para ver si el equipo existe y luego una segunda comprobación para ver si el jugador haya sido añadido anteriormente o no, por lo tanto 
la acción principal **depende** de estas dos comprobaciones para poder ejectuarse correctamente.

En el caso de uso "Consultar lista de equipos y jugadores" que pueden desempeñar los dos actores mencionados anteriormente para hacer comprobaciones de si han registrado correctamente tanto los equipos como los jugadores que forman parte de dichos equipos. El sistema tiene que comprobar si el equipo existe y luego si los jugadores de dicho equipo existen a través de los casos de uso de "Comprobar si equipo existe" y "Comprobar si jugador ha sido añadido" una vez realizado estas acciones, en mi opinion, el sistema le puede mostrar tanto al Administrador de equipos como el Administrador de torneos (y según que información desea que se le muestre el sistema) tanto una lista de equipos (a través del caso de uso "Mostrar lista de equipos" que está include/incluido en "Consultar lista de equipos y jugadores"), o una lista de jugadores de dichos equipos (a través del caso de uso "Mostrar lista de jugadores que está include/incluido en "Consultar lista de equipos y jugadores" y extend/extiende de "Mostrar lista de equipos").


## Conclusiones
Poner aquí el conocimiento que he adquirido durante la realización de esta tarea.