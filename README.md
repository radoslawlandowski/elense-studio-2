# Elense Studio Portfolio

Statyczna strona portfolio hostowana na GitHub Pages, zbudowana przy użyciu silnika Jekyll.

## Struktura Strony

Strona posiada 3 główne sekcje (kafelki na stronie głównej):
- **Elense Software**
- **Elense Engineering**
- **Elense Leathercraft**

## Jak dodawać nowe elementy do portfolio?

Silnik Jekyll używa tzw. "Collections". Aby dodać nową pracę, stwórz nowy plik Markdown (`.md`) w odpowiednim folderze:

1. **Software**: Dodaj plik do folderu `_software/`
2. **Engineering**: Dodaj plik do folderu `_engineering/`
3. **Leathercraft**: Dodaj plik do folderu `_leathercraft/`

### Format pliku (np. `_software/moj-projekt.md`):

```markdown
---
title: Nazwa Mojego Projektu
layout: post
---
Tutaj wpisz opis projektu. Możesz używać Markdown, dodawać linki i obrazki.
```

## Hostowanie na GitHub Pages

1. Wrzuć (push) ten kod do swojego repozytorium na GitHubie.
2. Wejdź w **Settings** -> **Pages**.
3. Ustaw **Build and deployment** -> **Source** na "GitHub Actions".
4. GitHub automatycznie wykryje Jekyll i zbuduje stronę.

Alternatywnie, jeśli używasz klasycznego podejścia:
1. Ustaw **Branch** na `main` (lub `master`).
2. GitHub zbuduje stronę automatycznie.

## Uruchamianie lokalne

Najprostszą metodą uruchomienia strony lokalnie (bez konieczności instalowania Ruby i zależności) jest użycie **Docker**:

1. Upewnij się, że masz zainstalowany Docker.
2. Uruchom komendę:
   ```bash
   docker-compose up
   ```
3. Strona będzie dostępna pod adresem: `http://localhost:4000`

### Metoda klasyczna (Ruby)

Jeśli wolisz uruchomić projekt bezpośrednio przez Ruby:

1. Zainstaluj Ruby (zalecane 3.0+).
2. Zainstaluj Bundler: `gem install bundler`
3. Zainstaluj zależności: `bundle install`
4. Uruchom serwer: `bundle exec jekyll serve`
