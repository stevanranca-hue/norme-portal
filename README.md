# Rezultati obračuna (portal)

Statična stranica za editore da provjere svoj bonus/ocjenu za obračunski period, zaštićena ličnim ID + PIN kodom.

Rezultat svakog editora je enkriptovan (AES-256-GCM, ključ izveden iz PIN-a preko PBKDF2-HMAC-SHA256 sa 300.000 iteracija) i dekriptuje se isključivo u browseru editora. `payloads.json` ne sadrži nijedno ime ni čitljiv podatak — samo šifrat. Dekriptovanje bez tačnog PIN-a nije moguće.

Generiše se iz privatnog obračunskog motora: https://github.com/stevanranca-hue/norme (taj repo ostaje privatan jer sadrži stvarna imena i obračune).

PIN kodovi se distribuiraju editorima van ovog repozitorijuma (npr. email/lično), nikad ne idu u git.
