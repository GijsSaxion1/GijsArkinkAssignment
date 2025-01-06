# Sequence Diagram voor de functie
De code beschrijft een sequentiediagram tussen "Task3" en de functie "POU". "Task3" roept "Function" aan om de tijd (Timer.ET) op te halen. "Function" zet deze tijd om naar seconden, berekent de transportsnelheid van de band en geeft vervolgens de gemiddelde snelheid terug aan "Task3".

```plantuml

@startuml
participant "Case 3" as Task3
participant "POU" as Function

Task3 -> Function : Aanroep(Timer.ET)
Function -> Function : Tijd omzetten naar seconden
Function -> Function : TransportBandSnelheid berekenen
Function -> Task3 : Gemiddelde snelheid van de band teruggeven
@enduml

