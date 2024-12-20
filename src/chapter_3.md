# Stoppen van de band
```plantuml

@startuml
[*] --> Case3
Case3 --> Stoppen : ProductGedetecteerd2 && Timer.ET > 1s
Stoppen --> Case1 : MotorStatus = 0
@enduml
