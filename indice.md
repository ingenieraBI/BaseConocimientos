# Índice de Conceptos DAX

## 1. Concepto DAX

## 2. CC_CON TABLA FECHAS
### 2.1. Año = `YEAR(CALENDARIO[Fechakey])`
### 2.2. Mes = `FORMAT(CALENDARIO[Fechakey], "mmmm")`
### 2.3. Día Nombre = `FORMAT(CALENDARIO[Fechakey], "DDDD")`
### 2.4. Trimestre = `"Trimestre " & Q UARTER(CALENDARIO[Fechakey])`
### 2.5. Semestre = `"Semestre " & ROUNDUP(MONTH(CALENDARIO[Fechakey])/6, 0)`
### 2.6. Semana = `"Semana " & WEEKNUM(CALENDARIO[Fechakey], 2)`
### 2.7. Día = `FORMAT(CALENDARIO[Fechakey], "dd")`

## 3. COLUMNAS CALCULADAS DESDE LA MISMA EXPRESIÓN CON LA FUNCIÓN ADDCOLUMNS

## 4. MEDIDAS VENTAS | SUM
### 4.1. Total Cantidades Vendidas = `sum(VENTAS[Cantidad_vendida])`
### 4.2. Total Cantidades Devueltas = `sum(VENTAS[Cantidad_Devoluciones])`
### 4.3. Total Unidades Vendidas Netas = `[Total Cantidades Vendidas] - [Total Cantidades Devueltas]`

## 5. COLUMNAS CALCULADAS | Productos | Condicionales IF
### 5.1. Función IF
### 5.2. Función IF Anidada
### 5.3. Operador OR
### 5.4. Operador Pipes
### 5.5. Con IN
### 5.6. Con &&

## 6. Medidas | Productos | COUNT, COUNTA, COUNTROWS, DISTINCTCOUNT
