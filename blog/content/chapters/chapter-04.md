🇩🇪 [Deutsch](#de) · 🇬🇧 [English](#en)

---

<a name="de"></a>
### 🇩🇪 Deutsch

---

## 📗 Kapitel 4 — Max Mutation

Max kam am nächsten Morgen zurück.

Okto sah ihn von weitem — die zu grosse Jacke, die bunten unordentlichen Haare. Er kam durch die Gasse 19, diesmal ohne zu zögern. Er wusste wo er hinmusste.

„Passbüro", sagte er zu Okto. Kein Guten Morgen. Kein Zögern. „Ich muss einen neuen Ausweis ausstellen lassen."

Okto schaute ihn an. Dann schob er seinen Behälter zur Seite.

Er kam mit.

---

## 🏙️ Das Passbüro

Das Passbüro lag am Rand des Stack Districts — ordentlich, ruhig, mit langen Gängen und nummerierten Schaltern. Genau das Gegenteil vom Heap District.

Am Eingang stand ein Schild:

```
PASSBÜRO — RUST CITY
Ausweis ausstellen : nur der Inhaber
Ausweis lesen      : jeder
Ausweis ändern     : nur der Inhaber — exklusiv
```

Max las das Schild. Dann nickte er — einmal, kurz, als würde er etwas bestätigen das er bereits wusste.

Sie traten ein.

---

## 🔐 Das Ausstellungs-Terminal

Der Beamte am Schalter schaute kurz auf Max. Dann auf Okto. Dann wieder auf Max.

„Neuer Ausweis ?"

„Ja."

„Terminal 3. Nur Sie. Niemand sonst darf während der Ausstellung in den Bereich."

Max nickte. Er ging zu Terminal 3.

Okto wollte folgen — aber Officer Borrowing trat um die Ecke. Als hätte er gewusst dass er hier gebraucht wurde. Er schaute Okto an. Ruhig. Ohne Theatralik — für einmal.

„Warten", sagte er.

Dann zog er ein Absperrband aus seiner Uniform — leuchtend gelb, mit der Aufschrift `&mut — EXKLUSIVER ZUGRIFF` — und spannte es um Terminal 3. Niemand konnte hineinschauen. Niemand konnte eingreifen. Nur Max.

„Jetzt", sagte Borrowing zu Max. „Nur du. Nur dein Ausweis. Nur du bist verantwortlich."

Max schaute auf das Terminal. Auf seine Hände. Dann tippte er.

```rust
// Mein Ausweis — gehört mir.
// Nur ich darf ihn ausstellen. Nur ich bin verantwortlich.
let mut mein_ausweis = String::from("Einwohner: Max Mutation — Ausweis: ABGELAUFEN");

// Borrowing sperrt ab — niemand sonst schaut rein.
let ausstellen = &mut mein_ausweis;
ausstellen.push_str(" -> GÜLTIG");
// Ich greife ein. Alleine. Vollständig verantwortlich.
```

Das Terminal piepte einmal. Kurz. Dann leuchtete es grün.

Officer Borrowing nahm das Absperrband ab. Faltete es sorgfältig zusammen. Steckte es zurück.

„Fertig", sagte er.

---

## 🏙️ Okto versteht

Okto hatte draussen gewartet. Er hatte nicht gesehen was Max getippt hatte. Er hatte nicht gesehen was auf dem Terminal stand.

Aber er hatte gesehen wie Officer Borrowing das Absperrband gespannt hatte. Wie niemand hineinschauen durfte. Wie Max alleine drinstand — nur er, sein Ausweis, seine Verantwortung.

*Das ist `&mut T`*, dachte Okto.

Nicht der Fehler den Max damals gemacht hatte. Nicht das Chaos im TC-0003. Das hier.

Eingreifen — aber nur ins Eigene. Alleine. Mit einer Sperre die andere draussen hält. Nicht weil sie nicht dürfen. Sondern weil Verantwortung nicht geteilt werden kann wenn jemand schreibt.

Alias hatte gezeigt: viele Augen brechen nichts.
Max hatte gezeigt: eine Hand schreibt — und trägt es alleine.

Beide Seiten. Dasselbe Gesetz.

Officer Borrowing trat neben Okto. Er schaute nicht zu ihm. Er schaute auf Max der aus dem Terminal-Bereich trat, den neuen Ausweis in der Hand.

„Verstanden ?" fragte Borrowing.

Okto dachte nach.

„Schau so viel du willst", sagte er langsam. „Solange du nicht eingreifst, bleibt alles sicher." Er pausierte. „Und wenn du eingreifst — nur ins Deine. Dann aber vollständig."

Officer Borrowing sagte nichts.

Aber er nickte.

---

## 🏙️ Das Tor

Auf dem Heimweg — Behälter vor sich, Gasse 7-C, der Morgennebel der sich langsam auflöste — blieb Okto an der Stelle stehen wo das Tor sichtbar wurde.

Drei Sätze. In Stein gemeisselt.

Er kannte sie. Er hatte sie immer gekannt.

Heute las er den ersten.

*Was du besitzt, das pflege.*

Nicht: was du hast, behalte es.
Nicht: was dir gehört, verteidige es.

Pflege es. Kümmere dich. Trag Verantwortung — solange es dir gehört, vollständig.

Max hatte in ein Register geschrieben das ihm nicht gehörte. Nicht aus Bosheit. Aus Ungeduld. Er hatte nicht gefragt: *gehört mir das ?*

Diese eine fehlende Frage hatte den TC-0003 zum Absturz gebracht.

*Was du besitzt, das pflege.*

Das war kein Rust-Konzept.

Das war älter.

Okto schob weiter. Aber etwas in ihm — ruhig, fast unmerklich — war nicht mehr ganz dasselbe.

---

### 📌 Lebensregel #4

> **Greif nur ins Deine. Dann aber vollständig.**

---

### 🦾 Arm #1 — Vertieft

*Sammeln bedeutet auch : pflegen was man hat.*

### 🦾 Arm #2 — Aktiv

*Beobachten. Zwei Richtungen gleichzeitig.*

### 🦾 Arm #3 — Kribbelt

*Stärker. Wärmer.*

Okto hat zwei Arme. Arm #1 ist nicht mehr nur Sammeln.
Er weiss jetzt: besitzen bedeutet Verantwortung tragen.
Nicht für immer. Aber solange es dir gehört — vollständig.

---

### 📎 Akte: Mutability & `&mut T`

*Gefunden in der Bibliothek des Verwaltungsturms. Abschnitt: Mutation.*

```rust
fn main() {
    // Mein Ausweis — gehört mir.
    // Nur ich darf ihn ändern. Alleine. Vollständig verantwortlich.
    let mut mein_ausweis = String::from("Max Mutation — Ausweis: ABGELAUFEN");

    // Borrowing sperrt ab — niemand sonst schaut rein während ich schreibe.
    let ausstellen = &mut mein_ausweis;
    ausstellen.push_str(" → GÜLTIG");

    // Wenn ich fertig bin — darf jeder wieder schauen.
    println!("{}", mein_ausweis); // ✅ — mein Eigenes, meine Verantwortung

    // &T:    schauen darf jeder — solange niemand eingreift.
    // &mut T: eingreifen darf nur einer — aber nur ins Eigene.
}
```

*Notiz am Rand, handgeschrieben:*
`// &mut T bedeutet nicht: ich darf alles. Es bedeutet: ich greife ins Meine — und trage es vollständig.`

---

*Ende Kapitel 4.*

*Max trägt seinen neuen Ausweis.*
*Der TC-0003 steht noch immer in Gasse 19 — aber das ist eine andere Geschichte.*
*Okto hat zwei Arme — und weiss was der erste Satz am Tor bedeutet.*
*Noch nicht alles. Aber den ersten Satz.*

---

---

<a name="en"></a>
## 🇬🇧 English

---

## 📗 Chapter 4 — Max Mutation

Max came back the next morning.

Okto saw him from a distance — the oversized jacket, the colourful untidy hair. He came through Alley 19, this time without hesitating. He knew where he needed to go.

"Passport office," he said to Okto. No good morning. No hesitation. "I need to get a new ID issued."

Okto looked at him. Then pushed his container to the side.

He came along.

---

## 🏙️ The Passport Office

The passport office was at the edge of the Stack District — neat, quiet, with long corridors and numbered counters. The exact opposite of the Heap District.

At the entrance stood a sign:

```
PASSPORT OFFICE — RUST CITY
Issue ID    : owner only
Read ID     : anyone
Change ID   : owner only — exclusive
```

Max read the sign. Then nodded — once, briefly, as if confirming something he already knew.

They went in.

---

## 🔐 The Issuance Terminal

The clerk at the counter glanced at Max. Then at Okto. Then back at Max.

"New ID?"

"Yes."

"Terminal 3. Only you. Nobody else may enter the area during issuance."

Max nodded. He walked to Terminal 3.

Okto wanted to follow — but Officer Borrowing stepped around the corner. As if he had known he was needed here. He looked at Okto. Calm. Without theatrics — for once.

"Wait," he said.

Then he pulled a barrier tape from his uniform — bright yellow, printed with `&mut — EXCLUSIVE ACCESS` — and stretched it around Terminal 3. Nobody could look in. Nobody could interfere. Only Max.

"Now," said Borrowing to Max. "Only you. Only your ID. Only you are responsible."

Max looked at the terminal. At his hands. Then he typed.

```rust
// My ID — belongs to me.
// Only I may issue it. Only I am responsible.
let mut my_id = String::from("Resident: Max Mutation — ID: EXPIRED");

// Borrowing seals the area — nobody else looks in.
let issue = &mut my_id;
issue.push_str(" → VALID");
// I reach in. Alone. Fully responsible.
```

The terminal beeped once. Brief. Then it lit up green.

Officer Borrowing removed the barrier tape. Folded it carefully. Put it back.

"Done," he said.

---

## 🏙️ Okto Understands

Okto had waited outside. He hadn't seen what Max typed. He hadn't seen what the terminal showed.

But he had seen Officer Borrowing stretch the barrier tape. How nobody could look in. How Max stood alone inside — just him, his ID, his responsibility.

*That is `&mut T`*, Okto thought.

Not the mistake Max had made before. Not the chaos in the TC-0003. This.

Reaching in — but only into what's yours. Alone. With a barrier that keeps others outside. Not because they aren't allowed. But because responsibility cannot be shared when someone is writing.

Alias had shown: many eyes break nothing.
Max had shown: one hand writes — and carries it alone.

Both sides. The same law.

Officer Borrowing stepped beside Okto. He didn't look at him. He looked at Max who stepped out of the terminal area, new ID in hand.

"Understood?" asked Borrowing.

Okto thought about it.

"Look as much as you want," he said slowly. "As long as you don't interfere, everything stays safe." He paused. "And if you do reach in — only into what's yours. But then completely."

Officer Borrowing said nothing.

But he nodded.

---

## 🏙️ The Gate

On the way home — container ahead of him, Alley 7-C, the morning fog slowly dissolving — Okto stopped at the spot where the gate became visible.

Three sentences. Carved in stone.

He knew them. He had always known them.

Today he read the first one.

*What you own, tend to it.*

Not: what you have, keep it.
Not: what belongs to you, defend it.

Tend to it. Take care. Carry responsibility — for as long as it's yours, completely.

Max had written into a register that didn't belong to him. Not out of malice. Out of impatience. He hadn't asked: *does this belong to me?*

That one missing question had brought the TC-0003 down.

*What you own, tend to it.*

That wasn't a Rust concept.

That was older.

Okto pushed on. But something inside him — quiet, almost imperceptible — was no longer quite the same.

---

### 📌 Life Rule #4

> **Only reach into what's yours. But then — completely.**

---

### 🦾 Arm #1 — Deepened

*Collecting also means tending to what you have.*

### 🦾 Arm #2 — Aktive

*Observe. Two directions at once.*

### 🦾 Arm #3 — Tingling

*Stronger. Growing warmer.*

Okto has two arms. Arm #1 is no longer just collecting.
He now knows: owning means carrying responsibility.
Not forever. But for as long as it's yours — completely.

---

### 📎 File: Mutability & `&mut T`

*Found in the library of the administration tower. Section: Mutation.*

```rust
fn main() {
    // My ID — belongs to me.
    // Only I may change it. Alone. Fully responsible.
    let mut my_id = String::from("Max Mutation — ID: NONE");

    // Borrowing seals the area — nobody else looks in while I write.
    let issue = &mut my_id;
    issue.push_str(" → NEWLY ISSUED");

    // When I'm done — everyone may look again.
    println!("{}", my_id); // ✅ — mine, my responsibility

    // &T:    anyone may look — as long as nobody interferes.
    // &mut T: only one may change — but only what is theirs.
}
```

*Margin note, handwritten:*
`// &mut T doesn't mean: I can do anything. It means: I reach into what's mine — and carry it completely.`

---

*End of Chapter 4.*

*Max carries his new ID.*
*The TC-0003 still stands in Alley 19 — but that is another story.*
*Okto has two arms — and knows what the first sentence above the gate means.*
*Not everything yet. But the first sentence.*

---