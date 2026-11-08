---
layout: page
title: Pomoc
permalink: /pl/help/
---

[English](../../help/?lang=en) · **Polski**

[Pierwsze kroki](#pierwsze-kroki) · [Używanie](#używanie) · [Ustawienia](#ustawienia) · [W Home Assistant](#w-home-assistant) · [Coś nie działa?](#coś-nie-działa)

## Pierwsze kroki

Potrzebujesz Home Assistant dostępnego przez **HTTPS** (np. Home Assistant Cloud) i telefonu z **Garmin Connect** w pobliżu zegarka - przez nią zegarek łączy się z domem.

1. **Zainstaluj integrację.** W Home Assistant dodaj [WristTalk](https://github.com/grzegorz-krzyzak/ha-wristtalk#readme) przez HACS.
2. **Skopiuj adres.** Opcje integracji pokazują adres dla zegarków jako link - skopiuj go.
3. **Wklej go w aplikacji Connect IQ.** WristTalk → Ustawienia → **Adres domu** → Zapisz.
4. **Sparuj.** W Home Assistant: WristTalk → **+ Dodaj zegarek**. Otwórz WristTalk na zegarku i wpisz pokazany kod w Home Assistant. Parowanie jest otwarte przez 3 minuty.

Zegarek zawsze łączy się z Home Assistant przez telefon - także w domu.

## Używanie

| Przycisk | Co robi |
|---|---|
| **START** | Powiedz komendę. Naciśnij ponownie, żeby wysłać ją od razu. |
| **BACK** | Przerwij komendę. Na ekranie bezczynności: zamknij aplikację. |
| **UP / DOWN** | Przewijaj rozmowę. |
| **Przytrzymaj UP** | Menu: *Tylko tekst* wł. / wył., *Sparuj ponownie*, wersja aplikacji. |
| **Dotyk** | Przeciągnij, żeby przewinąć. Stuknięcie tylko budzi ekran. |

## Ustawienia

W aplikacji Connect IQ na telefonie: WristTalk → Ustawienia.

| Ustawienie | Co robi |
|---|---|
| **Adres domu** | Gdzie zegarek znajdzie twój Home Assistant. |
| **Słuchaj od razu po otwarciu** | Otwarcie aplikacji od razu zaczyna słuchanie. |
| **Po odpowiedzi** | *Czekaj na START* albo *Słuchaj dalej* do rozmowy. Przy *Słuchaj dalej* zegarek może uznać rozmowę lub radio w pobliżu za komendę. |
| **Odpowiedź** | *Głos i tekst* albo *Tylko tekst*. |
| **Głośność odpowiedzi** | Cicho, Średnio albo Głośno. |
| **Wielkość tekstu** | Mała albo Duża. |
| **Wibracje** | *Wyłączone*, *Minimalne* (odpowiedź i błędy) albo *Pełne*. |
| **Zamknij po bezczynności** | Po tym czasie aplikacja pyta *Zostać?*, potem się zamyka. |

## W Home Assistant

Każdy zegarek ma własną kartę urządzenia z trzema ustawieniami i statusem.

| Ustawienie | Co robi |
|---|---|
| **Asystent** | Potok Assista, którego używa zegarek. |
| **Wykrywanie końca mowy** | Jak szybko komenda się kończy, gdy przestaniesz mówić. *Domyślne* pasuje najczęściej. |
| **Jakość głosu odpowiedzi** | *Szybka* (domyślna) dociera najszybciej. *Najlepsza* brzmi lepiej w słuchawkach. |
| **Status** | *Sparowany* albo *Wymaga ponownego sparowania*. |

**Sparuj ponownie:** ikona ⚙ przy zegarku w karcie integracji WristTalk. Zegarek i jego ustawienia zostają, zmienia się tylko klucz.

## Coś nie działa?

| Na zegarku | Co zrobić |
|---|---|
| **Brak połączenia z telefonem** | Włącz Bluetooth i otwórz Garmin Connect. |
| **Adres domu musi zaczynać się od `https://`** | Użyj adresu HTTPS.<br>Zwykłe `http://` nie działa, nawet w domu. |
| **Zaktualizuj WristTalk na zegarku** | Zaktualizuj aplikację na zegarku. |
| **Zaktualizuj integrację WristTalk w Home Assistant** | Zaktualizuj integrację w HACS. |
| **Nic nie usłyszałem** | Naciśnij START i powiedz jeszcze raz. |
| **Parowanie** z kodem | Po *Sparuj ponownie*: w Home Assistant ⚙ przy zegarku albo Ustawienia → Naprawy → **Napraw**. Zegarek usunięto w Home Assistant: **+ Dodaj zegarek**. Potem wpisz kod z zegarka. Jeśli kod nie zostanie wpisany w ciągu 3 minut, zegarek pokaże nowy. |

Pytania: [wristtalk.app@gmail.com](mailto:wristtalk.app@gmail.com)
