================================================================================
                           README - TypeWriter Script 

                        ██╗  ██╗██╗   ██╗██████╗  █████╗ 
                        ██║ ██╔╝╚██╗ ██╔╝██╔══██╗██╔══██╗
                        █████╔╝  ╚████╔╝ ██████╔╝███████║
                        ██╔═██╗   ╚██╔╝  ██╔══██╗██╔══██║
                        ██║  ██╗   ██║   ██║  ██║██║  ██║
                        ╚═╝  ╚═╝   ╚═╝   ╚═╝  ╚═╝╚═╝  ╚═╝
                                                     
================================================================================

Description:
This script simulates a "typewriter" effect on a Unity text component. It allows 
text to appear character by character with a delay between each character, 
with the option to add a leading character before each letter (like a cursor or 
prefix), as well as play a sound while typing. Additionally, it includes options 
to make the text blink once typing is finished, and whether to persist the text 
or not after blinking.

Requires:
- Unity 2020.3 or later
- A GameObject with a Text or TMP_Text component

--------------------------------------------------------------------------------
Setup in Unity:
--------------------------------------------------------------------------------

1. Create a GameObject in the scene and attach the `TypeWriter` script to it.

2. Assign a `Text` or `TMP_Text` component to the corresponding field:
   - `text`: Assign a Unity `Text` component.
   - `tmpProText`: Assign a `TMP_Text` component from TextMesh Pro.

3. Adjust the script properties as needed:

   - **Text Settings:**
     - `delayBeforeStart`: Time in seconds before the typing effect starts.
     - `timeBtwChars`: Time between the appearance of each character (in seconds).
     - `leadingChar`: Character (or string) added before each letter (e.g., a cursor or symbol).
     - `leadingCharBeforeDelay`: If the `leadingChar` should appear before typing starts.
     - `startOnEnable`: If the typing effect should start when the script is enabled.

   - **Sound Settings:**
     - `audioSource`: Audio source used to play the typing sound.
     - `typingSound`: Audio clip for the typing sound.

   - **Blink Settings:**
     - `blinkAfterTyping`: If the text should blink after typing finishes.
     - `blinkCount`: Number of times the text will blink.
     - `blinkDuration`: Duration of each blink in seconds.

   - **Text Persistence Settings:**
     - `persistAfterBlink`: If the text should persist after blinking.

   - **Activation Settings:**
     - `enableActivationWithTab`: If the typing effect should restart by pressing the TAB key once the text is finished.

4. **Automatic Start:**
   If you want the typing effect to start automatically when the script is enabled, check `startOnEnable`.

--------------------------------------------------------------------------------
Usage:
--------------------------------------------------------------------------------

- When running the scene, the script will begin typing the text in the assigned component.
- If `startOnEnable` is checked, the typing effect will begin when the script is enabled.
- If `enableActivationWithTab` is enabled, you can press the TAB key to restart the typing effect once the text has finished typing.
- The text will appear one character at a time with a delay, and it can include a "leadingChar" before each letter.
- After the typing effect finishes, the text can blink based on the `blinkAfterTyping` and `blinkCount` settings.
- After blinking, the text can either be cleared or persist depending on the value of `persistAfterBlink`.

--------------------------------------------------------------------------------
Additional Notes:
--------------------------------------------------------------------------------

- The script works with both Unity's `Text` component and `TMP_Text` from TextMesh Pro.
- If both components (Text and TMP_Text) are used, only the one with text assigned will be updated.
- Typing sound will only play if an `AudioSource` and `AudioClip` are assigned in the respective fields.

--------------------------------------------------------------------------------
License:
This code is provided "as-is". No warranty of any kind is provided.

================================================================================
