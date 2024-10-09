# Sequence Diagram voor communicatie
```plantuml

@startuml
Entity Product
participant "Taak 1" as Task1
participant "Taak 2" as Task2
participant "Taak 3" as Task3

Product -> Task1 : Controleer ProductGedetecteerd1
Task1 -> Task2 : Zet MotorStatus aan
Task2 -> Task2 : Start Timer
Task2 -> Task3 : Controleer ProductGedetecteerd2
Task3 -> Task2 : Stop Timer
@enduml

