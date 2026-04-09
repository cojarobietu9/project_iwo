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
pu_lista_gier_rec([Wyświetlenie listy gier przez recenzenta])
pu_lista_gier([Wyświetlenie listy gier])


tworca --> pu_lista_gier_tw
org --> pu_lista_gier_org
rec --> pu_lista_gier_rec

pu_lista_gier_org ~~~ pu_lista_gier
pu_lista_gier_tw ~~~ pu_lista_gier
pu_lista_gier_rec ~~~ pu_lista_gier
pu_lista_gier_org --"&lt;&lt;extends&gt;&gt;"--> pu_lista_gier 
pu_lista_gier_tw --"&lt;&lt;extends&gt;&gt;"--> pu_lista_gier
pu_lista_gier_rec --"&lt;&lt;extends&gt;&gt;"--> pu_lista_gier
pu_lista_gier_rec -."&lt;&lt;invoke&gt;&gt;".-> pu_komunikat

end
```

# Opisy przypadków użycia

## Przesłanie komunikatu do twórcy

Recenzent powinien być w stanie przesłać komunikaty do twórcy gry z poziomu gry. 

## Wyświeltenie listy swoich gier

Twórca jest w stanie wyświetlić listę gier, których jest autorem.
Z widoku listy powinien być w stanie wejść w tryby edycji i statystyk dotyczących danej gry.

## Wyświetlenie listy gier przez organizatora

Organizator jest w stanie wyświetlić listę gier możliwych do organizacji. Organizator może z tego miejsca wyświetlić sczegóły gry, oraz rozpocząć jej organizację.

## Wyświetlenie listy gier przez recenzenta

Recenzent jest w stanie wyświetlić nie opublikowane gry, które zostały przypisane mu do zrecenzowania. 
Recenzent może dalej przejść w tryb wyświetlenia gry, a następnie komunikatu lub dopuszczenia do publikacji gry.

## Wyświetlenie listy gier
Usecase abstrakcyjny, określający wyświetlenie listy. Podstawowe funkcje to filtrowanie i wyszukiwanie. 

# Wymagania funkcjonalne

## czas dostarczenia komunikatu do twórcy

Komunikat do twórcy przychodzi z opóźnieniem max 30 minut.



# Słownik dziedziny

- **Twórca**/**Twórca gry** - Osoba, która jest autorem, lub jednym z autorów gry w naszym serwisie

- **Gra** - Plan rozgrywki typu LARP zapisana w naszym serwisie. Jedna gra może być organizowana wielokrotnie.

- **Organizator** - Osoba odpowiedzialna za organizację rozgrywki gry LARP.

- **Recenzent** - Osoba odpowiedzialna za wstępną recenzję wydarzenia. Komunikuje swoje uwagi twórcy. Jest odpowiedzialny za ostateczne opublikowanie gry.
