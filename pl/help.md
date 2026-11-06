---
layout: page
title: Pomoc
permalink: /pl/help/
---

[English](../../help/?lang=en) · **Polski**

## Pierwsze uruchomienie

1. **W Home Assistant:** zainstaluj [integrację WristTalk](https://github.com/grzegorz-krzyzak/ha-wristtalk#readme) przez HACS i dodaj ją. Wybierz domyślny potok Assista dla nowych zegarków i **adres dla zegarków** - adres `https://` z zaufanym certyfikatem (np. Home Assistant Cloud). Opcje integracji pokazują go w całości jako link: na telefonie stuknij go i skopiuj z paska adresu przeglądarki.
2. **W Garmin Connect** na telefonie: ustawienia aplikacji WristTalk → **Adres domu** → wklej adres → Zapisz.
3. **W Home Assistant:** integracja WristTalk → **Dodaj zegarek**. Parowanie jest otwarte przez 5 minut.
4. **Na zegarku:** otwórz WristTalk. Pokaże kod - porównaj go z kodem w Home Assistant i potwierdź.

Zegarek łączy się z Home Assistant przez telefon (Garmin Connect musi działać, a telefon być w pobliżu) - także w domu; Wi-Fi zegarka nie jest używane.

## Na zegarku

| Przycisk | Co robi |
|---|---|
| **START** | Powiedz komendę; ponowny START wysyła ją od razu (inaczej zegarek sam zauważy, że skończyłeś mówić). W trakcie odpowiedzi: przerywa ją i słucha od nowa. |
| **BACK** | Przerywa komendę w toku; na ekranie bezczynności zamyka aplikację. |
| **UP / DOWN** | Przewijanie rozmowy. |
| **Przytrzymaj UP** | Tylko tekst wł. / wył. (pokazuje to ikona głośnika u góry). |
| **Dotyk** | Przeciągnij, żeby przewinąć. Stuknięcie tylko budzi ekran - komendy zaczyna START. |

## Ustawienia (Garmin Connect)

- **Adres domu** - gdzie zegarek znajdzie twój Home Assistant: adres dla zegarków z integracji WristTalk, zaczynający się od `https://`.
- **Połącz ponownie z domem** - włącz i zapisz, żeby sparować zegarek od nowa (nowy dom, nowy adres albo zegarek usunięty w Home Assistant). Po parowaniu wyłącza się sam.
- **Słuchaj od razu po otwarciu** - włączone: otwarcie aplikacji od razu zaczyna słuchanie. Wyłączone: aplikacja czeka na START.
- **Po odpowiedzi** - *Czekaj na START* (domyślnie) albo *Słuchaj dalej* do rozmowy w obie strony. Przy *Słuchaj dalej* rozmowa albo radio w pobliżu mogą zostać wzięte za komendę.
- **Odpowiedź** - *Głos i tekst* albo *Tylko tekst* (bez dźwięku; także przytrzymanie UP na zegarku).
- **Głośność odpowiedzi** - Cicho, Średnio, Głośno.
- **Wielkość tekstu** - Mały albo Duży tekst w rozmowie.
- **Wibracje** - *Pełne* (także na start słuchania i wysłanie komendy), *Minimalne* (odpowiedź i błędy, domyślnie), *Wyłączone*.
- **Zamknij po bezczynności** - po tym czasie bez używania aplikacja pyta „Zostać?” przez 10 sekund (START: zostań, BACK: zamknij), potem się zamyka.

## Każdy zegarek w Home Assistant

Karta urządzenia zegarka w Home Assistant ma trzy ustawienia:

- **Asystent** - potok Assista tego zegarka (rozpoznawanie mowy, agent, głos).
- **Wykrywanie końca mowy** - jak szybko komenda się kończy, gdy przestaniesz mówić. *Domyślne* pasuje najczęściej; *Agresywne* potrafi uciąć komendę na pauzie.
- **Jakość głosu odpowiedzi** - *Szybka* (domyślna, najmniejszy plik, najszybciej przez telefon), *Zrównoważona*, *Najlepsza* (warto przy słuchawkach).

## Gdy coś nie działa

- **„Brak połączenia z telefonem”** - Bluetooth jest wyłączony albo Garmin Connect nie działa na telefonie.
- **„Adres domu musi zaczynać się od https://”** - Home Assistant musi być dostępny przez HTTPS z zaufanym certyfikatem; zwykłe `http://` przez telefon nie działa, także w domu.
- **„Zaktualizuj WristTalk na zegarku” / „Zaktualizuj integrację WristTalk w Home Assistant”** - aplikacja i integracja mówią różnymi wersjami protokołu: zaktualizuj tę wskazaną.
- **„Nic nie usłyszałem”** - powiedz komendę jeszcze raz po START.
- **Zegarek znowu prosi o parowanie** - został usunięty w Home Assistant albo włączono „Połącz ponownie”: dodaj go ponownie przez **Dodaj zegarek**.

Pytania: [wristtalk.app@gmail.com](mailto:wristtalk.app@gmail.com) · [Polityka prywatności (po angielsku)](../../privacy/)
