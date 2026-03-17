<!--
```
@startuml
left to right direction

actor "Mistrz wydarzenia" as master
actor "Organizator zewnetrzny" as ngo

usecase "Uruchomienie wydarzenia" as UC1
usecase "Zakonczenie wydarzenia" as UC2
usecase "Wyswietlenie kalendarza przez organizatora zewnetrznego" as UC3

master -> UC1
master -> UC2
ngo -> UC3
@enduml

```
-->
![](julian_stefan.png)
