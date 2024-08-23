# Wstęp

Celem niniejszego opracowania jest stworzenie uporządkowanie i zaprezentowanie najważniejszych koncepcji z zakresu uczenia maszynowego i zaawansowanej analizy danych (ang. *data science*).

Z założenia, materiał ma być przeglądowy i przystępny dla osób, które nie miały wcześniej styczności z tematyką uczenia maszynowego, a także dla tych, którzy chcą uporządkować wiedzę rozproszoną w różnych źródłach.

W opracowaniu skupiono się głównie na praktycznych aspektach uczenia maszynowego, a omawiane zagadnienia poparto przykładami w języku Python. Gdzie to tylko możliwe - podano odsyłacze do materiałów źródłowych/przewodników/dokumentacji/tutoriali, które warto przeczytać, aby lepiej zrozumieć dany aspekt. Oczywiście, pojawią się też sekcje poświęcone np. teorii uczenia maszynowego czy szeregów czasowych - mają one na celu kompleksowe i całościowe przedstawienie danego tematu. Czytelnik lub Czytelniczka odnajdzie tu też szereg formalnych definicji, które starają się usystematyzować pojęcia powszechnie znane i stosowane w praktyce, ale niekoniecznie wyłożone w ustrukturyzowany sposób (np. czym różni się model od algorytmu uczenia maszynowego? Jak zdefiniować ograniczenia poznawcze modelu?).

Podręcznik ma charakter otwarty i płynny, co oznacza, że prace nad nim wciąż trwają, a ich efekty będą systematycznie udostępniane na niniejszej stronie.


## Dalsze plany i zakres prac / "early access"

Niniejsze opracowanie jest w fazie rozwoju. W miarę postępów w pracach nad skryptem, będziemy dodawać nowe rozdziały, poprawiać błędy, uzupełniać treści. Docelowo, planowane jest pokrycie następujących tematów:

1. **Data science** - czym jest, z czego się składa, jakie są narzędzia, jakie są etapy procesu analizy danych.
2. **Praca z danymi** - rozdział poświęcony obróbce i przetwarzaniu danych. W szczególności:
   1. Typy i struktury danych - ustruktyzowane i nieustrukturyzowane, numeryczne, itd.
   2. Typowe operacje na danych - filtrowanie, grupowanie, łączenie, itd.
   3. Analiza poprawności i kompletności danych.
   4. Potoki przetwarzania (ang. pipelines) - automatyzacja procesu przetwarzania danych.
   5. Wizualizacja danych.
3. **Wprowadzenie do uczenia maszynowego** - rozdział omawiający niezbędne minimum teorii i notacji potrzebnej do zrozumienia tej dziedziny. W szczególności:
   1. Podstawowe pojęcia - model, cechy, etykiety, funkcja kosztu, itd.
   2. Elementy teorii COLT - elementy teorii uczenia obliczeniowego i generalizacji.
   3. Taksonomia modeli uczenia maszynowego - modele liniowe, drzewiaste, sieci neuronowe, itd.
4. **Projektowanie eksperymentów** - w jaki sposób projektować i przeprowadzać eksperymenty związane z uczeniem maszynowym. W szczególności:
   1. Podział danych na zbiory treningowy, walidacyjny i testowy.
   2. Ocena modeli - metryki jakości, walidacja krzyżowa, itd.
   3. Optymalizacja hiperparametrów.
   4. Analiza wyników eksperymentów.
5. **Modele uczenia maszynowego** - rozdział poświęcony praktycznemu zastosowaniu modeli uczenia maszynowego. W szczególności:
   1. Regresja - modele liniowe, drzewiaste, sieci neuronowe.
   2. Klasyfikacja - modele liniowe, drzewiaste, sieci neuronowe.
   3. Grupowanie - k-means, DBSCAN, itd.
   4. Klasyfikacja wieloklasowa.
   5. Regresja wielowymiarowa.
   6. Modele sekwencyjne - sieci rekurencyjne, sieci splotowe.
   7. Modele generatywne - sieci GAN, VAE.
6. **Budowanie projektów data science** - w jaki sposób konstruować projekty DS. W szczególności:
   1. Metoda CRISP-DM zarządzania projektami.
   2. Szablony projektów DS i rozwiązań technicznych.
7. **Narzędzia i zaplecze techniczne Data Science** - czyli o technikach, narzędziach i rozwiązaniach, które warto znać, aby płynnie poruszać się po projektach DS. W szczególności:
   1. Środowiska pracy - Visual Studio Code, Jupyter, Google Colab, Lightning Studio, etc.
   2. Git, jako podstawowe narzędzie kontroli wersji.
   3. Przydatne biblioteki w Pythonie - czyli które trzeba znać obowiązkowo, które ułatwiają pracę, automatyzują zadania, itd.
   4. Docker o Kubernetes - narzędzia do konteneryzacji aplikacji.
   5. Kedro, DVC, MlFlow - narzędzia do zarządzania eksperymentami, danymi i modelami.
   6. MLOPS - szersze spojzrenie na to, jak zarządzać cyklem życia modeli uczenia maszynowego.


Opracowanie całego tego materiału zajmie oczywiście wiele czasu. Rozdziały, podrozdziały i sekcje będą udostępniane w miarę ich pojawiania się