```mermaid
flowchart LR

%% ===== AKTORZY =====
subgraph AKTORZY
User((Użytkownik))
Player((Gracz))
Recenzent((Recenzent Gier))
Organizator((Organizator))
GameMaster((Mistrz wydarzenia))
GameCreator((Twórca gier))
ExternalOrganizer((Organizator zewnętrzny))
Admin((Admin))
end

%% ===== FUNKCJE UZYTKOWNIKA =====
subgraph FUNKCJE_UZYTKOWNIKA
Register([Rejestracja])
Login([Logowanie])
History([Wyświetlenie historii wydarzeń])
end

User --> Register
User --> Login
User --> History

%% ===== FUNKCJE GRACZA =====
subgraph FUNKCJE_GRACZA
ShowUserCalendar([Wyświetlenie kalendarza przez gracza])
Search([Wyszukiwanie wydarzenia])
ScanQR([Skanowanie QR kodu])
JoinEvent([Dołączenie do wydarzenia])
ShowCalendar([Wyświetlenie kalendarza])
AcceptInvitation([Akceptowanie zaproszenie])
Trade([Targowanie się])
Complain([Wysyłanie skargi])
Leave([Wyjście z wydarzenia])
Fight([Walczenie z kimś])
MiniGame([Granie w mini-grę])
end

Player -->|generalization| User

Player -. "&lt;&lt;invoke&gt;&gt;" .-> ShowUserCalendar
Player -. "&lt;&lt;invoke&gt;&gt;" .-> AcceptInvitation

AcceptInvitation -. "&lt;&lt;invoke&gt;&gt;" .-> JoinEvent
ShowUserCalendar -. "&lt;&lt;invoke&gt;&gt;" .-> JoinEvent
ShowUserCalendar -. "&lt;&lt;invoke&gt;&gt;" .-> Search

JoinEvent -. "&lt;&lt;invoke&gt;&gt;" .-> ScanQR
JoinEvent -. "&lt;&lt;invoke&gt;&gt;" .-> Trade
JoinEvent -. "&lt;&lt;invoke&gt;&gt;" .-> Complain
JoinEvent -. "&lt;&lt;invoke&gt;&gt;" .-> Leave
JoinEvent -. "&lt;&lt;invoke&gt;&gt;" .-> Fight
JoinEvent -. "&lt;&lt;invoke&gt;&gt;" .-> MiniGame

Search -. "&lt;&lt;invoke&gt;&gt;" .-> JoinEvent

ShowUserCalendar -->|generalization| ShowCalendar

%% ===== FUNKCJE WSPÓLNE =====
subgraph FUNKCJE_WSPOLNE
ShowGameList([Wyświetlenie listy gier])
end

%% ===== RECENZENT =====
subgraph FUNKCJE_RECENZENTA
ShowRecenzentGameList([Wyświetlenie listy gier przez recenzenta])
SendMessageToCreator([Przesłanie komunikatu do twórcy])
LeaveReview([Recenzja gry])
end

Recenzent -->|generalization| User

ShowRecenzentGameList -->|generalization| ShowGameList
Recenzent --> ShowRecenzentGameList

ShowRecenzentGameList -. "&lt;&lt;invoke&gt;&gt;" .-> SendMessageToCreator
ShowRecenzentGameList -. "&lt;&lt;invoke&gt;&gt;" .-> LeaveReview

%% ===== ORGANIZATOR =====
subgraph FUNKCJE_ORGANIZATORA
ShowOrganizatorGameList([Wyświetlenie listy gier przez organizatora])
AddEvent([Dodanie wydarzenia do kalendarza])
PublishForOthers([Udostępnienie wydarzenia graczom])
InviteUsers([Zaproszenie graczy])
ShowOrganizatorCalendar([Wyświetlenie kalendarza przez organizatora])
end

Organizator -->|generalization| User

ShowOrganizatorGameList -->|generalization| ShowGameList
Organizator --> ShowOrganizatorGameList
Organizator --> ShowOrganizatorCalendar

ShowOrganizatorCalendar -->|generalization| ShowCalendar

ShowOrganizatorCalendar -. "&lt;&lt;invoke&gt;&gt;" .-> AddEvent
ShowOrganizatorGameList -. "&lt;&lt;invoke&gt;&gt;" .-> AddEvent

AddEvent -. "&lt;&lt;invoke&gt;&gt;" .-> InviteUsers
AddEvent -. "&lt;&lt;invoke&gt;&gt;" .-> PublishForOthers

%% ===== MISTRZ WYDARZENIA =====
subgraph FUNKCJE_MISTRZA
StartEvent([Uruchomienie wydarzenia])
EndEvent([Zakończenie wydarzenia])
end

GameMaster -->|generalization| User
GameMaster --> StartEvent
GameMaster --> EndEvent

%% ===== TWORCA GIER =====
subgraph FUNKCJE_TWORCY
DefineGame([Zdefiniowanie gry])
AddRole([Dodanie postaci/przedmiotu])
DefineMap([Zdefiniowanie mapy gry])
DefineRoom([Zdefiniowanie pomieszczenia])
DefineActions([Zdefiniowanie akcji])
SendToReview([Przesłanie komunikatu do recenzenta])
ShowOwnGames([Wyświetlenie listy swoich gier])
end

GameCreator -->|generalization| User
GameCreator --> DefineGame
GameCreator --> ShowOwnGames

DefineGame -. "&lt;&lt;invoke&gt;&gt;" .-> DefineActions
DefineGame -. "&lt;&lt;invoke&gt;&gt;" .-> SendToReview
DefineGame -. "&lt;&lt;invoke&gt;&gt;" .-> AddRole
DefineGame -. "&lt;&lt;invoke&gt;&gt;" .-> DefineMap
DefineMap -. "&lt;&lt;invoke&gt;&gt;" .-> DefineRoom
ShowOwnGames -. "&lt;&lt;invoke&gt;&gt;" .-> DefineGame



%% ===== ORGANIZATOR ZEWNĘTRZNY =====
subgraph FUNKCJE_ORGANIZATORA_ZEW
ShowExternalCalendar([Wyświetlenie kalendarza przez organizatora zewnętrznego])
end

ExternalOrganizer --> ShowExternalCalendar

%% ===== ADMIN =====
subgraph FUNKCJE_ADMINA
ModerateSystem([Moderowanie systemu])
end

Admin --> ModerateSystem
