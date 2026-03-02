# Willkommen in Rust City

*Rust City – Eine Geschichte über Besitz, Regeln und perfekten Code.*

## 🪐 Der Mond Rust-K04

Rust-K04 ist schwarz und öde, ein kleiner Mond, der einen längst vergessenen Gasriesen umkreist. Nur bei Einstrahlung von Licht sieht man seine Oberfläche leuchten, bedeckt von der Legende - Rust City.

Rust City ist ein gigantischer Komplex aus Stahl, Silizium und strengen Regeln. Wer hier lebt, lebt nach den Regeln der Stadt. Ohne Ausnahme und ohne Alternative. Die Stadt gliedert sich in riesige Bezirke (**Crates**), jeder ein eigenes Universum mit strengen Ein- und Ausgangsregeln. Die Bezirke sind unterteilt in Stadtteile (**Modules**) in denen die eigentliche Arbeit passiert.

Die Cargo-Behörde, eine mächtige Institution in Rust City, ist das zentrale Dienst-Unternehmen der Stadt. Cargo übernimmt sämtliche Aufgaben wie Logistik, Verwaltung, Lieferungen und übernimmt sogar das Bauen neuer Stadtteile wenn notwendig. Ein Güterzug von std nach collection zum HashMap -Bahnhof ? Kein Problem, **Cargo ::** regelt das. Ohne Cargo würde die Stadt im Chaos versinken, Bezirke wären nicht erreichbar, Abhängigkeiten würden fehlen und niemand wüsste, wie man einen neuen Stadtteil baut.

Wissenschaftler nennen es Logik, wovon manche Bewohner benommen werden, andere süchtig. Sie nennen es **„Compiling High“** – wenn der Compiler alles akzeptiert und das perfekte Programm läuft. Die Sucht nach fehlerfreiem Code hat schon viele in die Überdosis getrieben: endlose **Loop-Träume**, **Memory-Leak-Halluzinationen**, **Stack-Overflow-Wahn**.


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
        // ⚠️  BIBLIOTHEKAR POINTER PETE "LEIHT" DAS BUCH AUS
        let leser = buch; 
        
        // Hier passiert etwas Merkwürdiges ..
        // In der C-Ära gab es keine Borrowing-Regeln!
        // Der Leser nimmt das Buch einfach mit ..
        // Damals gab es noch keinen Borrow-Checker, welcher vorhersah und sofort wusste wer das Buch zuletzt hatte

        
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

## 👤 Der Bürgermeister : fn main()

Im Herzen der Stadt, im Main-Crate, residiert der alte **fn main()**. Jeden Morgen tritt er auf den Balkon seines Rathauses und spricht die magischen Worte, die den Tag einläuten. Ohne ihn passiert nichts. Aber er ist alt und schlau genug um zu wissen, dass er nicht überall sein kann. Für die wirklich harten Fälle hat er zwei Spezialisten, deren Namen man ehrfürchtig und den Gängen der Bezirke flüstert. So kennt man den Detective Ownership von der Besitzbehörde und Officer Borrowing von der Borrow-Checker-Polizei auch in den Gassen von Rust City.

## 🚨 Der Vorfall

Detective Ownership lebt sein einigen Jahren im **Stack District**, wo alles ordentlich und vorhersehbar ist, viel angenehmer als im **Heap District**. Seine Eltern waren Kernel-Entwickler, starben bei einem mysteriösen **`unsafe`-Block-Exploit**. Entwickelt hat sich Own nicht alleine, er konnte viel von anderen lernen (mit halber Lichtgeschwindigkeit). Später entschloss er sich sein Hobby und sein Talent mit seinem heutigen Beruf als Detective zu vereinen, besser gesagt, es war ein Übergang, welches sich nie richtig mit Worten beschreiben lässt. Mit Worten eindeutig beschreiben lässt sich aber Own's besondere Gabe: Er riecht **Memory-Leaks**, **Dangling References**.

Wie jeden Morgen nahm er seinen üblichen Spaziergang durch das alte Industriegebiet aber heute sah er etwas merkwürdiges. Auf dem Weg zum Memory-Market sieht Own einen auffällig erstarrten Roboter. Auffällig deshalb, weil so ein **Trash-Collector-Bot**, der normalerweise die Fragmente aus dem Heap District einsammelt, nie still steht. Der Roboter macht keinen Wank, also macht Own einige Schritte in Richtung des Roboters, und sieht es zittern. Sein Display zeigt:

```rust
ERROR: expected value, found null .. thread 'main' **panicked** at 'called Option::unwrap() on a None value`
```


[Nächstes Kapitel →](/app/blog/content/chapters/02-detective-ownership-and-officer-borrowing.md)  
