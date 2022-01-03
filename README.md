##
# **Last Man Flying**

**Complete System Project**

### By

### **Tomorrow Studios**

Krzysztof Łazarz, Bartłomiej Tarcholik

### Wymagania projektu

- Gra wykorzystuje bazę danych
- Jest zaimplementowane logowanie
- Jest możliwość zmiany podstawowych parametrów gry bez rekompilacji
- Jest ranking graczy
- Jest ulepszanie pojazdu
- Jest zaprogramowana sama rozgrywka

### Możliwe zastosowania

Jako gra stworzona na komputery osobiste oraz urządzenia z systemem Android, Last Man Flying jest oprogramowaniem rozrywkowym. Dzięki zaimplementowaniu bazy danych w chmurze, gra jest wieloplatformowa, co pozwala na tworzenie turniejów niezależnie od tego, czy uczestnicy korzystają z telefonu, czy z komputera. Działanie oprogramowania na Androidzie pozwala na granie w dowolnym miejscu, a dzięki użyciu bazy danych, która pozostaje ciągle on-line, również o każdym czasie.

### Diagramy encji i relacji

## Relacje:

![](RackMultipart20220103-4-1w5m8op_html_2760229d80cd74f0.png)

## Encje:

![](RackMultipart20220103-4-1w5m8op_html_27f105f6143b04f8.png)

##
### Narzędzia

Visual Studio Community

Unity Editor 2019.4 LTS

GitHub

Google Drive

diagrams.net

### Interfejsy i Struktury danych

## Interfejsy

W tym projekcie są 3 interfejsy. Dwa robione w ramach projektu oraz jeden zapewniony przez Googla w postaci paczki do Unity.

![](RackMultipart20220103-4-1w5m8op_html_ccb1f3603ed39d3b.png)

### Cloud - Firebase

Usługa Firebase od Google zapewnia nam połączenie sieciowe z bazą oraz robi odpowiednie zapytania.

### Firebase - Backend

Klasa FirebaseManager zbiera żądania jakie mogą się pojawić od backendu oraz konwertuje je na komendy do API Firebase&#39;a. Posiada zintegrowane oczekiwanie na zakończenie połączenia z chmurą i obsługuje ewentualne wyjątki.

### Backend - Frontend

#### UI Manager

W Unity połączenie z interfejsem polega na ręcznym utworzeniu interfejsu, a następnie do każdej instancji przycisku podpinana jest instancja skryptu zwyczajnie przy pomocy myszki, metodą drag-and-drop. Po podpięciu skryptu, wybiera się funkcję, która ma zostać wywołana po wciśnięciu. Z reguły w tym projekcie, skrypt do którego odwołuje się przycisk, posiada w sobie funkcję o tej samej nazwie co instancja przycisku.

Pola tekstowe są podpinane w odwrotny sposób. Najpierw tworzy się instancje skryptu, a następnie jej publiczne zmienne typu TextField, są ręcznie ustawiane na instancje fragmentów GUI.

#### Player Manager

Kontrola gracza to podstawowy element gry i odbywa się on przez przekazywanie odczytu z klawiatury do skryptu gracza, który wykonuje adekwatne akcje.

### GUI

Poniżej prezentujemy szkic interfejsu graficznego. Przyjęliśmy skalę jak na smartfony, na komputerze ikonki będą zdecydowanie mniejsze.

Panel Logowania:

![](RackMultipart20220103-4-1w5m8op_html_20833323665ab99f.png)

Garaż:

![](RackMultipart20220103-4-1w5m8op_html_45af06b61a5ae104.png)

## Struktury danych

W grze wyróżniamy 6 struktur danych, w tym jedną abstrakcyjną ( niemogącą istnieć samodzielnie ).

### Struktura gracza

Posiada informacje o :

- Nazwie gracza
- Identyfikatorze w bazie danych
- Sposobie logowania
- Budżecie gracza
- Kupionych ulepszeniach
- Aktualnym wyposażeniu
- Rekordzie

### Struktura rekordu

Posiada informacje o :

- Nazwie gracza
- Identyfikatorze gracza
- Wartości rekordu
- Czasie pobicia rekordu

### Struktura części

Posiada informacje o :

- Nazwie części
- Ceny części

#### Struktura skrzydeł

Dodatkowo posiada informacje o :

- Sile nośnej

#### Struktura silnika

Dodatkowo posiada informacje o :

- Poborze paliwa
- Ciągu (sile)

#### Struktura zbiornika

Dodatkowo posiada informacje o :

- Pojemności

###


### Technologie

Unity 2019.4 LTS

Google Firebase

### Testy oprogramowania

Testy poszczególnych klas są robione w dwóch fazach. Pierwsza jest sposobem naturalnym - jeśli spełniają swoją funkcjonalność w trakcie tworzenia projektu, przechodzą początkowe testy konieczne do pełnej funkcjonalności gry.

Faza druga odbędzie się wraz z udostępnieniem limitowanej ilości alpha-testerów ukończonej wersji gry, która pozwoli na przetestowanie pełnej funkcjonalności oraz szukanie błędów i możliwych wykorzystań przeczących założeniom twórców. Tacy testerzy będą starać się wykonywać nietypowe ruchy, szukać luk na mapach lub sposobów na szybkie i łatwe osiągnięcie wysokich wyników punktowych. Tak wyłapane problemy zostaną usunięte przed wydaniem gry.

### Analiza ryzyka

| **Zagrożenie** | **Prawdopodobieństwo wystąpienia** | **Skutki** | **Wpływ zagrożenia na projekt** | **Ruch Zapobiegawczy** | **Działania profilaktyczne** |
| --- | --- | --- | --- | --- | --- |
| Utrata lokalnych zmian | Umiarkowane | Konieczność odtworzenia utraconych danych | Niewielki | Łagodzenie ryzyka | Regularne wysyłanie danych na repozytorium Git |
| Błąd kompatybilności skryptów | Ponadprzeciętne | Konieczność przeanalizowania kodu projektu od nowa i poprawienia wszystkich problemów wpływających na błąd kompatybilności | Średni | Unikanie ryzyka | Modułowa konstrukcja projektu pozwalająca na zminimalizowanie potencjalnego błędu jedynie do konkretnego modułu |
| Przeziębienie członka zespołu | Wysokie | Zmniejszenie efektywności pracy | Niewielki | Unikanie ryzyka | Adekwatne ubieranie się, odpowiednia dieta, dbanie o odporność |
| Wystąpienie objawów SARS-CoV-2 u członka zespołu | Dość wysokie | 2-tygodniowa kwarantanna, zmniejszenie efektywności pracy | Średni | Unikanie ryzyka | Przestrzeganie zasad sanitarnych |
| Opóźnienie związane z kumulacją zadań związanych ze studiowaniem | Wysokie | Mały lub zerowy postęp nad projektem do czasu oddania innych projektów | Średni | Unikanie ryzyka | Systematyczna praca |
| Uszkodzenie urządzenia jednego z członków zespołu | Niskie | Długotrwały problem z wykonywaniem projektu do czasu naprawy urządzenia | Poważny | Unikanie ryzyka | Traktowanie urządzeń z zachowaniem zasad ostrożności |
| Zmiana modelu finansowania Firebase | Znikome | Konieczność znalezienia darmowej alternatywnej bazy danych i ponownego napisania skryptów bazodanowych | Poważny | Akceptacja ryzyka | Brak działań profilaktycznych |
| Brak kompatybilności fragmentów dokumentacji z aktualną wersją Unity | Ponadprzeciętne | Konieczność znalezienia alternatywnych możliwości rozwiązania problemu | Pomijalny | Unikanie ryzyka | Gdy to możliwe używanie najnowszej dokumentacji Unity, używanie tylko wcześniej przetestowanych metod i funkcji |
| Opuszczenie studiów | Znikome | Utrata członka projektu, zwiększenie ilości obowiązków poszczególnych członków | Poważny | Akceptacja ryzyka | Zmiana założeń projektu tak, aby były w granicach możliwości pozostałego zespołu |
| Konieczność zmiany oprawy wizualnej gry | Niskie | Potrzeba utworzenia nowych modeli 3D i innych elementów wizualnych | Poważny | Akceptacja ryzyka | Posiadanie alternatywnego pomysłu, który będzie bezpieczny w realizacji |
| Maintenance-break Githuba | Umiarkowane | Brak dostępu do synchronizacji | Niewielki | Akceptacja ryzyka | Brak działań profilaktycznych |
| Maintenance-break Facebooka | Niemal pewne | Brak dostępu do komunikatora | Pomijalny | Łagodzenie ryzyka | Wykorzystywanie Discorda oraz Telegrama jako zapasowych możliwości komunikacji |
| Maintenance-break Google Drive | Niskie | Brak dostępu do dokumentacji | Niewielki | Akceptacja ryzyka | Lokalne backupy rozwiązują problem dostępu, jednak wspólne tworzenie dokumentów jest niemożliwe |