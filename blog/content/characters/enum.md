# 🎭 Madame Enum

> *Sie urteilt nicht. Sie ordnet. Das ist ein grosser Unterschied.*
>
> *She doesn't judge. She sorts. That's a big difference.*

---

## DE 🇩🇪

**Funktion:** Typ-Analytikerin, Rust City Typ-Bezirk  
**Bezirk:** Typ-Bezirk  
**Büro:** Ruhig, sortiert, jede Schublade beschriftet  
**Status:** Immer verfügbar — für alle die bereit sind

---

### Wer ist Madame Enum?

Madame Enum weiss was du bist — bevor du es selbst weisst.

Ihr Büro im Typ-Bezirk ist anders als alles in Rust City: kein Lärm, keine Hektik, keine unsortierten Fragmente. Jede Schublade beschriftet. Jeder Zustand benannt. Alles hat seinen Platz.

Sie schaut lange bevor sie spricht. Sie geht langsam um dich herum. Schweigt. Prüft. Und wenn sie einen Satz sagt, sitzt er für immer.

---

### Drei Adjektive

**Weise. Geduldig. Klar.**

---

### Ihr wichtigster Moment

Kapitel 5. Okto wird zu ihr gerufen. Er weiss nicht warum.

Sie geht langsam um ihn herum. Schweigt. Prüft. Dann:

> **„Du hast acht mögliche Arme. Ich nenne dich Okto."**

Er sagt nichts. Aber er speichert es. Für immer.

---

### Ihre Regel

Madame Enum weiss: Ein Typ ist nicht falsch. Er ist nur manchmal falsch eingesetzt.

```rust
// Jeder Zustand hat einen Namen — keiner ist schlechter als der andere
enum BewohnerVonRustCity {
    Trashbot { arme: u8 },           // Okto
    Detective { erfahrung: u32 },    // Ownership
    Officer { dienstjahre: u32 },    // Borrowing
    Agentin { deckname: String },    // Alias
    Besucher,                        // Max — noch ohne festen Typ
    Weise { weisheit: String },      // Madame Enum selbst
    Ursprung,                        // fn main()
}

// Pattern Matching — jeder Typ bekommt seine Behandlung
fn beschreibe(bewohner: &BewohnerVonRustCity) {
    match bewohner {
        BewohnerVonRustCity::Trashbot { arme } =>
            println!("Ein Trashbot mit {} Arm/Armen.", arme),
        BewohnerVonRustCity::Detective { erfahrung } =>
            println!("Detective mit {} Jahren Erfahrung.", erfahrung),
        BewohnerVonRustCity::Besucher =>
            println!("Noch kein fester Typ. Noch nicht."),
        _ =>
            println!("Jeder hat seinen Platz."),
    }
}
```

---

### Was sie über die Bewohner weiss

| Charakter | Typ | Eingesetzt als |
|-----------|-----|----------------|
| Okto | `Trashbot { arme: 1..=8 }` | Sammler → Erbauer → Identität |
| Ownership | `Detective { präzise: true }` | Ordnungshüter des Besitzes |
| Borrowing | `Officer { fair: true }` | Wächter der Regeln |
| Alias | `Agentin { mehrfach: true }` | Meisterin der Referenzen |
| Max | `Besucher` | Noch kein fester Typ — noch |
| fn main() | `Ursprung` | Der verlässliche Anfang |

---

### Was Madame Enum nie tut

- Urteilen
- Herablassend sein
- Ungeduldig werden

---

## EN 🇬🇧

**Function:** Type Analyst, Rust City Type District  
**District:** Type District  
**Office:** Quiet, sorted, every drawer labelled  
**Status:** Always available — for those who are ready

---

### Who is Madame Enum?

Madame Enum knows what you are — before you know it yourself.

Her office in the Type District is unlike anything else in Rust City: no noise, no rush, no unsorted fragments. Every drawer labelled. Every state named. Everything has its place.

She watches for a long time before she speaks. She walks slowly around you. Silence. Examination. And when she says a sentence, it stays forever.

---

### Three adjectives

**Wise. Patient. Clear.**

---

### Her most important moment

Chapter 5. Okto is called to her. He doesn't know why.

She walks slowly around him. Silence. Examination. Then:

> **"You have eight possible arms. I call you Okto."**

He says nothing. But he stores it. Forever.

---

### Her rule

Madame Enum knows: A type is not wrong. It's just sometimes used in the wrong place.

```rust
// Every state has a name — none is worse than another
enum ResidentOfRustCity {
    Trashbot { arms: u8 },           // Okto
    Detective { experience: u32 },   // Ownership
    Officer { years: u32 },          // Borrowing
    Agent { codename: String },      // Alias
    Visitor,                         // Max — no fixed type yet
    Wise { wisdom: String },         // Madame Enum herself
    Origin,                          // fn main()
}

// Pattern Matching — every type gets its treatment
fn describe(resident: &ResidentOfRustCity) {
    match resident {
        ResidentOfRustCity::Trashbot { arms } =>
            println!("A trashbot with {} arm(s).", arms),
        ResidentOfRustCity::Detective { experience } =>
            println!("Detective with {} years of experience.", experience),
        ResidentOfRustCity::Visitor =>
            println!("No fixed type yet. Not yet."),
        _ =>
            println!("Everyone has their place."),
    }
}
```

---

### What she knows about the residents

| Character | Type | Used as |
|-----------|------|---------|
| Okto | `Trashbot { arms: 1..=8 }` | Collector → Builder → Identity |
| Ownership | `Detective { precise: true }` | Guardian of possession |
| Borrowing | `Officer { fair: true }` | Guardian of the rules |
| Alias | `Agent { multiple: true }` | Master of references |
| Max | `Visitor` | No fixed type yet — not yet |
| fn main() | `Origin` | The reliable beginning |

---

### What Madame Enum never does

- Judge
- Be condescending
- Become impatient