================================================================================
                           README - TypeWriter Script
================================================================================

Beschreibung:
Dieses Skript simuliert einen "Schreibmaschinen"-Effekt auf einem Unity-Textkomponent. 
Es lässt Text Zeichen für Zeichen erscheinen, mit einer Verzögerung zwischen jedem 
Zeichen. Es gibt auch die Möglichkeit, ein führendes Zeichen vor jedem Buchstaben hinzuzufügen 
(z.B. einen Cursor oder ein Präfix) sowie einen Sound beim Tippen abzuspielen. 
Zusätzlich gibt es Optionen, den Text nach dem Tippen blinken zu lassen und ob der Text 
nach dem Blinken beibehalten werden soll oder nicht.

Voraussetzungen:
- Unity 2020.3 oder höher
- Ein GameObject mit einem Text- oder TMP_Text-Komponenten

--------------------------------------------------------------------------------
Einrichtung in Unity:
--------------------------------------------------------------------------------

1. Erstelle ein GameObject in der Szene und füge das `TypeWriter`-Skript hinzu.

2. Weisen Sie das `Text`- oder `TMP_Text`-Komponente dem entsprechenden Feld zu:
   - `text`: Weisen Sie eine Unity `Text`-Komponente zu.
   - `tmpProText`: Weisen Sie eine `TMP_Text`-Komponente von TextMesh Pro zu.

3. Passen Sie die Skript-Eigenschaften nach Bedarf an:

   - **Texteinstellungen:**
     - `delayBeforeStart`: Zeit in Sekunden, bevor der Tipp-Effekt beginnt.
     - `timeBtwChars`: Zeit zwischen dem Erscheinen jedes Zeichens (in Sekunden).
     - `leadingChar`: Zeichen (oder Zeichenfolge), das vor jedem Buchstaben hinzugefügt wird (z.B. ein Cursor oder Symbol).
     - `leadingCharBeforeDelay`: Ob das führende Zeichen vor dem Beginn des Tippens erscheinen soll.
     - `startOnEnable`: Wenn der Tipp-Effekt beim Aktivieren des Skripts beginnen soll.

   - **Sound-Einstellungen:**
     - `audioSource`: Die Audioquelle, die zum Abspielen des Tippgeräuschs verwendet wird.
     - `typingSound`: Audioclip für das Tippgeräusch.

   - **Blinkeinstellungen:**
     - `blinkAfterTyping`: Ob der Text nach dem Tippen blinken soll.
     - `blinkCount`: Anzahl der Blinkvorgänge.
     - `blinkDuration`: Dauer jedes Blinkens in Sekunden.

   - **Text-Persistenzeinstellungen:**
     - `persistAfterBlink`: Wenn der Text nach dem Blinken beibehalten werden soll.

   - **Aktivierungseinstellungen:**
     - `enableActivationWithTab`: Wenn der Tipp-Effekt mit der TAB-Taste nach Abschluss des Textes neu gestartet werden soll.

4. **Automatischer Start:**
   Wenn der Tipp-Effekt beim Aktivieren des Skripts automatisch beginnen soll, aktivieren Sie `startOnEnable`.

--------------------------------------------------------------------------------
Verwendung:
--------------------------------------------------------------------------------

- Beim Starten der Szene wird das Skript beginnen, den Text im zugewiesenen Komponent zu tippen.
- Wenn `startOnEnable` aktiviert ist, beginnt der Tipp-Effekt beim Aktivieren des Skripts.
- Wenn `enableActivationWithTab` aktiviert ist, können Sie die TAB-Taste drücken, um den Tipp-Effekt neu zu starten, sobald der Text fertig ist.
- Der Text erscheint Zeichen für Zeichen mit einer Verzögerung und kann ein "leadingChar" vor jedem Buchstaben enthalten.
- Nachdem der Tipp-Effekt abgeschlossen ist, kann der Text basierend auf den Einstellungen `blinkAfterTyping` und `blinkCount` blinken.
- Nach dem Blinken kann der Text entweder gelöscht oder beibehalten werden, je nachdem, was in `persistAfterBlink` eingestellt ist.

--------------------------------------------------------------------------------
Lizenz:
--------------------------------------------------------------------------------

Dieses Skript ist frei zur Nutzung, Modifikation und Verteilung. 
Ich würde es jedoch schätzen, wenn du "KyraEgon" erwähnst, wenn du dieses Skript in deinen Projekten verwendest.


================================================================================
