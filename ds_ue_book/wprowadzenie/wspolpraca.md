# Współpraca

Ten projekt jest tworzony w formacie *open-source* i udostępniany za darmo dla każdej osoby zainteresowane tematyką DS. Będziemy wdzięczni za wszelkie uwagi, poprawki, sugestie, które pomogą nam ulepszyć skrypt.

Na tym jednak nie koniec.

Jeśli chcesz wziąć udział w tworzeniu tego skryptu, zapraszamy do współpracy. Możesz pomóc w różny sposób:
1. **Poprawiając błędy** - jeśli zauważysz jakieś nieścisłości, błędy merytoryczne, literówki, itp., daj nam znać. Możesz to zrobić poprzez zgłoszenie błędu (ang.*issue*) na GitHubie, albo poprzez zgłoszenie *pull request* z poprawkami.
2. **Dodając nowe treści** - jeśli masz pomysł na dodanie nowego rozdziału, sekcji, przykładu, itp., również daj nam znać. Możesz to zrobić poprzez zgłoszenie *issue* na GitHubie, albo poprzez zgłoszenie *pull request* z nowymi treściami.
3. **Poprawiając styl** - jeśli masz doświadczenie w redagowaniu tekstów, możesz pomóc nam poprawić styl, zwiększyć czytelność, itp. Wszelkie sugestie mile widziane.

## Dodawanie treści do projektu

Niniejsze opracowanie jest tworzone z pomocą biblioteki [Jupyter Book](https://jupyterbook.org/) i umieszczony na GithubPages. Dodawanie nowych treści / nanoszenie poprawek itd. jest możliwe poprzez zgłoszenie *pull request* na GitHubie.

Prosilibyśmy o trzymanie się kilku zasad, które ułatwią nam wspólną pracę:
1. **Dodanie zależności za pomocą biblioteki Poetry** - każdy, kto pracował z Pythonem wie, jak ciężko jest zarządzać w nim zależnościami bibliotek. W tym projekcie zdecydowaliśmy się na **Poetry**, które stara się w sposób spójny utrzymywać wersje i powiązane biblioteki. Jeśli dodajesz nowy notebook lub fragmenty wykonywalnego kodu - upewnij się, że dodajesz odpowiednie zależności do pliku `pyproject.toml`. Więcej o Poetry i jego zastosowaniach: [https://python-poetry.org/](https://python-poetry.org/).
2. **Mieszanie treści tekstowych i notebooków** - to opracowanie zapewne mogłoby być książką wydaną tradycyjnie, jednak zdecydowaliśmy się na format JuypterBook, aby dołączyć kod, treści interaktywne, obrazy itd. Jeśli to możliwe - dodając nowe fragmenty umieść w nich zarówno tekst, jak i kod, aby zilustrować opisywane koncepcje.
3. **Równania, dowody, definicje, obrazki** - chcemy, żeby to opracowanie pozwalało na dynamiczną nawigację między elementami. Kluczowe pojęcia powinny być dodawane do słownika (ang. *glossay* w JupyterBook), równania/dowody/obrazy - powinny być dodawane w formie umożliwiającej ich indeksowanie i budowanie odsyłaczy. Więcej o tym w [dokumentacji JupyterBook](https://jupyterbook.org/).
4. **Cytowania** - wszystkie treści będące odwołaniem do literatury naukowej lub istniejących opracowań powinny być cytowane, a odpowiednie materiały źródłowe - dodane do pliku `references.bib`. Więcej o tym w [dokumentacji JupyterBook](https://jupyterbook.org/).

Będziemy bardzo wdzięczni za wszelką pomoc przy realizacji projektu!

## Jak wprowadzać zmiany do projektu?

Projekt jest otwarty na współpracę i każde wsparcie jest mile widziane. W celu zapewnienia płynnej i zorganizowanej pracy nad podręcznikiem, prosimy o stosowanie się do poniższych zasad:

### 1. Forkowanie repozytorium (*fork*)

Aby rozpocząć współpracę, należy najpierw wykonać *fork* repozytorium na GitHubie. Oznacza to utworzenie własnej kopii projektu na Twoim koncie GitHub, gdzie możesz wprowadzać zmiany bez wpływu na główną wersję. Po zalogowaniu się na swoje konto GitHub, przejdź do strony repozytorium i kliknij przycisk „Fork” w prawym górnym rogu.

**Tutorial:**
- [Fork a Repo - GitHub Docs](https://docs.github.com/en/get-started/quickstart/fork-a-repo)

### 2. Tworzenie nowej gałęzi (*branch*)

Przed wprowadzeniem jakichkolwiek zmian w swoim *forku*, zalecamy utworzenie nowej gałęzi (*branch*), która będzie zawierała Twoje zmiany. Dzięki temu Twoje modyfikacje będą odseparowane od głównej gałęzi (*main*) i łatwiej będzie je przetestować i przejrzeć. Możesz nazwać swoją gałąź odpowiednio do rodzaju zmian, np. `poprawki-stylistyczne` lub `nowa-sekcja-uczenie-maszynowe`.

**Tutorial:**
- [Creating and Deleting Branches - GitHub Docs](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-and-deleting-branches-within-your-repository)

### 3. Wprowadzanie zmian i tworzenie commitów (*commit*)

Wprowadź zmiany, które uważasz za konieczne, na nowo utworzonej gałęzi. Po zakończeniu pracy, zapisz zmiany w repozytorium lokalnym za pomocą commitów. Każdy *commit* powinien być opisany w sposób zwięzły, ale informatywny, np. „Dodano nową sekcję o regresji liniowej” lub „Poprawiono literówki w rozdziale 3”.

**Tutorial:**
- [About commits - GitHub Docs](https://docs.github.com/en/github/committing-changes-to-your-project/about-commits)

### 4. Zgłoszenie Pull Request (*pull request*)

Gdy Twoje zmiany są gotowe do włączenia do głównego repozytorium, zgłoś *pull request* z gałęzi, na której pracowałeś/aś. *Pull request* to prośba o włączenie Twoich zmian do głównej gałęzi (*main*) projektu. Przed wysłaniem *pull requestu* upewnij się, że Twój kod jest zgodny ze standardami projektu i został przetestowany. W opisie *pull requestu* jasno określ, jakie zmiany zostały wprowadzone i dlaczego.

**Tutorial:**
- [About Pull Requests - GitHub Docs](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests)

### 5. Wyznaczenie recenzenta (*reviewer*)

Po zgłoszeniu *pull requestu*, prosimy o wyznaczenie recenzenta (*reviewer*), który sprawdzi Twoje zmiany. Recenzentem może być jeden z członków zespołu projektowego lub inna osoba, która zna się na danym temacie. Recenzent dokona przeglądu zmian, zgłosi ewentualne uwagi i zatwierdzi (lub odrzuci) zmiany. Dopiero po akceptacji przez recenzenta Twoje zmiany zostaną połączone z główną gałęzią.

**Tutorial:**
- [Requesting a Pull Request Review - GitHub Docs](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/requesting-a-pull-request-review)

### 6. Dokumentacja i zasoby

Zachęcamy do zapoznania się z dokumentacją [Jupyter Book](https://jupyterbook.org/) oraz z narzędziami używanymi w projekcie, takimi jak [Poetry](https://python-poetry.org/). Dzięki temu Twoje zmiany będą w pełni zgodne ze standardami projektu i łatwiejsze do zintegrowania.

Będziemy bardzo wdzięczni za wszelką pomoc i wkład w rozwój tego projektu! Razem możemy stworzyć wartościowy materiał edukacyjny dostępny dla wszystkich.