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