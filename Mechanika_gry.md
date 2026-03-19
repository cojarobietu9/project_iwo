```mermaid
flowchart LR

projektant["Projektant gry"]

subgraph "Mechanika i projektowanie gry"

UC0(("Projektowanie mechaniki gry"))

UC1(("Projektowanie przedmiotu"))
UC2(("Projektowanie mini-gier"))
UC3(("Projektowanie zadań"))
UC4(("Projektowanie przeszkód"))
UC5(("Określanie warunków zwycięstwa"))

UC6(("Projektowanie systemu walki między graczami"))
UC7(("Definiowanie poziomu trudności gry"))
UC8(("Ustawienie limitu czasu gry"))
UC9(("Aktywacja zaawansowanego trybu gry"))

UC0 -. include .-> UC1
UC0 -. include .-> UC2
UC0 -. include .-> UC3
UC0 -. include .-> UC4
UC0 -. include .-> UC5
UC0 -. include .-> UC6
UC0 -. include .-> UC7
UC0 -. include .-> UC8
UC0 -. include .-> UC9

end

projektant --> UC0

```






