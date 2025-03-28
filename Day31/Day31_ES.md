## **Inmutabilidad y Finalidad en las Transacciones en Blockchain**


La inmutabilidad es la capacidad de una blockchain para **mantener intacto su historial de transacciones**, evitando cualquier tipo de alteración o eliminación. Una vez que las transacciones se confirman, se vuelven **permanentes e irreversibles**.

![i](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day31/images/ChatGPT%20Image%2028%20mar%202025%2C%2014_45_23.png)

### Elementos Clave:

- **Estructura de bloques y hashes**  
  Cada bloque contiene un hash único vinculado al bloque anterior. Alterar un bloque rompería la cadena.

- **Algoritmos de consenso**  
  Pruebas como PoW (Prueba de Trabajo) y PoS (Prueba de Participación) dificultan la manipulación.

- **Descentralización**  
  La necesidad de modificar todos los nodos de una red grande como Bitcoin hace casi imposible alterar los datos.

###  Ventajas de la Inmutabilidad:

- Garantiza la **integridad de los datos**  
- Fomenta la **transparencia** en redes públicas  
- Previene **fraudes** y genera **confianza** en los usuarios

### Aplicaciones Reales:

- **Rastreo de productos** en cadenas de suministro  
- **Almacenamiento seguro** de datos sensibles en educación y salud

---

## **Finalidad en las Transacciones**

La finalidad es el punto en el que una transacción se considera **irreversible y permanente**, eliminando la posibilidad de fraudes como el doble gasto.

### Tipos de Finalidad:

- **Finalidad probabilística**  
  La seguridad aumenta con cada bloque añadido  
  _Ejemplo: Bitcoin_

- **Finalidad económica**  
  Las redes PoS sancionan económicamente el comportamiento deshonesto  
  _Ejemplo: Ethereum_

- **Finalidad absoluta**  
  Las transacciones confirmadas son inmutables de inmediato  
  _Ejemplo: Stellar_

- **Finalidad instantánea**  
  Finalidad inmediata en redes privadas  
  _Ejemplo: Ripple_

### Importancia de la Finalidad:

- Asegura la **permanencia y confianza** en las transacciones  
- Previene **disputas** y ataques como el **doble gasto**

---

## **Ataques que Amenazan la Inmutabilidad y Finalidad**

| Tipo de Ataque         | Descripción |
|------------------------|-------------|
| **Ataque del 51%**     | Requiere controlar más del 50% del poder de hash para manipular transacciones (casi imposible en redes grandes). |
| **Ataque de carrera**  | Un usuario envía dos transacciones simultáneamente para invalidar una de ellas. |
| **Ataque de Finney**   | Un minero malicioso crea un bloque fraudulento con una transacción reversible. |
| **Ataque por fuerza bruta** | Intenta generar variantes fraudulentas de la blockchain (extremadamente difícil). |


- La **inmutabilidad** protege el historial de la blockchain, evitando manipulaciones.  
- La **finalidad** garantiza que las transacciones confirmadas no puedan revertirse.  
- Ambos conceptos son fundamentales para la **confianza**, **seguridad** y **transparencia** en las redes blockchain.

---
