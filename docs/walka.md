# Walka

Pomoc znajduje się pod `/walka` wraz z opisem kompletnego zestawu bindów oraz klikalnych akcji. Prawe górne okno to okno kondycji, gdzie drukowani są wszyscy na lokacji, jeden wiersz na jedną osobę. Pierwszy wiersz to Ty, kolejni to (jeśli jesteś w) drużyna, kolejni to wrogowie i na końcu neutralni. Kolorowanie dość intuicyjne: zieloni to Twoi, fioletowi to wrogowie Twoi/drużyny, czerwony to aktualnie bity przez Ciebie, biali to neutralni. Czerwony znacznik `>>` przy osobie wskazuje, że ta osoba to cel ataku, zielony znacznik `>>` to cel obrony.

Opis wiersza wroga:

`[ 1][#######] Postac Z -> [@,A,B]`

Najpierw jest ID postaci używane w bindach (patrz `/walka`), później pasek życia, później imię/short, później identyfikatory postaci z drużyny, które biją tę postać (drużynowi są oznaczani `A`, `B`, `C`..., `@` to JA). 

Wiersz członków drużyny wygląda tak:

`[ C][#######] Postac Y -> [2,3,4]`

Tutaj inne znaczenie ma jedynie ostatni kawałek - oznacza to, że naszego kolegę/koleżankę z drużyny biją wrogowie o ID `2`, `3` i `4`.

W oknie kondycji (prawy górny róg) numerowani (pierwsza kolumna) są domyślnie tylko aktualni przeciwnicy. Czyli, praktycznie wszystkie bindy ataku typu `/z 2` itp. będą działały tylko na wrogach, z którymi aktualnie już walczymy. Można to zmienić, aby numerować wszystkich (ale wtedy należy uwazać, bo bindy + klikalne akcje na oknie działają na wszystkich). Aby zmienić to należy użyć opcji `/numeruj` w kliencie. Aby zmienić domyślne ustawienie wraz ze startem Mudleta, w pliku ustawień trzeba zmienić opcję `ateam.all_numbering`
