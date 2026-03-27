# 🏙️ Rust City — Bibel v9

---

## 🤖 Okto

**Modell:** TC-0008 — **Funktion:** Trashbot — **Bezirk:** Gasse 7-C, Heap District — **Status:** Wachsend

Still. Neugierig. Ausdauernd.

Okto ist ein Trashbot. Das ist alles was er über sich weiss — am Anfang. Er sammelt, leert, gibt zurück. Einen Arm. Eine Aufgabe. Keine Fragen.

Aber in ihm summt es. Er ist nie im Mittelpunkt des Lärms. Immer am Rand — beobachtend, denkend, wachsend. Genau dort wo der Leser auch ist.

### Die acht Arme

| Arm | Erwacht | Fähigkeit | Kribbeln beginnt |
|-----|---------|-----------|-----------------|
| 🦾 #1 | Kap. 1 | Sammeln — leeren, zurückgeben | — |
| 🦾 #2 | Kap. 3 | Beobachten — zwei Richtungen gleichzeitig | Kap. 1 kaum spürbar, Kap. 2 stärker |
| 🦾 #3 | Kap. 5 | Einordnen — Typen erkennen ohne zu urteilen | Kap. 3 Ende |
| 🦾 #4 | Kap. 5 | Verstehen — Zusammenhänge sehen die andere übersehen | Kap. 3 Ende |
| 🦾 #5 | Kap. 7 | Bauen — Strukturen die über einen selbst hinausgehen | Kap. 5 Ende |
| 🦾 #6 | Kap. 8 | Weitergeben — Wissen und Erfahrung teilen | Kap. 7 Ende |
| 🦾 #7 | Kap. 10 | Identität — sich selbst kennen | Kap. 9 Ende |
| 🦾 #8 | Kap. 11 | Schwarm — Teil von etwas Grösserem sein | Kap. 10 Ende |

*Vor jedem Erwachen kribbelt es. Der Leser merkt es bevor Okto es versteht.*

**Kap. 4 kein neuer Arm:** `&mut T` vertieft Arm #1 — besitzen bedeutet auch eingreifen und Verantwortung tragen.

### Was Okto nie tut
- Laut werden
- Aufgeben
- Sich selbst bemitleiden

---

## 🎩 fn main()

**Standort:** Balkon, zweiter Stock, Verwaltungsturm — **Status:** Immer da

Präsent. Still. Verlässlich.

Jeden Morgen, kurz nach dem Nebel, tritt er auf den Balkon. Kaffee in der Hand. Er sagt nichts. Aber er ist immer da.

```rust
fn main() {
    println!("Willkommen in Rust City.");
    // Er fängt an. Er beendet. Er ist immer da.
}
```

**Drei Momente mit Okto:**
- Kap. 1: Okto sieht ihn von der Gasse. Schaut kurz. Schiebt weiter.
- Kap. 7: fn main() nickt. Okto nickt zurück. Zum ersten Mal.
- Kap. 11: Okto steht neben ihm auf dem Balkon. Alle acht Arme aktiv.

---

## 🕵️ Detective Ownership

**Bezirk:** Stack District — **Konzept:** Ownership — **Kapitel:** 2

Ruhig. Präzise. Väterlich.

Ownership trägt das Konzept von Kapitel 2: ein Wert, ein Besitzer. Was dir gehört, gehört nur dir — und damit auch die Verantwortung dafür. Er kann Memory-Leaks und Dangling References riechen. Kein Tool — reiner Instinkt, geschärft durch Verlust.

```rust
let stadt = String::from("Rust City");
let besitzer = stadt;         // übertragen — nicht kopiert
// println!("{}", stadt);     // ❌ — existiert nicht mehr
println!("{}", besitzer);     // ✅ — Verantwortung übertragen
```

**Sein wichtigster Satz zu Okto** — Kapitel 9:
> *„Benenn es. Dann können wir es beheben."*

---

## 👮 Officer Borrowing

**Bezirk:** Reference District — **Konzept:** Borrowing — **Kapitel:** 3 + 4 — **Namensschild:** `ID: &'static mut self`

Knallhart. Theatralisch. Fair.

Officer Borrowing trägt das Dach über Kapitel 3 und 4. Er kennt beide Regeln des Borrowing — und stellt sicher dass sie eingehalten werden. Nicht weil er Regeln liebt, sondern weil er weiss was passiert wenn sie fehlen.

**Sein Konzept lebt in zwei Charakteren:**

| Charakter | Regel | Kapitel |
|-----------|-------|---------|
| Agentin Alias | Borrowing Regel 1 — `&T` | Kap. 3 |
| Max Mutation | Borrowing Regel 2 — `&mut T` | Kap. 4 |

Alias und Max sind nicht eigenständige Konzepte — sie sind die zwei Seiten von Borrowing's Gesetz, gelebt und erfahren.

*Officer Borrowing taucht in Kap. 2 auf weil er den Fall untersucht — nicht weil sein Konzept dort gelehrt wird. Sein Konzept gehört in Kap. 3 und 4.*

```rust
let mut wert = String::from("Rust City");

// Regel 1 — &T: viele lesen, kein Problem
let r1 = &wert;
let r2 = &wert;
println!("{} — {}", r1, r2); // ✅

// Regel 2 — &mut T: einer schreibt, alleine
let r3 = &mut wert;
r3.push_str(" — sicher");
println!("{}", r3);           // ✅

// Niemals beides gleichzeitig.
```

**Sein Satz:**
> *„Ein Amateur bricht Regeln weil er sie nicht versteht. Ein Profi kann sie biegen — weil er sie vollständig versteht."*

---

## 🕵️‍♀️ Agentin Alias

**Bezirk:** Heap District, Glasraum — **Konzept:** Borrowing Regel 1 — `&T` — **Kapitel:** 3

Elegant. Ungreifbar. Präzise.

Alias lebt Borrowing's erste Regel durch ihr Wesen — nicht durch Erklärung. Viele können dasselbe sehen, gleichzeitig, solange niemand eingreift. Keine Kollision. Stärke durch Teilen.

Sie ist die elegante Seite von Officer Borrowing's Gesetz.

In Kapitel 3 bemerkt sie Okto kaum. In Kapitel 10 begegnet sie ihm als Gleiche.

---

## 🎭 Max Mutation

**Konzept:** Borrowing Regel 2 — `&mut T` — **Kapitel:** 4 — Kein eigenes Kapitel

Impulsiv. Neugierig. Ehrlich.

Max lebt Borrowing's zweite Regel — zuerst falsch, dann richtig. Er greift ins Falsche ein. Absturz. Er versteht warum. Beim zweiten Mal: ins Eigene, alleine, vollständig verantwortlich.

Er ist nicht böse. Er ist strukturlos. Das ist kein Charakter-Fehler — das ist ein Typ-Fehler. Typ-Fehler kann man beheben.

Er ist die harte Seite von Officer Borrowing's Gesetz.

---

## 🎭 Madame Enum

**Standort:** Rand des Heap Districts — **Konzept:** Enums, Pattern Matching — **Kapitel:** 5

Weise. Geduldig. Klar.

Sie sieht jeden Bewohner von Rust City so wie er wirklich ist. Sie sieht Okto — und weiss sofort was er ist. Er weiss es noch nicht.

> *„Du hast acht mögliche Arme. Ich nenne dich Okto."*

---

## 📖 Kapitel-Übersicht Buch 1

### Die vier Ebenen — müssen in jedem Kapitel übereinstimmen:
**Story · Rust-Konzept/Code · Lebensregel · Arm**

---

### Kapitel 1 — Willkommen in Rust City
**Charakter:** fn main() im Hintergrund
**Rust-Konzept:** Crates, Modules, Cargo. C-Ära & Pointer Pete.
**Code:** `id_register` im Fehler-Display. Pointer Pete: Ownership ohne Regeln.
**Lebensregel:** *Rust City schützt dich vor Fehlern, die du noch nicht kennst. Du musst nicht alles wissen — die Regeln passen auf dich auf.*
**Arm #1:** Aktiv. Kribbeln #2: kaum spürbar.

---

### Kapitel 2 — Detective Ownership & Officer Borrowing
**Charakter:** Detective Ownership trägt das Konzept. Officer Borrowing taucht auf — als Ermittler, nicht als Lehrer.
**Rust-Konzept:** Ownership — ein Wert, ein Besitzer.
**Code:** `id_register` — gleichzeitig lesen und schreiben. Absturz.
**Lebensregel:** *Was dir gehört, gehört nur dir — und damit auch die Verantwortung dafür.*
**Arm #1:** Noch aktiv. Kribbeln #2: stärker.

---

### Kapitel 3 — Agentin Alias
**Charakter:** Officer Borrowing (Gesetz) + Agentin Alias (Regel 1 gelebt)
**Rust-Konzept:** Borrowing Regel 1 — `&T`. Viele lesen gleichzeitig, kein Konflikt.
**Code:** `ausweis` — mehrere `&ausweis` gleichzeitig. ✅
**Lebensregel:** *Viele Augen brechen nichts — solange keine Hand greift.*
**Arm #2:** Erwacht. Kribbeln #3: beginnt.

---

### Kapitel 4 — Max Mutation
**Charakter:** Officer Borrowing (Gesetz) + Max Mutation (Regel 2 gelebt)
**Rust-Konzept:** Borrowing Regel 2 — `&mut T`. Wer schreibt ist alleine verantwortlich.
**Code:** `id_register` — Max liest (`&id_register`), findet Eintrag, verändert nichts Fremdes.
**Lebensregel:** *Greif nur ins Deine. Dann aber vollständig.*
**Arm #1:** Vertieft. Kribbeln #3: wärmer.

---

### Kapitel 5 — Madame Enum und ihre Typen
**Charakter:** Madame Enum
**Rust-Konzept:** Enums, Structs, Pattern Matching.
**Code:** `enum Okto` + `enum Ausweis` — alle Zustände, `match` erzwingt jeden Fall.
**Lebensregel:** *Die Welt hat viele Typen. Keiner ist falsch — nur falsch eingesetzt.*
**Arm #3 + #4:** Erwachen gleichzeitig. Kribbeln #5: beginnt.

---

## 🧭 Motto-Threading

| Kapitel | Moment |
|---------|--------|
| Kap. 1 | Okto liest das Motto am Tor. Versteht es nicht. Schiebt weiter. |
| Kap. 4 | Okto *fühlt* Satz 1: *„Was du besitzt, das pflege."* |
| Kap. 8 | Okto *lebt* Satz 2: *„Was du leihst, das schütze."* |
| Kap. 11 | Okto versteht alle drei Sätze vollständig. |

---

## ✏️ Die goldene Schreibregel

Alle Kapitel aus Okto's Perspektive. Kein Kapitel ohne Okto. Immer am Rand.

**Der Filter für jeden Satz:** *Gibt das dem Leser Sicherheit — oder nimmt es ihm welche?*

**Die vier Ebenen müssen übereinstimmen.** Wenn Story, Code, Lebensregel und Arm nicht dasselbe sagen — ist das Kapitel nicht fertig.

---

## ❌ Was nie passiert

- Das Wort «Oktopus» fällt nie
- Ein Kapitel ohne Okto
- Max bekommt ein eigenes Kapitel
- Okto gibt auf oder wird selbstmitleidig
- Own und Borrowing werden Freunde
- Glück wird versprochen — nur Schutz durch Struktur
- Das Motto wird erklärt — es wird erlebt
- Moralische Belehrungen — die Geschichte zeigt, sie predigt nicht