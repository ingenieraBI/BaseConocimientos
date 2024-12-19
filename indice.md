# Índice de Conceptos DAX

# Concepto DAX

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


**3. COLUMNAS CALCULADAS DESDE LA MISMA EXPRESIÓN CON LA FUNCIÓN ADDCOLUMNS**

**4. MEDIDAS VENTAS | SUM**
4.1. **Total Cantidades Vendidas**  
   `SUM(VENTAS[Cantidad_vendida])`

4.2. **Total Cantidades Devueltas**  
   `SUM(VENTAS[Cantidad_Devoluciones])`

4.3. **Total Unidades Vendidas Netas**  
   `[Total Cantidades Vendidas] - [Total Cantidades Devueltas]`


## 5. COLUMNAS CALCULADAS | Productos | Condicionales IF
### 5.1. Función IF
### 5.2. Función IF Anidada
### 5.3. Operador OR
### 5.4. Operador Pipes
### 5.5. Con IN
### 5.6. Con &&

## 6. Medidas | Productos | COUNT, COUNTA, COUNTROWS, DISTINCTCOUNT
