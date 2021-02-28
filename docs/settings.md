# Ustawienia postaci

Skrypty mają swoje ustawienia przechowywane w pliku `<imie>.json` w katalogu profilu Mudleta. Aby dowiedzieć się gdzie siedzi katalog profilu, należy w linii komend w Mudlecie wykonać komendę:

`lua getMudletHomeDir()`

Plik ustawień postaci można załadować komendą `/laduj imie` która ładuje plik o nazwie `imie.json`.

W przypadku pierwszego uruchomienia automatycznie uruchomi się konfigurator, służący do utworzenia ustawień postawić. 
Konfigurator można przywołać komendą `/konfiguruj`.

![Konfigurator](assets/configurator.png)

Pomoc dotyczaca konfiguracji dostepna jest dostępna pod adresem: http://arkadia.kamerdyner.net/config.html 

Dodatkowo opis kluczy konfiguracyjnych dostępny [tutaj](../config.md)

# UWAGA: 

Czasami jest tak, że tekst wygląda lekko _rozjechany_. To znaczy, można to poznać po tym, że widać, że odstępy między tekstem są większe niż normalnie, wtedy podczas zaznaczania tekstu, tekst 'zsuwa' się ze sobą i odstępy są normalne. Jest to błąd Mudletowy. Wystarczy wtedy chwycić za tekst i zaznaczając go przeciagnac na sam dół aby najechać na dolny pasek - wtedy tekst _dosunie się_ i będzie już równo. Po wykonaniu `/ui_restart`, trzeba zawsze takie coś wykonać.
