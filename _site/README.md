# Elense Studio Portfolio

Statyczna strona portfolio hostowana na GitHub Pages, zbudowana przy użyciu silnika Jekyll z motywem **Slate** i niestandardowym, nowoczesnym designem.

## Funkcje
- **Nowoczesny UI**: Ciemny motyw (Slate) z autorskimi komponentami CSS.
- **Responsywność**: Strona w pełni dostosowana do urządzeń mobilnych.
- **Dynamiczne Kolekcje**: Łatwe zarządzanie projektami w trzech kategoriach.

## Struktura Strony
- **Software**: `_software/`
- **Engineering**: `_engineering/`
- **Leathercraft**: `_leathercraft/`

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

## Deployment na GitHub Pages

Projekt jest skonfigurowany do automatycznego wdrażania za pomocą GitHub Actions.

1. **Push do repozytorium**: Po przesłaniu zmian na gałąź `main` lub `master`, GitHub Actions automatycznie zbuduje i wdroży stronę.
2. **Konfiguracja Pages**:
   - Wejdź w ustawienia swojego repozytorium na GitHub (`Settings`).
   - Wybierz sekcję `Pages` w menu po lewej stronie.
   - W sekcji `Build and deployment > Source` upewnij się, że wybrano **GitHub Actions**.
3. **URL strony**: Adres strony zostanie wyświetlony w zakładce `Pages` po zakończeniu pierwszego wdrożenia. Pamiętaj, aby zaktualizować `url` w pliku `_config.yml` na właściwy adres Twojej strony (obecnie ustawiono `https://elensestudio.com`).
4. **Własna domena (`elensestudio.com`)**:
   - W ustawieniach repozytorium **Settings > Pages** upewnij się, że w sekcji "Custom domain" widnieje `elensestudio.com`.
   - Skonfiguruj u swojego dostawcy domeny rekordy DNS (A records wskazujące na IP GitHub Pages lub CNAME na `<user>.github.io`).

### Metoda klasyczna (Ruby)

Jeśli wolisz uruchomić projekt bezpośrednio przez Ruby:

1. Zainstaluj Ruby (zalecane 3.0+).
2. Zainstaluj Bundler: `gem install bundler`
3. Zainstaluj zależności: `bundle install`
4. Uruchom serwer: `bundle exec jekyll serve`
