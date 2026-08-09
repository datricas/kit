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
