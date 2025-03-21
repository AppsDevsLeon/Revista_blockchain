
## **Incremento de Dificultad en el Minado de Blockchain**


Ahora que entendemos el rompecabezas criptográfico del minado, es momento de avanzar y analizar cómo se incrementa la dificultad de este proceso y por qué es necesario hacerlo. Como hemos visto, el minado se enfoca en gran medida en el campo del nonce, un campo controlado por los mineros que va variando para generar distintos hashes hasta encontrar uno válido.

La probabilidad de encontrar un hash válido es muy pequeña, lo que genera una competencia constante entre los mineros.

## **El Rango de Nombres y la Dificultad de Encontrar un Hash Válido**

Un bloque tiene un campo que contiene un valor de 32 bits de memoria asignados. Esto significa que hay un rango limitado de alrededor de 4 mil millones de valores posibles para el nonce.

### **¿Cómo Sabemos Cuántos Valores?**

Un valor de 32 bits puede ser un bit 1 o 0, es decir, tiene dos valores posibles. Esto nos da un total de:

```text
2^32 = 4,294,967,296 valores posibles
```

Esto nos da un rango de aproximadamente 4 mil millones de posibles valores para el nonce.

### **Ejemplo: Cálculos de un Minero Promedio**

Un minero promedio puede calcular hasta 100 millones de hashes por segundo. Esto significa que puede calcular todo el rango de 4 mil millones de valores posibles en solo 40 segundos.

```text
4,294,967,296 valores / 100,000,000 cálculos por segundo = 40.000 segundos
```

Las **pools mineras** y los **mineros industriales** son capaces de recorrer todo este rango de valores en fracciones de segundo.

### **El Problema: Probabilidad Baja de Encontrar un Hash Válido**

Aunque el cálculo sea rápido, la probabilidad de encontrar un hash válido es extremadamente baja, incluso después de recorrer los 4 mil millones de intentos posibles. La probabilidad de encontrar un hash válido es de:

```text
P(hash válido) = 16^(-18) (una probabilidad extremadamente baja)
```

## **¿Cómo Aumentar la Dificultad del Minado?**

Para evitar que los bloques se creen en segundos o fracciones de segundo, es necesario aumentar la dificultad del rompecabezas criptográfico. Esto se logra agregando un nuevo campo en el bloque: **la marca de tiempo** o **timestamp**.

### **¿Qué es la Marca de Tiempo?**

La marca de tiempo es un campo que representa el número de segundos transcurridos desde el 1 de enero de 1970 (hora UNIX). Esta marca de tiempo varía cada segundo y se incluye como parte del cálculo del hash del bloque.

La fórmula del hash del bloque, ahora, depende del identificador del bloque (número de bloque), la marca de tiempo, el nonce, los datos y el hash previo.

### **Ejemplo de Cálculo con Marca de Tiempo**

```text
Hash = SHA256(número_bloque + timestamp + nonce + datos + hash_prev)
```

### **El Problema con los Mineros Industriales**

Si bien los mineros promedio pueden tardar hasta 40 segundos en calcular todo el rango del nonce, los mineros industriales o pools mineras pueden hacerlo en fracciones de segundo. Sin embargo, la marca de tiempo, que varía segundo a segundo, permite que los mineros promedio reinicien sus cálculos, ya que el cambio en la marca de tiempo hace que el cálculo de hash sea distinto cada segundo.

### **Cómo se Aumenta la Dificultad para los Mineros Industriales**

Para complicar aún más el proceso para los mineros industriales, las pools mineras de gran escala, con su enorme potencia computacional, pueden realizar cálculos en fracciones de segundo. Para contrarrestar esto, se ajusta la dificultad para asegurar que un nuevo bloque se cree en aproximadamente **10 minutos**, no en fracciones de segundo.

### **Solución: Uso de MemPool y Ajustes de Dificultad**

Una solución eficaz al incremento de la potencia computacional de los mineros industriales es el uso de **MemPool** y el ajuste automático de la dificultad. Esto asegura que el minado siga siendo un proceso eficiente y justo para todos los participantes, independientemente de su poder computacional.

## **La Dificultad y la Creación de Bloques en Blockchain**

El minado en blockchain es un proceso altamente competitivo, donde los mineros deben calcular hashes válidos mientras enfrentan una probabilidad extremadamente baja de éxito. Para asegurarse de que la creación de bloques sea eficiente y no se realice en fracciones de segundo, se incrementa la dificultad ajustando la marca de tiempo y utilizando mecanismos como el MemPool. Esto mantiene el proceso bajo control y asegura que el objetivo de generar un bloque cada 10 minutos se cumpla.

