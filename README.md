# kit

Instalador de la terminal para los workshops de Claude Code de **Datricas**.

Este repositorio es público a propósito: contiene **solo el arranque**, que no tiene
nada sensible. Instala lo mínimo (Homebrew o WSL2, `git`, `gh`), autentica contra
GitHub y de ahí clona el kit completo, que es privado.

## Uso

**macOS**
```bash
bash <(curl -fsSL https://datricas.github.io/kit/mac)
```

**Windows** — PowerShell como administrador
```powershell
irm https://datricas.github.io/kit/win | iex
```

Si eso falla, `win.txt` es el mismo script servido como `text/plain`:

```powershell
irm https://datricas.github.io/kit/win.txt | iex
```

**Modo chequeo** (no toca nada):

```powershell
$env:FSPRINT_CHECK=1; irm https://datricas.github.io/kit/win | iex
```

Se usa una variable de entorno y no un parametro porque a un script traido
con `irm | iex` no se le pueden pasar parametros de forma confiable.

**Linux / WSL** (lo invoca el de Windows, no hace falta correrlo a mano)
```bash
bash <(curl -fsSL https://datricas.github.io/kit/linux)
```

## Qué hay acá

| Archivo | Qué es |
|---|---|
| `mac` | Arranque para macOS |
| `win` | Arranque para Windows: instala WSL2 y llama a `linux` |
| `linux` | Arranque para Linux y WSL |
| `index.html` | La página con los dos comandos |

El instalador de verdad vive en `datricas/fsprint-claude-kit` (privado).

## Desinstalar

Deja la máquina como estaba: restaura las configuraciones que había y borra
todo lo que agregó el kit.

**macOS · Linux · WSL**
```bash
bash <(curl -fsSL https://datricas.github.io/kit/desinstalar)
```

Por defecto no toca herramientas de uso general (git, node, tmux, Homebrew,
Oh My Zsh) porque pueden estar en uso por otras cosas. Para sacar también eso:

```bash
bash <(curl -fsSL https://datricas.github.io/kit/desinstalar) --todo
```

**Windows** — para sacar Ubuntu y WSL, en PowerShell como administrador:
```powershell
irm https://datricas.github.io/kit/desinstalar-win | iex
```
