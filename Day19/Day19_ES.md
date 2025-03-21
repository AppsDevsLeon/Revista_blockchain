## **Tolerancias a Fallas Bizantinas**

La Tolerancia a Fallas Bizantinas (BFT) es la capacidad de un sistema distribuido para continuar funcionando correctamente incluso si algunos de sus componentes fallan o se comportan de manera maliciosa. Este concepto es fundamental en sistemas donde se requiere alta disponibilidad y resistencia a fallas, como en las redes blockchain.

## **Definición del Problema**

El *Problema de los Generales Bizantinos* plantea la dificultad de alcanzar un acuerdo confiable en un sistema distribuido, incluso cuando algunos participantes (nodos) pueden fallar o actuar maliciosamente. Se define formalmente como un problema de consenso en presencia de fallos arbitrarios (también conocidos como fallos bizantinos).

Un grupo de nodos debe acordar una única decisión (por ejemplo, atacar o retirarse), pero algunos de ellos pueden enviar mensajes contradictorios o falsos. El objetivo es garantizar que:

1. Todos los nodos leales acuerden la misma decisión.
2. Si el nodo líder (comandante) es leal, entonces los nodos leales siguen su orden.

## **Condiciones del Modelo**

- Comunicación punto a punto (todos los nodos pueden comunicarse entre sí).
- Los mensajes pueden ser enviados por canales poco confiables (con posibilidad de manipulación por parte de nodos defectuosos).
- Se desconoce de antemano cuántos nodos son maliciosos.
- Los nodos deben alcanzar consenso basado en los mensajes intercambiados.


## **Caso de Estudio: 4 Generales, 1 Traidor**

Supongamos un conjunto de 4 generales rodeando un objetivo militar. Cada general puede enviar mensajes a los otros. El objetivo común es tomar una decisión coherente entre "atacar" o "retirarse".

### Escenario 1: Un General Leal da la Orden

- El comandante envía la orden "atacar".
- Un general actúa como traidor y altera el mensaje recibido por los demás.
- Los generales leales se comunican entre ellos para confirmar los mensajes.
- Al recibir mayoría de mensajes "atacar", se decide proceder con el ataque.

Resultado: **consenso alcanzado** (3 de 4 generales toman la misma decisión).

### Escenario 2: El Comandante es el Traidor

- El comandante envía "atacar" a algunos y "retirarse" a otros.
- Los generales leales intercambian mensajes para validar el contenido recibido.
- Cada uno sigue el valor mayoritario entre los mensajes recibidos.

Resultado: **consenso aún alcanzado**, si hay solo un traidor.

### ¿Cuántos Traidores Puede Haber?

Aquí viene lo importante:

 **La tolerancia a fallos bizantinos solo funciona si no hay más de un tercio de traidores.**

| Total de Generales | Máximo de Traidores Tolerables |
|--------------------|-------------------------------|
| 3                  | 0                             |
| 4                  | 1                             |
| 10                 | 3                             |
| 100                | 33                            |

 Si hay más del 33%, el consenso ya no es confiable.

---


## **Límite de Tolerancia a Fallos**

Para resolver correctamente el Problema de los Generales Bizantinos:

> **Un sistema tolerante a fallos bizantinos debe cumplir con la condición:**  
>  
> **n ≥ 3f + 1**

Donde `n` es el número total de nodos, y `f` es el número máximo de nodos defectuosos o maliciosos que se pueden tolerar.


## **Aplicaciones del Problema de los Generales Bizantinos**

Este problema no es solo una historia divertida. Es un **problema real** con implicaciones **tecnológicas críticas**. Aquí algunos ejemplos:

###  Aviones
- Los sensores de un avión deben compararse entre sí para evitar catástrofes.
- Si un sensor falla, los demás deben **ponerse de acuerdo** para ignorar la información errónea.

###  Plantas Nucleares
- La coordinación entre múltiples sistemas críticos garantiza seguridad ante fallos o sabotajes.

### Estaciones Espaciales
- El sistema de acoplamiento de una nave con la Estación Espacial Internacional requiere **coordinación total** entre subsistemas.

### Blockchain
- En una blockchain descentralizada, los **nodos** deben llegar a un **consenso sobre las transacciones**, incluso si algunos están comprometidos.



## **Relación con Blockchain**

En blockchain, usamos protocolos de consenso inspirados en este problema, como:

- **Proof of Work (PoW)**
- **Proof of Stake (PoS)**
- **Practical Byzantine Fault Tolerance (PBFT)**

Estos protocolos permiten:

- Mantener la red segura.
- Tolerar ataques.
- Asegurar que todos los nodos lleguen al mismo resultado, aún cuando algunos actúen maliciosamente.

## **Visualizando los Enlaces de Blockchain y el Impacto de un Nodo Bizantino**

Se ilustra cómo los bloques en una blockchain están interconectados y cómo un nodo malicioso puede romper la cadena al alterar un solo bloque.

---

### Estructura de un Bloque en Blockchain**

```plaintext
+-------------+       +-------------+       +-------------+       +-------------+
|  Bloque #1  | ----> |  Bloque #2  | ----> |  Bloque #3  | ----> |  Bloque #4  |
| (Génesis)   |       | PrevHash: 1 |       | PrevHash: 2 |       | PrevHash: 3 |
| Hash: #1    |       | Hash: #2    |       | Hash: #3    |       | Hash: #4    |
| Nonce: 💡    |       | Nonce: 💡    |       | Nonce: 💡    |       | Nonce: 💡    |
+-------------+       +-------------+       +-------------+       +-------------+
```

Cada bloque contiene:

- ✅ Datos de transacciones  
- 🔗 Hash del bloque anterior  
- 🔒 Su propio hash  
- 🎯 Un **nonce**: número que se ajusta hasta encontrar un hash válido

---

### ¿Qué Ocurre si un Nodo Malicioso Modifica el Bloque #2?**

```plaintext
+-------------+       +-------------+       +-------------+       +-------------+
|  Bloque #1  | ----> |  Bloque #2  | -X->  |  Bloque #3  |  ???  |  Bloque #4  |
| (Génesis)   |       | 🔧 Alterado |       | PrevHash: ❌ |       | PrevHash: ❌ |
| Hash: #1    |       | Hash: ⚠️     |       | Hash: ??    |       | Hash: ??    |
| Nonce: ❓    |       | Nonce: 🔁    |       | Nonce: 🔁    |       | Nonce: 🔁    |
+-------------+       +-------------+       +-------------+       +-------------+
```

-  Al cambiar cualquier dato en el Bloque #2 (incluyendo el **nonce**), su **hash cambia por completo** debido al **efecto avalancha** de las funciones hash.
-  Esto invalida el hash previo almacenado en el Bloque #3, que a su vez arrastra el error hacia el Bloque #4 y los siguientes.
- Para que la cadena siga siendo válida, se tendría que **recalcular el nonce de todos los bloques posteriores**, lo cual es computacionalmente inviable en una red distribuida.
-  La red detecta automáticamente esta manipulación, ya que los hashes ya no coinciden.



- Si todos los bloques están correctamente enlazados (hash + nonce válidos), la cadena es segura y válida.
- Si se modifica un solo bloque, se activa el **efecto avalancha**:  
  Se deben rehacer todos los hashes y nonces de los bloques siguientes.
- Esto demuestra la **inmutabilidad y seguridad** de la blockchain:  
  **Cualquier intento de alterar un bloque rompe la cadena y es detectado inmediatamente.**


## **Referencias**

- 📄 **The Byzantine Generals Problem** (1982) – Leslie Lamport, Robert Shostak y Marshall Pease.
- 📝 Blog: *Understanding Blockchain Fundamentals* – Medium, 2017, por George Cox.


