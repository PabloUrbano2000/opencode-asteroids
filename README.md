# Asteroids

Clon del clásico arcade **Asteroids** implementado en canvas HTML5 puro, sin dependencias ni bundler.

## Descripción

Nave espacial en un campo de asteroides con envolvimiento de bordes (el espacio es toroidal). Destruye asteroides para sumar puntos: los grandes se parten en medianos, los medianos en pequeños. Incluye power-ups especiales y tipos de asteroides únicos como la estrella fugaz.

## Tecnologías

- **HTML5 Canvas** — renderizado 2D
- **JavaScript (ES6+)** — lógica del juego en un solo archivo `game.js`
- Sin frameworks, sin bundler, sin dependencias

## Cómo correr

Abre `index.html` directamente en el navegador (doble clic), o usa un servidor local:

```bash
npx serve .
```

Luego visita `http://localhost:3000`.

## Controles

| Tecla     | Acción            |
| --------- | ----------------- |
| `←` `→`   | Rotar nave        |
| `↑`       | Propulsar         |
| `Espacio` | Disparar          |
| `1`–`4`   | Cambiar skin nave |

## Puntuación

| Asteroide | Puntos |
| --------- | ------ |
| Grande    | 20     |
| Mediano   | 50     |
| Pequeño   | 100    |

## Características

- 3 vidas con invencibilidad temporal al reaparecer (parpadeo)
- Asteroides se parten en fragmentos más pequeños al ser destruidos
- Partículas de explosión al destruir asteroides
- Estrellas fugaces que cruzan la pantalla (no bloquean el fin de nivel)
- Power-ups: **velocidad** (propulsión extra 5s), **triple** (disparo triple 5s) y **escudo** (protege de asteroides 8s)
- 4 skins de nave intercambiables con las teclas `1`–`4` (se guardan en localStorage). La skin **MORADA** (`4`) es el doble de grande y otorga el doble de puntos.
