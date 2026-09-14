# Arch Linux VM para VirtualBox (Edición AI Agents)

Máquina virtual oficial de Arch Linux configurada y empaquetada en formato `.ova` para uso educativo y desarrollo con agentes de IA.

## 🚀 Descarga
Puedes descargar el archivo `.ova` listo para importar en VirtualBox desde la web oficial o directamente desde GitHub Releases:

* 🌐 **Página Web / GitHub Pages**: [https://balejosg.github.io/archlinux-vm/](https://balejosg.github.io/archlinux-vm/)
* 📦 **Descarga directa (.ova, ~738 MB)**: [ArchLinux.ova (v1.1.0)](https://github.com/balejosg/archlinux-vm/releases/download/v1.1.0/ArchLinux.ova)

---

## 🔑 Credenciales y Configuración

| Parámetro | Valor |
| :--- | :--- |
| **Usuario** | `alumno` |
| **Contraseña** | `alumno` |
| **Permisos** | Administrador completo (`sudo`) |
| **Localización** | España (`es_ES.UTF-8`, zona horaria `Europe/Madrid`) |
| **Teclado** | Español (`KEYMAP=es`, distribución X11 `es`) |
| **SSH** | Habilitado (`sshd`) |
| **Port Forwarding SSH** | Puerto anfitrión `2222` ➡️ Puerto VM `22` |
| **Guest Additions** | `virtualbox-guest-utils` activo |

---

## 🤖 Herramientas de IA y Agentes preinstaladas

* **`antigravity-cli` (`agy`)**: CLI oficial de Google Antigravity.
* **`opencode`**: Entorno CLI y TUI para agentes de código.
* **`herdr`**: Multiplexor de terminales para agentes de IA (compatible y conectado con `antigravity-cli` y `opencode` mediante plugins de estado y skills).

---

## 📖 Instrucciones de instalación

1. Descarga el archivo `ArchLinux.ova`.
2. Abre **VirtualBox**.
3. Haz doble clic en el archivo descargado (o ve a **Archivo** > **Importar servicio virtualizado**).
4. Pulsa en **Importar**.
5. Inicia la máquina virtual.
6. Inicia sesión con `alumno` / `alumno` o conéctate por SSH:
   ```bash
   ssh -p 2222 alumno@127.0.0.1
   ```
