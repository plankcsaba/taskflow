#Taskflow

Taskflow egy modern feladatkezelő és projektmenedzsment webalkalmazás, amelyet a Rendszerfejlesztési technológiák tantárgy keretében fejlesztettünk. A rendszer célja a csapatok napi munkájának, feladatainak és határidőinek átlátható kezelése Kanban-stílusú táblák és részletes projektnézetek segítségével.

Főbb Funkciók:
- Felhasználókezelés: Biztonságos regisztráció, bejelentkezés és szerepköralapú jogosultságkezelés.
- Feladatkezelés (CRUD): Feladatok létrehozása, szerkesztése, törlése, prioritások és határidők beállítása.
- Kanban Státuszkezelés: A feladatok állapotának nyomon követése és drag-and-drop mozgatása (Teendő, Folyamatban, Kész oszlopok között).
- Felelősök rendelése: Feladatok hozzárendelése konkrét csapattagokhoz.
- Kommentrendszer: Megjegyzések írása és olvasása a feladatkártyákon belül a hatékonyabb egyeztetésért.

Nem Funkcionális Követelmények:
- Teljesítmény: Gyors válaszidő 500ms az alapvető műveleteknél.
- Biztonság: Titkosított kommunikáció (HTTPS / TLS) és biztonságos jelszó-hash-elés.
- Reszponzivitás: Mobilbarát kialakítás különböző képernyőméretekre.
- Adatbiztonság: Napi automatikus adatbázis-mentések.

Javasolt Technológiai StackFrontend: React.js / Vite / Tailwind CSSBackend: Node.js, Express.js
Adatbázis: PostgreSQL vagy MongoDB
Verziókezelés: Git / GitHubTelepítés és Futtatás (Lokális környezet)
A repository klónozása:
    git clone https://github.com/szervezet/taskflow.git
    cd taskflow

Backend függőségek telepítése és indítása:cd backend
    npm install
    npm run dev

Frontend függőségek telepítése és indítása:cd frontend
    npm install
    npm run dev

Dokumentáció & CsapatA projekt részletes funkcionális és nem funkcionális specifikációit, valamint a Teamwork Agreementet a projekt dokumentációs mappájában találjátok.
Készítette a Taskflow Csapat.