 🇩🇪 [Deutsch](#de) · 🇬🇧 [English](#en)

---

<a name="de"></a>
### 🇩🇪 Deutsch

---

## 📗 Kapitel 3 — Agentin Alias

Der Name fiel wie ein einzelner Token in einen leeren Puffer.

Detective Ownership und Officer Borrowing wandten sich vom Roboter ab und liefen langsam in Richtung Heap District. Okto durfte diesmal mitkommen.

Er schaute noch einmal auf den TC-0003. Auf das flackernde Display. Auf die Fehlermeldung, die er jetzt - zum ersten Mal - ein kleines bisschen verstand.

Dann hob er seinen Behälter auf und schob weiter.

Okto hätte umkehren können. Der **Heap District** war nicht sein Bezirk - er gehörte zu Gasse 19, zum Industriegebiet, zum geordneten Rhythmus von Greifen und Loslassen im **Stack District**. Aber die beiden Männer waren hier hineingegangen. Und das Kribbeln - das neue, benennbare Kribbeln - liess ihn nicht umkehren.

Er folgte. Nicht ihnen. Eher dem Gefühl.

---

### Die Halle

Am Ende einer schmalen Gasse lag eine Halle - kein Schild, keine Nummer, keine offizielle Existenz in den Karten der Cargo-Behörde. Aber die Tür stand offen. Und drinnen flackerte Licht.

Detective Ownership trat zuerst ein. Officer Borrowing folgte, die Hand am Borrow-Checker.

Okto blieb im Eingang stehen. Er passte nicht rein - sein Behälter war zu breit - also liess er ihn draussen und trat alleine ein. Er tat das leise, wie immer.

Die Halle war voller Terminals. Kabel. Spiegel. Überall Spiegel - aber keiner zeigte dasselbe Bild. In einem sah Okto sich selbst, klein und einarmig. In einem anderen sah er nur den Behälter draussen. In einem dritten - nichts. Nur das Flackern.

Und dann sah er sie.

---

### Agentin Alias

Sie stand mit dem Rücken zu ihnen, die Hände über einer Tastatur schwebend. Kein Overcoat, keine Uniform. Nur eine dunkle Jacke, schlicht, als hätte sie keine Aufmerksamkeit nötig.

Sie wartete nicht darauf, angesprochen zu werden.

„fn main() lässt grüssen."

Die Stimme war ruhig. Keine Theatralik wie bei Borrowing, keine Stille wie bei Own. Nur ein Satz — präzise, ohne Umweg.

Own blieb stehen. Officer Borrowing liess den Borrow-Checker sinken, nur einen Moment.

„Alias", sagte Own.

„Detective." Sie tippte weiter. „Sie suchen den Ursprung des TC-0003-Ausfalls. Ich habe ihn gefunden. Setzen Sie sich."

„Es gibt keine Stühle", sagte Borrowing.

„Dann stehen Sie eben."

---

### Die Lektion

Alias drehte sich nicht um. Sie öffnete auf dem grössten Terminal einen neuen Block - sauber, leer, bereit.

„Das Problem in Gasse 19 war kein Unfall", begann sie. „Jemand hat eine Referenz angelegt - und dann wahrscheinlich später vergessen, dass sie noch existiert. Oder nicht vergessen." Sie machte eine kurze Pause. „Das ist der Unterschied zwischen einem Fehler und einem Vorsatz."

Own trat einen Schritt näher. „Zeigen Sie."

Alias tippte. Auf dem Display erschien Code - langsam, als würde sie ihn nicht eingeben, sondern enthüllen.

<details>
<summary>📜 <strong>Terminal Alias-7 : Referenz & Alias (Klicken zum Anzeigen)</strong></summary>

```rust
// ============================================
// AGENTIN ALIAS — LEKTION #1
// ORT : HALLE OHNE NUMMER / HEAP DISTRICT
// QUELLE : TRASHBOT TC-0003 / GASSE 19
// ============================================

// Das war der Fehler. So hätte es aussehen sollen :

let protokoll = String::from("10:37 .. Mülltonnen Leerung.");

// Eine Referenz — kein neuer Besitzer.
// Alias zeigt auf das Protokoll. Sie besitzt es nicht.
let alias_ref = &protokoll;

// Mehrere dürfen gleichzeitig schauen.
let alias_ref_2 = &protokoll;

println!("Referenz 1 liest : {}", alias_ref);
println!("Referenz 2 liest : {}", alias_ref_2);

// protokoll gehört noch immer dem Original.
println!("Original : {}", protokoll);

// ✅ Kein Konflikt. Kein Absturz.
// Weil niemand schreibt während jemand liest.

// ============================================
// TYPE ALIAS — ein neuer Name. Kein neuer Typ.
// ============================================

type Protokolltext = String;
type Uhrzeit = (u8, u8); // Stunde, Minute

let eintrag: Protokolltext = String::from("10:37 .. Mülltonnen Leerung.");
let zeit: Uhrzeit = (10, 37);

// Alias verändert nicht. Sie zeigt.
// Ein Alias ist kein Duplikat —
// er ist ein anderer Name für dasselbe.
```

</details>

„Eine Referenz ist kein Besitz", sagte Alias. „Sie ist ein Blick. Solange ich schaue, darf niemand schreiben. Wenn ich gehe, bleibt alles intakt." Sie tippte einen letzten Befehl. „Das ist meine Sicherheit. Und die Sicherheit aller anderen."

Officer Borrowing nickte langsam. „Shared references. Protokollkonform."

„Ich kenne das Protokoll", sagte Alias trocken. „Ich kenne auch alles, was ausserhalb davon liegt."

---

### Okto's zweiter Moment

Okto stand am Rand der Halle und schaute.

Alias hatte ihn nicht angeschaut. Kein Blick, keine Geste, kein Zeichen dass sie wusste, dass er da war. Für sie war er ein Trashbot in einer Halle - einer von vielen Dingen die existierten, ohne zu stören.

Aber Okto schaute.

Er sah wie sie die Referenzen erklärte - wie ein Zeigen ohne ein Nehmen möglich war. Wie man schauen konnte ohne zu besitzen. 

Sie demonstrierte es mit dem Detective Ownership. Sie nannte ihn einmal Detective, dann nannte sie ihn Detective Ownership, zuletzt nannte sie ihn nur Own. Sie zeigte, wie die Bedeutung zur selben Sache getarnt sein konnte.

Und dann spürte er es.

Nicht das bekannte Kribbeln an der linken Seite - dem Arm der da war, dem Arm der griff und hob und losliess. Sondern auf der anderen Seite. Rechts. Dort wo nichts war.

Ein neues Kribbeln.

Schwach. Kaum spürbar. Als würde etwas fragen ob es anfangen dürfte.

Okto schaute auf seine rechte Seite. Auf die Stelle wo ein zweiter Arm sein könnte. Er verstand nicht warum - er war ein Trashbot, er hatte einen Arm, das hatte immer gereicht. Aber das Kribbeln blieb. Ruhig, wartend, ohne Druck.

Als hätte sein System etwas registriert, das er noch nicht benennen konnte.

Er schaute wieder zu Alias.

Sie tippte weiter. Sie hatte ihn nicht bemerkt.

Aber Okto vergass sie nicht.

---

### Die Spur

„Wer hat die Referenz angelegt ?" fragte Own.

Alias schloss das Terminal. Eine einzige Bewegung — präzise, endgültig.

„Jemand der weiss wie man unsichtbar bleibt", sagte sie. „Jemand der Regeln nicht bricht, weil er sie nicht kennt - sondern weil er genau weiss was er tut." Sie wandte sich zum ersten Mal um und schaute Own direkt an. „Jemand der verändert, was er anfasst. Immer."

„Max Mutation", sagte Borrowing leise.

Alias sagte nichts. Das war Antwort genug.

„Warum helfen Sie uns ?" fragte Own.

Alias schaute zur Tür. Irgendwo draussen, im Heap District, flackerte ein Schild im Wind.

„Weil fn main() mich darum gebeten hat", sagte sie. „Und weil jemand der verändert was er anfasst - irgendwann auch das anfasst, was nicht verändert werden darf."

Sie drehte sich wieder zu ihrem Terminal.

„Sie finden ihn im alten Compiler-Viertel. Er wartet nicht — er verändert. Also beeilen Sie sich."

Own und Borrowing tauschten einen Blick. Dann gingen sie.

Okto folgte — langsam, mit seinem Behälter, den er draussen wieder aufgenommen hatte. Er schaute noch einmal zurück zur Halle.

Alias stand im Flackern der Terminals. Schon wieder mit dem Rücken zu allem.

Unsichtbar. Präzise. Unvergesslich.

---

### 📌 Lebensregel #3

> **Ein Alias ist kein Duplikat.**  
> **Er ist ein anderer Name für dasselbe.**  
> **Wer das versteht, braucht halb so viel — und sieht doppelt so viel.**

---

### 🦾 Arm #2 — Kribbeln

*Noch nicht da. Aber nicht mehr ganz absent.*

Okto hat einen Arm. Er weiss was er damit tut.  
Aber rechts — dort wo noch nichts ist — hat etwas gefragt ob es anfangen dürfte.  
Er hat nicht nein gesagt.

---

### 📎 Akte: References & Type Aliases

*Gefunden in der Bibliothek des Verwaltungsturms. Abschnitt: Referenzen.*

```rust
fn main() {
    // Referenz — schauen ohne zu besitzen
    let akte = String::from("Fall #42 — offen");
    let r = &akte;
    println!("{}", r);     // ✅ — nur lesen
    println!("{}", akte);  // ✅ — besitzt noch

    // Type Alias — ein neuer Name, kein neuer Typ
    type AktenId = u32;
    let fall_nr: AktenId = 42;
    println!("Fall Nr. : {}", fall_nr);
}
```

*Notiz am Rand, handgeschrieben:*  
`// Zeigen ist nicht dasselbe wie Nehmen.`

---

*Ende Kapitel 3.*

*Im alten Compiler-Viertel wartet jemand.*  
*Er wartet nicht — er verändert.*  
*Und er weiss nicht, dass sie kommen.*

---

---

<a name="en"></a>
## 🇬🇧 English

---

### 📗 Chapter 3 — Agent Alias

He stood still for a moment. The TC-0003 flickered. The alley was quiet again.

Then he pushed his container toward the Heap District.

Not because it was his job. Simply because the tingling wouldn't let him go.

---

The Heap District smelled different from Alley 19.

Okto noticed immediately. Not unpleasant — but livelier. More untidy. As if things existed here that hadn't yet decided what they wanted to be. Cables hung between buildings like half-loaded references. Signs pointed to places that might still be there, or might not.

He pushed his container slowly forward.

He could have turned back. The Heap District wasn't his zone — he belonged to Alley 19, to the industrial area, to the ordered rhythm of reaching and letting go. But the two men had gone in here. And the tingling — the new, nameable tingling — wouldn't let him turn back.

He followed. Not them. More the feeling.

---

### The Hall

They found nothing. Then they found everything.

At the end of a narrow alley stood a hall — no sign, no number, no official existence on the Cargo authority's maps. But the door was open. And inside, light flickered.

Own entered first. Officer Borrowing followed, hand on the Borrow-Checker.

Okto stopped at the entrance. He didn't fit — his container was too wide — so he left it outside and stepped in alone. Quietly, as always. Nobody looked.

The hall was full of terminals. Cables. Mirrors. Mirrors everywhere — but none showed the same image. In one, Okto saw himself, small and one-armed. In another, only the container outside. In a third — nothing. Just the flickering.

And then he saw her.

---

### Agent Alias

She stood with her back to them, hands hovering over a keyboard. No overcoat, no uniform. Just a dark jacket, plain, as if she needed no attention.

She didn't wait to be addressed.

"fn main() sends his regards."

The voice was calm. No theatrics like Borrowing, no silence like Own. Just a sentence — precise, without detour.

Own stopped. Officer Borrowing lowered the Borrow-Checker, just for a moment.

"Alias," said Own.

"Detective." She kept typing. "You're looking for the origin of the TC-0003 failure. I found it. Stand somewhere."

"There are no chairs," said Borrowing.

"Then stand."

---

### The Lesson

Alias didn't turn around. She opened a new block on the largest terminal — clean, empty, ready.

"The problem in Alley 19 was no accident," she began. "Someone created a reference — and then forgot it still existed. Or didn't forget." She paused briefly. "That is the difference between a mistake and intent."

Own stepped closer. "Show me."

Alias typed. Code appeared on the display — slowly, as if she wasn't entering it but revealing it.

<details>
<summary>📜 <strong>Terminal Alias-7 : Reference & Alias (Click to expand)</strong></summary>

```rust
// ============================================
// AGENT ALIAS — LESSON #1
// LOCATION : HALL WITHOUT NUMBER / HEAP DISTRICT
// SOURCE : TRASHBOT TC-0003 / ALLEY 19
// ============================================

// That was the error. This is how it should have looked:

let protokoll = String::from("10:37 .. Bin collection started.");

// A reference — no new owner.
// Alias points to the log. She doesn't own it.
let alias_ref = &protokoll;

// Multiple can look at the same time.
let alias_ref_2 = &protokoll;

println!("Reference 1 reads : {}", alias_ref);
println!("Reference 2 reads : {}", alias_ref_2);

// protokoll still belongs to the original.
println!("Original : {}", protokoll);

// ✅ No conflict. No crash.
// Because no one writes while someone reads.

// ============================================
// TYPE ALIAS — a new name. Not a new type.
// ============================================

type LogEntry = String;
type Timestamp = (u8, u8); // hour, minute

let entry: LogEntry = String::from("10:37 .. Bin collection started.");
let time: Timestamp = (10, 37);

// Alias doesn't change. She shows.
// An alias is not a duplicate —
// it's a different name for the same thing.
```

</details>

"A reference is not ownership," said Alias. "It's a look. As long as I look, no one may write. When I leave, everything stays intact." She typed a final command. "That is my safety. And everyone else's."

Officer Borrowing nodded slowly. "Shared references. Protocol-compliant."

"I know the protocol," said Alias drily. "I also know everything outside it."

---

### Okto's Second Moment

Okto stood at the edge of the hall and watched.

Alias hadn't looked at him. No glance, no gesture, no sign that she knew he was there. To her, he was a trashbot in a hall — one of many things that existed without disturbing.

But Okto watched.

He saw how she explained references — how looking without taking was possible. How you could observe without owning. How a name could just be another entrance to the same thing.

And then he felt it.

Not the familiar tingling on the left side — the arm that was there, the arm that reached and lifted and released. But on the other side. Right. Where nothing was.

A new tingling.

Faint. Barely noticeable. As if something was asking whether it might begin.

Okto looked at his right side. At the spot where a second arm could be. He didn't understand why — he was a trashbot, he had one arm, that had always been enough. But the tingling stayed. Calm, waiting, without pressure.

As if his system had registered something he couldn't yet name.

He looked back at Alias.

She kept typing. She hadn't noticed him.

But Okto didn't forget her.

---

### The Trail

"Who created the reference?" asked Own.

Alias closed the terminal. A single movement — precise, final.

"Someone who knows how to stay invisible," she said. "Someone who doesn't break rules because they don't know them — but because they know exactly what they're doing." She turned around for the first time and looked directly at Own. "Someone who changes everything they touch. Always."

"Max Mutation," said Borrowing quietly.

Alias said nothing. That was answer enough.

"Why are you helping us?" asked Own.

Alias looked toward the door. Somewhere outside, in the Heap District, a sign flickered in the wind.

"Because fn main() asked me to," she said. "And because someone who changes everything they touch — will eventually touch what must not be changed."

She turned back to her terminal.

"You'll find him in the old Compiler Quarter. He doesn't wait — he changes. So hurry."

Own and Borrowing exchanged a glance. Then they left.

Okto followed — slowly, with his container, which he had picked up again outside. He looked back once more toward the hall.

Alias stood in the flickering of the terminals. Already with her back to everything again.

Invisible. Precise. Unforgettable.

---

### 📌 Life Rule #3

> **An alias is not a duplicate.**  
> **It's a different name for the same thing.**  
> **Those who understand this need half as much — and see twice as much.**

---

### 🦾 Arm #2 — Tingling

*Not there yet. But no longer entirely absent.*

Okto has one arm. He knows what he does with it.  
But on the right — where nothing is — something asked whether it might begin.  
He didn't say no.

---

### 📎 File: References & Type Aliases

*Found in the library of the administration tower. Section: References.*

```rust
fn main() {
    // Reference — looking without owning
    let file = String::from("Case #42 — open");
    let r = &file;
    println!("{}", r);     // ✅ — read only
    println!("{}", file);  // ✅ — still owns it

    // Type Alias — a new name, not a new type
    type CaseId = u32;
    let case_nr: CaseId = 42;
    println!("Case No. : {}", case_nr);
}
```

*Margin note, handwritten:*  
`// Showing is not the same as taking.`

---

*End of Chapter 3.*

*In the old Compiler Quarter, someone is waiting.*  
*He doesn't wait — he changes.*  
*And he doesn't know they're coming.*

---