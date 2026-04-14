```mermaid
flowchart LR

subgraph Aktorzy
rec((Recenzent))
org((Organizator))
tworca((Twórca))
end

subgraph Przypadki użycia
pu_lista_gier_tw([Wyświetlenie listy swoich gier])
pu_komunikat([Przesłanie komunikatu do twórcy])
pu_lista_gier_org([Wyświetlenie listy gier przez organizatora])
pu_lista_gier([Wyświetlenie listy gier])
pu_recenzja_gry([Recenzja gry])

tworca --> pu_lista_gier_tw
org --> pu_lista_gier_org
rec --> pu_recenzja_gry

pu_lista_gier_org ~~~ pu_lista_gier
pu_lista_gier_tw ~~~ pu_lista_gier
pu_lista_gier_org --> pu_lista_gier 
pu_lista_gier_tw --> pu_lista_gier
pu_recenzja_gry -."&lt;&lt;invoke&gt;&gt;".-> pu_komunikat

end
```

# Opisy przypadków użycia

## Przesłanie komunikatu do twórcy

Recenzent powinien być w stanie przesłać komunikaty do twórcy gry z poziomu gry. 

## Wyświeltenie listy swoich gier

Twórca jest w stanie wyświetlić listę gier, których jest autorem.
Z widoku listy powinien być w stanie wejść w tryby edycji danej gry.

## Wyświetlenie listy gier przez organizatora

Organizator jest w stanie wyświetlić listę gier możliwych do organizacji/organizowanycch. Organizator może z tego miejsca wyświetlić sczegóły gry, oraz rozpocząć jej organizację.

## Wyświetlenie listy gier
Usecase abstrakcyjny, określający wyświetlenie listy. Podstawowe funkcje to filtrowanie i wyszukiwanie. 

# Wymagania funkcjonalne

## czas dostarczenia komunikatu do twórcy

Komunikat między twórcą a recenzentem przychodzi z opóźnieniem max. 30 minut.



# Słownik dziedziny

- **Twórca**/**Twórca gry** - Osoba, która jest autorem, lub jednym z autorów gry w naszym serwisie

- **Gra** - Plan rozgrywki typu LARP zapisana w naszym serwisie. Jedna gra może być organizowana wielokrotnie.

- **Organizator** - Osoba odpowiedzialna za organizację rozgrywki gry LARP.

- **Recenzent** - Osoba odpowiedzialna za wstępną recenzję wydarzenia. Komunikuje swoje uwagi twórcy. Jest odpowiedzialny za ostateczne opublikowanie gry.
