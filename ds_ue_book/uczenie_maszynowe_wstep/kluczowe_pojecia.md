# Kluczowe pojęcia [^autor]
[^autor]: Autor sekcji: {ref}`authors:filip-wojcik`.


Ten podrozdział poświęcono kluczowym pojęciom z zakresu uczenia maszynowego. Obejmuje on definicje i wyjaśnienia terminów, które są niezbędne do zrozumienia dalszych zagadnień.


## Uczenie się

Dla zrozumienia koncepcji uczenia maszynowego, warto zacząć od podstaw - od zdefiniowania samego zjawiska nauki. Aspekt ten jest i był przedmiotem badań w ramach różnych dziedzin - od psychologii po informatykę.
Poniższe zestawienie przedstawia kilka wybranych definicji z rozmaitych źródeł.

````{tab-set}
```{tab-item} Herbert Simon
Uczenie się oznacza takie zmiany adaptacyjne w
systemie, iż jest on w stanie lepiej wykonać w
przyszłości takie same zadania lub zadania należące
do tej samej kategorii.
{cite:ps}`simon1983should`
```

```{tab-item} Paweł Cichosz
Uczeniem się systemu jest każda autonomiczna zmiana w systemie zachodząca na podstawie doświadczeń, która prowadzi do poprawy jakości
jego działania.
{cite:ps}`cichosz2007systemy`
```

```{tab-item} Tom Mitchell
Uważa się, iż program uczy się na bazie
doświadczeń E w ramach klasy zadań T i względem
miary dopasowania P, jeśli jego trafność w
zadaniach T, mierzona przez P, wzrasta wraz z
nabywanym doświadczeniem E.
{cite:ps}`learning1997tom`
```
````

W powyższych definicjach na pierwszy plan wysuwają się kluczowe pojęcia, takie jak
dostosowywanie działania, gromadzenie doświadczenia, czy wreszcie poprawa jakości
działania. Mając na uwadze formę przytoczonych definicji, dopuszczalne jest zdefiniowanie, na nasze potrzeby, uczenia w sposób następujący:

```{glossary}
Uczenie się
    jest to proces będący ciągiem (sekwencją) zachodzących zmian, którego głównymi składowymi są:
    1. możliwość gromadzenia doświadczenia w miarę wykonywania zadań;
    2. posiadanie przez system wewnętrznego stanu wiedzy i doświadczenia, aktualizowanego w miarę powtarzania zadanych czynności;
    3. funkcja lub procedura oceniająca jakość wykonywanych zdań;
    4. wewnętrzny mechanizm reagowania na pozytywny/negatywny sygnał zwrotny, opisujący
    jakość wykonanego zadania.
    {cite:ps}`wojcik2021`
```

(chapter:indukcja_dedukcja)=
## Indukcja i dedukcja

Uczenie indukcyjne i dedukcyjne to dwa najważniejsze paradygmaty prowadzenia rozumowań.

```{sidebar} Dedukcja Sherlocka Holmesa
Kto czytał lub zna historie o Sherlocku Holmesie, ten na pewno będzie kojarzyć rozumowanie dedukcyjne właśnie ze słynnym detektywem.
```

```{glossary}
Uczenie dedukcyjne
    Pojęcie to odnosi się do klasy systemów uczących się na bazie zestawu założeń i koncepcji, co do których zachodzi założenie (możliwe do dowiedzenia), że są poprawne.
    Tego typu systemy stosowane są zwykle do przyspieszania i wspomagania działania innych narzędzi, poprzez uproszczenie procesu wnioskowania.
    [tł. wł.] {cite:ps}`sammut2017encyclopedia`

Uczenie indukcyjne
    Rozumowanie indukcyjne jest odwróceniem dedukcji - zachodzi, gdy obserwowane dane uznamy za konkluzje, będące następstwami nieznanych faktów. Algorytm uczy się na ich podstawie, próbując odnaleźć lub skonstruować mechanizmy wyjaśniające zastany stan rzeczy {cite:ps}`wojcik2021`.
    Innymi słowy - model stara się odnaleźć uogólnione reguły, na podstawie zaobserwowanych, przykładowych danych [tł. wł.] {cite:ps}`sammut2017encyclopedia`
```

Podobieństwa i różnice pomiędzy tymi podejściami możemy podsumować w tabeli poniżej:

| | Uczenie dedukcyjne | Uczenie indukcyjne |
|---|---|---|
| Cel | Wykorzystywanie teorii i wiedzy początkowej do formułowania konkluzji. |Tłumaczenie zjawisk poprzez generalizację przykładów |
| Uzyskanie predykcji| Wnioskowanie od przesłanek i założeń do konkluzji, przy założeniu, że przesłanki i reguły wnioskowania są prawdziwe. | <ul><li>Poszukiwanie ogólnych reguł na podstawie przykładów </li> <li> Analiza statystyczna i ilościowa zjawisk.</li></ul> |
| Słabości | Wymóg zdefiniowania przesłanek a priori oraz posiadania wyczerpującego opisu mechanizmów | <ul> <li>Obarczone błędami wynikającymi z przykładów.</li><li>Wymaga (relatywnie) dużych ilości danych.</li></ul> |
| Typowe zastosowania | Objaśnianie niewielkich zbiorów danych, za pomocą ugruntowanej teorii  | Objaśnianie zbiorów danych, gdy nie ma jasno sformułowanej teorii i opisanych mechanizmów wnioskowania. |


Jak łatwo się domyślić - w otaczającym nas świecie rzadko kiedy mamy podane na tacy teorie i wyjaśnienia zjawisk, których doświadczamy.Z tego względu, uczenie indukcyjne jest częściej stosowane w praktyce, ze względu na możliwość wykorzystania danych do wygenerowania modelu.

Tu kryje się jednak pułapka: wnioskowanie indukcyjne jest tylko tak dobre, jak dane, na których się opiera. W związku z tym, kluczowe jest, aby dane były reprezentatywne i niezafałszowane.

`````{admonition} GIGO
:class: tip
Warto zapamiętać zasadę, którą można streścić w skrócie jako GIGO (Garbage In, Garbage Out) - jeśli dane wejściowe są złe, to wyniki będą złe.
`````

Porównywanie indukcji i dedukcji czasem ociera się o dyskusję filozoficzną. Kto nam bowiem zagwarantuje, że prawa fizyki albo matematyka są nienaruszalnymi aksjomatami: w końcu też je zaobserwowano, albo wynaleziono eksperymentalnie. Warto jednak pamiętać, że w praktyce, zazwyczaj mamy do czynienia z pewnymi ustalonymi prawami, które przyjmujemy jako punkt wyjścia.

````{admonition} Ćwiczenie - dedukcja vs indukcja
:class: note
Zastanów się, jakie z poniższych zdań są przykładami dedukcji, a które indukcji:

```{dropdown} Widzę gotującą się wodę w garnku. Mogę opisać i uzasadnić proces wrzenia wody.
Dedukcja. Przy założeniu, że przyjmujemy prawa fizyki, jako aksjomaty / niezmienniki, możemy za ich pomocą wyznaczyć parametry i etapy procesu wrzenia wody.
```
```{dropdown} Wszystkie ptaki, które widziałem w moim mieście mają skrzydła. Wnioskuję, że wszystkie ptaki mają skrzydła.
Indukcja. Na podstawie obserwacji, wnioskujemy, że wszystkie ptaki mają skrzydła.
```
```{dropdown} Ludzie, którzy jedzą dużo owoców, są zdrowsi. Wnioskuję, że jedzenie owoców jest zdrowe.
Indukcja. Na podstawie obserwacji, wnioskujemy, że jedzenie owoców jest zdrowe.
```

```{dropdown} Klient otrzymał kredyt zgodnie z procedurą. Należy sprawdzić, czy spełnione zostały wszystkie warunki.
Dedukcja. Na podstawie procedury, możemy sprawdzić, czy klient spełnia warunki. Badamy je krok-po-kroku.
```

```{dropdown} Ludzie chorują z powodu nowego wirusa. Należy ustalić u kogo występują powikłania.
Indukcja. Na podstawie obserwacji, sprawdzamy jakie cechy występują u osób z powikłaniami.
```
````

## Dane wykorzystywane w uczeniu

Uczenie maszynowe nie istnieje bez zbiorów danych. Formalnie, możemy sobie zdefiniować zbiór danych i jego składowe w następujący sposób:

````{glossary}
Dziedzina
  dziedziną nazywamy oznaczany przez $\mathcal{X}$ zbiór obiektów, których dotyczyć ma wiedza nabywana przez model. Mogą to być przedmioty, osoby, wydarzenia, sytuacje, etc. {cite:ps}`cichosz2007systemy`, {cite:ps}`learning1997tom`

Przykłady
  każdy obiekt, element dziedziny $x \in \mathcal{X}$ nazywamy przykładem. W praktyce, obiekty te są opisywane za pomocą swojego zbioru cech, najczęściej wyrażanych w postaci macierzy lub wektora. {cite:ps}`cichosz2007systemy`, {cite:ps}`learning1997tom`, {cite:ps}`wojcik2021`

Próbka ucząca
    jest zbiorem par $(\mathbf{x}, y)$, gdzie $\mathbf{x} \in \mathcal{X}$ to wektor cech przykładu, a $y$ to etykieta (numeryczna lub dyskretna). W przypadku uczenia nadzorowanego, etykieta $y$ jest zazwyczaj wartością, którą model ma przewidzieć. W przypadku uczenia nienadzorowanego, próbka ucząca składa się z samych wektorów cech $\mathbf{x}$.
    Formalnie, w postaci zbioru, możemy ją zapisać jak w równaniu {eq}`probka_uczaca`.
    ```{math}
    :label: probka_uczaca
    \mathcal{D} = \left\{ \left(\mathbf{x}_1, y_1\right), \left(\mathbf{x}_2, y_2\right), \dots, \left(\mathbf{x}_n, y_n\right) \mid \forall \mathbf{x} \in \mathcal{X}, y \in \mathcal{Y}  \right\}
    ```
    W postaci macierzowej ma postać, jak w równaniu {eq}`probka_uczaca_macierz`.
    ```{math}
    :label: probka_uczaca_macierz
    D = (\mathbf{X}, \mathbf{y}), \mathbf{X} \in \mathbb{R}^{n \times m}, \mathbf{y} \in \mathbb{R}^{n}
    ```
    gdzie, $n$ jest ilością próbek, $m$ jest ilością cech, $\mathcal{X}$ to przestrzeń cech, a $\mathcal{Y}$ to przestrzeń etykiet.
    {cite:ps}`wojcik2021`
````

Wszystko to brzmi w teorii dużo bardziej skomplikowanie niż jest w rzeczywistości. W przypadku danych tabelarycznych, próbka ucząca się strukturą danych przypominającą tabelę w bazie, albo arkusz Excela, w którym:
1. Każdy wiersz jest obiektem (np. osobą / klientem).
2. Każda kolumna reprezentuje cechę obiektu / atrybut (np. wiek, płeć, dochód).
3. Jedna z kolumn jest etykietą, którą model ma przewidzieć (np. czy klient kupi produkt).

Spójrzmy na poniższy przykład: mamy tabelę {ref}`tabelę <przyklad_filmy>` z filmami, opisanymi za pomocą pewnych cech. Ostatnia kolumna - "ocena Filmweb.pl" - podaje średnią ocen z portalu.

```{list-table} Filmy
:header-rows: 1
:name: przyklad_filmy

* - Tytuł
  - Gatunek
  - Rok produkcji
  - Ocena Filmweb.pl
* - Matrix
  - SF / cyberpunk
  - 1999
  - 7.6
* - Pulp Fiction
  - Kryminał
  - 1994
  - 8.3
* - Titanic
  - Dramat
  - 1997
  - 7.3
* - Ghost in the shell
  - SF / cyberpunk
  - 1995
  - 7.9
```
Przekładając to na formalną notację zdefiniowaną równaniem {eq}`probka_uczaca_macierz` i zakładając przez chwilę, że zamienilibyśmy etykiety tekstowe np. `SF/cyberpunk` na liczby naturalne, otrzymamy:

```{math}
D = (\mathbf{X}, \mathbf{y}), \mathbf{X} \in \mathbb{N}^{4 \times 3}, \mathbf{y} \in \mathbb{N}^{4}
```
mając cztery wiersze z filmami o trzech atrybutach (tytuł, gatunek, rok produkcji), oraz wektor 4 etykiet (ocen).


## Algorytmy i modele uczenia maszynowego

Bardzo ważne jest wprowadzenie rozróżnienia pomiędzy algorytmami i modelami uczenia maszynowego. O dziwo, jest to pytanie, które dość często pojawia się na rozmowach kwalifikacyjnych, ale zagadnienie jest warte zbadania również z innych powodów.

(terms:ml_algo_model)=
```{glossary}
Algorytm uczenia maszynowego
    pod nazwą algorytm uczenia maszynowego (lub skrótowo: algorytm bądź procedura) funkcjonować będzie określona procedura, będąca instrukcją
    wykonania kolejnych kroków, mających na celu nauczenie systemu komputerowego
    rozpoznawania wzorców, w ramach postawionego zadania klasyfikacji, regresji, grupowania
    czy odkrywania zależności. Procedura ta ma postać zapisu (symbolicznego, słownego,
    matematycznego lub hybrydowego, w postaci pseudokodu) kolejnych czynności. Algorytm jest
    zatem niezależny od kontekstu, w jakim się go wykonuje. {cite:ps}`wojcik2021`

Model uczenia maszynowego
    pod nazwą model uczenia maszynowego (lub skrótowo: model) funkcjonować będzie instancja (w rozumieniu informatyki: konkretny egzemplarz) algorytmu, zastosowany do zadanego problemu, w celu utworzenia uproszczonego opisu wycinka rzeczywistości. Proces ten nosi nazwę szkolenia, uczenia lub trenowania27 i odbywa się na podstawie dostępnych danych, mając najczęściej postać procesu indukcyjnego. Jest to zatem algorytm o ukształtowanym i ustalonym wewnętrznym stanie – konkretyzacja abstrakcyjnie i symbolicznie zdefiniowanej procedury. {cite:ps}`wojcik2021`
```

```{admonition} Model uczenia maszynowego - jeszcze krótsza definicja
:class: tip
W tym kontekście można podsumować model uczenia maszynowego jeszcze prościej: jest to uproszczony opis pewnego wycinka rzeczywistości, skonstruowany przez model, na bazie dostępnych danych.
```

Niejednokrotnie możemy się spotkać z formalną definicją modelu, jako funkcji, która przyjmuje na wejściu dane oraz parametry/wewnętrzny stan i zwraca predykcję. Możemy to zapisać w postaci równania {eq}`parametryczna-postac-modelu`:

```{math}
:label: parametryczna-postac-modelu

\hat{y} = f(\mathbf{X}, \theta)
```

Parametry modelu są przedmiotem szkolenia, zwanego także treningiem lub strojeniem/tuningiem.