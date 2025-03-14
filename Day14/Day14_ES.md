## **Bloques en Blockchain**

Vamos a ampliar el concepto de hash y llevarlo a lo que llamamos un bloque en blockchain.

## **¿Qué es un Bloque?**

Un bloque en blockchain organiza la información en tres partes principales claramente diferenciadas:

- **Número de Bloque:** Identificador único que indica la posición del bloque en la cadena.
- **Nonce:** Número arbitrario que se utiliza para ajustar el hash del bloque y cumplir ciertos requisitos.
- **Datos:** Información específica almacenada en el bloque (por ejemplo, transacciones).

La siguiente imagen ilustra cómo se estructura un bloque típico:

![Bloque Blockchain](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a20.png)

El hash del bloque incluye toda la información anterior. Por ejemplo, el hash de arriba comienza con cuatro ceros (`0000`). Este tipo de hash es relativamente raro y representa un bloque válido o "firmado".

## **¿Qué sucede al modificar los datos del bloque?**

Si modificamos cualquier información del bloque, el hash generado cambia completamente y probablemente ya no cumplirá con el requisito inicial (empezar con cuatro ceros). Por ejemplo:

![Bloque modificado](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a21.png)

Aquí el hash ya no comienza con cuatro ceros, indicando que el bloque ya no es válido. El fondo rojo indica visualmente que el bloque está inválido o no firmado.

Para solucionar esto, se ajusta el valor del Nonce hasta encontrar un hash que nuevamente cumpla con el requisito inicial (empezar con cuatro ceros). Por ejemplo:

![Bloque válido después de ajustar Nonce](https://raw.githubusercontent.com/AppsDevsLeon/Revista_blockchain/refs/heads/main/Day02/Images/a22.png)

En este caso, se encontró un Nonce que genera nuevamente un hash válido, haciendo que el bloque sea válido y "firmado" nuevamente.



## **Información almacenada en bloques según la red Blockchain (Tabla Comparativa)**

Cada red blockchain puede almacenar información ligeramente diferente en sus bloques, pero generalmente incluye elementos clave similares. Aquí tienes una tabla comparativa en español:

| Red Blockchain | Contenido del Bloque                                                |
|----------------|---------------------------------------------------------------------|
| **Bitcoin**    | Hash anterior, Timestamp, Nonce, Transacciones, Raíz Merkle         |
| **Ethereum**   | Hash anterior, Timestamp, Nonce, Transacciones, Raíz Merkle, Gas usado, Número del bloque |
| **Litecoin**   | Hash anterior, Timestamp, Nonce, Transacciones, Raíz Merkle         |
| **Solana**     | Hash anterior, Timestamp (Proof of History), Transacciones, Firmas, Validadores |
| **Cardano**    | Hash anterior, Timestamp, Nonce, Transacciones, Pruebas criptográficas, Raíz Merkle |
| **Polkadot**   | Hash anterior, Timestamp, Transacciones, Validaciones de Parachains, Pruebas de validez |

## **Componentes Clave del Bloque**

- **Hash Anterior:** Enlace criptográfico al bloque anterior.
- **Timestamp:** Marca de tiempo que indica cuándo se creó el bloque.
- **Nonce:** Número arbitrario que permite ajustar el hash del bloque.
- **Transacciones:** Registros de operaciones almacenados en el bloque.
- **Raíz Merkle:** Permite la rápida validación y verificación de integridad de las transacciones.
