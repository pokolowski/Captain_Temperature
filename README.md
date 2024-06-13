# Strona do wyświetlania temperatur w serwerowniach

Strona za pomocą API oraz RaspberryPI i czujnika temperatury, sprawdza temperaturę w 3 serwerowniach znajdujących się w różnych lokalizacjach (Poznań, Września, Obłaczkowo). System ten służy do monitorowania przez dział na bieżąco temperatury jakie panują w serwerowniach.

Różne lokalizacje mają różną wartość dla powiadomienia o podwyższonej temperaturze. Gdy pierwszy próg podwyższonej temperatury zostanie osiągnięty - kafelek z nazwą lokalizacji podświetli się na żółto. Znaczy to, że ktoś powinien się zainteresować skokiem temperatury.
Gdy temperature osiądnie następny próg kafelek lokalizacji podświetli się na czerwono, oznaczając zagrożenie dla urządzeń wewnątrz serwerowni.

Strona jest napisana za pomocą React.js oraz wyświetlana jest w godzinach pracy na telewizorze w dziale.


## Kod strony

Ze względu na wrażliwe dane zdecydowałem się nie udostępniać kodu źródłowego. Jeśli pojawią się jakieś pytania chętnie na nie odpowiem w trakcie rozmowy :)

## Wykresy

Na stronie można wybrać zakres wyświetlanych danych pobranych z czujnika.
 - Można wyświetlać ostatnie 20 minut wykresu (opcja "Na żywo")
 - Można wyświetlać ostatnie 24 godziny wykresu (opcja "24h")
 - Można wyświetlać ostatnie 3 dni wykresu (opcja "3 dni")
 - Można wyświetlać wszystkie pobrane dane od uruchomienia (opcja "Wszystko")

## Raspberry wraz z czujnikiem Enviro+

W serwerowniach znajduję się urządzenie Raspberry PI wraz z skonfigurowanym czujnikiem temperatury Enviro+. Na urządzeniu zainstalowane jest rozwiązanie Domoticz, które pobiera informację z czujnika i wystawia swoje API.

## API

Moja Strona pobiera dane z API w odstępach czasowych i wyświetla te dane, a także za pomocą biblioteki chart.js rysuje wykres temperatur, który umożliwia obserwowanie jak temperatura się zmienia (np. zauważenie nagłej tendencji wzrostowej).

## Czujnik światła

Z API pobierana jest również ilość lumenów, dzięki czemu można sprawdzić czy światło w serwerowni zostało zgaszone :) 

## Galeria

Zdjęcie strony wyświetlanej na telewizorze
![Zdjecie z tendencja wzrostowa temperatury z jedna lokalizacja](https://github.com/pokolowski/Captain_Temperature/blob/main/photos/kapitan.jpg?raw=true)

Screen strony wraz z informacją o zapalonym świetle w serwerowni w lokalizacji Obłaczkowo
![Zdjecie z tendencja wzrostowa temperatury z jedna lokalizacja](https://github.com/pokolowski/Captain_Temperature/blob/main/photos/unnamed%20(1).png?raw=true)

Screen strony - wszystkie światła zgaszone, temperatury w normie.
![Zdjecie z tendencja wzrostowa temperatury z jedna lokalizacja](https://github.com/pokolowski/Captain_Temperature/blob/main/photos/unnamed%20(2).png?raw=true)

Screen strony - lokalizacja (Poznań) - temperatura przekroczyła pierwszy próg ostrzeżenia.
![Zdjecie z tendencja wzrostowa temperatury z jedna lokalizacja](https://github.com/pokolowski/Captain_Temperature/blob/main/photos/temperature_alert?raw=true)


