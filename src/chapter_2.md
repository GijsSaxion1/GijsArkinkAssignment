# Timer
```plantuml

@startuml
[*] --> Wachten
Wachten --> TimerLopen : Timer = True
TimerLopen --> TimerStoppen : ProductGedetecteerd2 && Timer.ET > 1s
TimerStoppen --> Wachten : Timer = False
@enduml

