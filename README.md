# Predykcja Cen Samochodów Używanych w Polsce

Projekt zrealizowany w ramach przedmiotu **Podstawy Reprezentacji i Analizy Danych (PRiAD)**. Celem projektu była kompleksowa analiza danych oraz budowa modelu uczenia maszynowego szacującego wartość rynkową pojazdów na podstawie ich parametrów technicznych.

## Cel projektu
Głównym zadaniem było stworzenie modelu regresyjnego, który na podstawie cech takich jak rok produkcji, przebieg, pojemność silnika czy marka, potrafi z przewidzieć cenę ofertową samochodu na polskim rynku wtórnym.

## Dane
Wykorzystano zbiór danych **"Car Prices in Poland"** z platformy Kaggle (autor: Aleksandr Glotov). Dane zawierają tysiące ogłoszeń sprzedaży samochodów, w tym:
* **Cechy numeryczne:** rok produkcji, przebieg, pojemność i moc silnika.
* **Cechy kategoryczne:** marka, model, generacja, rodzaj paliwa, województwo, miasto.

## Technologie
Projekt został wykonany w języku **Python** przy użyciu następujących bibliotek:
* **Analiza i czyszczenie danych:** `Pandas`, `NumPy`
* **Wizualizacja:** `Matplotlib`, `Seaborn`
* **Uczenie maszynowe:** `Scikit-learn` (Regresja Liniowa, Drzewa Decyzyjne)

## Kluczowe etapy analizy (EDA)
1.  **Czyszczenie danych:** Obsługa brakujących wartości (np. w nazwach generacji), usunięcie błędnych rekordów (np. przebieg 0 km dla aut spalinowych) oraz filtracja wartości odstających.
2.  **Analiza korelacji:** Zidentyfikowanie silnej zależności między rokiem produkcji a przebiegiem oraz ich wpływu na cenę.
3.  **Wnioski rynkowe:** Analiza wykazała dominację marek niemieckich na polskim rynku oraz silną asymetrię cenową (przewaga aut budżetowych).

## Wyniki modelowania
Porównaliśmy dwa podejścia regresyjne:
* **Regresja Liniowa:** Posłużyła jako model bazowy, pozwalając na identyfikację ogólnych trendów, jednak nie poradziła sobie z nieliniowym spadkiem wartości aut.
* **Drzewo Regresyjne:** Okazało się znacznie skuteczniejsze, osiągając wynik **$R^2 = 0,93$**. Model ten zredukował średni błąd o ponad połowę względem regresji liniowej i wykazał się dużą stabilnością dla aut z rynku masowego.

## Jak uruchomić projekt
1. Sklonuj repozytorium: `git clone https://github.com/TwojUser/car-price-prediction.git`
2. Zainstaluj wymagane biblioteki: `pip install pandas numpy matplotlib seaborn scikit-learn kagglehub`
3. Otwórz plik `PRiAD_projekt_zaliczeniowy.ipynb` w środowisku Jupyter Notebook lub Google Colab.

## Autorzy
Projekt wykonany wspólnie przez:
* Daniel Kaźmierczak
* Jakub Sak