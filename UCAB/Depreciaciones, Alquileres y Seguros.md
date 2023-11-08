### Depreciación de Activos
#### Método de la Linea Recta

Dada la **Fecha de Adquisición de un Activo, Costo del Activo y Vida Util del Activo,** se puede calcular el gasto de depreciación anual de un activo mediante la siguiente operación: $$depreciacionActivo = \frac{costo}{vidaUtil}\cdot(fechaCierre - fechaAdquisicion)$$

*Importante:*  Años anteriores al año de cierre no requieren de $fechaCierre - fechaAdquisicion$, pues se parte suponiendo que ya están depreciados. Ademas, se debe tener cuidado con los **Terrenos** (no se deprecian) y la **Vida Util,** pues si se pide calcular la depreciación de un activo en un año donde ya supera su vida util, pues simplemente no sera posible.
<br>
#### Método de Km Recorridos

Dada la **Vida Util del Vehículo, Costo del Vehículo y Km Recorridos,** se puede calcular por año el gasto de depreciación anual de un vehículo mediante la siguiente operación: $$depreciacionVehiculo = \frac{costo}{vidaUtil}\cdot KmRecorridos$$
<br>
#### Método de Horas Maquina

Dada la **Vida Util de la Maquinaria, Costo de la Maquinaria y Horas Maquina,** se puede calcular por año el gasto de depreciación anual de maquinaria mediante la siguiente operación: $$depreciacionMaquinaria = \frac{costo}{vidaUtil}\cdot horasMaquina$$
<br>
#### Cálculo de Alquileres

Dados la **Fecha de Renovación del Alquiler, Costo del Alquiler y Fecha de Cierre,** se puede calcular el costo total de alquileres por año de la siguiente forma: $$alquileres = \frac{costo}{unidadFecha}\cdot(fechaCierre - fechaRenovacion)$$
<br>
#### Cálculo de Pólizas de Seguro

Dados la **Fecha Inicial de Contratación, Precio de Compra y Fecha Final del Contrato,** se puede calcular el costo total de las pólizas de seguro de la siguiente forma :$$poliza = \frac{costo}{unidadFecha}\cdot(fechaCierre - fechaRenovacion)$$

Se debe calcular cada póliza anual por separado, y la póliza total vendrá dada por: $$polizaTotal=poliza_{1}+poliza_{2}+\dots{}+poliza_{n}$$

*Importante:*  Cuidado con las pólizas de años anteriores, pues al realizar la operación de $fechaCierre - fechaRenovacion$, se deberá restar ese valor a **12 meses** para poder determinar lo restante de la póliza anterior, ese valor se deberá multiplicar en el calculo de la póliza sustituyendo la resta de fechas.

##### Tags

#clase #class