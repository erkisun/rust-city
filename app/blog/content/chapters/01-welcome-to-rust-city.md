# Willkommen in Rust City

*Rust City – Eine Geschichte über Besitz, Regeln und perfekten Code.*

## 🪐 Die Mond - Rust-K04

Rust-K04 ist schwarz und öde, nur bei Einstrahlung von Licht sieht man seine Oberfläche bedeckt von der legendären Stadt - Rust City. Die Stadt ist ein gigantischer Komplex aus Stahl, Silizium und strengen Regeln. Wer hier lebt, lebt nach den Regeln der Stadt. Ohne Ausnahme und ohne Alternative.

Die Stadt gliedert sich in riesige Bezirke (**Crates**), jeder ein eigenes Universum mit strengen Ein- und Ausgangsregeln (pub und priv). Die Bezirke sind unterteilt in Stadtteile (**Modules**) in denen die eigentliche Arbeit passiert.

Die Cargo-Behörde, eine mächtige Institution in Rust City, ist das zentrale Dienst-Unternehmen der Stadt. Cargo übernimmt sämtliche Aufgaben wie Logistik, Verwaltung, Lieferungen und sogar das Bauen neuer Stadtteile wenn notwendig. Ein Güterzug von std nach collection zum HashMap -Bahnhof ? Kein Problem, **Cargo ::** regelt das. Ohne Cargo würde die Stadt im Chaos versinken, Bezirke wären nicht erreichbar, Abhängigkeiten würden fehlen und niemand wüsste, wie man einen neuen Stadtteil baut.

Manche Bewohner werden von der reinen Logik benommen, andere süchtig. Sie nennen es **„Compiling High“** – wenn der Compiler alles akzeptiert und das perfekte Programm läuft. Die Sucht nach fehlerfreiem Code hat schon viele in die Überdosis getrieben: endlose **Loop-Träume**, **Memory-Leak-Halluzinationen**, **Stack-Overflow-Wahn**.


## 🕵️  Die Vorgeschichte: Der Mord an Pointer Erki

Bevor Rust City gegründet wurde, gab es eine dunklere Zeit. Man nannte sie die **"C-Ära"** – eine Zeit, in der Speicherzugriffe chaotisch und gefährlich waren. 
Der berühmteste ungelöste Fall war der **Mord an Pointer Erki** in der alten Speicher-Bibliothek auf dem Mond Rust-K73.

Die Akte ist noch heute in den Archiven einsehbar:

<details>
<summary>📜 <strong>Cold Case: Mord an Pointer Erki (Klicken zum Anzeigen)</strong></summary>

```rust
// ============================================
// AKTENNOTIZ: FALL #001 - MORD AN POINTER Erki
// ORT: Speicher-Bibliothek, Memory City (vor Rust City)
// ZEIT: Während der C-Ära
// ============================================
fn main() {
    // Die Bibliothek kauft ein neues Buch
    let buch = String::from("Geheimakte X"); 
    
    { // EIN LESER BETRITT DIE BIBLIOTHEK (SCOPE)
        let leser = buch; // ⚠️  BIBLIOTHEKAR POINTER Erki "LEIHT" DAS BUCH AUS
        
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
    // - Resultat: Ein dangling pointer – eine Referenz auf nicht-existierenden Speicher
    // - Damals gab es keinen Borrow-Checker, welcher vorhersah und sofort wusste wer das Buch zuletzt hatte
}
```

Das Opfer: Pointer Erki ein Bibliothekar, der immer sagte: "Ich weiß genau, wo jedes Buch ist." Bis er auf ein nicht-existierendes Buch zeigte und dabei draufging ..

</details>

Im Herzen der Stadt, im Main-Crate, residiert der alte Bürgermeister **fn main()**. Jeden Morgne tritt er auf den Balkon seines Rathauses und spricht die magischen Wort, die den Tag einläuten. Ohne ihn passiert nichts. Aber er ist alt und weise, und schlau genug um zu wissen, dass er nicht überall sein kann. Für die wirklich harten Fälle hat er zwei Spezialisten, deren Namen man ehrfürchtig und den Gängen der Bezirke flüstert. So kennt man den Detective Ownership und Officer Borrowing auch in den Gassen von Rust City, von der Besitzbehörde und der Borrow-Checker-Polizei.

## 👤 Der Protagonist: Detective Ownership

Er heisst Own, aber alle nennen ihn Detective Ownership. Mit 19 lebt er im **Stack District**, wo alles ordentlich und vorhersehbar ist, viel angenehmer als im **Heap District**. Seine Eltern waren Kernel-Entwickler, starben bei einem mysteriösen **`unsafe`-Block-Exploit**. Aufgewachsen und gelebt von kleinen Bug-Bounties (er reparierte, was andere kaputt kompilierten)entwickelte sich Own sehr schnell (mit halber Lichtgeschwindigkeit) und hatte viel von anderen gelernt. Später einmal entschloss er sich sein Hobby und sein Talent mit seinem heutigen Beruf als Detective zu vereinen. Own hat eine besondere Gabe: Er riecht **Memory-Leaks**, **Dangling References** und **Wert ohne Besitzer**.

## 🚨 Der Vorfall

Auf dem Weg zum **Memory-Market** sieht Own den ersten Roboter. Einen **Trash-Collector-Bot**, der normalerweise die Fragmente aus dem Heap District einsammelt. Er steht still, zittert, sein Display zeigt:

ERROR: expected value, found null .. thread 'main' **panicked** at 'called Option::unwrap() on a None value`

Dahinter: Dutzende weitere Roboter, alle in derselben Starre. 
Eine **Null-Pointer-Epidemie** ? .. Owns Nase kribbelt. Das ist kein Zufall, für ihn nicht .. vielleicht Absicht ? ?

---
[Nächstes Kapitel →](/app/blog/content/chapters/02-detective-ownership-and-officer-borrowing.md)  
