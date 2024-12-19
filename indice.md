# Índice de Conceptos DAX

## 1. Concepto DAX

El DAX (Data Analysis Expressions) es un lenguaje funcional que se utiliza en herramientas como Power BI, Power Pivot y SSAS Tabular para crear columnas calculadas, medidas y tablas calculadas.

## 2. CC_CON TABLA FECHAS

### 2.1. Año
```DAX
YEAR(CALENDARIO[Fechakey])
Devuelve el año de la columna Fechakey.

2.2. Mes
DAX
Copiar código
FORMAT(CALENDARIO[Fechakey], "mmmm")
Devuelve el nombre completo del mes.

2.3. Día Nombre
DAX
Copiar código
FORMAT(CALENDARIO[Fechakey], "DDDD")
Devuelve el nombre completo del día de la semana.

2.4. Trimestre
DAX
Copiar código
"Trimestre " & QUARTER(CALENDARIO[Fechakey])
Devuelve el trimestre del año correspondiente.

2.5. Semestre
DAX
Copiar código
"Semestre " & ROUNDUP(MONTH(CALENDARIO[Fechakey])/6, 0)
Devuelve el semestre (1 o 2) al que pertenece el mes.

2.6. Semana
DAX
Copiar código
"Semana " & WEEKNUM(CALENDARIO[Fechakey], 2)
Devuelve el número de la semana.

2.7. Día
DAX
Copiar código
FORMAT(CALENDARIO[Fechakey], "dd")
Devuelve el día del mes.

3. COLUMNAS CALCULADAS DESDE LA MISMA EXPRESIÓN CON LA FUNCIÓN ADDCOLUMNS
Ejemplo de uso de ADDCOLUMNS:

DAX
Copiar código
ADDCOLUMNS(
    TablaBase,
    "NuevaColumna", [ColumnaExistente] * 2
)
Devuelve una tabla con columnas adicionales basadas en expresiones.

4. MEDIDAS VENTAS | SUM
4.1. Total Cantidades Vendidas
DAX
Copiar código
SUM(VENTAS[Cantidad_vendida])
Suma el total de cantidades vendidas.

4.2. Total Cantidades Devueltas
DAX
Copiar código
SUM(VENTAS[Cantidad_Devoluciones])
Suma el total de cantidades devueltas.

4.3. Total Unidades Vendidas Netas
DAX
Copiar código
[Total Cantidades Vendidas] - [Total Cantidades Devueltas]
Calcula las unidades vendidas netas restando las devoluciones.

5. COLUMNAS CALCULADAS | Productos | Condicionales IF
5.1. Función IF
DAX
Copiar código
IF(Condición, ResultadoVerdadero, ResultadoFalso)
Devuelve un valor basado en la evaluación de la condición.

5.2. Función IF anidada
DAX
Copiar código
IF(Condición1, Resultado1, IF(Condición2, Resultado2, ResultadoFalso))
Anida varias condiciones.

5.3. Operador OR
DAX
Copiar código
Condición1 || Condición2
Devuelve verdadero si alguna de las condiciones es verdadera.

5.4. Operador Pipes
DAX
Copiar código
Condición1 || Condición2
Devuelve verdadero si alguna de las condiciones es verdadera (alternativa a OR).

5.5. Con IN
DAX
Copiar código
Valor IN {Lista_valores}
Devuelve verdadero si el valor está en la lista.

5.6. Con &&
DAX
Copiar código
Condición1 && Condición2
Devuelve verdadero si ambas condiciones son verdaderas.

6. Medidas | Productos | COUNT, COUNTA, COUNTROWS, DISTINCTCOUNT
COUNT
DAX
Copiar código
COUNT(Columna)
Cuenta el número de valores no nulos en la columna especificada.

COUNTA
DAX
Copiar código
COUNTA(Columna)
Cuenta todos los valores (incluyendo texto) en la columna especificada.

COUNTROWS
DAX
Copiar código
COUNTROWS(Tabla)
Cuenta el número de filas en una tabla.

DISTINCTCOUNT
DAX
Copiar código
DISTINCTCOUNT(Columna)
Cuenta el número de valores únicos en la columna.

Instrucciones:

Copia todo este contenido.
Pega directamente en tu archivo en GitHub.
Realiza el commit con un mensaje como: Añadido índice completo de conceptos DAX.
Si necesitas alguna revisión o ajuste después de que lo veas en GitHub, ¡solo dime!





Tú dijiste:



ves, que no se ve bien como esperaba, lo único que veo bien es lo que ves en la imagen 3
ChatGPT Plus
ChatGPT
Entiendo que estás buscando una estructura limpia y organizada como en la imagen 3. Para que todo quede bien alineado y claro, lo organizaremos de esta manera:

Usaremos encabezados para las secciones principales.
Dentro de cada sección, utilizaremos bloques de código para las fórmulas.
Aseguraremos que la descripción de las fórmulas esté debajo de cada bloque.
Aquí está un ejemplo corregido y mejorado:

markdown
Copiar código
# Índice de Conceptos DAX

## 1. Concepto DAX
El DAX (Data Analysis Expressions) es un lenguaje funcional que se utiliza en herramientas como Power BI, Power Pivot y SSAS Tabular para crear columnas calculadas, medidas y tablas calculadas.

## 2. CC_CON TABLA FECHAS

### 2.1. Año
```DAX
YEAR(CALENDARIO[Fechakey])
Devuelve el año de la columna Fechakey.

2.2. Mes
DAX
Copiar código
FORMAT(CALENDARIO[Fechakey], "mmmm")
Devuelve el nombre completo del mes.

2.3. Día Nombre
DAX
Copiar código
FORMAT(CALENDARIO[Fechakey], "DDDD")
Devuelve el nombre completo del día de la semana.

2.4. Trimestre
DAX
Copiar código
"Trimestre " & QUARTER(CALENDARIO[Fechakey])
Devuelve el trimestre del año correspondiente.

2.5. Semestre
DAX
Copiar código
"Semestre " & ROUNDUP(MONTH(CALENDARIO[Fechakey])/6, 0)
Devuelve el semestre (1 o 2) al que pertenece el mes.

2.6. Semana
DAX
Copiar código
"Semana " & WEEKNUM(CALENDARIO[Fechakey], 2)
Devuelve el número de la semana.

2.7. Día
DAX
Copiar código
FORMAT(CALENDARIO[Fechakey], "dd")
Devuelve el día del mes.

DISTINCTCOUNT
DAX
Copiar código
DISTINCTCOUNT(Columna)
Cuenta el número de valores únicos en la columna.
