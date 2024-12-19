# Índice de Conceptos DAX

## 1. Concepto DAX

---

## 2. CC_CON TABLA FECHAS

### 2.1. Año
```DAX
YEAR(CALENDARIO[Fechakey])
```
Devuelve el año de la columna `Fechakey`.

### 2.2. Mes
```DAX
FORMAT(CALENDARIO[Fechakey], "mmmm")
```
Devuelve el nombre completo del mes.

### 2.3. Día Nombre
```DAX
FORMAT(CALENDARIO[Fechakey], "DDDD")
```
Devuelve el nombre completo del día de la semana.

### 2.4. Trimestre
```DAX
"Trimestre " & Q UARTER(CALENDARIO[Fechakey])
```
Devuelve el trimestre del año correspondiente.

### 2.5. Semestre
```DAX
"Semestre " & ROUNDUP(MONTH(CALENDARIO[Fechakey])/6, 0)
```
Devuelve el semestre (1 o 2) al que pertenece el mes.

### 2.6. Semana
```DAX
"Semana " & WEEKNUM(CALENDARIO[Fechakey], 2)
```
Devuelve el número de la semana.

### 2.7. Día
```DAX
FORMAT(CALENDARIO[Fechakey], "dd")
```
Devuelve el día del mes.

---

## 3. COLUMNAS CALCULADAS DESDE LA MISMA EXPRESIÓN CON LA FUNCIÓN ADDCOLUMNS
(No se especificó contenido adicional para este tema.)

---

## 4. MEDIDAS VENTAS | SUM

### 4.1. Total Cantidades Vendidas
```DAX
SUM(VENTAS[Cantidad_vendida])
```
Calcula la suma total de las cantidades vendidas.

### 4.2. Total Cantidades Devueltas
```DAX
SUM(VENTAS[Cantidad_Devoluciones])
```
Calcula la suma total de las cantidades devueltas.

### 4.3. Total Unidades Vendidas Netas
```DAX
[Total Cantidades Vendidas] - [Total Cantidades Devueltas]
```
Calcula las unidades netas vendidas restando las devoluciones.

---

## 5. COLUMNAS CALCULADAS | Productos | Condicionales IF

### 5.1. Función IF
```DAX
IF(Condición, Valor_si_verdadero, Valor_si_falso)
```
Evalúa una condición y devuelve un valor si es verdadero o falso.

### 5.2. Función IF anidada
```DAX
IF(Condición1, Valor1, IF(Condición2, Valor2, Valor3))
```
Permite evaluar varias condiciones anidadas.

### 5.3. Operador OR
```DAX
OR(Condición1, Condición2)
```
Devuelve verdadero si alguna de las condiciones es verdadera.

### 5.4. Operador Pipes
```DAX
Condición1 || Condición2
```
Devuelve verdadero si alguna de las condiciones es verdadera (alternativa a `OR`).

### 5.5. Con IN
```DAX
Valor IN {Lista_valores}
```
Devuelve verdadero si el valor está en la lista.

### 5.6. Con &&
```DAX
Condición1 && Condición2
```
Devuelve verdadero si ambas condiciones son verdaderas.

---

## 6. MEDIDAS | Productos | COUNT, COUNTA, COUNTROWS, DISTINCTCOUNT

### COUNT
```DAX
COUNT(Columna)
```
Cuenta el número de valores no nulos en la columna especificada.

### COUNTA
```DAX
COUNTA(Columna)
```
Cuenta el número de valores (incluidos nulos) en la columna especificada.

### COUNTROWS
```DAX
COUNTROWS(Tabla)
```
Devuelve el número de filas en una tabla.

### DISTINCTCOUNT
```DAX
DISTINCTCOUNT(Columna)
```
Cuenta el número de valores únicos en la columna especificada.
