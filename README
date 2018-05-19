# Distributed monitor for study project - Rozproszony monitor - algorytm Suzuki-Kasami


## Requirements
- Python 3
- ZeroMQ library (pip install zmq)


### Examples/Przykłady


#### producent.py
Program generuje liczby i dokłada je do współdzielonej listy. Po wygenerowaniu 20 liczb kończy swoje działanie.

Parametry:
1. Służy do oznaczenia, który węzeł jako pierwszy będzie miał token. 1 oznacza token.
2. Adres i port bieżącego węzła.
3. i następne to adresy innych węzłów

#### konsument.py
Program pobiera ze wspóldzielonej listy liczby i wyświetla je. Po 5 nieudanych próbach (lista jest pusta) pobrania liczby kończy swoje działanie.

Parametry:
1. Adres i port bieżącego węzła
2. i następne to adresy innych węzłów

#### konfiguracja systemu producent-konsument dla 2 producentów i 2 konsumentów
Każdy z węzłów nasłuchuje na swoim porcie i adresie 127.0.0.1

- python3 producent.py 1 127.0.0.1:2222 127.0.0.1:3333 127.0.0.1:4444 127.0.0.1:5555
- python3 producent.py 0 127.0.0.1:3333 127.0.0.1:2222 127.0.0.1:4444 127.0.0.1:5555
- python3 konsument.py 127.0.0.1:4444 127.0.0.1:5555 127.0.0.1:2222 127.0.0.1:3333
- python3 konsument.py 127.0.0.1:5555 127.0.0.1:4444 127.0.0.1:2222 127.0.0.1:3333
