# SHModbus - Podręcznik Użytkownika

![Aplikacja SHModbus](../shared-images/shmodbus-app.png)

## Przegląd

SHModbus Client to aplikacja do monitorowania i wizualizacji danych przemysłowych w czasie rzeczywistym, która łączy się z urządzeniami Modbus i wyświetla dane sensorów na żywo, status urządzeń oraz informacje systemowe przez intuicyjny interfejs webowy.

## Kluczowe Funkcje

### Monitorowanie Danych w Czasie Rzeczywistym
- **Tabela Danych na Żywo**: Wyświetlanie wartości w czasie rzeczywistym z podłączonych urządzeń Modbus z automatycznymi aktualizacjami
- **Auto-odświeżanie**: Dane aktualizują się automatycznie co kilka sekund bez ręcznego odświeżania
- **Wyświetlanie Znaczników Czasowych**: Zobaczysz dokładnie, kiedy każdy punkt danych został ostatnio zaktualizowany
- **Formatowanie Wartości**: Wszystkie wartości numeryczne wyświetlają się z konsystentną precyzją 2 miejsc po przecinku

### Wizualizacja Danych
- **Interaktywne Wykresy**: Wizualna reprezentacja trendów danych w czasie
- **Wiele Typów Wykresów**: Wykresy liniowe, słupkowe i inne opcje wizualizacji
- **Dane Historyczne**: Wyświetlanie trendów i wzorców danych z przeszłości
- **Powiększanie i Przesuwanie**: Interakcja z wykresami w celu skupienia się na określonych okresach

### Zarządzanie Urządzeniami
- **Status Połączenia**: Wskazanie w czasie rzeczywistym łączności urządzeń Modbus
- **Informacje o Urządzeniach**: Wyświetlanie szczegółów o podłączonym sprzęcie i sensorach
- **Obsługa Wielu Urządzeń**: Monitorowanie wielu urządzeń Modbus jednocześnie
- **Kondycja Połączenia**: Wizualne wskaźniki pokazujące czy urządzenia są online/offline

### Funkcje Interfejsu Użytkownika
- **Responsywny Design**: Działa na komputerach stacjonarnych, tabletach i urządzeniach mobilnych
- **Motyw Ciemny/Jasny**: Wybierz preferowany motyw wizualny
- **Sortowalne Tabele**: Kliknij nagłówki kolumn aby sortować dane według dowolnego pola
- **Wyszukiwanie i Filtrowanie**: Szybkie znajdowanie określonych punktów danych
- **Możliwości Eksportu**: Zapisywanie danych do plików dla zewnętrznej analizy

### Komunikacja w Czasie Rzeczywistym
- **Integracja SignalR**: Natychmiastowe aktualizacje danych bez odświeżania strony
- **Powiadomienia na Żywo**: Natychmiastowe alerty gdy status urządzenia się zmienia
- **Automatyczne Ponowne Łączenie**: Utrzymuje połączenie nawet podczas przerw w sieci
- **Niska Latencja**: Minimalne opóźnienie między aktualizacjami urządzenia a wyświetlaniem

### Zarządzanie Danymi
- **Dane w Cache**: Najnowsze wartości przechowywane lokalnie dla szybkiego dostępu
- **Historia Danych**: Dostęp do historycznych odczytów i trendów
- **Walidacja Wartości**: Automatyczne wykrywanie i obsługa nieprawidłowych danych
- **Obsługa Stref Czasowych**: Wyświetla czasy w lokalnej strefie czasowej

## Zastosowania Przemysłowe

- **Monitorowanie Procesów**: Śledzenie temperatury, ciśnienia, przepływów i innych zmiennych procesowych
- **Status Urządzeń**: Monitorowanie prędkości silników, pozycji zaworów, statusu pomp
- **Monitorowanie Alarmów**: Alarmy w czasie rzeczywistym dla warunków poza zakresem
- **Kontrola Jakości**: Śledzenie wskaźników produkcji i parametrów jakości
- **Zarządzanie Energią**: Monitorowanie zużycia energii i wskaźników efektywności

## Funkcje Dostępności

- **Nawigacja Klawiaturą**: Pełna kontrola aplikacji używając tylko klawiatury
- **Obsługa Czytników Ekranu**: Kompatybilne z technologiami wspomagającymi
- **Opcje Wysokiego Kontrastu**: Zwiększona widoczność dla użytkowników z wadami wzroku
- **Skalowalny Interfejs**: Regulowane rozmiary tekstu i elementów

## Optymalizacja Wydajności

- **Efektywne Aktualizacje**: Odświeża tylko dane, które rzeczywiście się zmieniły
- **Optymalizacja Przepustowości**: Minimalne użycie sieci dla ciągłego monitorowania
- **Kompatybilność z Przeglądarkami**: Działa ze wszystkimi nowoczesnymi przeglądarkami
- **Szybkie Ładowanie**: Szybki start i responsywny interfejs

## Opcje Konfiguracji

- **Konfigurowalne Widoki**: Układaj wyświetlacze danych zgodnie z przepływem pracy
- **Preferencje Użytkownika**: Zapisuj preferowane ustawienia i układy
- **Wybór Punktów Danych**: Wybieraj które sensory i wartości monitorować
- **Interwały Aktualizacji**: Dostosowuj jak często dane się odświeżają

## Funkcje Bezpieczeństwa

- **Bezpieczne Połączenia**: Szyfrowana komunikacja z urządzeniami i serwerami
- **Uwierzytelnianie Użytkowników**: Kontrola dostępu i zarządzanie użytkownikami
- **Integralność Danych**: Weryfikacja, że wyświetlane dane są dokładne i niezmienione
- **Ścieżka Audytu**: Logowanie działań użytkowników i zdarzeń systemowych

## Typowe Przypadki Użycia

- **Produkcja**: Monitorowanie sprzętu linii produkcyjnej i wskaźników jakości
- **Systemy HVAC**: Śledzenie temperatury, wilgotności i jakości powietrza
- **Oczyszczanie Wody**: Monitorowanie przepływów, poziomów chemicznych i statusu pomp
- **Systemy Energetyczne**: Śledzenie wytwarzania, zużycia i efektywności energii
- **Automatyka Budynkowa**: Monitorowanie oświetlenia, bezpieczeństwa i systemów środowiskowych
- **Sprzęt Laboratoryjny**: Śledzenie warunków testowych i wyników pomiarów

## Pierwsze Kroki

1. Otwórz aplikację w przeglądarce internetowej
2. Poczekaj na ustanowienie połączenia z urządzeniami Modbus
3. Wyświetl dane w czasie rzeczywistym w Tabeli na Żywo
4. Eksploruj wykresy i wizualizacje dla trendów
5. Dostosuj swój widok sortując i filtrując dane
6. Ustaw alerty i monitorowanie dla krytycznych parametrów

Aplikacja automatycznie obsługuje wszystkie szczegóły techniczne komunikacji Modbus, formatowania danych i aktualizacji w czasie rzeczywistym, pozwalając skupić się na monitorowaniu procesów przemysłowych i sprzętu.