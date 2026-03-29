 🇩🇪 [Deutsch](#de) · 🇬🇧 [English](#en)

---

<a name="de"></a>
### 🇩🇪 Deutsch

---

## 📗 Kapitel 1 — Rust City

Tief im All, um einen längst vergessenen Gasriesen, kreist der kleine Mond Rust-K04. Nur bei Einstrahlung von Licht sieht man seine Oberfläche leuchten, bedeckt von der Legende - **Rust City**.

Rust City ist ein gigantischer Komplex aus Stahl, Silizium und strengen Regeln. Wer hier lebt, lebt nach den Regeln der Stadt. Ohne Ausnahme und ohne Alternative. Die Stadt gliedert sich in riesige Bezirke (**Crates**), jeder ein eigenes Universum mit strengen Ein- und Ausgangsregeln. Die Bezirke sind unterteilt in Stadtteile (**Modules**) in denen die eigentliche Arbeit passiert.

Hier gilt ein einziges Gesetz, älter als jede Programmiersprache, älter als Computer selbst. Es steht in Stein gemeisselt über dem Eingangstor von Rust City :

**„.. Was du besitzt, das pflege .. Was du leihst, das schütze .. Was du nicht mehr brauchst, gib es der Welt zurück .."**

Physiker nennen es das Gesetz der Erhaltung - nichts entsteht aus Nichts, nichts verschwindet spurlos. Biologen nennen es Kreislauf des Lebens. Ethiker nennen es Verantwortung.

Andere Wissenschaftler nennen es Logik, wovon manche Bewohner benommen werden, andere süchtig. Sie nennen es **„Compiling High"** - wenn der Compiler alles akzeptiert und das perfekte Programm läuft. Die Sucht nach fehlerfreiem Code hat schon viele in die Überdosis getrieben: endlose **Loop-Träume**, **Memory-Leak-Halluzinationen**, **Stack-Overflow-Wahn**. Das ist Rust City.

---

## 🕵️ Die Vorgeschichte

Bevor Rust City gegründet wurde, gab es eine dunklere Zeit. Man nannte sie die **"C-Ära"** – eine Zeit, in der Speicherzugriffe chaotisch und gefährlich waren.
Der berühmteste ungelöste Fall war der **Mord an Pointer Pete** in der alten Speicher-Bibliothek auf dem Mond Rust-K73.

Die Akte ist noch heute in den Archiven einsehbar:

<details>
<summary>📜 <strong>Cold Case: Mord an Pointer Pete (Klicken zum Anzeigen)</strong></summary>

```rust
// ============================================
// AKTENNOTIZ: FALL #001 - MORD AN POINTER PETE
// ORT: Speicher-Bibliothek, Memory City (vor Rust City)
// ZEIT: Während der C-Ära
// ============================================
fn main() {
    // DIE BIBLIOTHEK KAUFT EIN NEUES BUCH
    let buch = String::from("Buch : Geheimakte X (Thriller)");

    // EIN LESER BETRITT DIE BIBLIOTHEK (SCOPE)
    {
        // ⚠️ BIBLIOTHEKAR POINTER PETE "LEIHT" DAS BUCH AUS
        let leser = buch;

        // In der C-Ära gab es keine Borrowing-Regeln ..
        // Der Leser konnte das Buch einfach mitnehmen ..

    } // ❌ LESER VERLÄSST DIE BIBLIOTHEK (SCOPE)
      // UND DAS BUCH WIRD AUTOMATISCH GELÖSCHT!

    // 💥 ERROR! BUCH EXISTIERT NICHT MEHR
    println!("Suche nach: {}", buch);

    // In der C-Ära passierte das ständig:
    // - Bücher verschwanden (use-after-free)
    // - Zwei Leser änderten gleichzeitig ein Buch (data races)
    // - Bücher wurden doppelt gelöscht (double free)
    // - Resultat: Ein dangling pointer – eine Referenz auf nicht-existierenden Speicher
}
```

</details>

Das Opfer, der Bibliothekar Pointer Pete, hatte immer gesagt : "Ich weiß genau, wo jedes Buch ist." .. bis er auf ein nicht-existierendes Buch zeigte und dabei draufging ..

---

## 🏙️ Die Gegenwart

Wie jeden Morgen nahm Okto seinen üblichen Spaziergang im alten Industriegebiet und streifte durch die Gasse 19.

Okto sammelt. Das ist was er tut.

Sein linker Arm - der einzige den er hat - greift, hebt, sortiert. Fragment nach Fragment. Er denkt nicht viel dabei. Oder vielleicht denkt er doch - er weiss nur nicht genau wie man das nennt .. ein Kribbeln ? Ein leises Verarbeiten ?

Er schiebt weiter.

Auf dem Weg zum Memory-Market steht ein erstarrter **Trash-Collector-Bot**, auch ein Roboter wie er. Auffällig, weil so einer normalerweise nie still steht. Der Roboter macht keinen Wank. „Was ist da los ?" fragt sich Okto und geht zu ihm hinüber.

Okto stellt seinen Behälter ab. Beugt sich vor. Das ist nicht sein Job - er ist ein Roboter, kein Mechaniker, aber er schaut trotzdem auf das Display :

```
ERROR: cannot assign to 'id_register' because it is borrowed
thread 'main' panicked at 'dangling pointer detected'
```

*Scheint etwas nicht mehr vorhanden zu sein, weil bereits ausgeliehen .. Panik .. ?*

Die Frage lässt ihn nicht los, es kribbelt in ihm.

Und dann - Schritte.

Andere Schritte als seine.

---

### 📌 Lebensregel #1

> **Rust City schützt dich vor Fehlern, die du noch nicht kennst. Du musst nicht alles wissen — die Regeln passen auf dich auf.**

---

### 🦾 Arm #1 — Aktiv

*Sammeln. Leeren. Zurückgeben.*

### 🦾 Arm #2 — Kribbelt

*Kaum spürbar. Fast eingebildet.*

---

### 📎 Akte: Was ist Rust City?

*Gefunden in der Bibliothek des Verwaltungsturms. Abschnitt: Grundlagen.*

```rust
// Cargo.toml — die Identitätskarte jedes Projekts in Rust City
// Jedes Projekt hat einen Namen. Eine Version. Regeln.

[package]
name    = "rust-city"
version = "0.1.0"
edition = "2021"

// fn main() — der Ursprung
// Jede Geschichte in Rust City beginnt hier.

fn main() {
    println!("Willkommen in Rust City.");
}
```

*Notiz am Rand, handgeschrieben:*  
`// Rust fragt immer zuerst: Wem gehört das? Wie lange? Und wer darf schauen?`

---

*Ende Kapitel 1.*

*In Gasse 19 liegen schwere Schritte auf dem Pflaster.*  
*Zwei Männer. Ledercoat. Uniform.*  
*Okto kennt sie nicht. Noch nicht.*

---

---

<a name="en"></a>
## 🇬🇧 English

---

## 📗 Chapter 1 — Rust City

Deep in space, orbiting a long-forgotten gas giant, the small moon Rust-K04 drifts. Only when light strikes its surface does it glow — covered by the legend of **Rust City**.

Rust City is a gigantic complex of steel, silicon, and strict rules. Those who live here live by the rules of the city. Without exception and without alternative. The city is divided into vast districts (**Crates**), each its own universe with strict entry and exit rules. The districts are subdivided into neighbourhoods (**Modules**) where the actual work happens.

One single law governs here, older than any programming language, older than computers themselves. It is carved in stone above the gate of Rust City :

**".. What you own, tend to it .. What you borrow, protect it .. What you no longer need, give it back to the world .."**

Physicists call it the law of conservation — nothing is created from nothing, nothing disappears without a trace. Biologists call it the cycle of life. Ethicists call it responsibility.

Other scientists call it logic, which leaves some residents dazed and others addicted. They call it **"Compiling High"** — when the compiler accepts everything and the perfect program runs. The addiction to error-free code has driven many to overdose: endless **loop dreams**, **memory-leak hallucinations**, **stack-overflow madness**. That is Rust City.

---

## 🕵️ The Backstory

Before Rust City was founded, there was a darker time. They called it the **"C-Era"** — a time when memory access was chaotic and dangerous.
The most famous unsolved case was the **murder of Pointer Pete** in the old memory library on the moon Rust-K73.

The file is still accessible in the archives today:

<details>
<summary>📜 <strong>Cold Case: The Murder of Pointer Pete (Click to expand)</strong></summary>

```rust
// ============================================
// CASE FILE: CASE #001 - MURDER OF POINTER PETE
// LOCATION: Memory Library, Memory City (before Rust City)
// TIME: During the C-Era
// ============================================
fn main() {
    // THE LIBRARY BUYS A NEW BOOK
    let book = String::from("Book : Secret File X (Thriller)");

    // A READER ENTERS THE LIBRARY (SCOPE)
    {
        // ⚠️ LIBRARIAN POINTER PETE "LENDS OUT" THE BOOK
        let reader = book;

        // In the C-Era there were no borrowing rules ..
        // The reader could simply take the book ..

    } // ❌ READER LEAVES THE LIBRARY (SCOPE)
      // AND THE BOOK IS AUTOMATICALLY DELETED!

    // 💥 ERROR! BOOK NO LONGER EXISTS
    println!("Searching for: {}", book);

    // In the C-Era this happened constantly:
    // - Books disappeared (use-after-free)
    // - Two readers changed a book simultaneously (data races)
    // - Books were deleted twice (double free)
    // - Result: A dangling pointer — a reference to non-existent memory
}
```

</details>

The victim, librarian Pointer Pete, always said : "I know exactly where every book is." .. until he pointed to a book that no longer existed — and didn't survive the encounter ..

---

## 🏙️ The Present

Like every morning, Okto took his usual walk through the old industrial district and drifted through Alley 19.

Okto collects. That's what he does.

His left arm — the only one he has — reaches, lifts, sorts. Fragment by fragment. He doesn't think much about it. Or maybe he does — he just doesn't know what to call the thing happening inside him when he works. A tingle. A quiet processing.

He pushes on.

On the way to the Memory-Market, a frozen **Trash-Collector-Bot** stands motionless — a robot, just like him. Unusual, because one of those never stands still. The robot doesn't move an inch. "What's going on there?" Okto wonders, and walks over.

Okto sets down his container. Leans forward. This isn't his job — he's a robot, not a mechanic — but he looks at the display anyway :

```
ERROR: cannot assign to 'id_register' because it is borrowed
thread 'main' panicked at 'dangling pointer detected'
```

*Seems like something no longer exists because it was already borrowed .. panic .. ?*

The question won't let him go. Something tingles inside him.

And then — footsteps.

Different footsteps than his.

---

### 📌 Life Rule #1

> **Rust City protects you from mistakes you don't know yet. You don't have to know everything — the rules watch over you.**

---

### 🦾 Arm #1 — Active

*Collect. Empty. Return.*

### 🦾 Arm #2 — Tingling

*Barely noticeable. Almost imagined.*

---

### 📎 File: What is Rust City?

*Found in the library of the administration tower. Section: Fundamentals.*

```rust
// Cargo.toml — the identity card of every project in Rust City
// Every project has a name. A version. Rules.

[package]
name    = "rust-city"
version = "0.1.0"
edition = "2021"

// fn main() — the origin
// Every story in Rust City begins here.

fn main() {
    println!("Welcome to Rust City.");
}
```

*Margin note, handwritten:*  
`// Rust always asks first: Who owns this? For how long? And who's allowed to look?`

---

*End of Chapter 1.*

*In Alley 19, heavy footsteps echo across the cobblestones.*  
*Two men. Leather coat. Uniform.*  
*Okto doesn't know them. Not yet.*

---