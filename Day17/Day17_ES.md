## **Tolerancias a Fallas Bizantinas**

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

La solución al problema de los generales bizantinos requiere que:

 **Para que un sistema tolerante a fallos bizantinos funcione correctamente, debe cumplirse:**

```math
**n ≥ 3f + 1**

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

## **Referencias**

- 📄 **The Byzantine Generals Problem** (1982) – Leslie Lamport, Robert Shostak y Marshall Pease.
- 📝 Blog: *Understanding Blockchain Fundamentals* – Medium, 2017, por George Cox.


