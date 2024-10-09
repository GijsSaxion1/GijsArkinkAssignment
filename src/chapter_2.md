# Timer
```plantuml

@startuml
[*] --> Wachten
Wachten --> TimerLopen : MotorStatus = 1
TimerLopen --> Stoppen : ProductGedetecteerd2 && Timer.ET > 1s
Stoppen --> Wachten : MotorStatus = 0
@enduml

