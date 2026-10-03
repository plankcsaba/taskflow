Funkcionális Követelmények:

    - Felhasználókezelés: Biztonságos regisztráció, bejelentkezés, valamint szerepköralapú jogosultságkezelés (Adminisztrátor, Projektmenedzser, Fejlesztő/Tag).
    - Feladatkezelés (CRUD): Feladatok létrehozása, szerkesztése, törlése és megtekintése, részletes leírással, prioritással (alacsony, közepes, magas) és határidővel.
    - Státuszkezelés és Tábla: A feladatok életciklusának követése (Teendő, Folyamatban, Kész) Kanban-tábla vagy lista nézetben.
    - Projektmenedzsment: Projektek létrehozása, csoportosítása, valamint felhasználók hozzárendelése az adott projektekhez.

    User Story-k és Elfogadási Kritériumok:


    US1: Új feladat létrehozása

        User Story: Mint projektmenedzser, szeretnék új feladatot létrehozni a rendszerben, hogy a csapattagok lássák az elvégzendő teendőket.

        Elfogadási kritériumok:
            - A feladatnak kötelező megadni a címét és a leírását.
            - Opcionálisan beállítható határidő, becsült idő és prioritás.
            - Mentés után a feladat azonnal megjelenik a projekt backlogjában vagy a "Teendő" oszlopban.



    US2: Feladat státuszának módosítása

        User Story: Mint fejlesztő, szeretném a feladat státuszát frissíteni a Kanban-táblán, hogy a csapat lássa a munka aktuális állását.

        Elfogadási kritériumok:
            - A kártya áthúzható (drag-and-drop) az oszlopok között (Teendő -> Folyamatban -> Kész).
            - A státuszváltozás azonnal mentődik az adatbázisban anélkül, hogy az egész oldalt újra kellene tölteni.
            - A rendszer rögzíti az utolsó státuszmódosítás időpontját.



    US3: Feladat hozzárendelése felelőshöz

        User Story: Mint csapatvezető, szeretnék egy feladatot konkrét csapattaghoz rendelni, hogy egyértelmű legyen, ki a felelős a végrehajtásért.

        Elfogadási kritériumok:
            - A feladat szerkesztésekor egy legördülő menüből kiválasztható a projekthez tartozó bármelyik felhasználó.
            - Mentés után a hozzárendelt személy neve/avatárja megjelenik a feladatkártyán.



    US4: Megjegyzések írása a feladathoz

        User Story: Mint csapattag, szeretnék megjegyzéseket írni egy feladathoz, hogy a feladattal kapcsolatos egyeztetéseket, kérdéseket vagy frissítéseket közvetlenül a kártyánál rögzíthessem a többiekkel.

        Elfogadási kritériumok:
            - A feladat részleteit megnyitva elérhető egy kommentmező szöveges üzenetek írására.
            - A beküldött megjegyzés mellett automatikusan megjelenik a szerző neve (vagy avatárja) és a pontos időbélyeg.
            - A kommentek időrendi sorrendben látszódnak, és a projekt minden hozzáféréssel rendelkező tagja elolvashatja vagy kiegészítheti azokat.

Nem Funkcionális Követelmények:

    - Teljesítmény (Válaszidő)
        Leírás: A felhasználói felületen végzett alapvető interakcióknak (pl. feladat státuszának módosítása drag-and-drop módszerrel, új feladat mentése, komment beküldése) legfeljebb 500 milliszekundumon belül válaszolniuk kell, hogy a rendszer folyamatos és zökkenőmentes élményt nyújtson.

    - Biztonság (Adatvédelem és Hitelesítés)
        Leírás: Az alkalmazásnak minden kommunikációt titkosított csatornán (HTTPS / TLS) kell lebonyolítania. A felhasználói jelszavakat soha nem szabad nyers szövegben tárolni; azokat erős, egyirányú hash algoritmussal (pl. bcrypt vagy Argon2) titkosítva kell rögzíteni az adatbázisban.

    - Használhatóság és Reszponzivitás
        Leírás: A felületnek reszponzív designnal kell rendelkeznie, amely automatikusan alkalmazkodik a különböző képernyőméretekhez (asztali monitorok, tablet, mobiltelefon), biztosítva a kényelmes használatot mobil böngészőkben is.

    - Megbízhatóság és Adatbiztonság
        Leírás: A rendszer adatbázisáról legalább napi automatikus biztonsági mentést (backup) kell készíteni, megelőzve az esetleges rendszerhibákból adódó adatvesztést.