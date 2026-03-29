 🇩🇪 [Deutsch](#de) · 🇬🇧 [English](#en)

---

<a name="de"></a>
### 🇩🇪 Deutsch

---

## 📗 Kapitel 5 — Madame Enum und ihre Typen

Es gab in Rust City einen Ort, den die meisten Bewohner kannten aber selten besuchten.

Nicht weil er gefährlich war. Nicht weil er schwer zu finden war. Sondern weil man ihn erst dann aufsuchte, wenn man nicht mehr wusste wer man war — oder wer jemand anderes war. Er lag am Rand des Heap Districts, dort wo der Lärm langsam aufhörte und die Gassen breiter wurden. Ein altes Gebäude, drei Stockwerke, keine Beschriftung. Nur eine kleine Messingplakette neben der Tür:

**Madame Enum — Typen & Zustände**

Okto kannte den Ort. Er war daran vorbeigegangen, hundert Mal, ohne anzuhalten.

Heute hielt er an.

Nicht weil er wusste warum. Sondern weil Max neben ihm stand und sagte: „Ich glaube, die kann helfen."

---

## 🎭 Madame Enum

Sie sass im Erdgeschoss, an einem runden Tisch, umgeben von Regalen voller beschrifteter Schachteln. Jede Schachtel trug einen Namen. Jede Schachtel war anders. Keine war falsch.

Madame Enum war älter als Own und jünger als fn main(). Ihr Haar war grau, ihr Blick war klar, und sie trug eine Brille die sie nie wirklich zu brauchen schien — sie schaute immer leicht darüber hinweg, als würde sie etwas sehen das andere nicht sahen.

Sie schaute auf als sie eintraten. Zuerst zu Max.

„Max Mutation", sagte sie. Nicht als Frage. „Impulsiv. Neugierig. Ehrlich." Sie lehnte sich zurück. „Du hast etwas verloren."

„Meinen Ausweis", sagte Max.

„Nein", sagte Madame Enum ruhig. „Deinen Ausweis hast du nur verlegt. Was du verloren hast, ist etwas anderes." Sie schaute ihn an. „Du dachtest, Schnelligkeit ersetzt Struktur. Das stimmt nicht. Das war die Lektion."

Max schwieg. Aber er nickte.

Dann schaute Madame Enum zu Okto.

Und blieb.

---

## 🎭 Der Blick

Sie schaute ihn an wie niemand ihn je angeschaut hatte.

Nicht wie Own — präzise, prüfend, auf der Suche nach Fehlern. Nicht wie Borrowing — streng, theatralisch, regelprüfend. Nicht wie Alias — kurz, scannend, einlesend.

Madame Enum schaute ihn an als würde sie etwas sehen das bereits da war. Etwas das er selbst noch nicht gesehen hatte.

„Komm näher", sagte sie.

Okto trat einen Schritt vor. Dann noch einen.

Sie betrachtete seinen linken Arm. Die Stelle an seiner Seite wo manchmal das Kribbeln war. Seine Hände. Seine Augen.

„Interessant", sagte sie leise. Nicht zu ihm — zu sich selbst, fast. „Sehr interessant."

„Was ?" fragte Okto.

„Du weisst nicht was du bist", sagte sie. „Das ist selten. Die meisten wissen es zu gut — oder denken es zu wissen." Sie faltete die Hände. „Du weisst es wirklich nicht. Noch nicht."

---

## 📦 Die Schachteln

Madame Enum stand auf und ging zu einem der Regale. Sie zog eine Schachtel heraus — mittelgross, beschriftet mit einem einzigen Wort: **Zustand**.

„Ich arbeite mit Typen", sagte sie, während sie die Schachtel öffnete. „Jeder Bewohner von Rust City hat einen Typ. Einen Zustand. Manchmal mehrere." Sie stellte verschiedene kleinere Schachteln auf den Tisch. „Ein Typ sagt nicht wer du bist. Er sagt was du kannst — und was du gerade bist."

Sie zeigte auf die erste Schachtel: **Sammler**.
Dann auf die zweite: **Beobachter**.
Dann auf eine dritte, vierte, fünfte — immer weiter.

Okto schaute auf die Schachteln. Dann auf Madame Enum.

„Ich bin ein Trashbot", sagte er. „Ich sammle."

„Ja", sagte sie. „Das ist einer deiner Zustände." Sie schaute ihn an. „Aber nicht der einzige."

---

## 📦 Der Code

Sie setzte sich wieder und zog ihr Notizbuch heraus. Sie schrieb langsam, sorgfältig.

```rust
// Was ist Okto ?
// Ein Enum — mehrere mögliche Zustände, einer aktiv.

enum Okto {
    Sammler,      // Arm #1 — aktiv seit Kapitel 1
    Beobachter,   // Arm #2 — aktiv seit Kapitel 3
    Einordner,    // Arm #3 — ?
    Verstehender, // Arm #4 — ?
    // ... und mehr. Viel mehr.
}

// Welcher Zustand ist gerade aktiv ?
let okto_jetzt = Okto::Sammler;

match okto_jetzt {
    Okto::Sammler     => println!("Ich sammle. Das ist was ich tue."),
    Okto::Beobachter  => println!("Ich sehe. In beide Richtungen."),
    Okto::Einordner   => println!("Ich erkenne. Ohne zu urteilen."),
    Okto::Verstehender => println!("Ich sehe was andere übersehen."),
    // Rust fragt immer : hast du alle Fälle bedacht ?
    // Kein Zustand darf vergessen werden.
}
```

Sie schob das Notizbuch zu Okto.

Er las es. Langsam. Zeile für Zeile.

*Mehrere mögliche Zustände*, dachte er. *Einer aktiv.*

„Das bin ich ?" fragte er.

„Das bist du", sagte Madame Enum. „Unter anderem."

---

## 🎭 Der Satz

Eine lange Stille. Max sass auf einem Stuhl in der Ecke und schaute zu — still, was für Max ungewöhnlich war.

Madame Enum faltete wieder die Hände. Sie schaute Okto an, ruhig, geduldig.

„Du hast acht mögliche Arme", sagte sie.

Okto sagte nichts.

„Acht Zustände. Acht Fähigkeiten. Alle möglich. Nicht alle aktiv — noch nicht." Sie lächelte leicht. „Zwei kennst du bereits. Zwei weitere wachen heute auf. Der Rest kommt."

Okto schaute auf seinen linken Arm. Auf die Stelle wo manchmal das Kribbeln war. Auf die anderen Stellen — rechts, oben, unten — die er nie beachtet hatte weil er nicht gewusst hatte dass er sie beachten sollte.

„Wie heisse ich ?" fragte er leise.

Madame Enum schaute ihn an. Ein langer Moment.

„Du heisst Okto", sagte sie.

---

## 🏙️ Zwei Arme auf einmal

Es war kein Blitz. Kein Lärm. Kein Compiler-Error der sich in sein Gegenteil verwandelte.

Es war leise.

An zwei Stellen gleichzeitig — eine rechts, eine links, beide an Orten die er bisher ignoriert hatte — wurde es warm. Nicht unangenehm. Wie wenn man lange in der Kälte war und dann in einen Raum tritt der geheizt ist. Der Körper erkennt es bevor der Kopf es versteht.

Okto stand still.

Er schaute auf seine Hände. Auf seine Seiten. Auf Madame Enum.

„Was passiert gerade ?" fragte er.

„Du lernst einzuordnen", sagte sie ruhig. „Und du lernst zu verstehen. Beides gleichzeitig — das ist selten. Aber bei dir nicht überraschend."

Max schaute von der Ecke aus zu. Er sagte nichts. Aber sein Gesicht zeigte etwas das Okto noch nie bei ihm gesehen hatte.

Staunen.

---

## 🏙️ Was Okto versteht

Später — draussen, Gasse 7-C, der Abend der langsam über den Heap District kroch — dachte Okto nach.

Nicht über die acht Arme. Nicht über den Namen. Nicht über Enums und Zustände und Pattern Matching.

Er dachte über Madame Enums Satz nach.

*Keiner ist falsch — nur falsch eingesetzt.*

Max war nicht falsch. Max war impulsiv, strukturlos, ungeduldig — aber nicht falsch. Er hatte den falschen Zustand im falschen Moment aktiviert. Schreiben statt Lesen. Schnelligkeit statt Struktur. Das war kein Charakter-Fehler. Das war ein Typ-Fehler.

Und Typ-Fehler, das wusste Okto jetzt, konnte man beheben.

Er schaute auf seine Seiten. Vier Arme aktiv. Vier weitere irgendwo — wartend, kribbelig, noch nicht bereit.

Er hatte einen Namen.

Er hiess Okto.

---

### 📌 Lebensregel #5

> **Die Welt hat viele Typen. Keiner ist falsch — nur falsch eingesetzt.**

---

### 🦾 Arm #1 — Vertieft

*Sammeln bedeutet auch pflegen was man hat.*

### 🦾 Arm #2 — Aktiv

*Beobachten. Zwei Richtungen gleichzeitig.*

### 🦾 Arm #3 — Erwacht

*Einordnen. Typen erkennen ohne zu urteilen.*

### 🦾 Arm #4 — Erwacht

*Verstehen. Zusammenhänge sehen die andere übersehen.*

### 🦾 Arm #5 — Kribbelt

*Beginnt.*

Okto hat vier Arme. Er hat einen Namen.
Er heisst Okto — nicht weil jemand es entschieden hat.
Sondern weil es stimmt.

---

### 📎 Akte: Enums, Structs & Pattern Matching

*Gefunden in der Bibliothek des Verwaltungsturms. Abschnitt: Typen.*

```rust
// Ein Enum beschreibt alle möglichen Zustände.
// Rust stellt sicher dass keiner vergessen wird.

enum Ausweis {
    Gueltig,
    Abgelaufen,
    Verloren,
    InBearbeitung,
}

// Pattern Matching — jeder Fall muss behandelt werden.
let max_ausweis = Ausweis::Verloren;

match max_ausweis {
    Ausweis::Gueltig        => println!("Zugang gewährt."),
    Ausweis::Abgelaufen     => println!("Bitte erneuern."),
    Ausweis::Verloren       => println!("Bitte beim Fundbüro melden."),
    Ausweis::InBearbeitung  => println!("Bitte warten."),
    // Kein Fall vergessen. Rust lässt das nicht zu.
}
```

*Notiz am Rand, handgeschrieben:*
`// Ein Enum ist keine Einschränkung. Es ist Klarheit — über alle möglichen Zustände.`

---

*Ende Kapitel 5.*

*Max weiss jetzt wo sein Ausweis ist — Fundbüro, Crate 7, Fach 3.*
*Er geht ihn holen. Diesmal auf dem richtigen Weg.*
*Okto hat vier Arme. Einen Namen. Und das Kribbeln an Arm #5 hat begonnen.*
*Buch 1 ist fertig.*
*Die Frage bleibt : Was kann ich ?*

---

---

<a name="en"></a>
## 🇬🇧 English

---

## 📗 Chapter 5 — Madame Enum and her Types

There was a place in Rust City that most residents knew but rarely visited.

Not because it was dangerous. Not because it was hard to find. But because you only went there when you no longer knew who you were — or who someone else was. It sat at the edge of the Heap District, where the noise slowly stopped and the alleys grew wider. An old building, three floors, no sign. Only a small brass plaque beside the door:

**Madame Enum — Types & States**

Okto knew the place. He had walked past it, a hundred times, without stopping.

Today he stopped.

Not because he knew why. But because Max was standing beside him saying: "I think she can help."

---

## 🎭 Madame Enum

She sat on the ground floor, at a round table, surrounded by shelves of labelled boxes. Each box carried a name. Each box was different. None was wrong.

Madame Enum was older than Own and younger than fn main(). Her hair was grey, her gaze was clear, and she wore glasses she never really seemed to need — she always looked slightly over them, as if she saw something others didn't.

She looked up when they entered. First at Max.

"Max Mutation," she said. Not a question. "Impulsive. Curious. Honest." She leaned back. "You lost something."

"My ID," said Max.

"No," said Madame Enum calmly. "Your ID you only misplaced. What you lost is something else." She looked at him. "You thought speed replaces structure. It doesn't. That was the lesson."

Max was quiet. But he nodded.

Then Madame Enum looked at Okto.

And stayed.

---

## 🎭 The Look

She looked at him the way nobody had ever looked at him.

Not like Own — precise, examining, searching for errors. Not like Borrowing — strict, theatrical, rule-checking. Not like Alias — briefly, scanning, reading.

Madame Enum looked at him as if she could see something that was already there. Something he himself hadn't seen yet.

"Come closer," she said.

Okto stepped forward. Then once more.

She looked at his left arm. The spot on his side where the tingle sometimes was. His hands. His eyes.

"Interesting," she said quietly. Not to him — almost to herself. "Very interesting."

"What?" asked Okto.

"You don't know what you are," she said. "That's rare. Most know it too well — or think they do." She folded her hands. "You genuinely don't know. Not yet."

---

## 📦 The Boxes

Madame Enum stood up and went to one of the shelves. She pulled out a box — medium-sized, labelled with a single word: **State**.

"I work with types," she said, as she opened the box. "Every resident of Rust City has a type. A state. Sometimes several." She placed various smaller boxes on the table. "A type doesn't say who you are. It says what you can do — and what you are right now."

She pointed to the first box: **Collector**.
Then the second: **Observer**.
Then a third, fourth, fifth — on and on.

Okto looked at the boxes. Then at Madame Enum.

"I'm a trashbot," he said. "I collect."

"Yes," she said. "That is one of your states." She looked at him. "But not the only one."

---

## 📦 The Code

She sat back down and pulled out her notebook. She wrote slowly, carefully.

```rust
// What is Okto?
// An enum — multiple possible states, one active.

enum Okto {
    Collector,    // Arm #1 — active since Chapter 1
    Observer,     // Arm #2 — active since Chapter 3
    Sorter,       // Arm #3 — ?
    Understander, // Arm #4 — ?
    // ... and more. Much more.
}

// Which state is currently active?
let okto_now = Okto::Collector;

match okto_now {
    Okto::Collector    => println!("I collect. That's what I do."),
    Okto::Observer     => println!("I see. In both directions."),
    Okto::Sorter       => println!("I recognise. Without judging."),
    Okto::Understander => println!("I see what others miss."),
    // Rust always asks: have you considered all cases?
    // No state may be forgotten.
}
```

She pushed the notebook toward Okto.

He read it. Slowly. Line by line.

*Multiple possible states*, he thought. *One active.*

"That's me?" he asked.

"That is you," said Madame Enum. "Among other things."

---

## 🎭 The Sentence

A long silence. Max sat on a chair in the corner and watched — quiet, which was unusual for Max.

Madame Enum folded her hands again. She looked at Okto, calm, patient.

"You have eight possible arms," she said.

Okto said nothing.

"Eight states. Eight abilities. All possible. Not all active — not yet." She smiled slightly. "Two you already know. Two more will wake up today. The rest will come."

Okto looked at his left arm. At the spot where the tingle sometimes was. At the other spots — right, above, below — that he had never paid attention to because he hadn't known he should.

"What is my name?" he asked quietly.

Madame Enum looked at him. A long moment.

"Your name is Okto," she said.

---

## 🏙️ Two Arms at Once

It wasn't a flash. Not a sound. Not a compiler error turning into its opposite.

It was quiet.

In two places at once — one on the right, one on the left, both in spots he had ignored until now — it grew warm. Not unpleasantly. Like when you've been in the cold for a long time and step into a heated room. The body recognises it before the mind understands.

Okto stood still.

He looked at his hands. At his sides. At Madame Enum.

"What's happening?" he asked.

"You're learning to sort," she said calmly. "And you're learning to understand. Both at the same time — that's rare. But not surprising for you."

Max watched from the corner. He said nothing. But his face showed something Okto had never seen from him before.

Wonder.

---

## 🏙️ What Okto Understands

Later — outside, Alley 7-C, the evening slowly creeping over the Heap District — Okto thought.

Not about the eight arms. Not about the name. Not about enums and states and pattern matching.

He thought about Madame Enum's sentence.

*None is wrong — only wrongly placed.*

Max wasn't wrong. Max was impulsive, structureless, impatient — but not wrong. He had activated the wrong state at the wrong moment. Writing instead of reading. Speed instead of structure. That wasn't a character flaw. That was a type error.

And type errors, Okto now knew, could be fixed.

He looked at his sides. Four arms active. Four more somewhere — waiting, tingling, not yet ready.

He had a name.

His name was Okto.

---

### 📌 Life Rule #5

> **The world has many types. None is wrong — only wrongly placed.**

---

### 🦾 Arm #1 — Deepened

*Collecting also means tending to what you have.*

### 🦾 Arm #2 — Active

*Observe. Two directions at once.*

### 🦾 Arm #3 — Awakened

*Sort. Recognise types without judging.*

### 🦾 Arm #4 — Awakened

*Understand. See connections others miss.*

### 🦾 Arm #5 — Tingling

*Beginning.*

Okto has four arms. He has a name.
His name is Okto — not because someone decided it.
But because it's true.

---

### 📎 File: Enums, Structs & Pattern Matching

*Found in the library of the administration tower. Section: Types.*

```rust
// An enum describes all possible states.
// Rust makes sure none are forgotten.

enum ID {
    Valid,
    Expired,
    Lost,
    InProgress,
}

// Pattern matching — every case must be handled.
let max_id = ID::Lost;

match max_id {
    ID::Valid      => println!("Access granted."),
    ID::Expired    => println!("Please renew."),
    ID::Lost       => println!("Please report to lost and found."),
    ID::InProgress => println!("Please wait."),
    // No case forgotten. Rust doesn't allow that.
}
```

*Margin note, handwritten:*
`// An enum is not a restriction. It is clarity — about all possible states.`

---

*End of Chapter 5.*

*Max now knows where his ID is — Lost & Found, Crate 7, Slot 3.*
*He goes to get it. This time the right way.*
*Okto has four arms. A name. And the tingle at Arm #5 has begun.*
*Book 1 is complete.*
*The question remains: What can I do?*

---