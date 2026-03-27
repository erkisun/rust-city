# 🏙️ Rust City — Roadmap v9

**Drei Bücher. Ein Okto. Ein Motto.**

---

## Das Motto

> **Was du besitzt, das pflege.**
> **Was du leihst, das schütze.**
> **Was du nicht mehr brauchst, gib es der Welt zurück.**

*Kap. 4: Satz 1 gefühlt · Kap. 8: Satz 2 gelebt · Kap. 11: alle drei verstanden*

---

## Die zentrale Frage

> *Findet Okto seinen Platz — und versteht er, was am Eingangstor steht?*

---

## Die Philosophie

| Kein Pech | Okto's Geheimnis |
|-----------|-----------------|
| Rust City verspricht kein Glück. Es verspricht: kein Pech — wenn du die Regeln kennst. | Er ist Modell TC-0008. Einen Arm. Acht möglich. Er weiss es nicht. Das Wort «Oktopus» fällt nie. |

---

## Die goldene Schreibregel

Alle Kapitel aus Okto's Perspektive. Kein Kapitel ohne Okto. Immer am Rand.

**Die vier Ebenen müssen in jedem Kapitel übereinstimmen:**
Story · Rust-Konzept/Code · Lebensregel · Arm

**Der Filter:** *Gibt das dem Leser Sicherheit — oder nimmt es ihm welche?*

---

## 📗 BUCH 1 — Wer bin ich? *(Kapitel 1–5)*

**Was der Leser kann:** Ownership, Borrowing (`&T` + `&mut T`), Enums
**Was der Leser fühlt:** *Okto hat seinen Namen. Vier Arme aktiv. Kribbeln an #5 hat begonnen.*

---

### Kapitel 1 — Willkommen in Rust City
**Charakter:** fn main() im Hintergrund
**Rust-Konzept:** Crates, Modules, Cargo. C-Ära & Pointer Pete.
**Story:** Okto findet den abgestürzten TC-0003. Er versteht den Fehler nicht. Die Regeln schützen ihn — auch wenn er sie noch nicht kennt.
**Code:** `id_register` im Fehler-Display. Pointer Pete zeigt was ohne Regeln passiert.

**📌 Lebensregel #1:**
> *Rust City schützt dich vor Fehlern, die du noch nicht kennst. Du musst nicht alles wissen — die Regeln passen auf dich auf.*

**🦾 Arm #1 — Aktiv:** Sammeln. Leeren. Zurückgeben.
**Kribbeln #2:** Kaum spürbar. Fast eingebildet.

---

### Kapitel 2 — Detective Ownership & Officer Borrowing
**Charakter:** Detective Ownership (Konzept) · Officer Borrowing (Ermittler, noch kein Lehrer)
**Rust-Konzept:** Ownership — ein Wert, ein Besitzer.
**Story:** Own und Borrowing untersuchen den TC-0003. Okto erlebt: Own trägt die Untersuchung alleine. Was ihm gehört — der Fall — trägt er vollständig. Borrowing's Gesetz wird angedeutet. Bewusst unvollständig.
**Code:** `id_register` — gleichzeitig lesen und schreiben. Absturz sichtbar.

**📌 Lebensregel #2:**
> *Was dir gehört, gehört nur dir — und damit auch die Verantwortung dafür.*

**🦾 Arm #1 — Noch aktiv:** Halten. Besitzen. Loslassen.
**Kribbeln #2:** Stärker. Noch nicht warm.

---

### Kapitel 3 — Agentin Alias
**Charakter:** Officer Borrowing (Dach) + Agentin Alias (Borrowing Regel 1 gelebt)
**Rust-Konzept:** Borrowing Regel 1 — `&T`. Viele lesen gleichzeitig. Solange niemand schreibt, kein Konflikt.
**Story:** Alias zeigt `&T` durch ihr Wesen. Okto sieht: viele Augen, keine Hand, kein Absturz. Das System bleibt stabil weil niemand eingreift. Arm #2 erwacht.
**Code:** `ausweis` — mehrere `&ausweis` gleichzeitig. ✅ Kein Konflikt.

**📌 Lebensregel #3:**
> *Viele Augen brechen nichts — solange keine Hand greift.*

**🦾 Arm #2 — Erwacht:** Beobachten. Zwei Richtungen gleichzeitig. Wie Alias.
**Kribbeln #3:** Beginnt am Ende des Kapitels.

---

### Kapitel 4 — Max Mutation
**Charakter:** Officer Borrowing (Dach) + Max Mutation (Borrowing Regel 2 gelebt)
**Rust-Konzept:** Borrowing Regel 2 — `&mut T`. Wer eingreift ist alleine verantwortlich.
**Story:** Max kommt zurück. Diesmal nur lesen — findet seinen Ausweis im Register. Okto erlebt: eingreifen darf man — aber nur ins Eigene, und dann vollständig. Auf dem Heimweg fühlt Okto Satz 1 des Mottos zum ersten Mal.
**Code:** `id_register` — Max liest (`&id_register`), findet Eintrag, verändert nichts Fremdes. ✅

*Erst nach Kapitel 4 ist Borrowing vollständig verstanden.*

**📌 Lebensregel #4:**
> *Greif nur ins Deine. Dann aber vollständig.*

**🦾 Arm #1 — Vertieft:** Besitzen bedeutet Verantwortung tragen. Vollständig.
**Kribbeln #3:** Wärmer.

---

### Kapitel 5 — Madame Enum und ihre Typen
**Charakter:** Madame Enum
**Rust-Konzept:** Enums, Structs, Pattern Matching — verschiedene Zustände, keiner ist falsch.
**Story:** Madame Enum sieht Okto wirklich. Sie nennt ihn Okto. Max' Fall wird eingeordnet: kein Charakter-Fehler, ein Typ-Fehler. Max holt seinen Ausweis — diesmal richtig.
**Code:** `enum Okto` + `enum Ausweis` — alle Zustände, `match` erzwingt jeden Fall.

**📌 Lebensregel #5:**
> *Die Welt hat viele Typen. Keiner ist falsch — nur falsch eingesetzt.*

**🦾 Arm #3 — Erwacht:** Einordnen. Typen erkennen ohne zu urteilen.
**🦾 Arm #4 — Erwacht:** Verstehen. Zusammenhänge sehen die andere übersehen.
**Kribbeln #5:** Beginnt.

---

✦ *Ende Buch 1 — Okto hat seinen Namen. Vier Arme aktiv. Kribbeln an #5 hat begonnen.* ✦

---

## 📘 BUCH 2 — Was kann ich? *(Kapitel 6–9)*

**Was der Leser kann:** Match/Patterns, Crates/Modules, Collections, Error Handling
**Was der Leser fühlt:** *Okto hat seinen festen Platz. Er scheitert, benennt es, wächst daran.*

| Kap. | Charakter | Rust-Konzept | Lebensregel | Arm |
|------|-----------|-------------|-------------|-----|
| 6 | Officer Borrowing — Nicken | Match, Patterns | *Wer Muster erkennt, muss das Leben nicht kontrollieren — er versteht es.* | — |
| 7 | fn main() — Nicken | Crates, Modules, pub vs private | *Wer seinen Platz kennt, kann ihn ausfüllen.* | #5 erwacht |
| 8 | Okto als stiller Mentor | Collections: Vec, HashMap, Iterators | *Was du besitzt, das pflege. Was du leihst, das schütze.* | #6 erwacht |
| 9 | Detective Ownership | Result, Option, ?, panic vs graceful | *Ein Fehler der benannt wird, kann behoben werden. Versteckt, wächst er.* | — |

✦ *Ende Buch 2 — Sechs Arme aktiv. Kribbeln an #7 hat begonnen.* ✦

---

## 📙 BUCH 3 — Was bin ich wirklich? *(Kapitel 10–11)*

**Was der Leser kann:** Traits, Lifetimes
**Was der Leser fühlt:** *Okto versteht das Motto vollständig.*

| Kap. | Charakter | Rust-Konzept | Lebensregel | Arm |
|------|-----------|-------------|-------------|-----|
| 10 | Agentin Alias — als Gleiche | Traits, trait bounds, impl | *Was du bist, ist wichtiger als wie du heisst.* | #7 erwacht |
| 11 | fn main() — Schulter an Schulter | Lifetimes, lifetime annotations | *Alles was lebt hat eine Lifetime. Nutze sie.* | #8 erwacht |

✦ *Ende Buch 3 — Okto versteht das Motto vollständig.* ✦

---

## 🦾 Okto's 8 Arme

| Arm | Kap. | Fähigkeit | Kribbeln ab |
|-----|------|-----------|-------------|
| #1 | 1 | Sammeln — leeren, zurückgeben | — |
| #2 | 3 | Beobachten — zwei Richtungen gleichzeitig | Kap. 1 |
| #3 | 5 | Einordnen — Typen erkennen ohne zu urteilen | Kap. 3 Ende |
| #4 | 5 | Verstehen — Zusammenhänge sehen die andere übersehen | Kap. 3 Ende |
| #5 | 7 | Bauen — Strukturen die über einen selbst hinausgehen | Kap. 5 Ende |
| #6 | 8 | Weitergeben — Wissen und Erfahrung teilen | Kap. 7 Ende |
| #7 | 10 | Identität — sich selbst kennen | Kap. 9 Ende |
| #8 | 11 | Schwarm — Teil von etwas Grösserem | Kap. 10 Ende |

*Kap. 4: kein neuer Arm — Arm #1 vertieft durch `&mut T`.*

---

## 🧭 Der Nordstern — 7 Fragen

| # | Frage | Filter |
|---|-------|--------|
| ① | Würde ein 13-Jähriger hier weiterlesen wollen? | Wenn nein — kürzen, nicht erklären. |
| ② | Ist Okto in dieser Szene? | Wenn nein — die Szene gehört nicht ins Buch. |
| ③ | Klingt das nach Okto — oder nach einem Lehrbuch? | Okto beobachtet, fragt sich, handelt leise. |
| ④ | Was ist die Lebensregel? | Wenn du sie nicht in einem Satz sagen kannst — ist das Kapitel nicht fertig. |
| ⑤ | Stimmen alle vier Ebenen überein? | Story · Code · Lebensregel · Arm — alle vier müssen dasselbe sagen. |
| ⑥ | Wo steht Okto mit dem Motto? | Kap. 1: liest. Kap. 4: fühlt Satz 1. Kap. 8: lebt Satz 2. Kap. 11: alle drei. |
| ⑦ | Welcher Arm kribbelt — und welcher erwacht? | Das Phantom-Kribbeln ist Okto's innerer Kompass. Und der des Lesers. |

---

## ❌ Was nie passiert

| | |
|---|---|
| ✕ | Das Wort «Oktopus» fällt nie |
| ✕ | Ein Kapitel ohne Okto |
| ✕ | Max bekommt ein eigenes Kapitel |
| ✕ | Okto gibt auf oder wird selbstmitleidig |
| ✕ | Own und Borrowing werden Freunde |
| ✕ | Glück wird versprochen — nur Schutz durch Struktur |
| ✕ | Das Motto wird erklärt — es wird erlebt |
| ✕ | Moralische Belehrungen — die Geschichte zeigt, sie predigt nicht |

---

*Für jeden der je das Gefühl hatte: nicht verstanden zu werden — willkommen.*

🏙️