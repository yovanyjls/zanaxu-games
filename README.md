# zanaxu-games

Lista de juegos de Zanaxú que muestra la pantalla **"Más juegos"** dentro de cada juego.

- `games.json`: lista de juegos, del más nuevo al más viejo.
  - Cada juego tiene `package`, `name` e `icon`.
  - `icon` es una ruta relativa a este archivo.
- `icons/<paquete>.png`: íconos de 192×192.

Los juegos la leen de `https://yovanyjls.github.io/zanaxu-games/games.json`. Cada juego omite su propio paquete, y si no
hay internet muestra la última lista guardada.

## Publicarla la primera vez
1. En GitHub, crea el repositorio **público** `zanaxu-games` en la cuenta `yovanyjls`. Hazlo vacío, sin README.
2. Sube los archivos de esta carpeta con **Add file → Upload files**: arrastra `games.json`, `README.md` y la carpeta `icons`.
3. En **Settings → Pages**, elige "Deploy from a branch", rama `main` y carpeta `/ (root)`, y guarda.
4. En 1-2 minutos debe abrir https://yovanyjls.github.io/zanaxu-games/games.json.

## Agregar un juego nuevo
```
python C:/YJLS/Workspace/AndroidStudioProjects/Apps/Scripts/mas_juegos/agregar_juego.py com.zanaxu.<nombre> "Nombre" C:/YJLS/Workspace/AndroidStudioProjects/Apps/Imagenes/<Proyecto>/icon.png
```
Después sube `games.json` y el ícono nuevo al repositorio. Los juegos ya publicados lo muestran sin actualizarse.
Agrégalo cuando el juego ya esté **publicado** en Play Store, para que el enlace no lleve a una ficha que todavía no existe.
