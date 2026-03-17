
 🇩🇪 [Deutsch](#de) · 🇬🇧 [English](#en)

---

<a name="de"></a>
### 🇩🇪 Deutsch

---

## 📗 Kapitel 1 - Rust City

Tief im All, um einen längst vergessenen Gasriesen, kreist der kleine Mond Rust-K04. Nur bei Einstrahlung von Licht sieht man seine Oberfläche leuchten, bedeckt von der Legende - **Rust City**.

Rust City ist ein gigantischer Komplex aus Stahl, Silizium und strengen Regeln. Wer hier lebt, lebt nach den Regeln der Stadt. Ohne Ausnahme und ohne Alternative. Die Stadt gliedert sich in riesige Bezirke (**Crates**), jeder ein eigenes Universum mit strengen Ein- und Ausgangsregeln. Die Bezirke sind unterteilt in Stadtteile (**Modules**) in denen die eigentliche Arbeit passiert.

Hier gilt ein einziges Gesetz, älter als jede Programmiersprache, älter als Computer selbst. Es steht in Stein gemeisselt über dem Eingangstor von Rust City :

**„.. Was du besitzt, das pflege .. Was du leihst, das schütze .. Was du nicht mehr brauchst, gib es der Welt zurück ..“**

Physiker nennen es das Gesetz der Erhaltung - nichts entsteht aus Nichts, nichts verschwindet spurlos. Biologen nennen es Kreislauf des Lebens. Ethiker nennen es Verantwortung. 

Andere Wissenschaftler nennen es Logik, wovon manche Bewohner benommen werden, andere süchtig. Sie nennen es **„Compiling High“** - wenn der Compiler alles akzeptiert und das perfekte Programm läuft. Die Sucht nach fehlerfreiem Code hat schon viele in die Überdosis getrieben: endlose **Loop-Träume**, **Memory-Leak-Halluzinationen**, **Stack-Overflow-Wahn**.

Das ist Rust City.

## 🕵️  Die Vorgeschichte: Der Mord an Pointer Pete

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

Das Opfer, der Bibliothekar Pointer Pete, hatte immer gesagt : "Ich weiß genau, wo jedes Buch ist." .. bis er auf ein nicht-existierendes Buch zeigte und dabei draufging ..

</details>

## 🏙️ Eines Morgens

Wie jeden Morgen nahm Okto seinen üblichen Spaziergang im alten Industriegebiet und streifte durch die Gasse 19.

Okto sammelt. Das ist was er tut.

Sein linker Arm - der einzige den er hat - greift, hebt, sortiert. Fragment nach Fragment. Er denkt nicht viel dabei. Oder vielleicht denkt er doch - er weiss nur nicht genau wie man das nennt .. ein Kribbeln ? Ein leises Verarbeiten ?

Er schiebt weiter.

Auf dem Weg zum Memory-Market steht ein erstarrter Roboter. Auffällig, weil so ein **Trash-Collector-Bot**, der normalerweise auch Fragmente aus dem Heap District einsammelt, nie still steht. Der Roboter macht keinen Wank. Okto ist nun neugierig und geht einige Schritte in Richtung des Roboters.

Okto stellt seinen Behälter ab. Beugt sich vor. Das ist nicht sein Job - er ist ein Trashbot, kein Mechaniker. Aber er ist neugierig und schaut trotzdem auf das Display :

```rust
ERROR: cannot assign to 'protokoll' because it is borrowed
thread 'main' **panicked** at 'dangling pointer detected`
```

*Wem gehört etwas — und wer darf es gerade benutzen?*

Die Frage lässt ihn nicht los, es kribbelt in ihm.

Und dann - Schritte.

Andere Schritte als seine.

---

### 📌 Lebensregel #1

> **Rust schützt dich vor Fehlern die du noch nicht kennst.**

---

### 🦾 Arm #1 — Aktiv

*Sammeln. Leeren. Zurückgeben.*

Okto hat einen Arm. Er weiss was er damit tut.  
Aber an einer Stelle — kaum spürbar, fast wie eingebildet — kribbelt es.  
Dort wo noch nichts ist.

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

### The Morning

The fog always comes first.

Before the first light grazes the towers of the Heap District, before footsteps fill the alleys, before anyone demands anything from anyone else — the fog arrives. It creeps through the cracks of the stack districts, hangs heavy over the canals of Stack Street, settles like a blanket over everything the night has left behind.

Okto knows the fog well.

He pushes his container through Alley 7-C, same as every morning. Left: an overturned crate container, contents scattered, no one has reported it. Right: the ruin of an old C-storage unit, abandoned for years, warning signs faded. Straight ahead: Rust City, waking up, humming, ready.

Okto collects. That's what he does.

His left arm — the only one he has — reaches, lifts, sorts. Fragment by fragment. He doesn't think much about it. Or maybe he does — he just doesn't know what to call the thing happening inside him when he works. A hum. A quiet processing. As if small voices inside him are calculating without him ever asking them to.

He pushes on.

At the corner leading to the main alley, he stops for a moment. Not because he's tired — trashbots don't get tired, as far as he knows. He stops because he always does. Because from this corner, the city gate becomes visible.

The great gate of Rust City.

Three sentences. Carved in stone. He knows them by heart, even though he's never really looked at them.

*What you own, tend to it.*  
*What you borrow, protect it.*  
*What you no longer need, give it back to the world.*

He doesn't really look at them today either.

He pushes on.

---

### fn main() and the Balcony

Every morning, just after the fog, fn main() steps out onto his balcony.

Okto can see him from the alley below — a calm figure on the second floor of the administration tower, coffee in hand, gaze over the city. fn main() never says anything. At least not downward. But he's always there. And that is — Okto isn't sure why — somehow important.

As if Rust City only truly wakes up once fn main() stands on the balcony.

Okto doesn't nod. He's a trashbot. Trashbots don't nod up at administrators.  
But he looks. Briefly. Then pushes on.

---

### The C-Era and Pointer Pete

In Alley 12 — where the Heap District bleeds into the older quarters — a monument still stands.

A weathered information board, mounted by the city long ago. Okto has passed it a hundred times. Today he stops in front of it.

```
⚠️  HISTORICAL MONUMENT — FILE NO. 001
    Location: Alley 12 / Corner of Old-C District

    POINTER PETE
    Pointer mechanic of the first generation.
    Active during the C-Era.

    Abilities: Unmatched.
    Problem: No one ever really knew who owned a memory block.

    Pete pointed to memory that wasn't his.
    Memory that had already been freed.
    Memory that belonged to no one.

    The city recovered.
    Pete didn't.

    LESSON:
    Power without rules protects no one.
    Not even the one who holds the power.
```

Okto reads the board. Really reads it, for the first time.

He doesn't understand everything. But he understands the last line.

*Power without rules protects no one.*

He pushes on. But the hum inside him has dropped one note lower.

---

### A Failed Trashbot

In Alley 19, he finds it.

Model TC-0003. Older than Okto. Motionless on the ground, red display, a rhythmic blinking that doesn't mean good code.

```
[ERROR] — MEMORY CONFLICT
Cause:  Two processes claim the same value.
Status: FROZEN
Fix:    UNKNOWN
```

Okto sets down his container. Leans forward. This isn't his job — he's a trashbot, not a mechanic. But he looks anyway.

Two processes. The same value. One wants to read while the other writes. Nobody has a clear picture of who the value actually belongs to right now.

The hum inside Okto grows louder.

*Who owns something — and who gets to use it right now?*

He doesn't know why that question matters to him. He's a trashbot. He has one arm. He collects fragments.

But the question won't let him go.

And then — footsteps.

Different footsteps than his.

---

### 📌 Life Rule #1

> **Rust protects you from mistakes you don't know yet.**

---

### 🦾 Arm #1 — Active

*Collect. Empty. Return.*

Okto has one arm. He knows what he does with it.  
But in one spot — barely noticeable, almost imagined — there's a tingle.  
Where nothing is yet.

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