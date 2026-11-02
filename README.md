# Sortides V3 · Josep Mestres i Busquets

Web externa connectada al mateix Apps Script i Google Sheets de la V3.
No conté dades d’alumnes, PINs ni còpies del full.

## Instal·lació

1. Crea un repositori a GitHub, per exemple `registre-sortides-v3`.
2. Puja els fitxers extrets d’aquest ZIP a l’arrel del repositori. `index.html` i `config.js` han de quedar directament a l’arrel, no dins una subcarpeta.
3. Ves a Settings → Pages → Source: Deploy from a branch → main → /(root) → Save.
4. Obre l’enllaç que indiqui GitHub Pages. La publicació pot trigar uns minuts.
5. Inicia sessió amb el correu i PIN que ja utilitzes a la V3.

## Apps Script

La V3 ja té `doPost` i les operacions necessàries. No cal tornar a executar la configuració ni activar de nou les còpies.
El desplegament ha d’executar-se com a propietari i acceptar peticions sense autenticació de Google (opció «Cualquier persona», si el domini ho permet). L’accés a les dades continua requerint el correu i el PIN de l’aplicació.
«Cualquier usuario con una cuenta de Google» o només el domini pot impedir l’accés des d’aquesta web externa. Si el centre no permet l’accés sense sessió Google, consulta l’administrador; aquesta versió no evita aquesta restricció.
No facis públic el full de Google Sheets.

## Prova de connexió

1. Obre GitHub Pages en un navegador normal i en un mòbil amb diversos comptes Google.
2. Entra amb un usuari autoritzat. Aquesta prova verifica també que la resposta es pot llegir des de l’origen de GitHub Pages.
3. Amb un alumne fictici, crea una sortida a GitHub i comprova que apareix a la web d’Apps Script.
4. Confirma el retorn des de l’altra entrada i actualitza GitHub.
5. Prova Altres motius, el circuit de lavabos i la consulta completa.
6. Per provar fora d’horari, activa el mode de proves des de l’editor i desactiva’l després.

La connexió real i les polítiques del domini encara s’han de validar. No s’han utilitzat credencials ni creat registres reals durant la preparació.

## Manteniment

- Alumnes i Autoritzats: es gestionen al mateix full de càlcul.
- Còpies i tancaments: continuen a Apps Script.
- Si canvies l’enllaç del desplegament: modifica només `config.js`.
- Si actualitzes la mateixa implementació d’Apps Script mantenint-ne l’URL, no cal canviar config.js.
- Per canvis de pantalla a GitHub: actualitza index.html. La pantalla nativa d’Apps Script es manté al seu propi Index.html.
- La consulta completa està a `index.html?page=consulta`.
- GitHub Pages necessita connexió a internet per llegir o registrar dades. Aquesta entrega no inclou servei fora de línia.

## Referències

https://docs.github.com/en/pages/quickstart
https://developers.google.com/apps-script/guides/web
