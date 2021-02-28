[![Version](https://img.shields.io/github/v/release/tjurczyk/arkadia?label=version&color=%23438f57)](https://github.com/tjurczyk/arkadia/releases)
![Verify config.md](https://github.com/tjurczyk/arkadia/workflows/Verify%20config.md/badge.svg)

## Arkadia Skrypty

Pomoc dostępna pod `/skrypty`<br>
Pomoc do mappera znajduje się [tutaj](README_MAPPER.md) \
Wersja, której używasz: sprawdź nagłówek komendy `/skrypty`.

## Spis treści

1. [Instalacja i konfiguracja Mudleta](docs/installation.md)
1. [Ustawienia postaci](docs/settings.md)
1. Moduły:
   1. [Walka](docs/walka.md)
   1. [Ekwipunek](docs/ekwipunek.md)
   1. [Ziola](docs/ziola.md)


## WALKA


---

## EKWIPUNEK


---



## UI

Pomoc znajduje się w `/ui`.
UI to dolna belka oraz okno stanów (prawy górny róg). Należy przejrzeć `/ui`, jest tam wszystko wyjaśnione.

Poza tym, w pliku z ustawieniami można sobie zdefiniować co ma być gagowane (dodawane [tagi]), co usuwane, a co zostawione tak jak przychodzi z Arkadii.

---

## BINDY

Pomoc znajduje się w `/bindy`. Kilka przydatnych bindów do wycinania, medytacji, masowej oceny kamieni (czyli 
zsumuje wartosc wszystkich), kowala itp.

---

## BRONIE

Pomoc znajduje się w `/bronie`. Można sobie ustawić do trzech pojemników na bronie (lub na tarczę, będzie to pojemnik _other_ albo plecy (opcja gz...)). Ustawienia wszystkich pojemników wraz ze szczegółami jak to zrobić jest w pliku konfiguracyjnym txt.

---

## STATYSTYKI

Są dostępne statystyki parowań, otrzymamych ciosów itp., Statystyki dostępne w `/stat`.

---

## LICZNIKI

**Liczniki zabitych**

`/zabici` - pokazuje zabitych,
<br>
`/zabici_reset` - resetuje licznik zabitych.
<br>
`/zabici2` - globalni zabici od ostatniego resetu licznika,
<br>
`/zabici2!` - globalni zabici z uwzglednieniem zabitych/dzien,
<br>
`/zabici2 [data]` - log zabitych z [dnia]. Przykładowo: `/zabici2 2017/1/22`.
<br>
`/zabici2_reset` - resetuje globalny licznik zabitych.
<br><br>
**Liczniki postępów**
<br>
`/postepy` - pokazuje postępy (czas, wrogowie itp),
<br>
`/postepy_reset` - resetuje licznik postępów.
<br>
`/postepy2` - globalny licznik postępów od ostatniego resetu,
<br>
`/postepy2+` - dodaje jeden postep do globalnego licznika,
<br>
`/postepy2+ [ile]` - dodaje [ile] postepow do globalnego licznika. Przykładowo: `/postepy2+ 4` doda 4 postepy,
<br>
`/postepy2- [id]` - usuwa wpis z globalnego licznika o tym _id_. _id_ można znaleźć jako pierwsza kolumna od lewej w `/postepy2`,
<br>
`/postepy2_reset` - resetuje globalny licznik postepow. 
<br><br>
**Licznik poziomu** 
<br>
`/cechy` - wyswietla cechy i poziom postaci (minilevele)

---

## ZBIERANIE Z CIAŁ

Pomoc dostępna w `/zbieranie`

Domyślnie ustawiona jest opcja, która sprawia, że będzie drukowane powiadomienie kiedy kogoś zabijemy i żeby użyc binda w celu zebrania monet + kamieni. Aby zmienić to należy użyć opcji `/zbieranie [numer_opcji]` w Mudlecie. Aby zmienić domyślne ustawienie wraz ze startem Mudleta, w pliku ustawień trzeba zmienić opcję: 

`scripts.inv.collect.current_mode = 3`

Dolny pasek zawiera też element `Collect`, który można klikać i zmieniać opcje.

---

## STATKI/DYLIŻANSE

Działają wszystkie statki. Przy wejściu będzie bind będzie brał pieniądze z pojemnika `money`, kupował bilet, wsiadał na statek oraz wkładał monety do pojemnika `money`; przy dopłynięciu zbindowane będzie zejście.
Dyliżanse w Imperium działają, wozy/powozy w Ishtar nie wszystkie.

Bindowany jest klawisz `[`.

---

## POJEMNIKI

[Instrukcja konfiguracji pojemników](http://arkadia.kamerdyner.net/pojemniki.html)

Komenda `/pojemniki` pokaże aktualną konfigurację pojemników. 

jak na razie dostępne bindy to `wem`/`/wlm` (branie/wkładanie monet) oraz `wep`/`wlp` (branie/wkładanie paczki).

---

## BAZA

W skryptach znajduje się wsparcie bazy postaci. W katalogu profilu jest plik: Database_scripts.db
Ten plik zawiera baze.

Wszystkie komendy i pomoc jest opisana pod `/baza`.
Bazę można pobrać korzystając z komendy `/pobierz_baze`.

Baza jest budowana następująco:

- jest możliwość zapisywania/aktualizowania wszystkich osób przedstawiających się na Arkadii. Domyślnie jest to wyłączone, aby włączyć trzeba sobie ustawić `scripts.people["updating_names"] = true` w ustawieniach;
- zapisywane jest `id` lokacji, na której dana osoba się przedstawiła;
- do NPCów na poczcie jest GPS: po 'obejrzyj tablice' na zielono podświetlą nam się na zielono osoby z paczkami, których lokacje są w bazie. Po wzięciu takiej paczki można ją obejrzeć i pojawi się informacja o `/idzdo`, która uruchomi chodzik do tej osoby. Jest też możliwy kolor pomarańczowy. Znaczy to, ze w bazie jest więcej niż jedna postać pasujaca. Można zrobić `/przeszukaj [imie]` i `/idzdo [id]`, gdzie `[id]` to będzie faktyczne `id` postaci, do której chcemy iść;
- wraz ze startem Mudleta, ładowane są triggery pokazujące imiona wszystkich graczy zgildiowanych (za wyjątkiem GP). NPC + osoby GP pojawią się gdy zostaną zobaczone w grze, wtedy jest ładowany ich trigger z bazy danych.

---


## ROZSZERZNIE SKRYPTÓW

W łatwy sposób można również dodać dodatkowe skrypty ładowane razem ze niniejszą paczką.
W katalog profilu, skrypty tworzą katalog `plugins`, należy w nim umieścić plik z paczka zawierającą plik `init.lua` z listą plików do załadowania.

Dodatkowo opcjonalnie można załączyc plik mudletowy .xml o nazwie odpowiadającej nazwie katalogu wtyczki

Rowniez opcjonalnie mozna zalaczy plik `config_schema.json`. Zaktualizuje on istniejaca scheme ustawien. Struktura powinna byc identyczna jak pliku z glownej paczki.

*Poprawna* paczka, *poprawnie* umieszczona zostanie automatycznie załadowana tuż po plikach skryptów z podstawowej paczki.

##### Przykład struktury
```
 .
 |____ katalog profilu
   |____ plugins
      |____ nasz_plugin
        |____ init.lua
        |____ nasz_plugin.xml
        |____ dodatkowe.lua
        |____ skrypty.lua
        |____ config_schema.json
```

##### _init.lua_
```
    return {
        "dodatkowe",
        "skrypty"
    }
```

## KONTAKT

1. Na forum: [@Adremen](http://arkadia.rpg.pl/forum/memberlist.php?mode=viewprofile&u=1084)
2. [Temat](https://arkadia.rpg.pl/forum/viewtopic.php?f=15&t=1023), w którym można uzyskać pomoc na forum
3. [Discord](https://discord.gg/76yaZnw)
