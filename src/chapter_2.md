# Timer
```plantuml

@startuml
[*] --> Case2
Case2 --> TimerLopen : Timer = True
TimerLopen --> TimerStoppen : ProductGedetecteerd2 && Timer.ET > 1s
TimerStoppen --> Case3 : Timer = False
@enduml

