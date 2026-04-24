# 🛡️ Cyber Study — Cyberbezpieczeństwo i cyberwojna

Interaktywne notatki egzaminacyjne w formie jednostronicowej aplikacji: 10 pytań, 10 odpowiedzi, flashcards. W pełni offline, optymalizowane pod iPhone'a i PWA.

Live: https://supermarcin71.github.io/cyber-study/

---

## ✨ Funkcje

- **10 pytań egzaminacyjnych** z pełnymi odpowiedziami, tabelami porównawczymi, timeline'ami
- **Flashcards** — tapnięcie obraca kartę, pokazuje odpowiedź
- **„Mark as learned"** — pod każdym pytaniem; postęp zapisany w `localStorage` (`2/10` w rogu)
- **Skróty klawiaturowe** — `←` `→` nawigacja, `L` oznacz jako opanowane, `Home` powrót na górę
- **Offline-first** — Service Worker cache'uje wszystko przy pierwszym załadowaniu
- **PWA** — „Add to Home Screen" w Safari iOS → działa jak natywna aplikacja
- **Responsywne** — testowane na iPhone 15 Pro Max, tablet, desktop
- **Ciemny motyw** — mesh gradient + glassmorphism + subtelne animacje

---

## 🚀 Uruchomienie lokalne

Plik `index.html` działa bezpośrednio w przeglądarce — nie wymaga żadnego serwera:

```bash
open index.html
```

Jedyny haczyk: Service Worker rejestruje się tylko przez HTTP(S). Na `file://` aplikacja zadziała, ale cache offline zbudujesz dopiero po pierwszym wejściu z poziomu strony serwowanej przez serwer (np. GitHub Pages).

Opcjonalnie, do podglądu lokalnego z pełnym SW:

```bash
python3 -m http.server 8000
# otwórz http://localhost:8000
```

---

## 📱 Instalacja jako aplikacja (iOS)

1. Otwórz stronę w Safari
2. Tapnij **Share** → **Add to Home Screen**
3. Ikona pojawi się na ekranie głównym — fullscreen, bez paska Safari, działa offline

---

## 🧰 Struktura plików

| Plik | Co to |
|---|---|
| `index.html` | Cała aplikacja (~72 KB) |
| `tw.css` | Skompilowany Tailwind (~18 KB) |
| `sw.js` | Service Worker (cache offline) |
| `manifest.webmanifest` | PWA manifest |
| `icon.svg`, `icon-*.png` | Ikony aplikacji |
| `og-image.png` | Podgląd w social media |

Brak zależności zewnętrznych. Brak buildu. Brak CDN.

---

## ⌨️ Skróty klawiaturowe (desktop)

| Klawisz | Akcja |
|---|---|
| `→` lub `J` | Następne pytanie |
| `←` lub `K` | Poprzednie pytanie |
| `L` | Oznacz / odznacz bieżące jako opanowane |
| `Home` | Powrót na górę |

---

## 🧱 Źródła merytoryczne

- Doktryna sojusznicza NATO (AJP-3.20 — operacje w cyberprzestrzeni)
- Ustawa o krajowym systemie cyberbezpieczeństwa z 5 lipca 2018 r. (wraz z nowelizacją)
- Strategia Cyberbezpieczeństwa RP (2026)
- Literatura przedmiotu — klasyczne definicje z polskiej politologii bezpieczeństwa

---

## 📜 Licencja

MIT — do swobodnego kopiowania, modyfikowania i udostępniania. Zerżnięcie layoutu przed swoim egzaminem mile widziane.
