# Principios SOLID

Los principios SOLID nos indican cómo ordenar nuestras funciones, estructuras de datos y como deben interconectarse estas clases.
El objetivo que persiguen los principios SOLID es la creación de estructuras de software de nivel medio que:
<li>toleren el cambio y el mantemiento</li>
<li>Sean fáciles de comprender</li>
<li>Sean la base de componenetes que puedan reutilizarse</li>

En definitiva, su objetivo principal es que el sistema sea fácil de cambiar sin sufrir un gran impacto con el cambio.

## Principio de responsabilidad única: SRP
*Una sola razón*

<strong>Principio: </strong>Un módulo deberá ser responsable de un, y solo un actor.

Entendiendo como módulo un grupo cohesionado de funciones y estructuras de datos. (en java llamariamos módulos a las clases)
Entendiendo como actor a la entidad interesada de que el sistema cambie. 

<strong>Soluciones comunes: </strong> Reunir las cosas que cambian por las mismas razones. Separar aquellas que cambian por razones diferentes. 

## Principio de abierto y cerrado. OCP
*extiende, no modifiques*

<strong>Principio: </strong>Un artefacto de software debe estar abierto para su extensión, pero cerrado para su modificación. 

<strong>Soluciones comunes: </strong> Separar la funcionalidad en base a cómo, por qué y cuándo cambia, y después organizar esa funcionalidad separada eb yba jerarquia de componentes. Teniendo en cuenta que, los componentes del nivel más alto de esa jerarquía están protegidos de los cambios realizados en los componentes de nivel más bajo. 

Es decir, si debemos proteger un componente A de cambios en el componente B, entonces B debe depender de componente A.

## Principio de sustitución de Liskov. LSP*
*De tal padre, tal hijo*

<strong>Principio: </strong> Asegurar que una sub-clase pueda asumir el lugar de su superclase sin errores. (si el código termina por comprobar el tipo de un objeto para realizar una acción, el principio de Liskov estará siendo violado)

Para crear sistemas de software a partir de partes intercambiables, esas partes debem adherirse a un contrato que
les permitan ser sustituidas por otros.
Patrón polimorfo. 

<strong>Soluciones comunes: </strong> Polimorfismo

## Principio de segregación de la interfaz. ISP
*No dependas de lo que no necesites*

<strong>Principio: </strong>Evitar depender de cosa que no utilizamos

<strong>Soluciones comunes: </strong>Interfaces pequeñas y acotadas. Que la interfaz pertenzca al cliente  y no a quien la implementa. Entendiendo como cliente la clase que implemente dicha interfaz. 
ejemplo estación de bús. 

## Principio de inversión de dependencias. DIP
*Lo abstracto también es bueno*

<strong>Principio: </strong>Los sistemas más flexibles son aquellos en los que las dependencias del código fuente se refieren sólo a abstracciones, no concreciones. Tenemos que tener en cuenta que estas dependencias serán para bloques de código de fácil modificación. 

<strong>Soluciones comunes: </strong>Comunmente utilizamos el patrón Inyección de dependencias para conseguir este principio. 
