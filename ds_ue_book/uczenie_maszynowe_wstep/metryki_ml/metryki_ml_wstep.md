# Wprowadzenie do zadań i metryk w uczeniu maszynowym

Autor sekcji: {ref}`authors:filip-wojcik`.

w poprzednich rozdziałach omówiliśmy sobie podstawowe zagadnienia związane z teorią uczenia się - błędami generalizacji i dopasowania. Brakuje nam w tej układance jednego elementu - odpowiedzi na pytanie: **jak oceniać jakość modeli uczenia maszynowego?**. Względem jakich kryteriów?
Metryki oceny są uzależnione od **zadania, jakie dany model ma realizować**.

W niniejszym rozdziale przedstawione zostaną podstawowe pojęcia związane z funkcjami kosztu i straty, omówiony zostanie podział zadań w uczeniu maszynowym oraz zaprezentowane zostaną najważniejsze metryki oceny modeli.
Omówimy sobie:
1. Funkcje kosztu i straty - Funkcje kosztu i straty stanowią fundament w ocenie jakości modeli uczenia maszynowego. Są to funkcje matematyczne, które kwantyfikują różnicę pomiędzy przewidywaniami modelu a rzeczywistymi wartościami. Celem nauki modelu jest minimalizacja tej różnicy, co prowadzi do poprawy jego dokładności.
2. Podział zadań w uczeniu maszynowym
    Zadania w uczeniu maszynowym można podzielić na kilka głównych kategorii, z których najważniejsze to:
   - **Klasyfikacja**: Przypisywanie elementów do określonych klas.
   - **Klasyfikacja probabilistyczna**: Szczególny przypadek klasyfikacji, różniący się nieco metrykami oceny.
   - **Regresja**: Przewidywanie wartości ciągłych.
   - **Grupowanie (klasteryzacja)**: Grupowanie podobnych elementów w zbiory.
   - **Ranking**: Ustalanie kolejności elementów, szczególnie w systemach rekomendacyjnych.
3. Klasyfikację i jej metryki.
4. Regresję i jej metryki.
5. Grupowanie i jego metryki.
6. Ranking i jego metryki.

```{admonition} Inne zadania, inne metryki
:class: tip
Warto zauważyć, że niektóre specyficzne dziedziny uczenia maszynowego, takie jak analiza grafów czy analiza obrazów, mają swoje unikalne metryki oceny. Ten rozdział jednak skupia się na klasycznych, ogólnych metrykach stosowanych w różnych zadaniach uczenia maszynowego, zapewniając solidne podstawy do 
dalszego zgłębiania bardziej zaawansowanych zagadnień.
```

## Funkcje kosztu i straty

W uczeniu maszynowym funkcje kosztu i straty odgrywają kluczową rolę w ocenie i optymalizacji modeli. Stanowią one formalne narzędzie do kwantyfikacji różnic między przewidywaniami modelu a rzeczywistymi wartościami, co pozwala na iteracyjne doskonalenie modeli poprzez minimalizację tych różnic.

```{admonition} Brak jednej definicji
:class: tip

Nie ma konsensusu odnośnie definicji tych terminów wśród autorów i praktyków uczenia maszynowego. W praktyce często używa się ich zamiennie, choć niektórzy wyróżniają między nimi różnice. W niniejszym rozdziale przedstawimy obie definicje oraz ich wspólne rozumienie, jako alternatywny punkt widzenia.
```
```{glossary}
Funkcja straty
    (ang. *loss function*) - oznaczana abstrakcyjnie jako $\mathcal{L}(\hat{y}, y)$ mierzy różnice między predykcja modelu $\hat{y} = h(\mathbf{x}_i; \theta)$ (gdzie $h$ jest modelem/hipotezą uczenia maszynowego przewidującą wynik dla przykładu uczącego $\mathbf{x}$) a rzeczywistą wartością oczekiwaną dla danego przykładu uczącego.

Funkcja kosztu
    (ang. *cost function*) - oznaczana abstrakcyjnie jako $\mathcal{J}(\theta)$ mierzy różnice między predykcjami modelu a rzeczywistymi wartościami dla **całego zbioru danych uczących**. Jest to agregacja funkcji straty dla wszystkich przykładów uczących. Agregację można przeprowadzić za pomocą średniej, mediany lub podobnych miar. Funkcja kosztu nierzadko zawiera również komponent regularyzujący złożoność modelu (np. złożoność wag) uzyskując postać:
    $J(\theta) = \text{AGG}\left\{ \mathcal{L}(\hat{y}_i, y_i), \forall i \in \mathcal{D} \right\} + \Omega(\theta)$
```

Definicje zamieszczone poniżej odnajdziemy w zbliżonej postaci m. in. w {cite:ps}`Ma2007CS229LN`, {cite:ps}`hastie2009elements`, {cite:ps}`goodfellow2016deep`. Co ciekawe, prof. Andrew Ng używa rozróżnia ang. *cost* i *loss function* w swoich kursach prowadzonych na platformie Coursera, **ale** w publikowanych materiałach Stanfordu do kursu CS229 posługuje się **czasami określeniem **cost** a czasem **cost/loss** function* dodając słowne określenie, czy mówi o funkcji dotyczącej wszystkich przykładów, czy całego zbioru danych.

Przykładowo:

1. W rozdziale 8 {cite:ps}`Ma2007CS229LN`, "Generalization" czytamy:
> (...) we typically learn a model $h(\theta)$ by minimizing a loss/cost function $J(\theta)$, which encourages $h(\theta)$ to fit the data. E.g., E.g., when the loss function is the least square loss (aka mean squared error), we have $J(\theta) = \frac{1}{n} \sum_{i=1}^{n} (y^{(i)} - h_\theta(x^{(i)}))^2$. This loss function for training purposes is oftentimes referred to as the training loss/error/cost.
2. W rozdziale 7.1. {cite:ps}`Ma2007CS229LN` "Deep learning" czytamy:
>  For simplicity, we start with the case where the output is a real number, that is, $y^{(i)} \in \mathbb{R}$ and thus the model $h(\theta)$ also outputs a real number (...). We define the least square cost function for the i-th example $(x^{(i)}, y^{(i)})$ as: $ J^{(i)}(\theta) = \frac{1}{2} (h_\theta(x^{(i)}) - y^{(i)})^2$, and define the mean-square cost function for the dataset as: $J(\theta) = \frac{1}{n} \sum_{i=1}^{n} J^{(i)}(\theta)$.


Z kolei Ian Goodfellow, uznany praktyk i naukowiec (do niedawna zaangażowany w DeepMind) w swojej książce "Deep Learning Book" {cite:ps}`goodfellow2016deep` w ogóle nie rozróżnia pojęć *loss / cost function* wprost, stosując je zamiennie i dodając, w definicji, czy opisuje funkcję dla pojedynczego przykładu czy dla całego zbioru danych.

```{admonition} Funkcje kosztu i straty w praktyce
:class: important
Nie chodzi nam tutaj o teoretyczne spory i rozważania. Ważna lekcja do zapamiętania ogranicza się do tych kilku punktów:
1. Możemy odróżniać funkcje opisujące błędy dla **pojedynczego przykładu**;
2. Wiele takich funkcji można **zagregować** (np. za pomocą średniej) i uzyskać funkcję kosztu dla całego zbioru danych, dodając np. karę za złożoność całego modelu;
3. Jeśli ktoś próbuje nam zarzucić, że źle używamy tych pojęć, to warto zwrócić uwagę, że nie ma zgody co do ich rozdziału wśród ekspertów.
```