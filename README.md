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

## Uruchamianie lokalne

Najprostszą metodą uruchomienia strony lokalnie (bez konieczności instalowania Ruby i zależności) jest użycie **Docker**:

1. Upewnij się, że masz zainstalowany Docker.
2. Uruchom komendę:
   ```bash
   docker-compose up
   ```
3. Strona będzie dostępna pod adresem: `http://localhost:4000`

## Deployment na AWS S3

Projekt jest skonfigurowany do automatycznego wdrażania na AWS S3 za pomocą GitHub Actions.

1. **Konfiguracja AWS**:
   - Utwórz bucket w S3 skonfigurowany pod hosting statycznej strony.
   - Upewnij się, że masz użytkownika IAM z uprawnieniami do zapisu w tym buckecie.

2. **Sekrety GitHub**:
   W ustawieniach repozytorium (**Settings > Secrets and variables > Actions**) dodaj następujące sekrety:
   - `AWS_ACCESS_KEY_ID`: Twój klucz dostępu AWS.
   - `AWS_SECRET_ACCESS_KEY`: Twój tajny klucz dostępu AWS.
   - `AWS_REGION`: Region Twojego bucketa (np. `eu-central-1`).
   - `AWS_S3_BUCKET`: Nazwa Twojego bucketa S3.

3. **Push do repozytorium**:
   Po przesłaniu zmian na gałąź `main`, GitHub Actions automatycznie zbuduje stronę i zsynchronizuje ją z bucketem S3.

4. **Własna domena (`elensestudio.com`)**:
   - Skonfiguruj CloudFront lub Route 53, aby wskazywały na Twój bucket S3.
   - Pamiętaj, aby zaktualizować `url` w pliku `_config.yml` na właściwy adres Twojej strony.

### Metoda klasyczna (Ruby)

Jeśli wolisz uruchomić projekt bezpośrednio przez Ruby:

1. Zainstaluj Ruby (zalecane 3.0+).
2. Zainstaluj Bundler: `gem install bundler`
3. Zainstaluj zależności: `bundle install`
4. Uruchom serwer: `bundle exec jekyll serve`
