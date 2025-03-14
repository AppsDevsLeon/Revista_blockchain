
##  **Redes Distribuidas Peer-to-Peer (P2P)**

Una red distribuida peer-to-peer está compuesta por múltiples ordenadores interconectados, cada uno manteniendo una copia exacta del libro mayor (registro de todas las transacciones).

La información se replica automáticamente a través de todos los nodos, permitiendo que cualquier modificación maliciosa o accidental pueda ser detectada y corregida rápidamente por la mayoría de los nodos.

![red](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day16/Images/2022-09-30_16-44-49-2f01f6aa2670c613df15c0aadae24c44.webp)

##  **¿Qué es un Nodo?**

Un nodo en una red blockchain es un ordenador individual que participa activamente en la red. Cada nodo posee una copia completa del libro mayor, lo que le permite verificar y auditar de manera independiente todas las transacciones y detectar cualquier irregularidad.

![node](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day16/Images/r2.png)


# Nodos en Blockchain

Una red blockchain mantiene la seguridad, integridad y rendimiento mediante varios tipos de nodos, cada uno desempeñando funciones específicas. Este documento detalla los tipos de nodos e incluye una comparación de las redes blockchain según el uso de estos nodos.

## **Tipos de Nodos**

### **Nodos Completos (Full Nodes)**
Los nodos completos almacenan el libro mayor blockchain íntegro. Validan de forma independiente todos los bloques y transacciones, aplicando estrictamente las reglas de la red, lo que aumenta la descentralización y seguridad.

### **Nodos de Minería**
Los nodos de minería tienen las siguientes responsabilidades:
- Agrupar nuevas transacciones en bloques.
- Verificar y validar dichas transacciones.
- Proponer nuevos bloques a la red.

### **Nodos Regulares**
Los nodos regulares almacenan una copia completa o parcial del libro mayor y realizan validaciones básicas de transacciones. Contribuyen a la salud general de la red.

### **Nodos Ligeros (Light Nodes)**
Los nodos ligeros almacenan únicamente los datos esenciales de la blockchain para verificar rápidamente transacciones. Dependen de los nodos completos para obtener la información blockchain completa.

### **Nodos Archivadores (Archival Nodes)**
Los nodos archivadores almacenan toda la historia de la blockchain, facilitando análisis detallados y auditorías.

## **Tabla Comparativa de Nodos**

| Tipo de Nodo       | Copia del Libro Mayor | Rol de Validación       | Capacidad de Minado | Requisitos de Almacenamiento |
|--------------------|-----------------------|-------------------------|---------------------|------------------------------|
| Nodo Completo      | Completa              | Validación completa     | No                  | Alta                         |
| Nodo de Minería    | Completa              | Validación y creación   | Sí                  | Alta                         |
| Nodo Regular       | Parcial/Completa      | Validación básica       | No                  | Moderada                     |
| Nodo Ligero        | Parcial               | Validación limitada     | No                  | Baja                         |
| Nodo Archivador    | Historia Completa     | Validación completa     | No                  | Muy alta                     |

## **Redes Blockchain y Tipos de Nodos Utilizados**

| Red Blockchain | Nodos Completos | Nodos de Minería | Nodos Ligeros | Nodos Archivadores |
|----------------|-----------------|------------------|---------------|--------------------|
| Bitcoin        | ✔️               | ✔️                | ✔️            | ✔️                 |
| Ethereum       | ✔️               | ✔️                | ✔️            | ✔️                 |
| Litecoin       | ✔️               | ✔️                | ✔️            | ❌                 |
| Solana         | ✔️               | ❌ (validadores)  | ✔️(validadores)| ❌                 |
| Cardano        | ✔️               | ❌ (validadores)  | ✔️(validadores)| ✔️                 |
| Polkadot       | ✔️               | ❌ (validadores)  | ✔️(validadores)| ✔️                 |

---

## **Beneficios de la Diversidad de Nodos**

- **Seguridad y Resiliencia:** La diversidad de tipos de nodos mejora la robustez general de la red.
- **Transparencia:** La validación a través de múltiples nodos asegura la precisión e integridad de los datos blockchain.
- **Descentralización:** Evita que una sola entidad pueda controlar significativamente la red blockchain.



## **Beneficios de las Redes Distribuidas**

- **Resiliencia**: Al mantener copias idénticas en múltiples ordenadores, cualquier dato corrupto puede ser fácilmente detectado y restaurado.
- **Transparencia**: Cada transacción es verificable y auditable por cualquier nodo.
- **Seguridad**: La modificación maliciosa requiere el control simultáneo de la mayoría de los nodos, lo cual es extremadamente difícil.

---

## **Descentralización**

Una red blockchain utiliza un modelo descentralizado, almacenando datos en múltiples nodos distribuidos. Esto difiere significativamente del almacenamiento tradicional centralizado, donde toda la información reside en un solo punto de control.

---

## **Problemas con la Centralización**

Algunos problemas significativos de los sistemas centralizados son:

- **Violaciones de seguridad**: Exponen grandes cantidades de datos en caso de ataques.
- **Censura**: Una autoridad centralizada puede censurar y cerrar contenidos o servicios.
- **Dependencia**: Problemas técnicos en una autoridad central afectan a todos los usuarios (por ejemplo, caída de AWS).

---

## **Beneficios de la Descentralización**

Por otro lado, la descentralización ofrece:

- **Resistencia a la censura**: No existe una autoridad única capaz de restringir información.
- **Alta disponibilidad**: Sin puntos centrales de fallo, la red permanece operativa incluso si algunos nodos fallan.
- **Seguridad reforzada**: Difícil de manipular, ya que requeriría control simultáneo sobre una mayoría de los nodos.

---

## **Seguridad en Redes P2P**

La seguridad en las redes peer-to-peer blockchain se logra mediante:

- **Vínculos criptográficos**: Cada bloque está conectado criptográficamente con el anterior, dificultando cualquier modificación.
- **Consenso distribuido**: Modificar la red requeriría alterar simultáneamente más de la mitad de los nodos, una tarea prácticamente imposible.
