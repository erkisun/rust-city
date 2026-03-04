# Detective Ownership & Officer Borrowing

## 🕵️‍♂️👮 Die Begegnung

Own bückte sich, die Gaze seiner eigenen Reflexion im stillgelegten Display des Trash-Collector-Bots. Er zog ein **Debug-Kabel** aus der Innentasche seines ledernen Overcoats – ein Erbstück seiner Eltern, durchsetzt mit isolierten Kupferdrähten und geheimen Compiler-Flags. Seine Finger tasteten nach dem Diagnose-Port unter dem Roboter-Arm, als ein Schatten über ihn fiel.

„Ich würde die Finger vom Beweismaterial lassen, wenn ich du wäre.“

Die Stimme war tief, ruhig, mit dem unverkennbaren Unterton jemandes, der mehr Lifetime-Annotationen gelesen hat, als er Stunden Schlaf hatte. Own drehte sich langsam um.

Der Mann, der vor ihm stand, war mindestens einen Kopf größer. Seine Uniform war kein gewöhnliches Polizei-Gewand – sie bestand aus überlagerten Schichten Compiler-Warnungen in sanftem Gelb und Lifetime-Visualisierungen in pulsierendem Blau. Sein Namensschild, direkt über dem Herzen, leuchtete in strengen Monospace-Buchstaben:

```rust
**OFFICER BORROWING**
ID: &'static mut self
DEPT: BORROW CHECKER
```

„Detective Ownership, nehme ich an“, sagte der Officer, ohne die Hand auszustrecken. Seine Augen – die Farbe von kühlem Stack-Speicher – scannten Own, als würde er einen Codeblock auf Memory-Leaks prüfen. „Ihr Ruf eilt Ihnen voraus. Man sagt, Sie können eine **dangling reference** auf hundert Meter riechen.“

Own nickte langsam. „Und man sagt, Sie können einen illegalen **mutable borrow** hören, bevor es passiert.“

Nach einigen Millisekunden kniete sich Officer Borrowing neben den Roboter und zog ein kleines Gerät aus seiner Uniform – ein **Borrow-Checker**, der in Echtzeit anzeigte, wer gerade wo zugreift. „Sehen Sie hier, Detective ?“ Er zeigte auf das Display :

<details>
<summary>📜 <strong>Trashbot Display : Beweismittel (Klicken zum Anzeigen)</strong></summary>

```rust
// ==============================================
// RUST CITY POLICE DEPT : BEWEISMITTEL #42-B
// SICHERSTELLUNG : AUSGEFALLENER TRASHBOT #4711218-DCAQ3
// ==============================================
//
// Modell : Trash-Collector v.3.4.2 "Müllosaurus"
// Baujahr : 2034
// Status : steht still und zittert
// Letzte Worte : .. error .. panic ..
let mut protokoll = String::from("10:37 .. blaue Mülltonne geleert.");
let analyze = &protokoll;
protokoll.push_str("10:38 .. gelbe Mülltonne geleert.");

// Dieser Code darf hier nicht so verwendet werden
println("{}", analyze);
// ==============================================

```

„.. es geht weiter, hier, wir können direkt in das LOG reinschauen ..“ 

```rust
// RUST CITY POLICE DEPT: BORROW-CHECKER LOG
//
// 10:37:12 - protokoll mut (Mutable Borrow beginnt)
// 10:37:13 - analyze &protokoll (Immutable Borrow beginnt) ❌
// 10:37:13 - BORROW CHECKER: VERLETZUNG!
// Regel: Keine immutable Borrows während mutable Borrows aktiv!

```

</details>

„Verstehen Sie ?“ fragte der Officer. „Wenn jemand das Protokoll liest (&), können viele gleichzeitig lesen. Wenn jemand ins Protokoll schreibt (&mut), darf nur einer schreiben, und niemand darf dann gleichzeitig lesen.“

Own nickte langsam. „Und der Roboter .. ?“

„.. hat versucht, auf etwas zuzugreifen (analyze), das nicht existierte (None). Ein klassischer Fall von dangling reference. Das Protokoll wurde verändert, während es noch gelesen wurde. Der Roboter bekam Panik und blieb stehen.“

Own wie immer blitzschnell : „Jemand hat dem Roboter beigebracht, die Regeln zu .."

„Psst .. " unterbrach ihn Officer Borrowing abrupt. „.. leise .. " fuhr er fort „.. ja, hier wurde eine Regel gebrochen." und schaute schweigend zum Industrie-Crate, wo das **Heap District** liegt. 


🧩 Detective Challenge

„Hier ist Ihr erster Fall, Detective“, sagte Officer Borrowing, nachdem er sich wieder gefangen hatte, und zeigte auf einen weiteren Monitor. „Wir haben diesen Code bei einem anderen ausgefallenen Roboter gefunden. Können Sie den Fehler finden ?“

<details> 
<summary>🕵️ <strong>Detective Challenge: Finde den Bug ! (Klicken für den Code)</strong></summary>

```rust
// ============================================
// 
// Gefunden im Speicher eines ausgefallenen 
// ============================================

// Code ..

// ============================================
// FRAGEN AN DICH, DETECTIVE:
// ============================================
// 1. Warum wird dieser Code einen Compiler-Fehler verursachen ?
// 2. Welche Borrowing-Regel wird verletzt ?
// 3. Wie würdest du den Code reparieren ?
```

Deine Aufgabe, Detective-in-Ausbildung:

    - Überlege: Warum könnte data.push(6) problematisch sein ?
    - Welche Borrowing-Regel wird hier verletzt ?
    - Wie würdest du den Code sicher machen ?

</details>

Denk daran: In Rust City gelten strenge Regeln !

## 🔍 Detective Ownership und Officer Borrowing

**Fortsetzung folgt in Kapitel 3: Agent Alias' Angriff**, wo Own und Officer Borrowing das erste Mal auf Agent Alias stossen – und lernen, dass in Rust City manchmal sogar die Regeln gebrochen werden müssen, um sie zu schützen.

---

*Rust City – Wo jeder Wert einen Besitzer hat, und jedes Ausleihen seinen Preis.*

---

[← Vorheriges Kapitel : Willkommen in Rust City →](/app/blog/content/chapters/01-welcome-to-rust-city.md) | [Nächstes Kapitel : Agent Alias →](/app/blog/content/chapters/03-agent-alias.md)  
