# Registro_Produccion_Sectores
Planillas y sistema de registro de producción para distintos sectores operativos
Este documento resume el circuito de registro y carga de la producción diaria, manteniendo una descripción clara, concisa y accionable.

📌 Objetivo

Centralizar en un Google Sheets la producción registrada por los operarios en planillas físicas para luego utilizar esos datos en reportes, análisis y control de eficiencia.

🏭 1. Circuito de Registro

Los operarios completan planillas físicas con:

-Código del artículo

-Cantidad producida

-Peso unitario (en gramos)

-Peso de colada (si corresponde)

-Maquinista

-Fecha

Envían fotos de las planillas al finalizar el turno.

Las fotos se transcriben al Google Sheets creado especialmente para registro de producción.

📄 2. Estructura del Google Sheets

El archivo contiene solapas por máquina, por ejemplo:

-Máquina 1

-Máquina 2

-Máquina 3

etc.

Cada solapa posee las siguientes columnas:

-Columna	Descripción
-Fecha	Día de producción
-Código	Código del artículo fabricado
-Maquinista	Operario responsable
-Cantidad	Unidades producidas
-Peso Unitario (g)	Peso del producto en gramos
-Colada (g)	Peso de colada por unidad, si aplica
-KG Total	Cálculo automático en kilogramos
⚙️ 3. Cálculo de KG Total

Los datos ingresados están en gramos, por lo que se convierten a kilogramos.

Fórmula utilizada (en Sheets):

=( (PesoUnitario + Colada) * Cantidad ) / 1000

Se suma peso + colada

Se multiplica por la cantidad producida

Se convierte a kg dividiendo por 1000

🧹 4. Objetivo del dataset resultante

Con este esquema se obtiene por cada máquina:

Producción por turno

KG totales fabricados

Trazabilidad por código y operario

Estos datos luego alimentan reportes de producción, análisis de eficiencia y control de scrap.

✔️ 5. Ventajas del método

Registro uniforme por máquina

Cálculos automáticos evitando errores manuales

Consolidación y análisis simple desde Sheets

Facilidad para integrar con Looker u otros dashboards
