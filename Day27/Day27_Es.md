
## **¿Cómo funciona el consenso en una cadena de bloques?**


Vistos los conceptos básicos, es importante entender cómo funciona el proceso de **consenso** en una cadena de bloques. A continuación, se describen los pasos clave que ilustran cómo se logra el consenso en este entorno descentralizado.

---

## **Pasos del Proceso de Consenso**

### 1. Creación de la transacción

Cuando un usuario desea realizar una transacción, esta se **crea y se envía** a la red de nodos.

### 2. Difusión de la transacción

La transacción creada se **difunde** a todos los nodos de la red. Cada nodo la recibe y la añade a su lista de transacciones pendientes, conocida como **mempool**.

### 3. Verificación de la transacción

Los nodos comienzan a **verificar** la transacción, comprobando que:

- El remitente tenga suficientes fondos.
- La transacción no haya sido enviada previamente (prevención de **doble gasto**).

### 4. Creación de un bloque

Una vez verificada, la transacción se **agrupa** junto con otras en un nuevo **bloque**, que es transmitido a la red para su validación.

### 5. Consenso

Los nodos deben llegar a un **acuerdo general** sobre la validez del nuevo bloque. Esto puede implicar:

- La **resolución de problemas matemáticos** (como en Bitcoin, mediante prueba de trabajo).
- La **selección aleatoria de validadores** (como en Ethereum, mediante prueba de participación).

Dependiendo del algoritmo de consenso utilizado, un nodo podrá:

- “**Minar**” (como en Bitcoin).
- “**Validar**” (como en Ethereum) el nuevo bloque.

### 6. Adición y enlazado a la cadena

Una vez alcanzado el consenso:

- El bloque se **añade** a la cadena de bloques existente.
- Todos los nodos actualizan su **copia del libro mayor** para reflejar el nuevo estado de la red.


Este mecanismo de consenso permite que la blockchain funcione de manera **segura y eficiente**, garantizando que todos los participantes tengan una **visión coherente y confiable** de las transacciones.

> El consenso no solo permite la validación descentralizada de bloques, sino que también es el corazón del sistema que mantiene la confianza y la integridad de toda la red blockchain.
