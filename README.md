# Extremos térmicos en el Mediterráneo occidental (1980–2024)

Visualización interactiva sobre la evolución de las olas de calor en el Mediterráneo occidental entre 1980 y 2024, su relación con la circulación atmosférica y su impacto humano.

El proyecto forma parte de la práctica final de la asignatura **Visualización de Datos** del **Máster en Ciencia de Datos de la UOC**.

## Objetivo del proyecto

El objetivo de esta visualización es comunicar de forma clara y exploratoria cómo han cambiado los extremos térmicos en el Mediterráneo occidental durante las últimas décadas.

La página permite analizar:

* La evolución temporal de las olas de calor.
* Las regiones donde el calor extremo es más intenso.
* La relación entre los eventos extremos y la circulación atmosférica.
* La exposición humana al calor extremo.
* La mortalidad en exceso y las diferencias por sexo durante grandes episodios cálidos.

El resultado es una visualización narrativa tipo **scrollytelling**, en la que el usuario avanza por distintas secciones y puede interactuar con gráficos, mapas, botones, selectores, tooltips y controles temporales.

## Qué muestra la visualización

La visualización está organizada en cinco bloques principales.

### 1. Tendencias temporales

La primera sección muestra cómo evolucionan los principales indicadores de ola de calor entre 1980 y 2024.

Se pueden explorar cuatro métricas:

* **HWF**: frecuencia anual de olas de calor.
* **HWD**: duración media de los episodios.
* **HWI**: intensidad térmica media.
* **HWMI**: índice de magnitud de ola de calor.

El gráfico incluye una línea anual, una línea de tendencia y marcadores de eventos extremos destacados, como 2003, 2019, 2022 y 2023.

### 2. Distribución espacial

La segunda sección muestra un mapa del Mediterráneo occidental con regiones de España, Portugal, Francia, Italia y Grecia.

El usuario puede cambiar:

* La década analizada.
* La métrica representada.
* La región consultada mediante interacción con el mapa.

La escala de color utiliza tonos oscuros, naranjas y rojos para representar la severidad térmica. Los valores más altos aparecen en rojo intenso.

El panel lateral muestra los valores concretos de cada región: HWMI, HWF, HWD, Humidex y tendencia.

### 3. Circulación atmosférica

La tercera sección analiza la relación entre las olas de calor y la dinámica atmosférica.

Incluye gráficos de dispersión que relacionan:

* **Blocking Index** con **HWI**.
* **NAO Index** con **HWMI**.
* Series alineadas de geopotencial, NAO y magnitud de ola de calor.

Esta parte ayuda a interpretar qué condiciones atmosféricas están asociadas a los eventos extremos más intensos.

### 4. Exposición humana

La cuarta sección introduce el indicador **exp_HWMI**, que combina la magnitud térmica con la exposición poblacional.

Se muestran:

* La evolución de la exposición por país.
* La relación entre exposición térmica y mortalidad en exceso.

Esta sección conecta el fenómeno climático con su impacto social y sanitario.

### 5. Perspectiva de género

La última sección analiza la mortalidad diferencial por sexo durante episodios extremos de calor.

Se representa:

* La razón de mortalidad mujer/hombre por país y evento.
* La evolución de la mortalidad estival en mujeres y hombres.

El color fucsia se utiliza para representar mujeres y el cian para representar hombres. Esta codificación facilita la lectura de diferencias entre ambos grupos.

## Preguntas que responde

La visualización está diseñada para responder a las siguientes preguntas:

1. ¿Cómo han evolucionado la frecuencia, duración e intensidad de las olas de calor entre 1980 y 2024?
2. ¿Qué años y décadas muestran eventos térmicos más extremos?
3. ¿Dónde se concentran espacialmente los valores más altos de calor extremo?
4. ¿Qué diferencias existen entre regiones interiores, costeras y países mediterráneos?
5. ¿Qué relación existe entre los bloqueos atmosféricos, la fase de la NAO y los eventos de calor extremo?
6. ¿Qué países o regiones presentan mayor exposición humana al calor extremo?
7. ¿Existe relación entre exposición térmica y mortalidad en exceso?
8. ¿Se observa un impacto diferencial por sexo durante las olas de calor?

## Datos e indicadores

El proyecto combina datos climáticos, atmosféricos, demográficos y sanitarios.

Las fuentes consideradas son:

| Fuente                  | Uso principal                                               |
| ----------------------- | ----------------------------------------------------------- |
| ERA5 - ECMWF/Copernicus | Temperatura, humedad, presión, geopotencial y precipitación |
| NOAA/CPC                | Índice de la Oscilación del Atlántico Norte                 |
| Eurostat                | Mortalidad semanal, población y estructura demográfica      |
| EuroMOMO / Eurostat     | Referencia para mortalidad en exceso                        |

A partir de estas fuentes se construyen indicadores derivados:

| Indicador      | Descripción                                     |
| -------------- | ----------------------------------------------- |
| HWF            | Número de olas de calor por año                 |
| HWD            | Duración media de los episodios                 |
| HWI            | Intensidad media de la ola de calor             |
| HWMI           | Índice combinado de duración e intensidad       |
| Humidex        | Temperatura aparente asociada al estrés térmico |
| BI             | Índice de bloqueo atmosférico                   |
| exp_HWMI       | Exposición humana ponderada al calor extremo    |
| sex_ratio_mort | Razón de mortalidad en exceso mujer/hombre      |

## Diseño visual

El diseño utiliza un fondo oscuro para aumentar el contraste y destacar los datos.

La codificación cromática principal es:

| Color       | Uso                                                   |
| ----------- | ----------------------------------------------------- |
| Rojo        | Calor extremo, eventos destacados y valores altos     |
| Naranja     | Intensidad térmica elevada                            |
| Amarillo    | Valores intermedios o variables auxiliares            |
| Azul / cian | Variables atmosféricas o comparación masculina        |
| Fucsia      | Mortalidad femenina                                   |
| Gris        | Ejes, etiquetas secundarias y elementos de referencia |

El uso de colores se complementa con etiquetas, tooltips, leyendas, líneas de tendencia y paneles informativos para mejorar la comprensión.

## Interactividad

La visualización incluye varios elementos interactivos:

* Botones para cambiar entre HWF, HWD, HWI y HWMI.
* Slider temporal para cambiar de década en el mapa.
* Selector de métrica espacial.
* Tooltips con información detallada al pasar el cursor.
* Panel lateral con valores regionales.
* Marcadores de eventos extremos.
* Botones de exportación de gráficos en SVG y PNG.

Estos elementos permiten que el usuario explore los datos de forma progresiva, sin saturar la pantalla con toda la información al mismo tiempo.

## Tecnologías utilizadas

El proyecto está desarrollado con:

* HTML5.
* CSS3.
* JavaScript.
* D3.js v7.
* SVG.
* GitHub Pages.

## Limitaciones

La visualización tiene finalidad académica y exploratoria.

Algunas limitaciones del proyecto son:

* La integración de datos climáticos, atmosféricos y demográficos requiere agregaciones y simplificaciones.
* La mortalidad en exceso depende de factores adicionales que no se representan completamente en todos los gráficos.
* Variables como edad, salud previa, vulnerabilidad socioeconómica o acceso a climatización no se muestran con todo el detalle posible.
* La visualización prioriza la claridad narrativa y la comunicación visual frente a la reproducción completa de todos los cálculos científicos subyacentes.
* Algunos recursos externos, como librerías JavaScript o fuentes web, pueden requerir conexión a internet.

## Licencia

Este proyecto se publica bajo licencia MIT.

Los datos originales mantienen sus respectivas licencias:

* Copernicus / ECMWF para ERA5.
* Dominio público para NOAA/CPC.
* Creative Commons CC BY 4.0 para Eurostat.

## Autoría

Proyecto desarrollado para la práctica final de la asignatura **Visualización de Datos** del **Máster en Ciencia de Datos de la UOC**.

**Título del proyecto:**
*Extremos térmicos en el Mediterráneo occidental (1980–2024): tendencias, circulación atmosférica e impacto humano*
