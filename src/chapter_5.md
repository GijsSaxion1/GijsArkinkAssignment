# Sequence Diagram voor de functie
```plantuml

@startuml
participant "Taak 3" as Task3
participant "POU" as Function

Task3 -> Function : Aanroep(Timer.ET)
Function -> Function : Tijd omzetten naar seconden
Function -> Function : TransportBandSnelheid berekenen
Function -> Task3 : Gemiddelde snelheid van de band teruggeven
@enduml

