# Sequence Diagram voor communicatie
```plantuml

@startuml
Entity Product
participant "Case 1" as Task1
participant "Case 2" as Task2
participant "Case 3" as Task3

Product -> Task1 : Controleer Product begin band
Task1 -> Task2 : Zet MotorStatus aan
Task2 -> Task2 : Start Timer
Task2 -> Task3 : Controleer Product einde band
Task3 -> Task2 : Stop Timer
Task2 -> Task1 : Zet MotorStatus uit
Task1 -> Product : Controleer Nieuw product
@enduml

