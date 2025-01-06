# Timer
De code maakt een toestandsdiagram met de staten "Case2", "TimerLopen", "TimerStoppen" en "Case3". De overgang van "Case2" naar "TimerLopen" gebeurt wanneer de timer op "True" staat. Als de timer langer dan 1 seconde loopt en een product wordt gedetecteerd, gaat de toestand naar "TimerStoppen", waarna de toestand naar "Case3" gaat wanneer de timer weer op "False" staat.

```plantuml

@startuml
[*] --> Case2
Case2 --> TimerLopen : Timer = True
TimerLopen --> TimerStoppen : ProductGedetecteerd2 && Timer.ET > 1s
TimerStoppen --> Case3 : Timer = False
@enduml

