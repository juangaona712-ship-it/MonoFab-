# 7. Soldaduras: Técnicas y Resultados

!!! abstract "Objetivo de esta fase"
    Esta sección documenta las técnicas de soldadura utilizadas para ensamblar las placas del proyecto, así como los resultados obtenidos en cada una. Se toma como proyecto práctico de aplicación la PCB del **Volante Gamer con ESP32** diseñada en Altium Designer, y la placa fresada en la **Roland MonoFab SRM-20**, abarcando desde la preparación de herramientas y materiales, hasta la soldadura de componentes, la verificación eléctrica y la corrección de defectos.

---

## 7.1 Materiales y Herramientas que se Ocupan

Antes de soldar, reúne todo el material en la mesa de trabajo. Trabajar con el material incompleto es la causa más común de soldaduras frías y puentes.

| Material / Herramienta | Uso | Notas |
| :--- | :--- | :--- |
| Cautín / estación de soldadura de punta fina | Calentar la unión y fundir la soldadura | Punta limpia y estañada antes de cada uso |
| Soldadura de estaño, 0.8 mm - 1.0 mm | Unir el componente al pad de cobre | 60/40 o SAC305, según la que uses en el laboratorio |
| Flux / pasta para soldar | Limpiar el óxido y ayudar a que la soldadura fluya | Aplicar solo una capa fina |
| Esponja húmeda o limpiador de punta de latón | Limpiar la punta del cautín | Limpiar la punta cada 2 o 3 uniones |
| Pinzas de punta fina | Sostener componentes pequeños y headers | Evita tocar la punta caliente con los dedos |
| Tercera mano / base con pinzas cocodrilo | Sujetar la PCB mientras se suelda | La placa no debe moverse durante la soldadura |
| Malla desoldadora y bomba desoldadora | Retirar soldadura en exceso o corregir puentes | Ver 7.6 |
| Multímetro en modo continuidad | Verificar que no haya cortos y que la unión conduzca | Ver 7.5 |
| Lupa o microscopio | Inspeccionar uniones pequeñas, pines del ESP32 y headers OLED | Una unión bien hecha se ve brillante y cónica |
| Alcohol isopropílico y cepillo / paño | Limpiar flux y polvo de cobre después de soldar | Sobre todo en la placa fresada en MonoFab |
| Lentes de seguridad | Proteger los ojos de salpicaduras de soldadura | Uso obligatorio |
| Extractor de humos o ventilación | Alejar el humo del flux de la cara | No soldar en un espacio cerrado sin ventilar |

![Herramientas y materiales de soldadura](img/imagenes_soldadura/Imagen1.png)
*Figura 7.1: Herramientas y materiales sobre la mesa de trabajo, antes de empezar.*

!!! tip "Preparación de la punta"
    Antes de soldar la primera unión, limpia la punta en la esponja o en el limpiador de latón y estañala con un poco de soldadura. Una punta negra u oxidada no transfiere calor y produce soldaduras frías.

---

## 7.2 Técnicas de Soldadura

### Soldadura Through-Hole (THT)

Es la técnica principal en este proyecto: el pin del componente pasa por el agujero de la PCB y se suelda por el lado opuesto.

1. Inserta el componente por el lado correcto de la placa.
2. Dobla ligeramente los pines por detrás para que el componente no se caiga.
3. Calienta a la vez el pad y el pin con la punta del cautín, 2 o 3 segundos.
4. Acerca la soldadura a la unión, no a la punta del cautín, y deja que fluya hasta formar un cono brillante.
5. Retira primero la soldadura y después el cautín, sin mover el componente hasta que la unión se enfríe.

![Soldadura through-hole, paso a paso](img/imagenes_soldadura/Imagen2.png)
*Figura 7.2: Calentamiento del pad y el pin, y formación del cono de soldadura.*

### Soldadura de Headers y Pines

Los headers del módulo ESP32 y de la pantalla OLED se sueldan pin por pin, para que queden rectos y alineados.

1. Suelda primero un solo pin de cada extremo del header, verifica que esté derecho y luego suelda el resto.
2. Si un header queda torcido, calienta de nuevo ese pin, acomódalo y deja enfriar.
3. No apliques soldadura en exceso: un puente entre dos pines vecinos es el error más común en los headers.

### Soldadura de Componentes Pequeños y Pines Finos

Para el diodo 1N4007, resistencias y pines de señal, usa la punta más fina, poco flux y poca soldadura.

* Calienta solo el tiempo necesario: demasiado calor levanta el pad, sobre todo en la placa fresada.
* Si la soldadura queda opaca y rugosa, es una soldadura fría: caliéntala de nuevo con un poco de flux hasta que quede brillante.

### Desoldadura y Retrabajo

Cuando hay un puente o un componente mal colocado:

1. Coloca la malla desoldadora sobre la unión y caliéntala con el cautín, para que absorba el exceso.
2. Para retirar un componente, usa la bomba desoldadora pin por pin.
3. Limpia el pad con alcohol isopropílico antes de volver a soldar.

![Retrabajo de una unión con puente](img/imagenes_soldadura/Imagen10.png)
*Figura 7.3: Corrección de un puente de soldadura con malla desoldadora.*

---

## 7.3 Procedimiento: Volante Gamer con ESP32 (Altium)

Esta es la PCB de dos capas diseñada en Altium: módulo ESP32, botones Omron, diodo 1N4007 de protección contra polaridad inversa, headers para pantalla OLED, etiquetas de red D21, D22 y D34, pistas de señal de 0.4 mm, agujeros de montaje de 3.2 mm para tornillería M3 y polygon pour de GND.

1. **Limpieza:** Limpia los pads con alcohol isopropílico. No debe quedar polvo ni grasa.
2. **Headers del ESP32:** Suelda los headers del módulo ESP32, pin por pin, verificando que queden rectos.

![Headers del ESP32 soldados](img/imagenes_soldadura/Imagen3.png)
*Figura 7.4: Headers del módulo ESP32 soldados en la PCB del volante.*

3. **Botones Omron:** Suelda los botones / pulsadores de los mandos, en su footprint correspondiente.

![Botones Omron soldados](img/imagenes_soldadura/Imagen4.png)
*Figura 7.5: Botones Omron soldados en la placa.*

4. **Diodo 1N4007:** Suelda el diodo rectificador de protección contra polaridad inversa. **Respeta la orientación: la banda del diodo debe quedar en el sentido indicado en la serigrafía y en el esquemático.** Un diodo al revés deja el circuito sin protección.

![Diodo 1N4007, orientación de la banda](img/imagenes_soldadura/Imagen5.png)
*Figura 7.6: Diodo 1N4007 soldado, con la banda en el sentido correcto.*

5. **Headers OLED:** Suelda los headers macho / hembra para la pantalla OLED y periféricos.

![Headers OLED soldados](img/imagenes_soldadura/Imagen6.png)
*Figura 7.7: Headers para la pantalla OLED.*

6. **Resistencias y pines restantes:** Suelda las resistencias de limitación de corriente y los pines de señal restantes, siguiendo las etiquetas de red D21, D22 y D34 del esquemático.
7. **Limpieza final:** Retira el flux sobrante con alcohol isopropílico y deja secar la placa antes de conectarla.

---

## 7.4 Procedimiento: Placa Fresada en MonoFab SRM-20

Esta es la placa fabricada en la fresadora Roland MonoFab SRM-20: placa fenólica de cobre, perforaciones de 0.8 mm, ruteo de pistas con fresa plana de 0.4 mm y corte de contorno con fresa de 2 mm, sobre cama de sacrificio de MDF.

1. **Limpieza:** Antes de soldar, retira todo el polvo de cobre y fibra de vidrio con aspiradora y un cepillo, y limpia la superficie con alcohol isopropílico. El polvo entre pistas produce cortos.

![Placa MonoFab antes de soldar](img/imagenes_soldadura/Imagen7.png)
*Figura 7.8: Placa fresada en MonoFab, con los pads limpios antes de soldar.*

2. **Revisión de pistas:** Inspecciona con lupa las pistas de 0.4 mm. Si una pista quedó cortada por el fresado, no la fuerces con soldadura: repárala con un puente de alambre fino, como se indica en 7.6.
3. **Soldadura:** Suelda los componentes con la misma técnica THT de 7.2, pero con menos calor y menos tiempo: en una placa fresada los pads son más delicados y se levantan con facilidad.
4. **Limpieza final:** Limpia de nuevo con alcohol isopropílico y verifica que no queden restos de cobre entre pistas.

![Placa MonoFab después de soldar](img/imagenes_soldadura/Imagen8.png)
*Figura 7.9: Placa fresada en MonoFab, ya con los componentes soldados.*

---

## 7.5 Verificación y Resultados

Una unión bien hecha se ve brillante, tiene forma de cono, cubre el pad y el pin, y no tiene puentes con el pin vecino.

![Detalle de una unión bien hecha](img/imagenes_soldadura/Imagen9.png)
*Figura 7.10: Detalle macro de una unión brillante y cónica.*

### Pruebas de continuidad

Con el multímetro en modo continuidad, y la placa sin energizar, verifica cada red antes de conectar el ESP32.

| Componente / Red | Prueba | Resultado esperado | Resultado obtenido |
| :--- | :--- | :--- | :--- |
| GND | Continuidad entre pads de GND | Suena / 0 Ω | *Pendiente* |
| VCC 3.3V | Continuidad VCC, sin corto a GND | Sin continuidad con GND | *Pendiente* |
| D21 | Continuidad pin - botón / header | Suena / 0 Ω | *Pendiente* |
| D22 | Continuidad pin - botón / header | Suena / 0 Ω | *Pendiente* |
| D34 | Continuidad pin - potenciómetro / entrada | Suena / 0 Ω | *Pendiente* |
| Diodo 1N4007 | Continuidad en un solo sentido | Conduce en un sentido, no en el otro | *Pendiente* |
| Botones Omron | Continuidad al presionar | Suena solo al presionar | *Pendiente* |
| Headers OLED | Continuidad, sin puentes entre pines vecinos | Sin continuidad entre pines vecinos | *Pendiente* |

![Verificación con multímetro](img/imagenes_soldadura/Imagen11.png)
*Figura 7.11: Verificación de continuidad con multímetro, antes de energizar la placa.*

### Resultados obtenidos

| Placa | ¿Qué se soldó? | ¿Qué salió bien? | ¿Qué se tuvo que corregir? |
| :--- | :--- | :--- | :--- |
| Volante Gamer con ESP32 (Altium) | Headers ESP32, botones Omron, diodo 1N4007, headers OLED | *Pendiente de llenar con tus resultados* | *Pendiente de llenar con tus resultados* |
| Placa fresada en MonoFab SRM-20 | *Pendiente de llenar: componentes soldados en esta placa* | *Pendiente de llenar con tus resultados* | *Pendiente de llenar con tus resultados* |

![Resultado final](img/imagenes_soldadura/Imagen12.png)
*Figura 7.12: Resultado final: volante y placa terminados.*

!!! warning "Antes de conectar la alimentación"
    No conectes el ESP32 ni la fuente hasta que la prueba de continuidad VCC - GND no dé corto. Un corto en alimentación puede dañar el módulo.

---

## 7.6 Errores Comunes y Cómo Corregirlos

| Error | Cómo se ve | Causa | Corrección |
| :--- | :--- | :--- | :--- |
| Soldadura fría | Opaca, rugosa, con forma de bola | Poco calor o punta sucia | Calentar de nuevo con flux hasta que quede brillante |
| Puente entre pines | Soldadura uniendo dos pines vecinos | Exceso de soldadura | Retirar el exceso con malla desoldadora |
| Pad levantado | El pad de cobre se despega de la placa | Demasiado calor o tiempo | Reparar con un puente de alambre fino a la siguiente pista |
| Diodo al revés | El circuito no enciende o no tiene protección | Orientación incorrecta del 1N4007 | Desoldar, girar el diodo y volver a soldar |
| Componente torcido | Header o botón inclinado | Se soldó sin verificar la posición | Calentar un pin, acomodar y dejar enfriar |

---

## 7.7 Seguridad

* Usa lentes de seguridad y ventilación durante toda la soldadura.
* No toques la punta del cautín ni la unión recién soldada.
* Apaga y deja enfriar el cautín en su base al terminar.
* Lávate las manos después de soldar y no comas en la mesa de trabajo.
