# zanaxu-games

Public page and game list of **Zanaxú Games**: https://yovanyjls.github.io/zanaxu-games/

- `index.html`: the public page, with one card per game linking to Google Play.
- `games.json`: the list of games, newest first. The "More games" screen inside each game reads it too.
  ```json
  { "version": 1, "games": [ { "package": "com.zanaxu.example", "name": "Example", "icon": "icons/com.zanaxu.example.png" } ] }
  ```
- `icons/<package>.png`: 192×192 icons.
