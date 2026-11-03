# Jóga Velem

Magyar nyelvű, reszponzív, egyoldalas bemutatkozó honlap. Egyszerű HTML, CSS és JavaScript; nincs csomagtelepítés vagy build.

## Helyi indítás

```sh
cd /workspace/gyarmatikrisztakata
python3 -m http.server 8000 --bind 127.0.0.1
```

Helyi böngészőben a 8000-es porton ellenőrizhető. A felhőkörnyezetben a socketműveletekhez az eszköz támogatott jogosultságkezelése lehet szükséges.

## Tartalom és publikálás

- A megjelenített név „Kriszta”. Nyilvános e-mail: gyarkrisz@gmail.com; a jelentkezési gomb a látogató levelezőjét nyitja meg. Telefonszám nincs megadva.
- Órák: minden kedden reggel 8:00-kor, 2700 Cegléd, Batthyány utca 15/a. Jelentkezés: gyarkrisz@gmail.com. Az ár és az időtartam nincs megadva; az oldal nem tárol űrlapadatokat.
- A mottó saját szöveg, nem Müller Péternek tulajdonított idézet. Szerzői idézet csak ellenőrzött forrással kerüljön a helyére.
- Az `assets/` képei a feltöltött eredetik optimalizált WebP-változatai. Az eredetik változatlanok; a webes változatok nem tartalmazzák az eredeti EXIF-adatokat.
- Publikáláshoz az `index.html`, `style.css`, `script.js` fájlok és az `assets/` mappa szükségesek, bármely statikus HTTPS-tárhelyen. Az eredeti fotókat nem szükséges publikálni.
- Nincsenek külső betűtípusok, követők, sütik vagy külső szolgáltatáshívások.
- A domain regisztrációja és tárhelyhez kapcsolása külön lépés. A GitHub Pages publikálást a `.github/workflows/pages.yml` munkafolyamat végzi; a sikeres Actions-futás igazolja az élesítést.

## Ellenőrzés

Asztali és mobil nézetben ellenőrizendő a navigáció, mobilmenü (bezárás linkválasztásra és Escape-re), belső hivatkozások, képbetöltés, konzolhibák és vízszintes túlcsordulás.

## Képi elrendezés

A nyitóképen a teljes jógás portré látható, eredeti képarányával. A bemutatkozás négyzetes lovas képet használ. A galéria mindkét képe azonos 2:3 arányú keretben, közös alapvonalon jelenik meg; a cicás képnél külön függőleges fókuszpont őrzi meg az arcokat. Mobilon azonos méretű, egymás alatti képek jelennek meg. A képfókuszok a `style.css` galériára vonatkozó szabályaiban állíthatók.

Az átdolgozás ellenőrzése: böngészőben 320, 390, 760, 768, 850, 1024 és 1440 pixel szélességen nincs vízszintes túlcsordulás; a galériakeretek mérete egyezik, asztali nézetben felső élük is közös. A mobilmenü, Escape-billentyű, belső hivatkozások, GYIK-lenyitás, e-mail-hivatkozások és csökkentett mozgás beállítása ellenőrizve. A galéria képeit a képernyőképek készítése előtt teljesen betöltöttük.

## Ideiglenes publikus cím – GitHub Pages

A GitHub tároló **Settings → Pages → Build and deployment → Source** mezőjében válaszd a **GitHub Actions** lehetőséget. Ezután az **Actions → Publish Jóga Velem → Run workflow → main** paranccsal indítható az első publikálás. Később minden main ágra feltöltött módosítás automatikusan publikálódik.

A munkafolyamat csak a honlap fájljait és az optimalizált assets mappát publikálja; a feltöltött eredeti fotókat nem teszi a weboldal részévé. A publikus webcímet a sikeres Deploy lépés és a Settings → Pages mutatja. Projektoldal esetén az alapértelmezett cím várhatóan `https://technogim.github.io/gyarmatikrisztakata/`.

Ha a Pages beállítás nem érhető el, ellenőrizd a tároló láthatóságát és a szervezet GitHub Pages jogosultságait/csomagját. Saját domaint csak a domain regisztrációja és a DNS-beállítások egyeztetése után adj meg.
