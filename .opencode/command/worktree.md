---
description: Crea un git worktree en .worktrees/<nombre>
---

Resuelve el <nombre-del-worktree> así:
- Si el usuario pasó un argumento, usa ese valor ($1).
- Si no llegó argumento, pregúntale al usuario el nombre.

Después ejecuta EXACTAMENTE este comando, en el directorio actual (sin cambiar de directorio):

git worktree add .worktrees/<nombre-del-worktree>

No cambies de directorio ni hagas ningún otro cambio.

Si el argumento es muy largo, simplificalo a algo significativo.