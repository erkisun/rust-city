 🇩🇪 [Deutsch](#de) · 🇬🇧 [English](#en)

---

<a name="de"></a>
### 🇩🇪 Deutsch

---

## 📗 Kapitel 4 — Max Mutation

Max kam am nächsten Morgen zurück.

Okto sah ihn von weitem — die zu grosse Jacke, die unordentlichen Haare. Er kam durch die Gasse 19, langsamer als sonst, als würde er sich nicht ganz sicher sein ob er willkommen war.

Der TC-0003 stand noch immer da. Display noch immer rot. Status noch immer FROZEN.

Max blieb davor stehen. Schaute lange.

„Ich will es diesmal richtig machen", sagte er.

Okto schob seinen Behälter einen Schritt zur Seite. Er sagte nichts. Aber er blieb.

---

## 🔧 Diesmal richtig

Max wusste was er falsch gemacht hatte. Das war gestern schon klar geworden — in Alias' Glasraum, in ihrer ruhigen, präzisen Art es ihm zu erklären. Er hatte eine lesende Referenz auf das Protokoll des TC-0003 gesetzt und gleichzeitig hineingeschrieben. Beides auf einmal. Das war der Absturz.

Heute wollte er nur lesen.

Er schloss sein Diagnose-Kabel an. Langsamer als sonst. Er schaute kurz zu Okto — nicht um Erlaubnis, aber fast.

Dann tippte er.

```rust
// ==============================================
// MAX' VERSUCH — DIESMAL NUR LESEN
// ORT : INDUSTRIEGEBIET / GASSE 19
// ==============================================
//
// Modell : Trash-Collector v.3.4.2 "TC-0003"
// Baujahr : 2034
// Status : steht still

// Die letzten Log-Einträge im Speicher des defekten Trashbots.
let mut id_register = String::from("Einwohner: Max Mutation — Ausweis: GÜLTIG");

// Max liest (&T) den Ausweis aus dem Register. Nur schauen.
let inspection = &id_register;

// Kein Konflikt !
println!("{}", inspection);

// Keine Mutation. Keine Kollision.
// Officer Borrowing würde nicken.
// ==============================================
```

Das Display des TC-0003 flackerte. Nicht rot. Nicht schwarz.

Gelb. Dann ein kurzes, vorsichtiges Grün.

Max lehnte sich zurück. Er atmete langsam aus.

„Da ist sie", sagte er leise.

Okto trat näher. Auf dem Display stand jetzt ein Eintrag — klein, fast am Ende des Protokolls, zwischen den Zeitstempeln:

`10:40 .. Ausweis liegt im Fundbüro, Crate 7, Fach 3.`

Max schaute hinüber zum Crate. Dann auf den Eintrag. Dann wieder auf den Crate.

„Sie war die ganze Zeit im Fundbüro", sagte er.

---

## 🏙️ Okto's Frage

Okto betrachtete das Display. Den Eintrag. Den Code den Max getippt hatte.

Diesmal kein Fehler. Diesmal keine Kollision. Nur eine lesende Referenz — ruhig, präzise, ohne einzugreifen. Der TC-0003 hatte nicht gezuckt. Das Protokoll war intakt.

*Lesen darf jeder*, dachte Okto. *Solange niemand gleichzeitig schreibt.*

Er wusste das bereits — seit Gasse 19, seit Alias, seit dem Glasraum. Aber jetzt hatte er es anders gesehen. Nicht als Verbot. Als Möglichkeit.

„Warum hast du gestern geschrieben ?" fragte Okto.

Max schaute ihn an. Eine kurze Pause.

„Weil ich dachte, wenn ich es ins Register schreibe, findet es jemand." Er zuckte mit den Schultern — eine Bewegung die aussah wie ein halbfertiges Argument. „Schneller. Einfacher."

„Aber das Register gehörte dir nicht."

„Nein", sagte Max. Kein Zögern. „Das war der Fehler."

---

## 🏙️ Was Max versteht

Sie sassen eine Weile auf den Crate-Boxen neben dem TC-0003. Das Display zeigte ein ruhiges Grün. Irgendwo im Heap District flackerte ein Compiler-Schild. Die Stadt arbeitete weiter.

„Alias hat gesagt, ein Profi biegt die Regeln weil er sie vollständig versteht", sagte Max. Er drehte die Teekanne in seinen Händen. „Ich glaube ich bin noch Amateur."

„Du weisst jetzt was du falsch gemacht hast", sagte Okto.

„Das wusste ich gestern auch schon."

„Aber heute hast du es anders gemacht."

Max schaute ihn an. Dann auf das Display.

„Ja", sagte er. „Heute hab ich erst gelesen."

Eine Pause.

„Vielleicht", sagte Okto langsam, „ist das der Unterschied. Nicht ob man die Regel kennt. Sondern ob man — bevor man handelt — fragt: gehört mir das ? Und was darf ich damit tun ?"

Max schwieg eine Weile.

„Das klingt nach dem was am Tor steht", sagte er schliesslich.

Okto sagte nichts. Aber er dachte daran.

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

Max hatte in ein Protokoll geschrieben das ihm nicht gehörte. Nicht aus Bosheit. Aus Ungeduld. Aus dem Gefühl dass Schnelligkeit genug war.

Aber das Protokoll gehörte ihm nicht. Also hatte er auch keine Verantwortung dafür getragen. Und genau das — diese eine fehlende Frage — hatte den TC-0003 zum Absturz gebracht.

*Was du besitzt, das pflege.*

Das war kein Rust-Konzept.

Das war älter.

Okto schob weiter. Aber etwas in ihm — ruhig, fast unmerklich, wie ein Wert der sich still verändert — war nicht mehr ganz dasselbe.

---

### 📌 Lebensregel #4

> **Coolness öffnet Türen. Struktur hält sie offen.**

---

### 🦾 Arm #1 — Vertieft

*Sammeln bedeutet auch: pflegen was man hat.*

Okto hat zwei Arme. Arm #1 ist nicht mehr nur Sammeln.
Er weiss jetzt: besitzen bedeutet Verantwortung tragen.
Nicht für immer. Aber solange es dir gehört — vollständig.

---

### 📎 Akte: Mutability & `&mut T`

*Gefunden in der Bibliothek des Verwaltungsturms. Abschnitt: Mutation.*

```rust
fn main() {
    let mut wert = String::from("TC-0003 Protokoll");

    // Entweder: viele lesen — gleichzeitig, kein Problem
    let r1 = &wert;
    let r2 = &wert;
    println!("{} — {}", r1, r2); // ✅

    // Oder: einer schreibt — alleine, ohne Zuschauer
    // Aber nur wenn der Wert dir gehört.
    let r3 = &mut wert;
    r3.push_str(" — bereinigt");
    println!("{}", r3); // ✅

    // Niemals beides gleichzeitig.
    // Und niemals in etwas schreiben das dir nicht gehört.
}
```

*Notiz am Rand, handgeschrieben:*
`// &mut T bedeutet nicht: ich darf alles. Es bedeutet: ich bin jetzt alleine verantwortlich — für etwas das mir gehört.`

---

*Ende Kapitel 4.*

*Der TC-0003 steht in Gasse 19.*
*Sein Display zeigt ein ruhiges, gleichmässiges Grün.*
*Max bringt die Teekanne ins Fundbüro, Crate 7, Fach 3.*
*Okto hat zwei Arme — und weiss was der erste Satz am Tor bedeutet.*
*Noch nicht alles. Aber den ersten Satz.*

---

---

<a name="en"></a>
## 🇬🇧 English

---

## 📗 Chapter 4 — Max Mutation

Max came back the next morning.

Okto saw him from a distance — the oversized jacket, the untidy hair, the teapot still under his arm. He came through Alley 19, slower than yesterday, as if he wasn't quite sure he was welcome.

The TC-0003 was still there. Display still red. Status still FROZEN.

Max stopped in front of it. Looked for a long time.

"I want to do it right this time," he said.

Okto pushed his container one step to the side. He said nothing. But he stayed.

---

## 🔧 This Time Right

Max knew what he had done wrong. That had already become clear yesterday — in Alias' glass room, in her calm, precise way of explaining it to him. He had set a reading reference on the TC-0003's log and written into it at the same time. Both at once. That was the crash.

Today he only wanted to read.

He connected his diagnostic cable. Slower than usual. He glanced briefly at Okto — not for permission, but almost.

Then he typed.

```rust
// ==============================================
// MAX' ATTEMPT — THIS TIME ONLY READING
// LOCATION : ALLEY 19 / TC-0003
// ==============================================

// The TC-0003's log — read without changes.
let protokoll = String::from(
    "10:37 .. Bin collection started. \
     10:38 .. blue bin emptied. \
     10:39 .. green bin emptied. \
     10:40 .. red bin emptied."
);

// Max reads — without writing. &T. Just looking.
let findmyteapot = &protokoll;
println!("{}", findmyteapot); // ✅ — no conflict

// No mutation. No collision.
// Officer Borrowing would nod.
// ==============================================
```

The TC-0003's display flickered. Not red. Not black.

Yellow. Then a brief, cautious green.

Max leaned back. He breathed out slowly.

"There it is," he said quietly.

Okto stepped closer. On the display there was now an entry — small, almost at the end of the log, between the timestamps:

`10:40 .. Teapot — Lost & Found, Crate 7, Slot 3.`

Max looked at the teapot under his arm. Then at the entry. Then back at the teapot.

"It was in the lost and found the whole time," he said.

---

## 🏙️ Okto's Question

Okto looked at the display. The entry. The code Max had typed.

No error this time. No collision. Just a reading reference — calm, precise, without intervening. The TC-0003 hadn't flinched. The log was intact.

*Anyone can read*, Okto thought. *As long as nobody writes at the same time.*

He already knew that — since Alley 19, since Alias, since the glass room. But now he had seen it differently. Not as a prohibition. As a possibility.

"Why did you write yesterday?" Okto asked.

Max looked at him. A brief pause.

"Because I thought if I write it into the log, someone would find it." He shrugged — a movement that looked like a half-finished argument. "Faster. Simpler."

"But the log wasn't yours."

"No," said Max. No hesitation. "That was the mistake."

---

## 🏙️ What Max Understands

They sat for a while on the crate boxes beside the TC-0003. The display showed a quiet green. Somewhere in the Heap District a compiler sign flickered. The city kept working.

"Alias said a professional bends the rules because he understands them completely," said Max. He turned the teapot in his hands. "I think I'm still an amateur."

"You now know what you did wrong," said Okto.

"I knew that yesterday too."

"But today you did it differently."

Max looked at him. Then at the display.

"Yes," he said. "Today I read first."

A pause.

"Maybe," said Okto slowly, "that's the difference. Not whether you know the rule. But whether — before you act — you ask: does this belong to me? And what am I allowed to do with it?"

Max was quiet for a while.

"That sounds like what's written above the gate," he said finally.

Okto said nothing. But he thought about it.

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

Max had written into a log that didn't belong to him. Not out of malice. Out of impatience. Out of the feeling that speed was enough.

But the log wasn't his. So he hadn't carried any responsibility for it. And that — that one missing question — had brought the TC-0003 down.

*What you own, tend to it.*

That wasn't a Rust concept.

That was older.

Okto pushed on. But something inside him — quiet, almost imperceptible, like a value that changes silently — was no longer quite the same.

---

### 📌 Life Rule #4

> **Coolness opens doors. Structure keeps them open.**

---

### 🦾 Arm #1 — Deepened

*Collecting also means: tending to what you have.*

Okto has two arms. Arm #1 is no longer just collecting.
He now knows: owning means carrying responsibility.
Not forever. But for as long as it's yours — completely.

---

### 📎 File: Mutability & `&mut T`

*Found in the library of the administration tower. Section: Mutation.*

```rust
fn main() {
    let mut value = String::from("TC-0003 Log");

    // Either: many read — simultaneously, no problem
    let r1 = &value;
    let r2 = &value;
    println!("{} — {}", r1, r2); // ✅

    // Or: one writes — alone, without observers
    // But only if the value belongs to you.
    let r3 = &mut value;
    r3.push_str(" — cleared");
    println!("{}", r3); // ✅

    // Never both at the same time.
    // And never write into something that isn't yours.
}
```

*Margin note, handwritten:*
`// &mut T doesn't mean: I can do anything. It means: I am now solely responsible — for something that is mine.`

---

*End of Chapter 4.*

*The TC-0003 stands in Alley 19.*
*Its display shows a calm, steady green.*
*Max takes the teapot to the lost and found, Crate 7, Slot 3.*
*Okto has two arms — and knows what the first sentence above the gate means.*
*Not everything yet. But the first sentence.*

---