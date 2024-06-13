# Strona do wyświetlania temperatur w serwerowniach

Strona za pomocą API oraz RaspberryPI i czujnika temperatury, sprawdza temperaturę w 3 serwerowniach znajdujących się w różnych lokalizacjach (Poznań, Września, Obłaczkowo). System ten służy do monitorowania przez dział na bieżąco temperatury jakie panują w serwerowniach. Strona jest napisana za pomocą React.js oraz wyświetlana jest w godzinach pracy na telewizorze w dziale.

## Raspberry wraz z czujnikiem Enviro+

W serwerowniach znajduję się urządzenie Raspberry PI wraz z skonfigurowanym czujnikiem temperatury Enviro+. Na urządzeniu zainstalowane jest rozwiązanie Domoticz, które pobiera informację z czujnika i wystawia swoje API.

## API

Moja Strona pobiera dane z API w odstępach czasowych i wyświetla te dane, a także za pomocą biblioteki chart.js rysuje wykres temperatur, który umożliwia obserwowanie jak temperatura się zmienia (np. zauważenie nagłej tendencji wzrostowej).

## Czujnik światła

Z API pobierana jest również ilość lumenów, dzięki czemu można sprawdzić czy światło w serwerowni zostało zgaszone :) co również jest 

## RESPONSYWNOŚĆ

Strona nie jest responsywna gdyż została stworzona jedynie na potrzeby wyświetlania na telewizorze.

## Galeria

Zdjęcie strony wyświetlanej na telewizorze
![Zdjecie z tendencja wzrostowa temperatury z jedna lokalizacja](https://github.com/pokolowski/kapitan-czujnik/blob/main/photos/kapitan.jpg?raw=true)

Screen strony wraz z informacją o zapalonym świetle w serwerowni w lokalizacji Obłaczkowo
![Zdjecie z tendencja wzrostowa temperatury z jedna lokalizacja](https://github.com/pokolowski/kapitan-czujnik/blob/main/photos/unnamed%20(1).png?raw=true)

Screen strony - wszystkie światła zgaszone, temperatury w normie.
![Zdjecie z tendencja wzrostowa temperatury z jedna lokalizacja](https://github.com/pokolowski/kapitan-czujnik/blob/main/photos/unnamed.png?raw=true)

Screen strony w pierwszej wersji z dodaną jedną lokalizacją (Poznań) - temperatura przekroczyła pierwszy próg ostrzeżenia.
![Zdjecie z tendencja wzrostowa temperatury z jedna lokalizacja](https://github.com/pokolowski/kapitan-czujnik/blob/main/photos/unnamed%20(3).png?raw=true)


