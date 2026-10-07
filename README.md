<div align="center">

# Mantenimeinto Preventivo de Máquinas 
## Un proyecto realizado y ejecutado por un científico de datos

*¿Cómo transformar datos de funcionamiento en decisiones de mantenimiento?*
</div>

## Breve descripción del autor del proyecto

**Oliver Kele** se presenta como científico de datos y actualmente estudia Ciencia de Datos en **Queensland University of Technology (QUT), Australia**, su graduación esta prevista para 2026. Sus principales areas de interés son la inteligencia artificial y la visualización de datos.

## ¿En que consiste?

El proyecto analiza las condiciones de funcionamiento de una máquina para identificar patrones relacionados con fallas. Su objetivo es convertir esos patrones en **reglas de mantenimiento sencillas** que puedan ser utilizadas por los operadores de dichas maquinas.

> La idea central es aprovechar los datos para determinar cuándo revisar una máquina o reemplazar una herramienta y de esta manera ahorrar recursos dentro de una organización.

INSERTAR UNA IMAGEN QUE TENGA QUE VER CON LO ANTERIOR

## ¿Que datos utiliza?
Se trabaja con **datos sintéticos**, generados para representar condiciones industriales. Para que su uso en un entorno real sea exitoso, es necesario utilizar **datos de funcionamiento de las máquinas en especifico que se quieran analizar**, ya que sus características, condiciones de operación y mantenimiento influyen en la aparición de fallas. Con esa información se deben ajustar los modelos y validar las reglas de mantenimiento propuestas.

| Variable | ¿Qué representa? | Unidad |
|----------|------------------|--------|
| Temperatura del aire | Temperatura del ambiente | K |
| Temperatura del proceso | Temperatura durante la operación | K |
| Velocidad de rotación | Rapidez de giro | rpm |
| Torque | Momento de fuerza aplicado | N·m |
| Desgaste de la herramienta | Uso acumulado de la herramienta | min |
| Falla | Indica si ocurrió una falla | Sí / No |

## ¿Como funciona?
1. **Explora los datos:** Compara las condiciones de funcionamiento con y sin fallas.
2. **Calcula nuevas variables:** Obtiene la diferencia de temperaturas y la potencia mecánica.
3. **Construye modelos estadísticos:** Utiliza regresión logística para estimar probabilidades de distintos tipos de falla.
4. **Propone reglas:** Establece límites que orientan las decisiones de mantenimiento.
5. **Evalúa las reglas:** Compara las fallas identificadas con las falsas alarmas.

La potencia mecánica se calcula mediante:

$$
P= \tau \omega
$$

Donde **P** es la potencia en watts, **τ** es el torque en N*m y **w** es la velocidad angular en rad/s.


<details>
<Summary> Un ejemplo para entenderlo mejor </Summary>
Si el análisis muestra que las fallas son más frecuentes después de cierto tiempo de uso, se podría proponer revisar o cambiar la herramienta antes de alcanzar ese límite.
Este ejemplo es ilustrativo: el límite debe obtenerse de los datos y validarse antes de aplicarlo a una máquina real.
</details>


INSERTAR UN GIF QUE TENGA QUE VER CON LO ANTERIOR
![gif 1](gif.gif)

## Resultados y alcance
- El autor encontró relaciones entre el desgaste de la herramienta y ciertos tipos de falla.
- Analizó la potencia y las condiciones de temperatura como señales relacionadas con problemas de operación.
- Propuso reglas comprensibles y evaluó cuántas falsas alarmas podían generar.
> [!Warning]
> El proyecto utiliza datos sintéticos. Sus resultados no demuestran que las reglas hayan reducido fallas en una fábrica ni permiten conocer el momento exacto en que una máquina se dañará.







