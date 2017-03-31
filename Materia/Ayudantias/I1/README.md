# Ayudantía para la I1

### Explicar:
1. ¿Qué es más importante, maximizar el outcome u el output? ¿Por qué?
  * outcome: Es el impacto de la aplicación en el usuario. La experiencia del usuario. Si le sirvió o no. Es más importante.
  * output: Es la aplicación en sí, lo que hace, lo que entrega.
2. Diferencia entre modelo de cascada y uno iterativo
  * Modelo de cascada: Desarrollar todo el programa. Es más lento. Pasos son fijos y se debe respetar el orden de los pasos a seguir, es decir no puedo hacer un paso posterior sin haber completado el actual.
  * Modelo iterativo: Realizar una versión del programa y después volver a realizarla en una siguiente iteración.
3. ¿Qué son y en qué se diferencian los requisitos funcionales de los no funcionales?
  * Requisitos funcionales: Tiene que ver con que queremos que haga nuestro programa. Son los features del mismo programa.
  * Requisitos no funcionales: Más relacionados con la eficiencia del programa en sí. No es lo que el usuario pide: que sea rápido, que no se caigan las bases de datos, etc...
4. Las principales diferencias entre el método SCRUM y el Kanban. ¿Cuál elegiría usted y por qué?
  *  SCRUM: Método ágil e incremental. Se conforma de distintos sprints donde se elige una cierta cantidad de features a implementar. Todos hacen todo. Si no se alcanzan a implementar features pueden quedar para el próximo sprint. Mejor si se tienen fechas límites y se puede priorizar mejor las features.
  *  **Kanban**: Lista de tipos de features (por hacer, en progreso, hechas) cada una con un límite de features que pueden haber en cada categoría. La idea es que las features se mueven de una categoría a otra a medida que se van completando. Equipos más especializados.

### ¿Qué concepto se refiere cada sentencia o conversación?

1. Lista priorizada de features
  * **Product Backlog**: Lista con todas las tareas que debe tener tu programa ordenadas por prioridad. Se intenta que haya poca dependencia entre las features para simplificar la priorización. Casi propia del SCRUM
2. Forma ordenada de los User Stories en Activities y Epics
  * **Story map**: Se ve comom una "linea de tiempo" con tarjetas que representan actividades hacia el lado.
3. "Ayer no pude avanzar mucho, pero hoy terminaré la feature 3 y 4 si o si", "Yo ayer tuve un problema pero hoy lo soluciono"
  * **Daily SCRUM**: Reunión de al rededor de 10-15 minutos que se realiza en la mañana donde participan todos los miembros del equipo de desarrollo, donde puede o no estar el product owner y donde se comenta el avance diario. Cada integrante debe decir tres cosas: Qué hizo ayer, qué piensa hacer hoy y qué obstáculos cree que pueden surgir. Normalmente frente a la tabla/pizarra para contextualizar.
4. Etapa del SCRUM en que se reune todo el team, el SCRUMMaster y, a veces, el product owner. Se realiza al final de cada iteracion, para analizar el proceso y cómo se va llevando.
  * **Retrospective** :Se determina el rumbo del proyecto. Se revisa si se está acercando efectivamente al objetivo. Se analiza el proceso.
5. Lider de un Scrum team
  * ScrumMaster

### Se desea crear una aplicación de compras con internet, con pago online y búsqueda de productos.
Después de una conferencia con el product owner se obtuvieron las siguientes actividades de un Story Map:

| Search products | Shopping Cart | Create accounte | Pay & Ship | Order Status |

1. Escribir al menos 3 relatos de usuario con sus respectivos criterios de aceptación:
  * Search products:
    * Yo como usuario, quiero poder buscar producto ingresando una palabra clave.
      * Test:
    * Yo como usuario, quiero filtrar por categoría los productos para buscar lo que realmente me interesa.
      * Test: Al buscar por una categoría aparecen solo productos de esa categoría.
    * Yo como usuario, quiero ordenar los productos por rating de comprador para encontrar a los vendedores más confiables/populares primero.
      * Test: Al seleccionar esta opción que la lista de productos se muestre ordenada por rating de usuario.
  * Pay & Ship:
    * Yo como usuario quiero que la aplicación recuerde mi dirección para no tener que ingresarla cada vez que compre.
      * Test: Si la dirección no es válida, no se guarda.
      * Test: Si tengo mi dirección guardada, debe aparecer automáticamente al comprar.
      * Test: Si no tiene dirección entonces que no muestre nada.
    * Yo como administrador, quiero poder ingresar a la información de los pagos, para revisar si la información detallada de la compra es correcta.
      * Test: Deben listarse todas las compras que se han hecho por un usuario.
2. Para esta misma aplicación, definida por suted en 1. Escriba los casos de uso apropiados. Recuerde identificar cuál es el Happy Path.
  * Lista numerada. Existe el happy path y los flujos alternativos.
  * Actores:
    * comprador
    * vendedor
  * 1) Vendedor agrega productos.
  * 2) Comprador busca productos.
  * 3) Comprador lo agrega a su carro.
  * 4) Comprador intenta pagar.
    * 4a) El comprador no está logueado.
      * 4a1) Se loguea, vuelve al pago
        * 4a1a) Comprador no tiene una cuenta
          * 4a1a1) Debe registrarse
          * 4a2a2) Obtiene su cuenta, vuelve al pago
