# Stoppen van de band
De code maakt een toestandsdiagram met de staten "Case3", "Stoppen" en "Case1". Van "Case3" naar "Stoppen" wordt overgegaan wanneer een product wordt gedetecteerd en de timer langer dan 1 seconde loopt. Van "Stoppen" gaat de toestand naar "Case1" wanneer de motorstatus gelijk is aan 0.

```plantuml

@startuml
[*] --> Case3
Case3 --> Stoppen : ProductGedetecteerd2 && Timer.ET > 1s
Stoppen --> Case1 : MotorStatus = 0
@enduml
