# Sequence Diagram voor communicatie
De code beschrijft een sequentiediagram met de entiteit "Product" en drie deelnemende taken: "Case 1", "Case 2" en "Case 3". Het proces begint met "Product" dat "Task1" aanroept om het product aan het begin van de band te controleren. Vervolgens zet "Task1" de motorstatus aan, waarna "Task2" de timer start. "Task2" controleert het product aan het einde van de band, en "Task3" stopt de timer en zet de motorstatus uit. Ten slotte keert het proces terug naar "Task1" om een nieuw product te controleren.

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
Task3 -> Task1 : Stop Timer & Zet MotorStatus uit
Task1 -> Product : Controleer Nieuw product
@enduml

