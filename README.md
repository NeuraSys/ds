# Data Science - przegląd zagadnień

To repozytorium zawiera kod źródłowy książki "Data Science - Przegląd Zagadnień". Na podstawie głównej gałęzi/*brancha* `main` generowana jest interaktywna wersja książki.

# Jak pracować z kodem tej książki

**Musimy mieć zainstalowaną `anacondę` lub `minicondę`**.
Polecanym środowiskiem do pracy jest Linux.


1. Sklonuj repozytorium / utwórz *fork*.
2. Utwórz nową głąź / *branch*.
3. Utwórz nowe środowisko condy z pliku `environment.yml`:
```bash
conda env create -f environment.yml
```
4. Aktywuj środowisko:
```bash
conda activate dsbook
```

5. Zainstaluj zależności za pomocą `poetry`
```bash
poetry install
```

6. Zbuduj książkę:
```bash
jupyter-book build ./ds_ue_book
```