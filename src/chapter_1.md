# Productdetectie
De code maakt een toestandsdiagram met de staten "Initialisatie", "MotorAan" en "Case2". Bij productdetectie gaat de toestand van "Initialisatie" naar "MotorAan". Van "MotorAan" gaat de toestand naar "Case2".

```plantuml

@startuml
[*] --> Initialisatie
Initialisatie --> MotorAan : Product gedetecteerd aan begin
MotorAan --> Case2 : Motor aan
@enduml
