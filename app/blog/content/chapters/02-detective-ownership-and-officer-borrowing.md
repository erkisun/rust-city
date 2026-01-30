# Detective Ownership & Officer Borrowing

## 🕵️‍♂️👮 Die Begegnung

Detective Ownership & Officer Borrowing

Own bückte sich, die Gaze seiner eigenen Reflexion im stillgelegten Display des Trash-Collector-Bots. Er zog ein **Debug-Kabel** aus der Innentasche seines ledernen Overcoats – ein Erbstück seiner Eltern, durchsetzt mit isolierten Kupferdrähten und geheimen Compiler-Flags. Seine Finger tasteten nach dem Diagnose-Port unter dem Roboter-Arm, als ein Schatten über ihn fiel.

„Ich würde die Finger vom Beweismaterial lassen, wenn ich du wäre.“

Die Stimme war tief, ruhig, mit dem unverkennbaren Unterton jemandes, der mehr Lifetime-Annotationen gelesen hat, als er Stunden Schlaf hatte. Own drehte sich langsam um.

Der Mann, der vor ihm stand, war mindestens einen Kopf größer. Seine Uniform war kein gewöhnliches Polizei-Gewand – sie bestand aus überlagerten Schichten Compiler-Warnungen in sanftem Gelb und Lifetime-Visualisierungen in pulsierendem Blau. Sein Namensschild, direkt über dem Herzen, leuchtete in strengen Monospace-Buchstaben:
text

**OFFICER BORROWING**
ID: &'static mut self
DEPT: BORROW CHECKER

„Detective Ownership, nehme ich an“, sagte der Officer, ohne die Hand auszustrecken. Seine Augen – die Farbe von kühlem Stack-Speicher – scannten Own, als würde er einen Codeblock auf Memory-Leaks prüfen. „Ihr Ruf eilt Ihnen voraus. Man sagt, Sie können eine **dangling reference** auf hundert Meter riechen.“

Own nickte langsam. „Und man sagt, Sie können einen illegalen **mutable borrow** hören, bevor er passiert.“

Ein kaum merkliches Lächeln spielte um Officer Borrowings Lippen. „Das hier ist kein gewöhnlicher Systemabsturz, Detective. Das ist eine Botschaft.“ Er deutete auf die Reihe erstarrter Roboter. „Jeder einzelne zeigt dieselbe **Panic-Nachricht**. Dieselbe Zeile. Dasselbe Muster.“

„Ein Coordinated Attack“, stellte Own fest.

„Mehr als das“, korrigierte Officer Borrowing. Er zog ein Holo-Tablet aus seinem Gürtel. Mit einer Geste projizierte er eine dreidimensionale Karte von Rust City in die Luft zwischen ihnen. Rote Punkte markierten jede Roboter-Panik. „Sehen Sie das Muster?“

Own trat näher. Die Punkte formten keine zufällige Verteilung. Sie bildeten eine Spirale, die vom **Stack District** ausging und sich zum **Heap District** hin wand.

„Es beginnt in meiner Nachbarschaft“, murmelte Own.

„Es beginnt bei Ihnen“, präzisierte der Officer. Seine Stimme wurde noch leiser. „Die ersten drei Ausfälle waren direkt vor Ihrem Apartment. Der vierte an der Bäckerei, wo Sie jeden Morgen Ihr Binary-Brot kaufen. Der fünfte…“

„…am Memory-Market, wo ich heute hin wollte“, vollendete Own. Ein kalter Schauer lief ihm den Rücken hinunter. „Jemand beobachtet mich.“

Officer Borrowing nickte und schaltete das Hologramm aus. „Jemand testet Sie. Und gleichzeitig provoziert er mich und mein Department. Dies hier…“ Er tippte auf das Tablet, und ein Code-Snippet erschien:
rust

fn main() {
    let target = "Detective Ownership";
    let message = "We see you";
    // TODO: Deliver warning
    println!("{}: {}", target, message);
}

„Das haben wir aus dem Speicherdump des ersten Bots extrahiert“, erklärte der Officer. „Unvollständig. Absichtlich. Als ob sie uns sagen wollten: ‚Wir haben mehr. Kommt und holt es euch.‘“

Own studierte den Code. „Die Variable target ist immutable. message auch. Aber der Kommentar… ‚TODO: Deliver warning‘. Das klingt nicht nach fertig geplantem Angriff. Das klingt nach .. Improvisation.“

„Oder Ablenkung“, warf Officer Borrowing ein. Seine Augen verengten sich. „Was, wenn die Roboter nur der Rauch sind, und das eigentliche Feuer woanders brennt?“

In diesem Moment piepte das Tablet. Ein neuer Alert. Officer Borrowing las die Nachricht, und seine Haltung versteifte sich. „Es gibt einen Zeugen. Ein Collector im Heap District. Er sagt, er habe gesehen, wie jemand den Compiler-Tower betreten hat. In der Nacht vor den Ausfällen.“

„Der Compiler-Tower ist gesperrt“, sagte Own. „Nur Kernel-Entwickler mit Level-10-Zugang ..“

„.. können die primären Sicherheitsprotokolle umgehen“, vollendete Officer Borrowing. Er sah Own direkt in die Augen. „Wie Ihre Eltern, Detective.“

Die Luft zwischen ihnen wurde plötzlich kalt. Own spürte, wie seine eigenen Lifetime-Annotationen sich zu straffen schienen. „Was implizieren Sie?“

„Ich impliziere nichts“, sagte der Officer ruhig. „Ich stelle Fakten fest. Ihre Eltern hatten Zugang. Sie sind tot. Jemand nutzt möglicherweise ihre Credentials. Und jetzt werden Sie beobachtet.“ Er machte eine Pause, ließ die Worte wirken. „Sie haben zwei Optionen, Detective. Sie können nach Hause gehen, Ihre Tür verriegeln und hoffen, dass dies vorübergeht. Oder…“

„Oder?“

Officer Borrowing nahm eine zweite Uniform-Jacke von der Rückbank seines Borrow-Checker-Vehicles. Sie war kleiner, aber mit denselben pulsierenden Visualisierungen. „Oder Sie kommen mit mir. Lernen die Regeln dieser Stadt wirklich zu verstehen. Und wir finden heraus, wer hinter diesem Angriff steckt – bevor die nächste Welle von Panics nicht nur Roboter, sondern die gesamte Memory-Safety der Stadt trifft.“

Own betrachtete die Jacke. Dann die Reihe erstarrter Roboter. Dann das ernste Gesicht des Officers, in dem sich die Reflexion der eigenen Unsicherheit spiegelte.

„Die Credentials meiner Eltern wurden nach ihrem Tod deaktiviert“, sagte er schließlich. „Aber .. es gab Backups. Physische Security Tokens. In einem Safe in ihrem alten Labor.“

Officer Borrowings Augen blitzten auf. „Wo ist dieses Labor?“

„Im Kernel District. Gesperrt seit fünf Jahren.“ Own holte tief Luft. „Aber ich weiß, wie man hineinkommt.“

Der Officer reichte ihm die Jacke. „Dann schlage ich vor, wir machen uns auf den Weg. Aber zuerst eine Lektion, Detective. In dieser Stadt überlebt man nur, wenn man die Regeln des Borrowing versteht. Und die erste Regel lautet…“

**„..du kannst etwas ausleihen, aber du musst es zurückgeben“**, sagte Own und zog die Jacke an. Sie passte perfekt.

Officer Borrowing lächelte zum ersten Mal richtig. „Sie haben zugehört. Gut. Regel zwei: **Nur eine mutable reference zur gleichen Zeit. Regel drei ..“**

**„.. Regel 3 : References müssen immer gültig bleiben“**, vollendete Own. „Ich kenne die Theorie, Officer. Meine Eltern haben sie mir eingebläut, bevor ich laufen konnte.“

„Theorie ist eine Sache“, sagte der Officer und öffnete die Fahrertür seines Vehicles. „Praxis ist etwas anderes. Heute lernen Sie die Praxis. Denn was immer in Ihrem Elternlabor wartet .. es wird nicht freundlich sein.“

Das Vehicle startete mit einem leisen Surren, die Borrow-Checker-Lichter begannen in einem komplexen Muster zu pulsieren – grün für sichere Pfade, gelb für Warnungen, rot für verbotene Zugriffe.

„Wohin genau fahren wir?“, fragte Own, als sie vom Bordstein wegzogen.

„Zuerst zur Borrow-Checker-Zentrale“, antwortete Officer Borrowing. „Wir müssen Ihren Access-Level erhöhen. Und dann…“ Er warf Own einen Seitenblick zu. „.. dann brechen wir in ein gesperrtes Kernel-Labor ein. Wenn wir erwischt werden, verlieren wir beide unsere Compilation-Privileges. Für immer.“

Die Straßen von Rust City zogen vorbei, eine blendende Lichterflut aus Code-Snippets und laufenden Prozessen. Own lehnte sich zurück und spürte das Gewicht der neuen Jacke, das Pulsieren der Sicherheitssysteme, die Präsenz des merkwürdigen, strengen Officers neben sich.

Der Fall hatte gerade erst begonnen. Und schon jetzt wusste er: In Rust City gibt es Bosse !


## 🔍 Was wir gelernt haben

1. **Charakter-Dynamik**: Detective Ownership und Officer Borrowing sind kein klassisches Team – sie sind zwei Seiten derselben Medaille: Besitz und Ausleihe.
2. **Plot-Vertiefung**: Der Angriff ist persönlich (gegen Own gerichtet) und systematisch (gegen die Stadt).
3. **Mystery-Elemente**: 
   - Wer nutzt die alten Credentials von Owns Eltern?
   - Was befindet sich im gesperrten Labor?
   - Warum wird Own beobachtet?
4. **Rust-Konzepte eingeführt**:
   - `&` und `&mut` als Grundprinzipien der Stadt
   - Lifetime-Annotationen (`'static`)
   - Memory-Safety als zentrales Thema

---

**Fortsetzung folgt in Kapitel 3: Agent Alias' Angriff**, wo Own und Officer Borrowing das erste Mal auf aktiven Widerstand stoßen – und lernen, dass in Rust City manchmal sogar die Regeln gebrochen werden müssen, um sie zu schützen.

---

*Rust City – Wo jeder Wert einen Besitzer hat, und jedes Ausleihen seinen Preis.*

---
[← Vorheriges Kapitel](/app/blog/content/chapters/01-welcome-to-rust-city.md) | [Nächstes Kapitel →](/app/blog/content/chapters/03-attack-of-agent-alias.md)  
