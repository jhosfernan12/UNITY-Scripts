================================================================================
                           README - TypeWriter Script 

                        ██╗  ██╗██╗   ██╗██████╗  █████╗ 
                        ██║ ██╔╝╚██╗ ██╔╝██╔══██╗██╔══██╗
                        █████╔╝  ╚████╔╝ ██████╔╝███████║
                        ██╔═██╗   ╚██╔╝  ██╔══██╗██╔══██║
                        ██║  ██╗   ██║   ██║  ██║██║  ██║
                        ╚═╝  ╚═╝   ╚═╝   ╚═╝  ╚═╝╚═╝  ╚═╝                                         
================================================================================

Descripción:
Este script simula un efecto de "máquina de escribir" en un componente de texto 
de Unity. Permite que el texto aparezca letra por letra con un retraso entre 
cada carácter, con la opción de agregar un carácter antes de cada letra (como 
un cursor o prefijo), así como reproducir un sonido mientras se escribe. Además, 
incluye opciones para hacer que el texto parpadee una vez que termine de escribirse 
y si el texto debe persistir o no después del parpadeo.

Requiere:
- Unity 2020.3 o superior
- Un GameObject con un componente Text o TMP_Text

--------------------------------------------------------------------------------
Configuración en Unity:
--------------------------------------------------------------------------------

1. Crea un GameObject en la escena y adjunta el script `TypeWriter` a él.

2. Asigna un componente `Text` o `TMP_Text` al campo correspondiente:
   - `text`: Asigna un componente `Text` de Unity.
   - `tmpProText`: Asigna un componente `TMP_Text` de TextMesh Pro.

3. Ajusta las propiedades del script según sea necesario:

   - **Configuración de texto:**
     - `delayBeforeStart`: Tiempo en segundos antes de que comience el efecto de tipeo.
     - `timeBtwChars`: Tiempo entre la aparición de cada carácter (en segundos).
     - `leadingChar`: Carácter (o cadena) que se agrega antes de cada letra (por ejemplo, un cursor o símbolo).
     - `leadingCharBeforeDelay`: Si el `leadingChar` debe aparecer antes de que comience el tipeo.
     - `startOnEnable`: Si el efecto de tipeo debe comenzar cuando el script se habilite.

   - **Configuración de sonido:**
     - `audioSource`: Fuente de audio que se usará para reproducir el sonido de tipeo.
     - `typingSound`: Clip de audio para el sonido de tipeo.

   - **Configuración de parpadeo:**
     - `blinkAfterTyping`: Si el texto debe parpadear después de que termine el tipeo.
     - `blinkCount`: Número de veces que parpadeará el texto.
     - `blinkDuration`: Duración de cada parpadeo en segundos.

   - **Configuración de persistencia del texto:**
     - `persistAfterBlink`: Si el texto debe persistir después de parpadear.

   - **Configuración de activación:**
     - `enableActivationWithTab`: Si se debe reiniciar el tipo de texto al presionar la tecla TAB una vez que el texto se haya terminado de escribir.

4. **Inicio automático:**
   Si deseas que el efecto de tipeo comience automáticamente cuando se habilite el script, marca `startOnEnable`.

--------------------------------------------------------------------------------
Uso:
--------------------------------------------------------------------------------

- Al ejecutar la escena, el script comenzará a escribir el texto en el componente asignado.
- Si `startOnEnable` está marcado, el efecto de tipeo comenzará cuando el script se habilite.
- Si `enableActivationWithTab` está habilitado, puedes presionar la tecla TAB para reiniciar el efecto de tipeo una vez que el texto haya terminado de escribirse.
- El texto aparecerá letra por letra con un retraso, y puede incluir un "leadingChar" antes de cada letra.
- Una vez terminado el efecto de tipeo, el texto puede parpadear según la configuración de `blinkAfterTyping` y `blinkCount`.
- Después de parpadear, el texto puede eliminarse o persistir dependiendo del valor de `persistAfterBlink`.

--------------------------------------------------------------------------------
Notas adicionales:
--------------------------------------------------------------------------------

- El script funciona tanto con el componente `Text` de Unity como con `TMP_Text` de TextMesh Pro.
- Si se usan ambos componentes (Text y TMP_Text), solo se actualizará el que tenga texto asignado.
- El sonido de tipeo solo se reproducirá si se asigna una `AudioSource` y un `AudioClip` en los campos correspondientes.

--------------------------------------------------------------------------------
Licencia:
Este script es de uso libre, puedes usarlo, modificarlo y distribuirlo. 
Sin embargo, te agradecería si me mencionas " KyraEgon "si usas este script en tus proyectos.

================================================================================
