# Detective Ownership & Officer Borrowing

## 🕵️‍♂️👮 In den Gassen von Rust City

Detective Ownership bückte sich, die Gaze seiner eigenen Reflexion im stillgelegten Display des Trash-Collector-Bots. Er zog ein **Debug-Kabel** aus der Innentasche seines ledernen Overcoats - ein uraltes Ding, durchsetzt mit isolierten Kupferdrähten und geheimen Compiler-Flags. Seine Finger tasteten nach dem Diagnose-Port unter dem Roboter-Arm, als ein Schatten über ihn fiel.

„Ich würde die Finger vom Beweismaterial lassen, wenn ich du wäre.“

Die Stimme war tief, ruhig, mit dem unverkennbaren Unterton jemandes, der mehr Lifetime-Annotationen gelesen hat, als er Stunden Schlaf hatte. Own drehte sich langsam um.

Der Mann, der neben ihm stand, war mindestens einen Kopf größer. Seine Uniform war kein gewöhnliches Polizei-Gewand – sie bestand aus überlagerten Schichten Compiler-Warnungen in sanftem Gelb und Lifetime-Visualisierungen in pulsierendem Blau. Sein Finger am Abzug seiner .rs-Pulse-Riffle. Sein Namensschild, direkt über dem Herzen, leuchtete in strengen Monospace-Buchstaben:

```rust
**OFFICER BORROWING**
ID: &'static mut self
DEPT: BORROW CHECKER
```

„Sehen Sie das, Detective ?" Er hielt das Gerät so, dass beide das Display sehen konnten. Seine Stimme hatte den Ton eines Lehrers - aber eines, der schon Schlimmes gesehen hat.

<details>
<summary>📜 <strong>Trashbot Display : Beweismittel (Klicken zum Anzeigen)</strong></summary>

```rust
// ==============================================
// RUST CITY POLICE DEPT : BEWEISMITTEL #42-B
// SICHERSTELLUNG : AUSGEFALLENER TRASHBOT #4711218-DCAQ3
// ORT : INDUSTRIEGEBIET / GASSE 19
// ==============================================
//
// Modell : Trash-Collector v.3.4.2 "Müllo K04"
// Baujahr : 2034
// Status : steht still
// Letzte Worte : .. error .. panic ..

let mut protokoll = String::from("10:37 .. Mülltonnen Leerung.");
// Detective Ownership übernimmt die mutable Variable 'protokoll'.

let analyze = &protokoll;
// Jemand tarnt sich als lesende Referenz 'analyze' auf denselben Fall.

protokoll.push_str("10:38 .. gelbe Mülltonne geleert.");
// Detective Ownership will die Daten verändern. Er hat das Recht dazu.
protokoll.push_str("10:38 .. blaue Mülltonne geleert.");
protokoll.push_str("10:38 .. grüne Mülltonne geleert.");
protokoll.push_str("10:38 .. rote Mülltonne geleert.");

println!("{}", analyze);
// Officer Borrowing schreitet ein wegen Verstoßes gegen die Regel !
// Keine immutable Borrows während mutable Borrows aktiv !
// Zur gleichen Zeit existieren eine mutable Referenz (Ownership) UND eine immutable Referenz (Alias) !
// In Rust City ist das strengstens verboten !
// ==============================================

```

</details>

„Der Bürgermeister schätzt Ehrlichkeit am meisten, alle müssen das akzeptieren." begann Detective Ownership und fuhr fort : „Ich trage die Verantwortung. Man kann nicht **neutraler Beobachter** sein und gleichzeitig die **Fakten verändern**."

Officer Borrowing zog einen kleinen Notizblock heraus - echter Papier, keine Datei, kein Chip - und tippte nachdenklich darauf. „Absolut richtig was Sie sagen" ergänzte Officer Borrowing, stand auf und streckte die Wirbelsäule durch. „Die Referenz zeigt ins Leere." fuhr er fort und schnippte diesmal mit den Fingern. „Dangling reference. Klassisch. Fast schon langweilig .. hätte ein Profi diesen Code geschrieben, hätte er drei saubere Wege gehabt." Er hielt den Block zu Own. „Sehen Sie hier :"

<details>
<summary>📜 <strong>Die 3 Wege : Notizblock Logik (Klicken zum Anzeigen)</strong></summary>

```rust
// 1. CLONE (unsichtbar)
let analyze = protokoll.clone();   // Eigene Kopie, kein Borrow
protokoll.push_str(...);           // Kein Konflikt
```

```rust
// 2. REIHENFOLGE (einfach, aber auffällig)
protokoll.push_str(...);           // Erst mutieren
let analyze = &protokoll;          // Dann borgen ✅
```

```rust
// 3. SCOPE (präzise, aber verdächtig)
{
    let analyze = &protokoll;      // Borrow nur hier
    println!("{}", analyze);
} // Borrow stirbt hier
protokoll.push_str(...);           // Dann mutieren ✅
```

</details>

Auch Okto richtete sich wieder gerade und sah sich kurz um. Die Gasse war leer, der Morgennebel noch nicht ganz verflogen. Er dachte für sich leise : „Es muss ein Fehler sein, da stimmt etwas nicht."

„Amateur-Arbeit .." Officer Borrowing wischte sich eine imaginäre Staubflocke vom Ärmel. „Wissen Sie, wie ich einen Amateur erkenne, Detective ? **Ein Amateur bricht Regeln, weil er sie nicht versteht.** Hingegen ein Profi .." er machte eine kurze Pause, fast theatralisch .. „kann die Regeln **biegen**.

„**Regeln biegen** .." fragte sich nun Okto „.. was wohl damit gemeint ist ?"

**Fortsetzung folgt in Kapitel 3**, wo Okto das erste Mal auf Agentin Alias stösst.

---

*Rust City – Wo jeder Wert einen Besitzer hat, und jedes Ausleihen seinen Preis.*

---
