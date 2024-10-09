# Stoppen van de band
```plantuml

@startuml
[*] --> Wachten
Wachten --> Stoppen : ProductGedetecteerd2 && Timer.ET > 1s
Stoppen --> Wachten : MotorStatus = 0
@enduml
