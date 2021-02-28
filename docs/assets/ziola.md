## ZIOŁA

Pomoc znajduje się w `/ziola`
Skrypt potrafi wydrukować wypis co jest w woreczku po `zajrzeniu do niego`. Potrafi też zbudować bazeę ziół - rozpozna co jest w którym woreczku i będą działały bindy do brania ziół z odpowiednich woreczków (skrypt będzie 
więdział w których jest ile którego zioła).
Jest również komenda do pakowania ziół: 

`/zapakuj [numer_woreczka] [ziolo]`

Czyli przykładowo, mając przy pasie/w ręce 7 woreczków, budujemy sobie bazę. 
Skrypt rozpozna wszystkie zioła w woreczkach (puste będzie widział jako puste). Załóżmy, że mamy zioła w woreczkach `1`, `3`, `4`, `6`, `7` i chcemy zapakować komuś cały woreczek delion. Możemy wykonać:

`/zapakuj 2 deliona`

_drugi_ woreczek jest pusty. 

#### UWAGA
Po każdej zmianie liczebników woreczków (przykładowo po wzieciu któregoś z plecaka/kupieniu jakiegoś/odłożeniu któregoś) skrypt ma w bazie nieprawidłowe przypisania liczebników woreczków (pierwszy, drugi...) do ziół. Dlatego, przy 
każdej takiej zmianie trzeba po prostu uruchomić `/ziola_buduj` - wtedy skrypt pozbiera i zbuduje mapę ziół na nowo.

Do poprawnego działania polecenie `/ziola_buduj` istotne jest też aby na Arkadii ustawić opcję szerokości tekstu na 0: `opcje szerokosc 0`.

Skrypt wspiera sytuacje, kiedy mamy przykladowo 10 woreczków, ale tylko 6 z nich przy sobie, czyli przy pasie/w rece (reszta w plecaku), baze zbuduje tylko z tych 6.

Przy ziołach są dwa ważne ustawienia w pliku z ustawieniami. Pierwsza to:

`herbs["many_to_int"] = 25`

skrypt widząc _wiele zoltych jasnych kwiatow_ w woreczku musi przypisać temu _wiele_ jakąś liczbę. Ustawiam tutaj domyślną liczbę 25, ale można ją dowolnie zmienić (czyli trzeba sprawdzić ile postać widzi w liczebniku, a od jakiej 
ilości zaczyna się _wiele_). Druga opcja to:

`herbs["full_bag_amount"] = 44`

sluży to do pakowania woreczków. Definicja ile to oznacza pełny woreczek, czyli ile ziół zapakuje podczas komendy `/zapakuj`.

---