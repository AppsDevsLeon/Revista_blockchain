## **Hash, Hashing y SHA-256**

Antes de comenzar, debemos entender qué es exactamente un hash y, más específicamente, el hash SHA-256. Un hash se asemeja a una secuencia aparentemente aleatoria de números y letras, actuando como una huella digital única de datos digitales específicos.

## ¿Qué es SHA-256?

SHA-256 (Secure Hash Algorithm 256-bit) es una función criptográfica que genera una cadena única y fija de 256 bits (32 bytes), generalmente representada en hexadecimal con 64 caracteres.

Antes de continuar, echemos un vistazo más profundo al hash SHA256. Un hash luce como un montón de números aleatorios y funciona como una huella digital de información digital específica.

Por ejemplo, el siguiente hash inicia con `e3b0`, y es la representación del hash SHA-256 cuando no hay ningún dato (un valor vacío):

![Metamask](https://raw.githubusercontent.com/spo0ds/Journey-to-become-a-Blockchain-Engineer/refs/heads/main/Day02/Images/a18.png)

Si escribimos cualquier texto en una caja, como por ejemplo la palabra `blockchain`, el hash generado cambia completamente:

![Metamask](https://raw.githubusercontent.com/spo0ds/Journey-to-become-a-Blockchain-Engineer/refs/heads/main/Day02/Images/a19.png)

Este hash, que inicia con `5318`, es el resultado único y constante del texto "blockchain" escrito completamente en minúsculas. Si borras el texto y vuelves a escribir exactamente lo mismo, obtendrás siempre el mismo hash. Por ello decimos que es la **"huella digital"** del texto ingresado.

Podrías escribir toneladas y toneladas de texto y siempre obtendrás un hash del mismo tamaño. Ya sea una pequeña cantidad de información, ninguna información o una biblioteca completa del Congreso, siempre obtendrás un hash con la longitud mostrada anteriormente. Nunca podrás adivinar cuál será el hash. Siempre tendrás el mismo hash sin importar cuántas veces ingreses la misma información.

## Propiedades Importantes del SHA-256

- **Longitud fija:** Independientemente del tamaño de entrada (desde un solo carácter hasta toda una biblioteca digital), la longitud del hash siempre será de 256 bits, representados como 64 caracteres hexadecimales.

- **Determinista:** La misma entrada siempre producirá el mismo hash.

- **Unidireccional:** No es posible revertir un hash para recuperar los datos originales.

- **Resistente a colisiones:** Es prácticamente imposible encontrar dos entradas diferentes que generen el mismo hash.

## Efecto Avalancha

El SHA-256 tiene una característica clave llamada **efecto avalancha**, que implica que si cambias una mínima porción de los datos originales (incluso un solo bit), el hash generado será completamente distinto e impredecible. Esto es crucial para asegurar la integridad y seguridad en aplicaciones criptográficas.

Por ejemplo:
- Texto original: `blockchain`
  - Hash: `5318...`
- Texto modificado: `blockchaiN` (solo la última letra en mayúscula)
  - Hash completamente diferente al original.

Esta propiedad hace imposible alterar datos sin cambiar radicalmente el resultado del hash, garantizando que cualquier modificación, por mínima que sea, sea fácilmente detectable.

## Aplicaciones del SHA-256

SHA-256 es ampliamente usado en:

- Blockchain (Bitcoin, Ethereum, etc.)
- Verificación de integridad de archivos
- Almacenamiento seguro de contraseñas
- Firmas digitales

La importancia de SHA-256 radica en la combinación de rapidez y seguridad que ofrece en un sinfín de aplicaciones tecnológicas actuales.

