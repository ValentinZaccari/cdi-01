## Mes de Noviembre

### Semana 1 de noviembre: Migración de Hardware y Diseño de Nueva Placa

**Objetivo de la semana:**
* Resolver la inestabilidad de la Raspberry Pi 4 (Pi 4).
* Decidir y ejecutar la migración a un nuevo microcontrolador.
* Diseñar y fabricar la nueva placa de control adaptada.

**Actividades realizadas:**
* Se realizaron pruebas para **estabilizar la Pi 4** intentando el arranque a través de la salida **Micro HDMI** a un monitor, pero aunque funcionó brevemente, la inestabilidad regresó.
* Se tomó la decisión de **cambiar de microcontrolador**, optando por la **Raspberry Pi Pico** debido a su mayor simplicidad y confiabilidad percibida para las tareas de control de motores.
* Se diseñó y se fabricó una **nueva placa de cobre** adaptada al formato de la Pi Pico.
* En el nuevo diseño de la placa, se **agrandaron las pistas** y se hicieron las conexiones más cómodas.

**Resultados obtenidos:**
* Se confirmó la **inviabilidad de la Raspberry Pi 4** para el proyecto.
* Se completó el diseño y la fabricación de la **placa de control adaptada a la Raspberry Pi Pico**. 

**Dificultades encontradas:**
* La persistente inestabilidad de la Raspberry Pi 4.

**Próximos pasos:**
* Testear los drivers de motor y el sensor LiDAR con la nueva Pi Pico.

---

### Semana 2 de noviembre: Control de Motores y Solución de Conectividad LiDAR

**Objetivo de la semana:**
* Lograr el control total de los motores con la nueva placa Pi Pico.
* Integrar el sensor LiDAR al nuevo microcontrolador.

**Actividades realizadas:**
* Se realizaron pruebas con los **drivers** en la nueva placa de la Pi Pico, logrando **mover dos motores paso a paso a la vez** con éxito.
* Se detectó que un **driver faltante no funcionaba**, por lo que se compró un reemplazo.
* Una vez que se tuvo el driver de reemplazo, **todos los motores funcionaron perfectamente**.
* Se intentó testear el **sensor LiDAR en la Pi Pico**, pero **no funcionaba** (a pesar de funcionar previamente en la Pi 4), lo que se consideró un problema inusual.
* Se realizaron múltiples pruebas y errores con **diferentes códigos** e **invirtiendo el cableado** del sensor sin éxito.
* Finalmente, se descubrió una solución atípica: para que el LiDAR funcionara en la Pi Pico, se tuvo que **puentear el TX y RX del propio sensor LiDAR**. Esta extraña corrección permitió continuar con el proyecto.

**Resultados obtenidos:**
* **Control total y estable de los tres motores** con la Raspberry Pi Pico.
* Se encontró una **solución de *hardware-software*** para la inoperatividad del sensor LiDAR en la Pi Pico.

**Dificultades encontradas:**
* Fallo inicial del tercer driver de motor.
* Problema de comunicación inexplicable del LiDAR con la Pi Pico, resuelto con un *hack* (puenteo de TX/RX).

**Próximos pasos:**
* Fabricar las piezas mecánicas necesarias para el sistema de ejes.

---

### Semana 3 de noviembre: Fabricación de Componentes Mecánicos y Diseño

**Objetivo de la semana:**
* Diseñar las piezas de acople necesarias para el sistema de ejes.
* Iniciar el testeo y la calibración de la impresora 3D.

**Actividades realizadas:**
* Se diseñaron **tres acoples en AutoCAD** para las tres varillas roscadas que se utilizarían en los ejes X e Y del escáner.
* Se modificaron y buscaron **dos soportes** para las varillas del eje Y.
* Se procedió a **imprimir en 3D** (utilizando filamento **PLA**) los acoples y soportes diseñados.
* Se realizaron las **primeras pruebas de impresión** y la **calibración inicial** de la impresora 3D utilizando filamento **PETG**.
* Se realizó el **cambio de filamento a PLA**, requiriendo la calibración específica para este material.

**Resultados obtenidos:**
* Se obtuvieron los **acoples y soportes impresos en 3D**.
* Se **calibró la impresora** para trabajar con **PLA**, el filamento de fabricación.

**Dificultades encontradas:**
* Ajustar la calibración de la impresora 3D para trabajar con diferentes filamentos.

**Próximos pasos:**
* Montar los componentes en el sistema de ejes y resolver los problemas de acoplamiento.

---

### Semana 4 de noviembre: Solución Mecánica Ingeniosa y Ensamblaje Final

**Objetivo de la semana:**
* Resolver el problema de la tuerca *anti-backlash*.
* Ensamblar y montar la estructura final del escáner.

**Actividades realizadas:**
* Se identificó un problema grave: la **tuerca *anti-backlash* comprada no encajaba** con las varillas roscadas, a pesar de que las medidas supuestamente coincidían.
* Se buscó una **solución ingeniosa y de bajo costo** al problema: se compraron **arandelas con tuercas a rosca** que sí coincidían con la medida de la varilla.
* Se **soldó la tuerca a la arandela** usando un soldador eléctrico para crear una pieza de acople funcional que asegurara el movimiento sin juego.
* Gracias a esta solución, la varilla pudo realizar los movimientos horizontales y verticales necesarios para el sensor LiDAR.
* Finalmente, se procedió a **unir y montar todo el escáner**, integrando la Pi Pico, los motores, el LiDAR y el sistema de ejes terminado.

**Resultados obtenidos:**
* Se encontró una **solución de *hardware* casera** (tuerca y arandela soldada) que resolvió el problema de acople y el *anti-backlash*.
* El **escáner fue completamente ensamblado y montado** en su estructura final, quedando listo para las pruebas de *software* de alto nivel.

**Dificultades encontradas:**
* Fallo en la compatibilidad de la tuerca *anti-backlash* comprada.

**Próximos pasos:**
* Pruebas finales de *software* y funcionalidad del escáner ensamblado.
