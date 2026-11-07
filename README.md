# IvanNG-27.github.io

Web de usuario de GitHub Pages. Sirve para dos cosas:

- `/__/auth/`: los archivos de inicio de sesión de Firebase de Nocta, servidos desde el mismo dominio que la app
  (`ivanng-27.github.io`). Así los navegadores que bloquean el almacenamiento entre sitios (Safari/iPhone,
  Chrome y Firefox recientes) no rompen el inicio de sesión con Google. Copiados de
  `https://nocta-5f52e.firebaseapp.com/__/auth/` (`handler` e `iframe` llevan `.html` para que GitHub Pages
  los sirva como página). Si algún día falla el inicio de sesión tras una actualización de Firebase, vuelve a
  copiarlos de ahí.
- `/`: redirige a Nocta (`/agenda/`).

`.nojekyll` es necesario: sin él, GitHub Pages ignora las carpetas que empiezan por `_`.
