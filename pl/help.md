---
layout: page
title: Pomoc
permalink: /pl/help/
---

[English](../../help/?lang=en) · **Polski**

[Pierwsze kroki](#pierwsze-kroki) · [Używanie](#używanie) · [Ustawienia](#ustawienia) · [W Home Assistant](#w-home-assistant) · [Coś nie działa?](#coś-nie-działa)

## Pierwsze kroki

Potrzebujesz Home Assistant dostępnego przez **HTTPS** (np. Home Assistant Cloud) i telefonu z **Garmin Connect** w pobliżu zegarka.

1. **Zainstaluj integrację.** W Home Assistant dodaj [WristTalk](https://github.com/grzegorz-krzyzak/ha-wristtalk#readme) przez HACS.
2. **Skopiuj adres.** Opcje integracji pokazują adres dla zegarków jako link. Na telefonie: stuknij go i skopiuj z przeglądarki.
3. **Wklej go w Garmin Connect.** WristTalk → Ustawienia → **Adres domu** → Zapisz.
4. **Sparuj.** W Home Assistant: WristTalk → **Dodaj zegarek**. Otwórz WristTalk na zegarku i potwierdź pokazany kod.

Zegarek zawsze łączy się z Home Assistant przez telefon - także w domu.

## Używanie

| | |
|---|---|
| **START** | Powiedz komendę. Naciśnij ponownie, żeby wysłać ją od razu. |
| **BACK** | Przerwij komendę. Na ekranie bezczynności: zamknij aplikację. |
| **UP / DOWN** | Przewijaj rozmowę. |
| **Przytrzymaj UP** | Tylko tekst wł. / wył. |
| **Dotyk** | Przeciągnij, żeby przewinąć. Stuknięcie tylko budzi ekran. |

## Ustawienia

W Garmin Connect: WristTalk → Ustawienia.

| Ustawienie | Co robi |
|---|---|
| **Adres domu** | Gdzie zegarek znajdzie twój Home Assistant. |
| **Połącz ponownie z domem** | Paruje zegarek od nowa. Potem wyłącza się sam. |
| **Słuchaj od razu po otwarciu** | Otwarcie aplikacji od razu zaczyna słuchanie. |
| **Po odpowiedzi** | *Czekaj na START* albo *Słuchaj dalej* do rozmowy. Słuchanie dalej może wziąć głos lub radio w pobliżu za komendę. |
| **Odpowiedź** | *Głos i tekst* albo *Tylko tekst*. |
| **Głośność odpowiedzi** | Cicho, Średnio albo Głośno. |
| **Wielkość tekstu** | Mała albo Duża. |
| **Wibracje** | *Pełne*, *Minimalne* (odpowiedź i błędy) albo *Wyłączone*. |
| **Zamknij po bezczynności** | Po tym czasie aplikacja pyta *Zostać?*, potem się zamyka. |

## W Home Assistant

Każdy zegarek ma własną kartę urządzenia z trzema ustawieniami.

| Ustawienie | Co robi |
|---|---|
| **Asystent** | Potok Assista, którego używa zegarek. |
| **Wykrywanie końca mowy** | Jak szybko komenda się kończy, gdy przestaniesz mówić. *Domyślne* pasuje najczęściej. |
| **Jakość głosu odpowiedzi** | *Szybka* (domyślna) dociera najszybciej. *Najlepsza* brzmi lepiej w słuchawkach. |

## Coś nie działa?

| Na zegarku | Co zrobić |
|---|---|
| **Brak połączenia z telefonem** | Włącz Bluetooth i otwórz Garmin Connect. |
| **Adres domu musi zaczynać się od https://** | Użyj adresu HTTPS. Zwykłe http:// nie działa, nawet w domu. |
| **Zaktualizuj WristTalk na zegarku** | Zaktualizuj aplikację na zegarku. |
| **Zaktualizuj integrację WristTalk w Home Assistant** | Zaktualizuj integrację w HACS. |
| **Nic nie usłyszałem** | Naciśnij START i powiedz jeszcze raz. |
| **Ponowne parowanie** | Zegarek usunięto w Home Assistant albo włączono „Połącz ponownie”. Użyj **Dodaj zegarek**. |

Pytania: [wristtalk.app@gmail.com](mailto:wristtalk.app@gmail.com) · [Polityka prywatności (po angielsku)](../../privacy/)
