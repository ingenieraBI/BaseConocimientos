# Índice de Conceptos DAX

## 1. Concepto DAX

### 2. CC_CON TABLA FECHAS

<div style="background-color: black; color: white; padding: 10px; border-radius: 5px;">
<code>
SUM(VENTAS[Cantidad_vendida])
</code>
</div>


#### 2.1. Año
```DAX
YEAR(CALENDARIO[Fechakey])
```
Devuelve el año de la columna `Fechakey`.

#### 2.2. Mes
```DAX
FORMAT(CALENDARIO[Fechakey], "mmmm")
```
Devuelve el nombre completo del mes.

#### 2.3. Día Nombre
```DAX
FORMAT(CALENDARIO[Fechakey], "DDDD")
```
Devuelve el nombre completo del día de la semana.

#### 2.4. Trimestre
```DAX
"Trimestre " & Q UARTER(CALENDARIO[Fechakey])
```
Devuelve el trimestre del año correspondiente.

#### 2.5. Semestre
```DAX
"Semestre " & ROUNDUP(MONTH(CALENDARIO[Fechakey])/6, 0)
```
Devuelve el semestre (1 o 2) al que pertenece el mes.

#### 2.6. Semana
```DAX
"Semana " & WEEKNUM(CALENDARIO[Fechakey], 2)
```
Devuelve el número de la semana.

#### 2.7. Día
```DAX
FORMAT(CALENDARIO[Fechakey], "dd")
```
Devuelve el día del mes.

## 3. COLUMNAS CALCULADAS DESDE LA MISMA EXPRESIÓN CON LA FUNCIÓN ADDCOLUMNS

## 4. MEDIDAS VENTAS | SUM

#### 4.1. Total Cantidades Vendidas
```DAX
sum(VENTAS[Cantidad_vendida])
```
Devuelve la suma total de las cantidades vendidas.

#### 4.2. Total Cantidades Devueltas
```DAX
sum(VENTAS[Cantidad_Devoluciones])
```
Devuelve la suma total de las cantidades devueltas.

#### 4.3. Total Unidades Vendidas Netas
```DAX
[Total Cantidades Vendidas] - [Total Cantidades Devueltas]
```
Devuelve el total neto de unidades vendidas.

## 5. COLUMNAS CALCULADAS | Productos | Condicionales IF

#### 5.1. Funciones IF
```DAX
IF(Condición, ValorSiVerdadero, ValorSiFalso)
```
Devuelve un valor basado en la evaluación de la condición.

#### 5.2. Funciones IF Anidadas
```DAX
IF(Condición1, Valor1, IF(Condición2, Valor2, ValorPredeterminado))
```
Evalúa múltiples condiciones anidadas.

#### 5.3. Operador OR
```DAX
Condición1 || Condición2
```
Devuelve verdadero si alguna de las condiciones es verdadera.

#### 5.4. Operador Pipes
```DAX
Condición1 || Condición2
```
Funciona como un operador OR alternativo.

#### 5.5. Con IN
```DAX
Valor IN {Lista_valores}
```
Devuelve verdadero si el valor está en la lista.

#### 5.6. Con &&
```DAX
Condición1 && Condición2
```
Devuelve verdadero si ambas condiciones son verdaderas.

## 6. Medidas | Productos | COUNT, COUNTA, COUNTROWS, DISTINCTCOUNT

#### 6.1. COUNT
```DAX
COUNT(Columna)
```
Cuenta el número de valores no nulos en la columna especificada.

#### 6.2. COUNTA
```DAX
COUNTA(Columna)
```
Cuenta todos los valores no vacíos en la columna especificada.

#### 6.3. COUNTROWS
```DAX
COUNTROWS(Tabla)
```
Cuenta el número total de filas en la tabla especificada.

#### 6.4. DISTINCTCOUNT
```DAX
DISTINCTCOUNT(Columna)
```
Cuenta el número de valores únicos en la columna especificada.
