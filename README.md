# SPECYFIKACJA WYMAGAŃ

## System wpierający organizację komnatowych wydarzeń LARP

**Redaktor:** zespół projektu  
**Status:**

**Wersja:** 1.0  
**Data modyfikacji:** 26.02.2026

**Abstrakt:**  
Dokument zawiera specyfikację wymagań dla systemu wpierającego organizację komnatowych wydarzeń LARP składającą się z wizji systemu, wymagań użytkownika oraz wymagań oprogramowania dla pierwszych iteracji projektu.

---

## Historia zmian:

- **26.02.2023** – Maksym Andrushchenko - dodany dokument md

---

# 1. Wprowadzenie

## 1.1 Cel dokumentu

Tutaj znajdzie się opis celu dokumentu...

## 1.2 Streszczenie dla kierownictwa

Tutaj znajdzie się streszczenie dla kierownictwa...

---

# 2. Opis biznesu

## 2.1 Procesy biznesowe

**Diagram:** Proces 1

---

# 3. Wizja systemu

## 3.1 Opis problemu

**Diagram:** Opis problemu

**P001: Problem obsługi klientów**

- Typ: «Wizja»
- Wersja: 1.0 (15.02.2023)
- Odpowiedzialny: smial
- Priorytet i trudność: Istotne 1
- Wydanie: 1.0

Problem związany z .... dotyczący... co powoduje ... można rozwiązać ...

---

## 3.2 Interesariusze

**Diagram:** Interesariusze

**Właściciel sieci ASO**

- Typ: «interesariusz»
- Wersja: 1.0 (15.02.2023)
- Odpowiedzialny: smial
- Priorytet i trudność:
- Wydanie: 1.0

---

## 3.3 Cechy funkcjonalne




F03: System powinien umożliwiać tworzenie profili postaci.
| Typ: _funkcjonalne_ | Wersja: 1.0 (01.03.2026) | Odpowiedzialny: Polina |
| :--- | :--- | :--- |
| Priorytet i trudność: Kluczowe || Wydanie: 1.0 |
| Zaimplementowanie funkcjonalności umożliwiającej użytkownikowi tworzenie nowych profili postaci do gry LARP. Użytkownik powinien móc zdefiniować podstawowe atrybuty postaci (imię, klasa/rasa np. elf, krasnolud, rycerz, poziom doświadczenia), dodać opis biografii oraz wybrać wygląd postaci. Każda utworzona postać jest automatycznie powiązana z kontem użytkownika, który ją stworzył. |
F04: System powinien umożliwiać edycję i przeglądanie szczegółów postaci.
| Typ: _funkcjonalne_ | Wersja: 1.0 (01.03.2026) | Odpowiedzialny: Polina |
| :--- | :--- | :--- |
| Priorytet i trudność: Istotne || Wydanie: 1.0 |

| Zaimplementowanie funkcjonalności pozwalającej użytkownikowi na edycję wszystkich danych istniejącej postaci (imię, biografia, atrybuty, ekwipunek) oraz przeglądanie jej szczegółowych statystyk. System powinien wyświetlać informacje o poziomie doświadczenia, posiadanych przedmiotach, osiągnięciach z poprzednich sesji oraz historię rozgrywek daną postacią. Edycja postaci powinna być możliwa tylko gdy postać nie bierze aktualnie udziału w trwającej sesji LARP. |
F05: System powinien umożliwiać przeglądanie historii uczestnictwa w wydarzeniach.
| Typ: _funkcjonalne_ | Wersja: 1.0 (01.03.2026) | Odpowiedzialny: Polina |
| :--- | :--- | :--- |
| Priorytet i trudność: Istotne || Wydanie: 1.0 |

| Zaimplementowanie sekcji pozwalającej użytkownikowi na przeglądanie pełnej historii wydarzeń LARP, w których brał udział. System powinien wyświetlać listę wszystkich ukończonych sesji z podstawowymi informacjami (data, nazwa wydarzenia, lokalizacja, odegrana postać, czas trwania), a także prezentować zagregowane statystyki takie jak: całkowita liczba ukończonych sesji, najczęściej grane role, ulubione scenariusze i typy wydarzeń. Historia powinna być sortowalna według daty oraz filtrowalna według typu wydarzenia, odgrywanej postaci lub organizatora. |
F06: System powinien umożliwiać edycję danych osobowych w profilu użytkownika.
| Typ: _funkcjonalne_ | Wersja: 1.0 (01.03.2026) | Odpowiedzialny: Polina |
| :--- | :--- | :--- |
| Priorytet i trudność: Kluczowe || Wydanie: 1.0 |
| Zaimplementowanie panelu umożliwiającego użytkownikowi edycję swoich danych osobowych w systemie. Użytkownik powinien móc zmienić imię, nazwisko, adres email, numer telefonu oraz hasło do konta. System powinien wymagać potwierdzenia zmiany wrażliwych danych (email, hasło) poprzez weryfikację aktualnego hasła lub kod wysłany na dotychczasowy adres email. Wszystkie zmiany danych osobowych powinny być zapisywane w historii zmian konta dla celów bezpieczeństwa. |

F07: System powinien umożliwiać zarządzanie preferencjami użytkownika.
| Typ: _funkcjonalne_ | Wersja: 1.0 (01.03.2026) | Odpowiedzialny: Polina |
| :--- | :--- | :--- |
| Priorytet i trudność: Przydatne || Wydanie: 1.0 |
| Zaimplementowanie sekcji konfiguracji preferencji systemowych użytkownika. Użytkownik powinien móc skonfigurować ustawienia powiadomień (email, SMS, powiadomienia push dla aplikacji mobilnej), określić preferencje dotyczące typów wydarzeń LARP (fantasy, sci-fi, horror, historyczne), wskazać preferowane dni tygodnia i przedziały czasowe uczestnictwa, oraz ustawić poziom prywatności profilu określający widoczność swoich danych i statystyk dla innych użytkowników systemu. |

F08: System powinien umożliwiać rejestrację nowego konta.
| Typ: _funkcjonalne_ | Wersja: 1.0 (02.03.2026) | Odpowiedzialny: cojarobietu9 |
| :--- | :--- | :--- |
| Priorytet i trudność: Kluczowe || Wydanie: 1.0 |
| Zaimplementowanie funkcjonalności umożliwiającej użytkownikowi rejestrację konta na platformie. Tworzone konto wymaga od użytkownika podania swojego adresu e-mail, dostępnej i unikatowej nazwy konta, oraz dwukrotnego podania hasła. System powinien posiadać odpowiednie wymagania dotyczące hasła (np. długość, rodzaj znaków) i informować, kiedy użytkownik podał odpowiedni przykład. Rejestracja konta możliwa jest po potwierdzeniu tożsamości za pomocą podanego adresu e-mail.|

F09: System powinien umożliwiać logowanie metodą dwuetapową.
| Typ: _funkcjonalne_ | Wersja: 1.0 (02.03.2026) | Odpowiedzialny: cojarobietu9 |
| :--- | :--- | :--- |
| Priorytet i trudność: Użyteczne || Wydanie: 1.0 |
| Zaimplementowanie funkcjonalności umożliwiającej użytkownikowi dwuetapowe potwierdzenie tożsamości, pierwszy raz za pomocą hasła i drugi raz np. za pomocą kodu QR pochodzącego od dezygnowanej aaplikacji. Użytkownik powinien mieć możliwość włączenia tej opcji wedle życzenia, oraz wyłączenia jej przy pomocy np. adresu mailowego.|

F10: System powinien umożliwiać interakcję z otoczeniem poprzez kody QR.
| Typ: _funkcjonalne_ | Wersja: 1.0 (02.03.2026) | Odpowiedzialny: Tomasz2004 |
| :--- | :--- | :--- |
| Priorytet i trudność: Istotne || Wydanie: 1.0 |
| Zaimplementowanie w aplikacji mobilnej skanera kodów QR, który pozwoli graczom na wchodzenie w interakcję z fizycznymi elementami gry. Po zeskanowaniu kodu system powinien wyświetlić opis obiektu, dodać przedmiot do ekwipunku lub uruchomić przypisaną akcję fabularną. |

F11: System powinien pozwalać użytkownikom na wybór postaci przed rozpoczęciem gry.

| Typ: Funkcjonalne | Wersja: 1.0 (2.03.2026) | Odpowiedzialny: mkkami |
| :--- | :--- | :--- |
| Priorytet i trudność: Kluczowe || Wydanie: 1.0|
| Uczestnicy powinni mieć możliwość wyboru roli z listy przypisanej do gry. System powinien prezentować listę dostępnych postaci wraz z ich opisami i umożliwiać zgłoszenie chęci odgrywania konkretnej postaci przez użytkownika. ||

F12: System powinien wspierać mechanizm priorytetyzacji wyboru ról.

| Typ: Funkcjonalne | Wersja: 1.0 (2.03.2026) | Odpowiedzialny: mkkami |
| :--- | :--- | :--- |
| Priorytet i trudność: Istotne || Wydanie: 1.0|
| Uczestnicy, którzy nie grali danej roli powinni mieć priorytet w zapisach, aby umożliwić im zdobycie nowych doświadczeń. Jednocześnie uczestnicy, którzy ostatnio odgrywali dane role powinni mieć mniejszy priorytet. ||

F13: System powinien umożliwiać obsługę płatności za wydarzenia poprzez integrację z systemem zewnętrznym.
| Typ: Funkcjonalne | Wersja: 1.0 (2.03.2026) | Odpowiedzialny: mkkami |
| :--- | :--- | :--- |
| Priorytet i trudność: Kluczowe || Wydanie: 1.0|
| Zapewnienie uczestnikom możliwości opłacenia udziału w wydarzeniu bezpośrednio po zatwierdzeniu ich zgłoszenia. System powinien integrować się z zewnętrznymi systemami płatności i automatycznie aktualizować status zapisu uczestnika po otrzymaniu potwierdzenia transakcji. ||
---

## 3.4 Cechy jakościowe

J02: System powinien wyświetlać dezygnowane ekrany oczekiwania w momentach ładowania się strony.
| Typ: _jakościowe_ | Wersja: 1.0 (02.03.2026) | Odpowiedzialny: cojarobietu9 |
| :--- | :--- | :--- |
| Priorytet i trudność: Istotne || Wydanie: 1.0 |
| Strona i aplikacja powinny posiadać ekrany oczekiwania w sytuacjach ładowania i przesyłania zasob

J03: System powinien zapewniać dostępność interfejsu mobilnego w trybie offline.
| Typ: _jakościowe_ | Wersja: 1.0 (02.03.2026) | Odpowiedzialny: Tomasz2004 |
| :--- | :--- | :--- |
| Priorytet i trudność: Istotne || Wydanie: 1.0 |
| Zapewnienie ciągłości działania kluczowych funkcji aplikacji (podgląd karty postaci, historia akcji) w warunkach braku połączenia z siecią. System musi lokalnie przechowywać najważniejsze dane i przeprowadzać synchronizację z serwerem natychmiast po odzyskaniu dostępu do Internetu. |


## 3.5 Słownik

**Diagram:** Słownik

**Model samochodu**

- Typ:
- Wersja: 1.0 (15.02.2023)
- Odpowiedzialny: smial
- Priorytet i trudność:
- Wydanie: 1.0

dokładny opis samochodów o tych samych parametrach

**Samochód**

- Typ:
- Wersja: 1.0 (15.02.2023)
- Odpowiedzialny: smial
- Priorytet i trudność:
- Wydanie: 1.0

konkretny egzemplarz danego modelu samochodu

---

# 4. Wymagania użytkownika

## 4.1 Wymagania funkcjonalne

### 4.1.1 Zarządzanie ofertą

**Diagram:** Zarządzanie ofertą

**PU001: Dodanie nowego samochodu**

- Wersja: 1.0 (15.02.2023)
- Odpowiedzialny: smial
- Priorytet i trudność: Istotne 1
- Wydanie: 1.0

**PU002: Przejrzenie cennika**

- Wersja: 1.0 (15.02.2023)
- Odpowiedzialny: kamil
- Priorytet i trudność: Istotne 1
- Wydanie: 1.0

**PU003: Wygenerowanie raportu sprzedaży**

- Wersja: 1.0 (15.02.2023)
- Odpowiedzialny: kamil
- Wydanie: 1.0

**PU004: Zmiana ceny samochodu**

- Wersja: 1.0 (15.02.2023)
- Odpowiedzialny: kamil
- Wydanie: 1.0

---

### 4.1.2 Zarządzanie sprzedażą

**Diagram:** Specyfikowanie wymagań użytkownika

**PU101: Dokonanie płatności online**

- Wersja: 1.0 (15.02.2023)
- Odpowiedzialny: kamil
- Wydanie: 1.0

**PU102: Dokonanie zamówienia na samochód**

- Wersja: 1.0 (15.02.2023)
- Odpowiedzialny: kamil
- Wydanie: 1.0

**PU103: Pokazanie listy samochodów**

- Wersja: 1.0 (15.02.2023)
- Odpowiedzialny: kamil
- Wydanie: 1.0

**PU104: Potwierdzenie zamówienia na samochód**

- Wersja: 1.0 (15.02.2023)
- Odpowiedzialny: kamil
- Wydanie: 1.0

**PU105: Przejrzenie listy zamówień**

- Wersja: 1.0 (15.02.2023)
- Odpowiedzialny: kamil
- Wydanie: 1.0

**PU106: Wydanie samochodu do sprzedaży**

- Wersja: 1.0 (15.02.2023)
- Odpowiedzialny: kamil
- Wydanie: 1.0

**PU107: Zarejestrowanie wydania samochodu**

- Wersja: 1.0 (15.02.2023)
- Odpowiedzialny: kamil
- Wydanie: 1.0

**PU108: Złożenie zamówienia specjalnego**

- Wersja: 1.0 (15.02.2023)
- Odpowiedzialny: kamil
- Wydanie: 1.0

---

## 4.2 Wymagania jakościowe i ograniczenia

**Diagram:** Wymagania jakościowe i ograniczenia

**J022-1: Maksymalna liczba kliknięć w celu otwarcia formularza awarii**

- Typ: «Uzytecznosc»
- Wersja: 1.0 (15.02.2023)
- Odpowiedzialny: smial
- Priorytet i trudność: Przydatne 1
- Wydanie: 1.0

**Sposób pomiaru:**  
Przeprowadzenie serii nawigacji do ekranu formularza awarii z różnych miejsc w interfejsie użytkownika, zgodnie ze scenariuszem TS112

**Oczekiwane wartości:**  
liczba kliknięć dla 90% sytuacji wynosi mniej niż 3; dla wszystkich sytuacji wynosi mniej niż 5

---

**J022-2: Rejestracja awarii powinna trwać średnio nie dłużej niż minutę**

- Typ: «Uzytecznosc»
- Wersja: 1.0 (15.02.2023)
- Odpowiedzialny: smial
- Priorytet i trudność: Istotne 1
- Wydanie: 1.0

**Sposób pomiaru:**  
Przeprowadzenie serii rejestracji zgodnie ze scenariuszem TS003 (…)

**Oczekiwane wartości:**  
średni czas wynosi < 1 min, maksymalny czas wynosi (…)

---

## 4.3 Słownik

### 4.3.1 Aktorzy

- Kierownik
- Klient
- Magazynier
- SI Producenta
- SI Płatności
- Sprzedawca

---

### 4.3.2 Słownik dziedziny

- Cennik
- Dodatek
- Dodatkowa pozycja cennika
- Model samochodu
- Podstawowa pozycja cennika
- Pozycja cennika
- Samochód
- Zamówienie na samochód

---

# 5. Scenariusze i scenopisy

## 5.1 PU001: Dodanie nowego samochodu

**Scenariusz główny**

1. Aktor wybiera opcję
2. System wyświetla ekran

**Diagram:** Dodanie nowego samochodu - scenopis

---

## 5.2 PU101: Dokonanie płatności online

**Scenariusz główny**

1. Aktor wybiera opcję
2. System wyświetla ekran

---

## 5.3 PU106: Wydanie samochodu do sprzedaży

**Scenariusz główny**

1. Aktor wybiera opcję
2. System wyświetla okno
3. System zapisuje dane

**Błąd danych**

1-2. -"-  
3a. System wyświetla komunikat
