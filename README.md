# Omarchy en Español

Traduce al español la interfaz del sistema de menús de [Omarchy](https://omarchy.com) — el entorno de escritorio Linux basado en Hyprland.

## Qué hace

Reemplaza el archivo `~/.config/omarchy/extensions/menu.sh` con una versión completamente traducida al español. Traduce todos los menús principales:

- Menú principal (Aplicaciones, Aprender, Acciones, Estilo, Configurar, Instalar, Quitar, Actualizar, Sistema)
- Submenús de aprendizaje, acciones, hardware, temas y más

Antes de aplicar cualquier cambio, el script hace una copia de seguridad automática del archivo original.

## Requisitos

- Arch Linux con [Omarchy](https://omarchy.com) instalado
- Bash 4+
- Python 3

## Uso

```bash
bash omarchy-spanish.sh
```

El script presenta tres opciones:

```
  Omarchy → Español
  ──────────────────
  1) Aplicar traducción española
  2) Restaurar backup anterior
  3) Salir
```

### Opción 1 — Aplicar traducción

Aplica la traducción al español. Si es la primera vez, guarda un backup automático del archivo original en:

```
~/.config/omarchy/extensions/backups/YYYYMMDD_HHMMSS/
```

Al terminar, reiniciá Walker para ver los cambios:

```bash
omarchy restart walker
```

### Opción 2 — Restaurar backup

Si algo no funciona bien, podés volver al estado anterior eligiendo cualquiera de los backups disponibles.

### Nota tras `omarchy update`

Cada vez que corrás `omarchy update` el archivo de menú puede sobreescribirse con la versión original en inglés. En ese caso, volvé a ejecutar el script para reaplicar la traducción.

```bash
omarchy update
bash omarchy-spanish.sh
```

## Archivos que modifica

| Archivo | Acción |
|---|---|
| `~/.config/omarchy/extensions/menu.sh` | Reemplaza con versión en español |
| `~/.config/omarchy/extensions/backups/` | Guarda backups con timestamp |

## Licencia

MIT
