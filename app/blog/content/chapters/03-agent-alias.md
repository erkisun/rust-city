# Agent Alias

*Rust City – Eine Geschichte über Besitz, Regeln und perfekten Code.*

## 🪐 Der Angriff auf Agent Alias 

Der Planet `main` riecht nach überhitztem Silizium und frischem Bitstrom. Eine dichte Schicht aus **Traits** und **Lifetimes** hält alles zusammen. Städte gliedern sich in **Modules**, Bezirke heißen **Crates**. Manche Bewohner werden von der reinen Logik benommen, andere süchtig. Sie nennen es **„Compiling High“** – wenn der Compiler alles akzeptiert und das perfekte Programm läuft. Die Sucht nach fehlerfreiem Code hat schon viele in die Überdosis getrieben: endlose **Loop-Träume**, **Memory-Leak-Halluzinationen**, **Stack-Overflow-Wahn**.

## 🕵️  Die Vorgeschichte: Regeln brechen um sie zu schützen !

Bevor Rust City gegründet wurde, gab es eine dunklere Zeit. Man nannte sie die **"C-Ära"** – eine Zeit, in der Speicherzugriffe chaotisch und gefährlich waren. 
Der berühmteste ungelöste Fall war der **Mord an Pointer Pete** in der alten Speicher-Bibliothek.

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
    // Die Bibliothek kauft ein neues Buch
    let buch = String::from("Geheimakte X"); 
    
    { // EIN LESER BETRITT DIE BIBLIOTHEK (SCOPE)
        let leser = buch; // ⚠️  BIBLIOTHEKAR POINTER PETE "LEIHT" DAS BUCH AUS
        
        // Hier passiert etwas Merkwürdiges ..
        // In der C-Ära gab es keine Borrowing-Regeln!
        // Der Leser nimmt das Buch einfach mit ..
        
    } // ❌ LESER VERLÄSST DIE BIBLIOTHEK
      // UND DAS BUCH WIRD AUTOMATISCH GELÖSCHT!
    
    // Später versucht jemand, das Buch zu finden und begeht dabei einen Mord
    println!("Suche nach: {}", buch); 
    // 💥 ERROR! BUCH EXISTIERT NICHT MEHR
    // PROGRAM ERROR : MORD GESCHEHEN
    
    // In der C-Ära passierte das STÄNDIG:
    // - Bücher verschwanden (use-after-free)
    // - Zwei Leser änderten gleichzeitig ein Buch (data races)
    // - Bücher wurden doppelt gelöscht (double free)
}
```

Was hier schief ging:

    Buch wurde an Leser übergeben (move), nicht ausgeliehen (borrow)

    Als Leser den Scope verließ, wurde Buch gelöscht

    Aber die Bibliothek wusste nichts davon und versuchte später, darauf zuzugreifen

    Resultat: Ein dangling pointer – eine Referenz auf nicht-existierenden Speicher

Das Opfer: Pointer Pete, ein Bibliothekar, der immer sagte: "Ich weiß genau, wo jedes Buch ist." Bis er auf ein nicht-existierendes Buch zeigte und dabei draufging ..

</details>

Auch nach dem Großen Compiler-Update hörten die Morde nie ganz auf – aber sie wurden vorhersehbar. 
Wenn heute ein Buch verschwindet, weiß der Borrow Checker sofort, wer es zuletzt hatte.

## 👤 Der Protagonist: Detective Ownership

Er heisst Own, aber alle nennen ihn **Detective Ownership**. Mit 17 lebt er im **Stack District**, wo alles ordentlich und vorhersehbar ist, viel angenehmer als im **Heap District**. Seine Eltern waren Kernel-Entwickler, starben bei einem mysteriösen **`unsafe`-Block-Exploit**. Seitdem lebt er von kleinen Bug-Bounties – er repariert, was andere kaputt kompilieren.

Own hat eine Gabe: Er riecht **Memory-Leaks und Dangling References**. Heute roch es nach .. **`None`** .. nach leerer Promise, nach **Wert ohne Besitzer.**

## 🚨 Der Vorfall

Auf dem Weg zum **Memory-Market** sieht Own den ersten Roboter. Einen **Trash-Collector-Bot**, der normalerweise die Fragmente aus dem Heap District einsammelt. Er steht still, zittert, sein Display zeigt:

ERROR: expected value, found null .. thread 'main' **panicked** at 'called Option::unwrap() on a None value`

Dahinter: Dutzende weitere Roboter, alle in derselben Starre. 
Eine **Null-Pointer-Epidemie** ? .. Owns Nase kribbelt. Das ist kein Zufall, für ihn nicht .. vielleicht Absicht ?

---
[Nächstes Kapitel →](/app/blog/content/chapters/02-detective-ownership-and-officer-borrowing.md)  
