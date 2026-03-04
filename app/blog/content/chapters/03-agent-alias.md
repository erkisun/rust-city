# Agent Alias

*Rust City – Eine Geschichte über Besitz, Regeln und perfekten Code.*

## 🪐 Der Angriff 

📖 Kapitel 3: Agent Alias' Angriff

Konzept: References, Aliasing, Type Aliases
Charakter: Agent Alias (eine zwielichtige, aber brillante Gestalt)
Die Handlung:

Officer Borrowing und Detective Ownership untersuchen den ausgefallenen Trashbot. Die Spuren führen sie in den Heap District, wo sie auf Agent Alias treffen – einen Meister der Tarnung und Abkürzungen. Alias arbeitet offiziell für die Cargo-Behörde als "Typberater", aber niemand weiß so recht, wem er wirklich dient.

Alias hat die Angewohnheit, Dinge umzubenennen. Er gibt langen, komplizierten Typen kurze Spitznamen (type UserId = String). Er taucht auf und verschwindet wieder, indem er Pfade abkürzt (use std::collections::HashMap). Seine Wohnung ist ein Labyrinth aus Spiegeln – überall Aliase, überall Verweise auf Dinge, die woanders stehen.

Der Konflikt: Alias hilft den Detectives zunächst bei der Suche nach der Ursache des Trashbot-Ausfalls. Aber dann stellen sie fest: Alias hat heimlich Aliase auf Beweismittel erstellt, ohne dass die Besitzbehörde davon wusste. Mehrere Namen zeigen auf dasselbe Objekt – ein gefährliches Spiel mit Referenzen.

Der Twist: Alias führt sie zu Max Mutation, einem bekannten Anarchisten. "Wenn ihr wissen wollt, wer wirklich hinter den Abstürzen steckt", flüstert Alias, "dann müsst ihr Max finden. Aber passt auf – er verändert alles, was er anfasst."

Code-Konzept:

    Einführung von Referenzen (&T)

    Type Aliases (type-Schlüsselwort)

    Pfade und das use-Schlüsselwort

    Erste Ahnung: Mehrere Referenzen auf dieselbe Ressource können gefährlich sein