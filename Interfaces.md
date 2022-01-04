# **Interfejsy i Struktury danych**

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

## Struktury danych

W grze wyróżniamy 6 struktur danych, w tym jedną abstrakcyjną ( niemogącą istnieć samodzielnie ).

### Struktura gracza

Posiada informacje o:

- Nazwie gracza
- Identyfikatorze w bazie danych
- Sposobie logowania
- Budżecie gracza
- Kupionych ulepszeniach
- Aktualnym wyposażeniu
- Rekordzie

### Struktura rekordu

Posiada informacje o:

- Nazwie gracza
- Identyfikatorze gracza
- Wartości rekordu
- Czasie pobicia rekordu

### Struktura części

Posiada informacje o:

- Nazwie części
- Ceny części

#### Struktura skrzydeł

Dodatkowo posiada informacje o:

- Sile nośnej

#### Struktura silnika

Dodatkowo posiada informacje o:

- Poborze paliwa
- Ciągu (sile)

#### Struktura zbiornika

Dodatkowo posiada informacje o:

- Pojemności