## **Algoritmos de consenso en blockchain: Proof of Stake (PoS)**

Otro algoritmo de consenso popular en el ecosistema blockchain es **Proof of Stake** o **Prueba de Participación**. Se trata de un algoritmo de consenso alternativo a **Proof of Work** que, en lugar de requerir nodos mineros, utiliza **validadores** para verificar las transacciones y validar nuevos bloques.

En este mecanismo, se requiere que los nodos posean una cierta cantidad de criptomonedas y que las **depositen o bloqueen en la red** como una forma de garantía. A esto se le conoce como **staking**. Los nodos que cumplan con lo anterior pueden convertirse en **validadores** de la cadena de bloques y, en función de la **cantidad de criptomonedas** que posean y hayan bloqueado en la red, podrán ser **elegidos aleatoriamente** para participar en el consenso, validar transacciones y crear nuevos bloques.

Por su participación, los validadores también reciben **recompensas en forma de criptomonedas**, además de las **tarifas de comisión** de las transacciones. No obstante, si actúan de forma deshonesta también pueden ser **penalizados**, mediante un mecanismo llamado **slashing**, creado para desincentivar los comportamientos que pueden ser dañinos en la red.

---

## **Las principales ventajas de PoS son:**

- En comparación con PoW, **Proof of Stake ofrece una mayor eficiencia energética**, ya que no requiere una gran capacidad de procesamiento.
- **Garantiza la seguridad y estabilidad de la red**, al incentivar a los validadores a actuar honestamente, ya que arriesgan su inversión (las criptomonedas depositadas en staking).
- **Es más escalable que PoW**, ya que no requiere del proceso de resolver complejos problemas matemáticos.

---

No obstante, este algoritmo de consenso es **más propenso a la centralización**, debido a que las entidades con mayor número de criptomonedas en *staking* tienen más probabilidades de ser elegidas como validadores.

**Ethereum**, cadena de bloques que inicialmente utilizaba el algoritmo de consenso **Proof of Work**, cambió a **Proof of Stake** el **15 de septiembre de 2022**.

Otras redes blockchain que implementan PoS son **Cardano** y **The Open Network (TON)**.

---

## **El Merge en Ethereum**

Se conoce como **Merge** al proceso de unión que ha permitido a la red Ethereum pasar de ser una red **Proof-of-Work** (con mineros que utilizaban el algoritmo ETHHash) a ser una red basada en **Staking**. Con la fusión entre la **cadena principal** y la **Beacon Chain**, Ethereum completó su transformación en una cadena **Proof-of-Stake**.

Con ello, el equipo de desarrolladores de Ethereum ha hecho a la blockchain más **eficiente a nivel energético**. El cambio a un sistema Proof-of-Stake, basado en nodos de validación que acumulan ETH, ha **reducido el consumo de energía** de Ethereum en un **99,95%**, ya que la red no depende más de los equipos de minería para operar.

Además, con el **Merge** se han creado las bases para la **escalabilidad** por medio del **sharding**, una tecnología de fraccionamiento de la red blockchain que podría llevar a Ethereum a alcanzar una escalabilidad superior a las **1.000 transacciones por segundo (TPS)** en sus primeros momentos.

> El **Sharding** es un proceso de fragmentación o división horizontal de las bases de datos en partes o fragmentos más pequeños. Esto con el fin de permitir un mejor manejo de las mismas, haciéndolas menos pesadas y más fáciles de operar.

Todo esto ha ocurrido **sin renunciar a la Ethereum Virtual Machine (EVM)**, sin interferencias en los **protocolos ni smart contracts desplegados** y sin perder absolutamente **ningún token o saldo** en el proceso.  
De hecho, todo el historial que forma parte del Ethereum actual (**ETH1**) será parte integral de **ETH2**, y la unión será **transparente** para todos.

---

## **Con el Merge surgen nuevos términos en Ethereum:**

- **Attestation:** Se denomina así al voto por el que el validador aprueba o no la validez de un bloque.
- **Checkpoint:** Par de bloques a la cabeza de una Época utilizado para determinar la validación.
- **Época:** Grupo de 32 Slots, aproximadamente 6,4 minutos. Cuando se afirma que está “justificada” significa que ha sido votada como válida y podrá utilizarse para iniciar el próximo Checkpoint. Cuando está “finalizada” significa que ya no podrá ser modificada.
- **Slashing:** Esta acción ocurre cuando un validador es calificado como malicioso. Entonces una parte significativa de los ETH estacados por el validador son recortados o eliminados como sanción.
- **Slot:** Periodo de 12 segundos en el que un validador elegido al azar tiene tiempo para proponer un bloque. Puede ocurrir que el Slot no tenga bloque si el validador está inactivo.
- **Validadores:** Entidades que validan y proponen nuevos bloques construidos por el nuevo mecanismo de consenso PoS. Son recompensados con ETH como antes lo eran los mineros.

---

## **Curiosidades tras la llegada de Ethereum Merge y ETH2**

- El **coste del gas y las comisiones** en la red **no se han visto afectadas** por el evento. Es decir, ETH2 **no hace más económicas** las operaciones dentro de Ethereum.
- La **escalabilidad de Ethereum** con ETH2 **no cambia aún**, ya que ni el tamaño ni la producción de bloques han cambiado. La escalabilidad dependerá de las **shard chains**, que se esperan para **2024**.
- Los actuales participantes en el staking de ETH2 deberán esperar a la actualización **Shanghai** para poder **retirar sus recompensas** generadas durante la Beacon Chain. Quienes participen en el staking después del Merge recibirán recompensas inmediatamente.
- La actualización de la **EVM** y la llegada de **Swarm** siguen en desarrollo. No hay una hoja de ruta clara con fechas específicas. Se recomienda revisar la web oficial de Ethereum para seguir su evolución.
