📖 Kapitel 5: Madame Enum und ihre Typen

Konzept: Enum, Struct, Pattern Matching
Charakter: Madame Enum (die Matriarchin der variantenreichen Familien)
Die Handlung:

Die Spur führt zu Madame Enum, einer angesehenen Geschäftsfrau im Data District. Sie leitet das größte Varianten-Haus der Stadt – eine Art Hotel für unterschiedlichste Datentypen. Ihre Familie, die Enums, kann viele verschiedene Formen annehmen: Mal ist sie eine Message::Quit, mal eine Message::Move { x: 10, y: 20 }, mal eine Message::Write(String). Aber im Gegensatz zu Max verändert sie sich nicht – sie entscheidet sich für eine Form und bleibt dann stabil.

Madame Enum empfängt die Detectives in ihrem Anwesen, umgeben von ihren Kindern – den Structs. Ihre Kinder sind solide, verlässliche Typen, die immer alle ihre Daten beisammen haben. Jeder Struct hat einen festen Platz für jede Information, nichts gerät durcheinander.

Der Konflikt: Madame Enum ist besorgt. Ihre jüngste Tochter, eine Option, ist verschwunden. Sie kann entweder Some(data) oder None sein – und gerade ist sie None, also eigentlich "nicht da". Die Detectives müssen verstehen: Wie findet man jemanden, der gerade nicht existiert?

Die Auflösung: Mit Hilfe von Pattern Matching – einer speziellen Detektivtechnik – können sie für jeden möglichen Zustand der Vermissten einen Plan entwickeln:

    Wenn sie Some(data) ist: Wo wäre die data?

    Wenn sie None ist: Wo versteckt sich jemand, der nicht existiert?

Sie finden die kleine Option schließlich im Error-Handling-Viertel, wo sie von einem Result-Typen festgehalten wurde. (Ok und Err – eine andere Enum-Familie!)

Der Twist: Max Mutation taucht wieder auf und will Madame Enums Kinder "verbessern", indem er sie ständig mutiert. Die Detectives müssen ihn aufhalten – aber sie erkennen auch, dass Max nicht böse ist, sondern einfach süchtig und orientierungslos. Vielleicht kann man ihm helfen?

Code-Konzept:

    Enums und ihre Varianten

    Structs als Datencontainer

    Pattern Matching (match)

    Option und Result als spezielle Enums

    Der Unterschied: Enum = Wahl zwischen festen Zuständen vs. Mutation = Veränderung eines Zustands