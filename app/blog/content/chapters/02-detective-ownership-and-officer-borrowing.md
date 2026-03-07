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

Nach einigen Millisekunden kniete sich Officer Borrowing neben den Roboter. 
Kein Zögern, keine Eile – die Bewegung eines Mannes, der schon tausend 
solcher Szenen gesehen hat. Er zog ein kleines Gerät aus seiner Uniform: 
ein **Borrow-Checker**, der in Echtzeit anzeigte, wer gerade wo zugreift. 
Die Anzeige flackerte nervös.

„Sehen Sie das, Detective ?" Er hielt das Gerät so, dass beide das 
Display sehen konnten. Seine Stimme hatte den Ton eines Lehrers – 
aber eines, der schon Leichen gesehen hat.

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
let mut protokoll = String::from("10:37 .. Mülltonnen Leerung.");
// Dieser Code darf hier nicht so verwendet werden (Teil 1/2)
let analyze = &protokoll;
protokoll.push_str("10:38 .. gelbe Mülltonne geleert.");
protokoll.push_str("10:38 .. blaue Mülltonne geleert.");
protokoll.push_str("10:38 .. grüne Mülltonne geleert.");
protokoll.push_str("10:38 .. rote Mülltonne geleert.");

// Dieser Code darf hier nicht so verwendet werden (Teil 2/2)
println("{}", analyze);
// ==============================================

```

„.. es geht weiter .. hier, wir können direkt ins LOG reinschauen ..“ 

```rust
// RUST CITY POLICE DEPT: BORROW-CHECKER LOG
//
// 10:37:12 - protokoll mut (Mutable Borrow beginnt)
// 10:37:13 - analyze &protokoll (Immutable Borrow beginnt) ❌
// 10:37:13 - BORROW CHECKER: VERLETZUNG!
// Regel: Keine immutable Borrows während mutable Borrows aktiv!

```

</details>

Own runzelte die Stirn. „Lesezugriff während eines Schreibvorgangs."

„Bingo." Officer Borrowing stand auf und streckte die Wirbelsäule durch, fast gelangweilt. Die Referenz zeigte ins Leere." Er schnippte mit den Fingern. „Dangling reference. Klassisch. Fast schon .. langweilig." 
„Regel Nummer Eins in Rust-City : Entweder lesen alle - oder einer schreibt. Nicht beides. **Niemals beides.**" Er tippte auf sein Namensschild. „Das steht nicht zufällig auf meiner Uniform."

Own wie immer blitzschnell : „Jemand hat aber eine Regel gebrochen .."

Borrowing antwortete nicht sofort. Er zog einen kleinen Notizblock heraus - echter Papier, keine Datei, kein Chip - und tippte nachdenklich darauf.

„Hätte ein Profi diesen Code geschrieben, hätte er drei saubere Wege gehabt." Er hielt den Block hoch :

<details>
<summary>📜 <strong>Korrekter Ablauf : Logikmittel (Klicken zum Anzeigen)</strong></summary>

```rust
// 1. CLONE (unsichtbar)
let analyze = protokoll.clone();  // Eigene Kopie, kein Borrow
protokoll.push_str(...);          // Kein Konflikt
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

Own stand auf und sah sich um. Die Gasse war leer, der Morgennebel noch nicht ganz verflogen. „Also ein Fehler. Amateur-Arbeit."

„Amateur-Arbeit." Officer Borrowing wischte sich eine imaginäre Staubflocke vom Ärmel. „Wissen Sie, wie ich einen Amateur erkenne, Detective ? **Ein Amateur bricht Regeln, weil er sie nicht versteht.** Ein Profi .." er machte eine kurze Pause, 
fast theatralisch .. „könnte die Regeln brechen, weil er sie besser versteht als alle anderen."

Own drehte sich zu ihm. „Sie meinen jemanden Bestimmtes."

„Jede dieser Möglichkeiten verrät etwas über die Person, die sie gewählt hätte."

Own wartete.

Borrowing schaute zum Industrie-Crate hinüber. 
Irgendwo dort, hinter Stahlwänden und Compiler-Schildern, 
lag das **Heap District** - unaufgeräumt, lebendig, 
gefährlich für jeden, der die Regeln nicht kannte.

„Drei Wege", sagte er leise. „Drei Wege – und *sie* 
hätte den elegantesten gewählt. Den einen, den man erst 
versteht, wenn man schon zweimal hinsieht."

„*Sie* ?" fragte Own.

Borrowing wandte sich ab, die Hände hinter dem Rücken, 
und ging langsam in Richtung Heap District.

„**Agent Alias.**" Der Name fiel wie ein einzelner 
Token in einen leeren Puffer. „Falls wir Glück haben, 
taucht sie nie auf." Er warf Own einen Blick über 
die Schulter zu. „Aber ich glaube nicht an Glück. 
Ich glaube an **Lifetimes**. Und ihre ist noch lange nicht vorbei."


**Fortsetzung folgt in Kapitel 3**, wo Own und Officer Borrowing das erste Mal auf Agent Alias stossen – und lernen, dass in Rust City manchmal sogar die Regeln gebrochen werden müssen, um sie zu schützen.

---

*Rust City – Wo jeder Wert einen Besitzer hat, und jedes Ausleihen seinen Preis.*

---

[← Vorheriges Kapitel : Willkommen in Rust City →](/app/blog/content/chapters/01-welcome-to-rust-city.md) | [Nächstes Kapitel : Agent Alias →](/app/blog/content/chapters/03-agent-alias.md)  
