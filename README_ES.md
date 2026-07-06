<h1 align="center">Open Interpreter</h1>

<p align="center">Un agente de programación para modelos de bajo costo.</p>

<p align="center">
  <a href="README.md">English</a> • <b>Español</b>
</p>

<p align="center">
  <a href="https://discord.gg/Hvz9Axh84z"><img alt="Discord" src="https://img.shields.io/discord/1146610656779440188?style=flat-square&label=Discord" /></a>
  <a href="https://www.openinterpreter.com/docs/terminal"><img alt="Documentación" src="https://img.shields.io/badge/Documentation-white?style=flat-square" /></a>
  <a href="LICENSE"><img alt="Licencia" src="https://img.shields.io/badge/License-Apache--2.0-white?style=flat-square" /></a>
</p>

<p align="center">
  <a href="https://www.openinterpreter.com/docs/terminal">
    <img alt="Un primer plano de la pantalla de una computadora portátil ejecutando un agente de terminal" src="https://www.openinterpreter.com/blog/open-interpreter-1-0/blog-hero-1.jpg" width="720" />
  </a>
</p>

> [!NOTE]
> Esta es la nueva versión en Rust de Open Interpreter. ¿Buscas el proyecto original en Python? Continúa como una bifurcación mantenida por la comunidad en [endolith/open-interpreter](https://github.com/endolith/open-interpreter).

> [!TIP]
> **Nuevo: GLM-5.2 con emulación ZCode.** Open Interpreter ahora incluye un arnés `zcode` nativo de Rust para GLM-5.2, diseñado para brindar a GLM su mejor flujo de trabajo de agente de programación directamente en tu terminal.

### Instalación

macOS y Linux:

```bash
curl -fsSL https://www.openinterpreter.com/install | sh
```

Windows:

```powershell
irm https://www.openinterpreter.com/install.ps1 | iex
```

Luego escribe `i` o `interpreter` en tu terminal para iniciar una sesión.

### Emulación de arnés

Open Interpreter es una bifurcación (fork) de Codex de OpenAI, con un enfoque en emular el arnés del agente que obtiene el mejor rendimiento de modelos de bajo costo.

Usa `/harness` para cambiar el arnés activo:

```text
> /harness

native
claude-code
claude-code-bare
zcode
kimi-cli
qwen-code
deepseek-tui
swe-agent
minimal
```

Lee más en la [documentación del arnés](https://www.openinterpreter.com/docs/terminal/harness) y en la [documentación de proveedores de modelos](https://www.openinterpreter.com/docs/terminal/providers).

### Uso de computadora

Open Interpreter incluye una habilidad de control de calidad (QA skill) que permite a cualquier modelo operar y probar interfaces. Puede controlar aplicaciones web en un navegador real con [agent-browser](https://github.com/vercel-labs/agent-browser), o bien operar y probar aplicaciones nativas con [trycua](https://github.com/trycua/cua).

### Características

- Ejecuta comandos dentro de un entorno aislado (sandboxing) nativo en macOS, Linux y Windows.
- Cambia proveedores y modelos desde la interfaz de usuario de terminal (TUI) con `/model`.
- Inspecciona o cambia arneses de modelos nativos de Rust con `/harness`.
- Prueba aplicaciones web y nativas a través de la habilidad de QA integrada.
- Se ejecuta como un agente del [Protocolo de Cliente de Agente](https://agentclientprotocol.com/) (ACP) para editores con `interpreter acp`.
- Mantiene la configuración y el estado de la sesión localmente bajo `~/.openinterpreter`.
- Soporta `exec`, MCP, habilidades, hooks (ganchos), permisos y `AGENTS.md`.

### Documentación

- [Docs de la Terminal](https://www.openinterpreter.com/docs/terminal)
- [Guía de inicio rápido](https://www.openinterpreter.com/docs/terminal/quickstart)
- [Guía de instalación](https://www.openinterpreter.com/docs/terminal/install)
- [Configuración](https://www.openinterpreter.com/docs/terminal/config)
- [Referencia de CLI](https://www.openinterpreter.com/docs/terminal/cli-reference)
- [Arneses](https://www.openinterpreter.com/docs/terminal/harness)
- [Proveedores de modelos](https://www.openinterpreter.com/docs/terminal/providers)
- [Aislamiento y aprobaciones](https://www.openinterpreter.com/docs/terminal/sandbox)

### Licencia

Apache-2.0
