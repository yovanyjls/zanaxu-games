# zanaxu-games

Lista de juegos de Zanaxú que muestra la pantalla **"Más juegos"** dentro de cada juego.

- `games.json`: lista de juegos, del más nuevo al más viejo.
  - Cada juego tiene `package`, `name` e `icon`.
  - `icon` es una ruta relativa a este archivo.
- `icons/<paquete>.png`: íconos de 192×192.

Los juegos la leen de `https://yovanyjls.github.io/zanaxu-games/games.json`. Cada juego omite su propio paquete, y si no
hay internet muestra la última lista guardada.

Copia local (repositorio git conectado a `https://github.com/yovanyjls/zanaxu-games`):
`C:\YJLS\Workspace\AndroidStudioProjects\Apps\GitHubPages\zanaxu-games`.
- Los commits usan `yovany.jls@gmail.com`, configurado solo en este repositorio.
- Las credenciales son las de Git Credential Manager de Windows.

## Agregar un juego (cuando ya esté publicado en Play Store)
```
python C:/YJLS/Workspace/AndroidStudioProjects/Apps/Scripts/mas_juegos/agregar_juego.py com.zanaxu.<nombre> "Nombre" C:/YJLS/Workspace/AndroidStudioProjects/Apps/Imagenes/<Proyecto>/icon.png --publicar
```
Con `--publicar`, el script hace todo esto:
- trae lo último del repositorio;
- actualiza `games.json` y el ícono;
- hace commit y push;
- espera a que GitHub Pages muestre el juego.

Si el remoto no es `zanaxu-games` o hay cambios sin subir, se detiene. Sin `--publicar`, solo edita los archivos locales.
Los juegos ya publicados muestran el juego nuevo sin actualizarse.
