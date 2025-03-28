## **Principales Redes Blockchain y sus Algoritmos de Consenso (2025)**

A continuación se presenta una tabla con las **principales redes blockchain** (públicas, privadas y de consorcio) existentes hasta la fecha, indicando el **algoritmo de consenso** que utilizan **actualmente**. En los casos donde la red haya **cambiado** de algoritmo, se menciona el algoritmo **actual**.

| **Blockchain**                   | **Tipo**                      | **Algoritmo de Consenso (Actual)**                                                                                                                                                                                                                                                                                              |
|----------------------------------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Bitcoin**                      | Pública (Permisionless)       | **Prueba de Trabajo (PoW)** – Mecanismo de consenso **descentralizado** donde mineros compiten para resolver puzzles criptográficos y validar bloques. (No ha cambiado desde su creación).                                                                                                                                  |
| **Ethereum**                     | Pública (Permisionless)       | **Prueba de Participación (PoS)** – Desde *The Merge* en sept. 2022 Ethereum utiliza PoS (antes usaba PoW). Los validadores bloquean ETH (staking) en lugar de minar para confirmar bloques.                                                                                                                              |
| **Solana**                       | Pública                       | **Prueba de Participación Delegada + Prueba de Historia (DPoS + PoH)** – Usa un PoS basado en validadores delegados junto con un reloj criptográfico **Proof of History** único para ordenar eventos, logrando altísimo rendimiento de ~65k TPS.                                                                         |
| **Ripple (XRP Ledger)**          | Pública (Permisionada)        | **Protocolo de Consenso XRP Ledger** – Algoritmo **federado** de acuerdo bizantino (FBA) donde una red de validadores de confianza alcanza consenso por **votación supermayoritaria** (80%) sin minería. (No usa PoW/PoS, sino su propio protocolo).                                                              |
| **Cardano**                      | Pública                       | **Prueba de Participación (PoS) – Ouroboros** – Algoritmo PoS desarrollado por Cardano (desde 2017) llamado Ouroboros. Validadores (stake pools) producen bloques según la cantidad de ADA delegada por usuarios. *(Nunca usó PoW).*                                                                      |
| **Polkadot**                     | Pública                       | **Nominated Proof of Stake (NPoS)** – Variante de PoS donde los **nominadores** respaldan validadores con DOT. Emplea un consenso híbrido: producción de bloques (BABE) y gadget de finalización **GRANDPA** (BFT) para rapidez y seguridad.                                                                       |
| **Avalanche**                    | Pública                       | **Prueba de Participación (PoS)** – Utiliza el **consenso Avalanche**, una familia de algoritmos probabilísticos (Snowball, Avalanche) basados en muestreo aleatorio repetido (aBFT). Su cadena de contratos usa el protocolo Snowman (versión lineal de Avalanche).                                               |
| **Algorand**                     | Pública                       | **Prueba de Participación Pura (PPoS)** – Algoritmo PoS único de Algorand en el que los validadores son seleccionados **aleatoriamente** mediante funciones VRF para proponer y votar bloques. Es altamente eficiente y evita bifurcaciones (“instant finality”).                                              |
| **Stellar**                      | Pública                       | **Protocolo de Consenso Stellar (SCP)** – Algoritmo basado en **Acuerdo Bizantino Federado**. Cada nodo confía en un conjunto (quorum slice) de nodos. Mediante votaciones federadas, la red logra consenso cuando se forma un quórum mayoritario.                                                               |
| **Cosmos (Cosmos Hub)**          | Pública                       | **Tendermint BFT (PoS)** – Cosmos Hub utiliza Tendermint Core, un algoritmo **BFT** clásico adaptado a PoS. Un conjunto de validadores apuesta ATOM y se turnan para proponer bloques, los cuales son validados con consenso Byzantine Fault Tolerant (finalidad inmediata en 2/3+ de votos).                        |
| **Tezos**                        | Pública                       | **Prueba de Participación Líquida (LPoS)** – Variante delegada de PoS utilizada por Tezos. Los validadores (“bakers”) son elegidos en proporción a su stake (propio + delegaciones) para crear bloques. Los usuarios pueden delegar XTZ libremente (“líquida”) sin ceder custodia.                                 |
| **Fantom**                       | Pública                       | **Lachesis (aBFT PoS)** – Algoritmo de consenso **asincrónico** BFT sin líder. Lachesis utiliza un **DAG** para registrar eventos y alcanzar consenso independientemente en cada nodo, logrando alta velocidad y finalización casi instantánea. Es una forma personalizada de PoS para validar transacciones.      |
| **NEAR Protocol**                | Pública                       | **Prueba de Participación (PoS) con fragmentación** – NEAR utiliza PoS (validadores con NEAR en stake) junto a una arquitectura **sharding** llamada *Nightshade*. Emplea un algoritmo de block production llamado **Doomslug** para lograr finalización rápida en cada ronda.                               |
| **Binance Smart Chain (BNB)**    | Pública                       | **Prueba de Autoridad Estacada (PoSA)** – Mecanismo híbrido de **PoA + DPoS** utilizado por BSC. Solo **21 validadores** (elegidos según stake en BNB) se turnan para producir bloques de 3 seg., lo que permite altas TPS y bajas comisiones. *(También llamada “Proof of Staked Authority” por Binance.)* |
| **Hedera Hashgraph**             | Pública (Gobernada por Consejo) | **Hashgraph (aBFT)** – Algoritmo basado en **gossip** sobre gossip y **votación virtual**. Los nodos difunden eventos aleatoriamente y usan los historiales de gossip para calcular virtualmente la votación mayoritaria, logrando consenso asíncrono bizantino muy rápido sin necesidad de minería.        |
| **TRON**                         | Pública                       | **Prueba de Participación Delegada (DPoS)** – 27 **Super Representantes** (validadores elegidos por la comunidad) producen bloques en turnos de 3 seg. y rotan cada 6 horas. Los holders de TRX votan para elegir estos representantes, manteniendo la seguridad de la red.                                      |
| **EOS**                          | Pública                       | **Prueba de Participación Delegada (DPoS)** – Utiliza DPoS con **21 Productores de Bloque** activos. Los titulares de EOS votan para elegir los productores, quienes se turnan para añadir bloques en rondas fijas, ofreciendo finalización rápida y alta capacidad, aunque con cierta centralización.                |
| **Hyperledger Fabric**           | Privada / Consorcio           | **Consenso por Ordering Service (Raft/CFT)** – Plataforma **permisionada** sin minería. Las transacciones son ordenadas por nodos *orderers*. Por defecto utiliza **Raft** (consenso Crash Fault Tolerant) para ordenar bloques de forma distribuida. *(Fabric soporta también algoritmos BFT en versiones recientes, como BFT-SMaRt.)* |

*Nota:* *“Permisionada” indica que los nodos validadores deben ser autorizados (típico en redes privadas o de consorcio), a diferencia de las redes públicas **permisionless** donde cualquiera puede participar como validador o minero.*

---

## **Otros Tipos de Algoritmos de Consenso en Blockchain**

## Proof of Authority (PoA)
Es un algoritmo que se basa en la reputación de validadores autorizados, quienes deben revelar su identidad y asumir responsabilidades, garantizando transparencia y seguridad.  
- **Ventajas**: alta eficiencia, bajos costos operativos, ecológico.  
- **Desventajas**: riesgos de privacidad, centralización, susceptibilidad a censura.  
- **Ideal para**: redes privadas que necesitan control y escalabilidad.

## Proof of History (PoH)
Diseñado por Solana, utiliza un registro temporal confiable que permite validar transacciones rápidamente gracias a una función hash en bucle.  
- **Ventajas**: velocidad (50.000+ transacciones por segundo), escalabilidad, descentralización, y eficiencia.  
- **Desventajas**: complejidad técnica y poca adopción fuera de Solana.  
- **Ideal para**: redes que buscan escalabilidad masiva y confirmación instantánea.

## Hybrid PoW/PoS
Combina Proof of Work (PoW) y Proof of Stake (PoS) para mejorar seguridad, sostenibilidad y flexibilidad.  
- **Ventajas**: resistente a ataques (como el del 51%), menor consumo energético, y adaptable.  
- **Desventajas**: implementación compleja.  
- **Ejemplos**: Decred y Hcash.

## Delayed Proof of Work (dPoW)
Permite que una blockchain más pequeña use la seguridad de una más grande (como Bitcoin). Combina PoW y PoS para crear una capa de respaldo en la blockchain principal.  
- **Ventajas**: mayor seguridad al respaldar transacciones en dos redes.  
- **Desventajas**: dependencia de la blockchain principal.

## Otros Algoritmos
- **XRP Ledger Consensus Protocol**: desarrollado por Ripple, enfocado en eficiencia y rapidez para pagos.  
- **Proof of Burn (PoB)**: usa la “quema” de monedas como mecanismo para validar transacciones.
