# Mechaniczny Obywatel – aplikacja demo (projekt edukacyjny)

Prototyp cyfrowego portfela dokumentów: PIN i symulowane logowanie twarzą (Face ID), dokumenty, kody QR, usługi, wiadomości i sprawy.
**Wszystkie dane są fikcyjne. Aplikacja nie jest dokumentem urzędowym i nie łączy się z żadnymi rejestrami.**

## Zawartość
- `index.html` – cała aplikacja (HTML + CSS + JS, bez zależności)
- `manifest.webmanifest`, `sw.js`, ikony – dzięki nim działa jako instalowalna aplikacja (PWA) i offline

## Uruchomienie na komputerze
- Szybki podgląd: otwórz `index.html` w przeglądarce (bez trybu offline i instalacji).
- Pełna wersja: w tym folderze uruchom `python -m http.server 8000` i wejdź na `http://localhost:8000`.

## Instalacja na telefonie
1. Wgraj folder na dowolny hosting HTTPS, np. Netlify Drop (przeciągnij folder na app.netlify.com/drop), GitHub Pages lub Cloudflare Pages.
2. Otwórz adres na telefonie.
   - Android (Chrome): menu ⋮ → „Zainstaluj aplikację” (albo przycisk w Więcej).
   - iPhone (Safari): Udostępnij → „Do ekranu początkowego”.
3. Aplikacja działa na pełnym ekranie, ma własną ikonę i działa bez internetu.

## Plik .apk (Android)
Wejdź na pwabuilder.com, wklej adres opublikowanej aplikacji i wybierz „Package for stores → Android”. Dostaniesz gotowy plik .apk.

## Jak działa
- PIN domyślny: **1234** (można zmienić w Więcej). W pamięci telefonu zapisywany jest tylko skrót PIN-u (rozwiązanie demonstracyjne, nie kryptograficzne).
- Blokada po 5 błędnych próbach (30 s) i automatyczne wylogowanie po 5 minutach bezczynności.
- Dokumenty, sprawy, wiadomości i ustawienia zapisują się w pamięci urządzenia. „Zresetuj dane demo” w zakładce Więcej przywraca stan początkowy.
- Logowanie twarzą jest symulacją (nie używa kamery).
- Czcionka Manrope ładuje się z Google Fonts; bez internetu, gdy nie była wcześniej zapisana, aplikacja użyje czcionki systemowej.
