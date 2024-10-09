# Notacja i oznaczenia

Autor sekcji: {ref}`authors:filip-wojcik`


W dyskusjach dotyczących *data science* i uczenia maszynowego, bardzo ważne jest ujednolicenie notacji i stosowanych oznaczeń. Nierzadko zdarza się, że różne źródła naukowe, czy też praktycy, stosują różne symbole dla tych samych pojęć. W celu uniknięcia nieporozumień, warto zdefiniować zestaw oznaczeń, które będą stosowane w dalszej części tego skryptu.

## Język polski vs język angielski

Dominacja języka angielskiego w (szeroko rozumianej) branży IT jest faktem, z którym trudno się spierać. Od lat toczą się debaty między zwolennikami tłumaczenia wszelkich terminów na język polski, nawet jeśli te nie przyjęły się jeszcze w codziennym użyciu, a entuzjastami pozostawiania oryginalnej nomenklatury. Nie inaczej jest w przypadku głównego tematu tego podręcznika.

Sama nazwa *data science* bywa tłumaczona na różne sposoby – najpopularniejszy to zapewne *danologia*, a bardziej opisowy wariant to *zaawansowana analiza danych*. Każdy z tych terminów ma swoje plusy i minusy, ale nie będziemy tu próbować rozstrzygać tej odwiecznej batalii.

Niniejszy podręcznik ma przede wszystkim służyć jako praktyczny przewodnik. Jego autorzy nie są wprawdzie ekspertami językowymi, ale za to mają doświadczenie w pracy w sektorze komercyjnym, często w międzynarodowych firmach. Nie popieramy bezmyślnego stosowania językowych kalek ani humorystycznie karykaturalnego “korpo-lengłydżu” („fokusujemy się na targecie, czekając na approvale tasków na tym ekałncie”), ale równie niekorzystne, naszym zdaniem, jest używanie polskich neologizmów, które mają zerową praktyczną użyteczność i rozpoznawalność.

Dlatego w tym podręczniku podajemy polskie terminy, o ile istnieją w powszechnie uznanej wersji, zawsze obok ich oryginalnych odpowiedników po angielsku. Jeśli polski odpowiednik nie istnieje, jest mało znany lub nie ma zgody co do jego stosowania – używamy jedynie oryginalnej nazwy, zapisanej kursywą.

Nasze założenie jest proste: Czytelnik lub Czytelniczka tego materiału najczęściej będą mieli do czynienia z terminologią anglojęzyczną – czy to przy przeglądaniu dokumentacji bibliotek, czy też współpracując z zagranicznymi partnerami. Osoba rozwiązująca problem w Pythonie z pomocą modułu `scikit-learn` raczej nie będzie używać terminu „przeszukiwanie siatki parametrów”, tylko *grid search*. Dlatego też taki zapis będziemy stosować: przeszukiwanie siatki parametrów (ang. *grid search*).

Zachęcamy więc do odkrywania zagadnień **zaawansowanej analizy danych**, czyli *data science* – w duchu praktycznym, ale bez nadmiernego zapętlenia się w językowe rozważania.


## Skalary i wektory

- Skalar oznaczamy małą literą zwykłą, np. $x$ lub wielką, niepogrubioną (zwł. w przypadku wymiarowości macierzy lub liczności elementów zbioru).
- Wektor oznaczamy małą literą zwykłą z pogrubieniem, np. $\mathbf{x}$.
- Macierze oznaczamy dużą literą z pogrubieniem, np. $\mathbf{X}$.
- Wymiarowość macierzy lub wektorów będzie oznaczana słowem dim np. $\text{dim}(\mathbf{X}): N \times K$ lub w notacji przynależności do domeny np. $\mathbf{X} \in \mathbb{R}^{N \times K}$.
- Krotki / n-tki (ang. *tuple*) oznaczamy symbolami zgodnymi z ich zawartością (np. macierze, wektory, skalary), w okrągłym nawiasie: $(x_1, x_2, \ldots, x_n)$.
- Zbiory oznaczamy wielkimi literami z frakturą/ręcznym pismem np. $\mathcal{X}$.
- Klasyczne zbiory / domeny takie jak liczny naturalne i rzeczywiste oznaczane są podwójnymi, wielkimi literami: $\mathbb{N}$, $\mathbb{R}$.

## Operacje na macierzach

Niejednokrotnie będzie stosowany zapis charakterystyczny dla bibliotek i narzędzie w Pythonie, związanych z indeksowaniem macierzy:

- $\mathbf{X}^T$ - transpozycja macierzy $\mathbf{X}$.
- $\mathbf{X}^{-1}$ - odwrotność macierzy $\mathbf{X}$.
- $a_i$ - $i$-ty element wektora $\mathbf{a}$.
- $\mathbf{X}_{i,j}$ - element macierzy $\mathbf{X}$ w $i$-tym wierszu i $j$-tej kolumnie.
- $\mathbf{X}_{i,:}$ - $i$-ty wiersz macierzy $\mathbf{X}$. Taki zapis bezpośrednio koresponduje z notacją w Pythonie, w bibliotece `NumPy`.
- $\mathbf{X}_{:,j}$ - $j$-ta kolumna macierzy $\mathbf{X}$. Taki zapis bezpośrednio koresponduje z notacją w Pythonie, w bibliotece `NumPy`.
- $\mathbf{X}_{i:j,k:l}$ - wycinek macierzy $\mathbf{X}$ od wiersza $i$ do $j$ i od kolumny $k$ do $l$.

## Funkcje

- Funkcje oznaczamy małą literą zwykłą, np. $f$.
- $f: \mathbb{A}^N \rightarrow \mathbb{B}^M$ - funkcja $f$ o dziedzinie $\mathbb{A}^N$ i przeciwdziedzinie $\mathbb{B}^M$.
- $f(x)$ - wartość funkcji $f$ w punkcie $x$.
- $f \circ g$ - złożenie funkcji $f$ i $g$.
- $f(\mathbb{x}, \theta)$ - funkcja $f$ wektora $\mathbb{x}$ i parametrów $\theta$.