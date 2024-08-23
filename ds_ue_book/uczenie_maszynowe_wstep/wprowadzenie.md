# Wprowadzenie do Uczenia Maszynowego [^autor]
[^autor]: Autor sekcji: {ref}`authors:filip-wojcik`.

Uczenie maszynowe (ML, *ang* Machine learning) jest bardzo szeroką dziedziną, łączącą w sobie elementy:
1. statystyki,
2. matematyki,
3. informatyki,
4. a nawet psychologii.

Co więcej, w ostatnich latach wykształciły się w jej ramach pod-dziedziny poświęcone między innymi:
1. Uczeniu głębokiemu i sieciom neuronowym,
2. Wielkim modelom językowym (ang. LLM),
3. Uczeniu ze wzmocnieniem (ang. RL) za pomocą symulatorów i (bardzo szeroko rozumianym) gier (np. giełdowych, optymalizacyjnych).
4. Uczeniu grafowemu i analizom sieci (w tym społecznościowych).

Płynne poruszanie się po zagadnieniach ML wymaga znajomości między innymi:
1. Podstaw algebry liniowej -w zakresie wymaganym do zrozumienia działania modeli liniowych, sieci neuronowych, operacji na macierzach.
2. Podstaw statystyki i probabilistyki - w zakresie zrozumienia próbkowania, kształtowania eksperymentów, oceny jakości modeli.
3. Podstaw teorii uczenia obliczeniowego COLT - w zakresie zrozumienia generalizacji, złożoności modeli, zbieżności algorytmów.
4. Znajomości specyfiki poszczególnych rodzin modeli, sposobów szkolenia, dobrych praktyk, itd.


Częstym problemem dla osób rozpoczynających przygodę w tej dziedzinie jest z jednej strony ogromna ilość dostępnych materiałów, z drugiej kwestia wybiórczości podejścia. Wiele osób, które chcą zapoznać się np. z grafowymi sieciami neuronowymi napotyka na kaskadę problemów. Najpierw należałoby zacząć od przypomnienia sobie, czym są grafy i z czego się składają. Grafowe sieci neuronowe korzystają z całego aparatu matematycznego i mechaniki sieci klasycznych - też należałoby je znać. Na grafach wykonuje się typowo zadania takie jak: klasyfikacja lub regresja dla wierzchołków, klasyfikacja lub regresja dla połączeń, klasyfikacja lub regresja dla całych grafów. Jeśli ktos nie zna zagadnień klasyfikacji lub regresji - trzeba doczytać czym są, jakich metryk się używa.Materiały o metrykach z kolei odwołują się do pojęć statystycznych, próbkowania, estymacji, walidacji krzyżowej itd.W efekcie, osoba, która planowała nauczyć się czegoś o sieciach neuronowych , musi najpierw zapoznać się z całym bagażem pokrewnych zagadnień.

Kolejną kwestią jest kompletność wiedzy. Wyrywkowe zapoznanie się ze specyfiką poszczególnych modeli, bez zrozumienia ich teoretycznych podstaw, może prowadzić do sytuacji, w której osoba, która zna np. sieci neuronowe lub drzewa decyzyjne, ale potrafi je stosować jedynie w prostych, standardowych przypadkach, bez zapewnienia rzetelnej statystycznej ewaluacji błędów, mocy modelu, etc.

W tym opracowaniu postanowiliśmy zacząć od podstaw, budując na tym fundamencie kolejne piętra budynku. I tak, Czytelnik lub Czytelniczka będzie się zapoznawać kolejno:

1. Z podstawowymi pojęciami i terminami, charakterystycznymi dla uczenia maszynowego.
2. Z podstawami teorii COLT, czyli teorii uczenia obliczeniowego.
3. Z taksonomią zadań realizowanych przez różne modele.
4. Z podstawowymi zagadnieniami z zakresu błędów, ograniczeń modeli oraz projektowaniem eksperymentów dla nich.
5. Z przekrojem przez najważniejsze rodziny modeli uczenia maszynowego.
6. (i dopiero potem) Ze szczegółami dotyczącymi po kolei każdej z wielkich rodzin modeli uczenia maszynowego, w tym:
   1. Klasyczne modele drzew decyzyjnych.
   2. Modele minimalnoodległościowe (KNN, etc.).
   3. Modele typu "ensemble" czyli zespoły połączonych estymatorów.
   4. Podstawy sieci neuronowych.
   5. Podstawowe modele dla szeregów czasowych.

Mamy nadzieję, że taka prezentacja zagadnień, nawet w formie hasłowej i skróconej, ułatwi nawigowanie w skomplikowanym świecie analizy danych :)