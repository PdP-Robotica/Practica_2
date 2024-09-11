# practica2
## Integrantes.

•	Luis Fernando Duarte Reséndiz.

•	Mauricio Alberto Gómez Arroyo.

•	Diego Brandon Guzmán Sierra.

•	Bryan Hiadim Vera Hernández.

## Introducción.
En esta práctica, partiendo del conocimiento previo sobre cómo controlar un brazo robótico mediante el software Epson RC+, se procederá a establecer la posición de home del brazo robótico. Además, se programarán diversas posturas que resultarán útiles para automatizar un sistema, específicamente el proceso de recolección y colocación de un fusible, aprovechando al máximo las capacidades del equipo.

## Instrucciones.
## 1.	Entrar a Epson RC+ e ingresar a las herramientas.
Como primer paso, una vez abierto el programa Epson RC+, se deben abrir las pestañas Robot Manager y Simulator, que se encuentran en el apartado de herramientas. Esto permitirá una mejor visualización de las acciones que realizamos.

![image](https://github.com/user-attachments/assets/ff2ae04f-ea92-4532-a767-0846f0b250fd)

## 2.	Selección del Home del brazo.
A continuación, debemos generar la primera memoria para nuestro brazo robótico, siendo la más importante la posición Home, ya que esta servirá como punto de referencia base. Para ello, es necesario ubicarse en la pestaña Robot Manager y encender los motores.

![image](https://github.com/user-attachments/assets/db78573f-c8ec-4f1e-abec-81998ff71cc4)

Una vez estos estén encendidos pasamos a la etapa de jog & teach, donde se debe colocar el brazo robótico con los siguientes ángulos.

![image](https://github.com/user-attachments/assets/1899d161-2459-45f4-88bd-2710c89fae14)

Una vez que el brazo esté en la posición deseada, podemos configurarla como el Home a establecer. Para ello, es necesario desplazarse hacia abajo en la pestaña Robot Manager, en el apartado Home Config. Allí, se debe leer la posición actual del brazo para guardarla como la nueva posición Home.

![image](https://github.com/user-attachments/assets/d6e5cf74-9e10-4b74-a71a-780150c24ab7)

## 3.	Generar las memorias de posiciones.
Para generar las posiciones, primero se debe mover el brazo robótico a un punto específico. En este caso cualquier posición es válida, ya que se trata solo de una prueba.
Una vez que el brazo esté en el punto deseado, en la pestaña Robot Manager, en el apartado Jog & Teach, se debe seleccionar la tecla Teach y guardar la posición con el nombre que prefiramos.

![image](https://github.com/user-attachments/assets/ccf1a880-7e74-4221-ba04-5d87bbdcc208)

## 4.	Programación para ejecutar los comandos de posición.
Una vez se tienen las posiciones, debemos de ubicarnos en el main con los siguientes conceptos:

•	Para poner en el home, se escribe: home

•	Para ir a algún punto se escribe: Go (nombre de la posición)

•	Para abrir la garra de la punta: on 2

•	Para cerrar la garra de la punta: off 2

Como ejemplo tenemos el siguiente código:

![image](https://github.com/user-attachments/assets/eac77ee8-20e2-4dc2-9122-d51ff13c525b)

Donde su recorrido es: home, uno, home, dos, home, tres, home, cuatro, home, abre la garra y finalmente cierra la garra.

## 5.	Ejecución en físico.
Primeramente, se nos pide utilizar lo que se aprendió anteriormente para poder programar el brazo para poder tomar un fusible de su base y colocarlo sobre una caja, para lo cual tenemos que mencionar que el brazo siempre buscará moverse en línea recta entre posición y posición por ello se deberá de colocar justo por encima del fusible y bajarlo en línea recta esto para evitar posibles golpes.

De esta manera se tienen las siguientes posiciones:

![image](https://github.com/user-attachments/assets/93024b41-f961-49b1-ba50-5cb2f49d5e54)

En este punto se encuentra sobre el fusible.

![image](https://github.com/user-attachments/assets/48183be5-5776-4299-b032-7586f2937148)

En este punto el brazo robótico se encuentra listo para tomar el fusible.


![image](https://github.com/user-attachments/assets/2980b48b-6add-4ccd-8320-1585582eb5e8)

Una vez se toma se sube un poco hacia arriba para evitar posibles colisiones.


![image](https://github.com/user-attachments/assets/c0715355-83f4-4385-98b1-9ee3fbc394fb)

Finalmente se deja sobre la caja para soltarlo.

Una vez se tienen todas las posiciones aprendidas se procede a programar el patrón que seguirá el brazo robótico.
Viéndose de la siguiente manera:

![image](https://github.com/user-attachments/assets/1957d657-6344-41b2-8f4f-b7dc5356d372)

A continuación, se tiene la visualización del video a la hora de ejecutarlo:
https://itecm-my.sharepoint.com/:v:/g/personal/l20121223_morelia_tecnm_mx/Ed1gyJf6QZRPugkNFbvu4zsBdWR4i28lLy8Jgc9fmFNWnQ?e=W3BIiB

## Conclusiones.
Bryan Hiadim Vera Hernández.

El uso del software Epson RC+ facilita el control del brazo robótico, permitiendo establecer y guardar posiciones clave, como el Home, lo que garantiza que el brazo pueda operar de manera segura ya que siempre tiene a donde debe regresar, para evitar errores o daños, es fundamental planificar las trayectorias del brazo robótico, como se vio en el proceso de recoger y colocar el fusible, ya que al programar las posiciones por las cuales se moverá el brazo debemos de tener en cuenta que este se moverá en línea recta entre posición y posición.
Finalmente, se concluye con que la programación y ejecución de un brazo robótico se basa en la correcta planeación de los trayectos que este tomará, ya que si no se planifica antes este tenderá a chocar.

Luis Fernando Duarte Reséndiz.

La utilización del software Epson RC+ para el control del brazo robótico asegura una alta precisión operativa al permitir el establecimiento y almacenamiento de posiciones clave. La planificación meticulosa de las trayectorias, como la programación de movimientos en línea recta, previene errores y colisiones, optimizando así la precisión en las tareas automatizadas. La función Jog & Teach añade una capa adicional de flexibilidad, facilitando la programación y ajuste de diversas posturas. La aplicación efectiva de los conocimientos previos en el uso del software y en los principios de control robótico es esencial para alcanzar un rendimiento eficiente y confiable del brazo robótico.

Mauricio Alberto Gómez Arroyo.

La correcta optimización del control robótico con el software Epson RC+ es crucial para el manejo efectivo del brazo robótico. La planificación adecuada de los movimientos, especialmente en línea recta, ayuda a minimizar el riesgo de errores y colisiones, mejorando la exactitud de las operaciones automatizadas. La función que se utilizó para las memorias ofrece la flexibilidad necesaria para probar y ajustar diferentes posturas, facilitando la automatización de tareas tanto simples como complejas. 
Esta práctica se concluye, con el conocimiento del control básico de un brazo robótico.

Diego Brandon Guzmán Sierra.

La integración del software Epson RC+ en el control del brazo robótico permite una operación precisa al establecer y guardar posiciones críticas, como el Home. La planificación detallada de los movimientos, como las trayectorias en línea recta, es esencial para evitar errores y mejorar la precisión en las tareas automatizadas. La capacidad de programar y ajustar diversas posturas mediante la función Jog & Teach proporciona una mayor flexibilidad, facilitando la automatización de procesos repetitivos y complejos. El éxito en la programación y operación del brazo robótico demuestra la importancia de aplicar conocimientos previos en el software y los principios de control robótico para lograr un desempeño eficiente y preciso.










