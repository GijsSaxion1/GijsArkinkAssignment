# Productdetectie
```plantuml

@startuml
[*] --> Wachten
Wachten --> MotorAan : ProductGedetecteerd1 && !ProductGedetecteerd2
MotorAan --> Wachten : MotorStatus = 0
@enduml