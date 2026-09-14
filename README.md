# Arch Linux VM para VirtualBox (Edición AI Agents + Workspace)

Máquina virtual oficial de Arch Linux configurada y empaquetada en formato `.ova` para uso educativo, desarrollo con agentes de IA y carpetas compartidas con el equipo anfitrión.

## 🚀 Descarga
Puedes descargar el archivo `.ova` listo para importar en VirtualBox desde la web oficial o directamente desde GitHub Releases:

* 🌐 **Página Web / GitHub Pages**: [https://balejosg.github.io/archlinux-vm/](https://balejosg.github.io/archlinux-vm/)
* 📦 **Descarga directa (.ova, ~1 GB)**: [ArchLinux.ova (v1.2.0)](https://github.com/balejosg/archlinux-vm/releases/download/v1.2.0/ArchLinux.ova)

---

## 🔑 Credenciales y Configuración

| Parámetro | Valor |
| :--- | :--- |
| **Usuario** | `alumno` |
| **Contraseña** | `alumno` |
| **Permisos** | Administrador completo (`sudo`) |
| **Carpeta compartida Host** | Preconfigurada en `/home/alumno/trabajo` |
| **Localización** | España (`es_ES.UTF-8`, zona horaria `Europe/Madrid`) |
| **Teclado** | Español (`KEYMAP=es`, distribución X11 `es`) |
| **SSH** | Habilitado (`sshd`) |
| **Port Forwarding SSH** | Puerto anfitrión `2222` ➡️ Puerto VM `22` |
| **Guest Additions** | `virtualbox-guest-utils` activo |

---

## 📁 Carpeta Compartida con el Anfitrión (`~/trabajo`)

La máquina ya viene preparada para vincular cualquier carpeta de tu ordenador real (Windows, Mac o Linux) directamente en la `$HOME` del alumno:

1. En la ventana de VirtualBox, ve al menú superior:  
   **Dispositivos** ➡️ **Carpetas compartidas** ➡️ **Preferencias de carpetas compartidas...**
2. Pulsa en el botón **Añadir carpeta (+)**:
   * **Ruta de la carpeta**: Selecciona cualquier carpeta de tu ordenador (por ejemplo, una carpeta en tu Escritorio).
   * **Nombre de la carpeta**: Escribe **`trabajo`** (en minúsculas).
   * Marca las casillas **Automontar** y **Hacer permanente**.
3. Pulsa **Aceptar**.

> Al arrancar la máquina virtual, la carpeta se montará automáticamente en `/home/alumno/trabajo`.  
> Si la añades con la máquina ya encendida, solo ejecuta en la terminal:
> ```bash
> montar-trabajo
> ```

---

## 🤖 Herramientas de IA y Agentes preinstaladas

* **`antigravity-cli` (`agy`)**: CLI oficial de Google Antigravity.
* **`opencode`**: Entorno CLI y TUI para agentes de código autónomos.
* **`herdr`**: Multiplexor de terminales para agentes de IA (con plugins de estado y skills instalados para `antigravity-cli` y `opencode`).

---

## 📖 Instrucciones de instalación

1. Descarga el archivo `ArchLinux.ova`.
2. Abre **VirtualBox** y haz doble clic en el archivo descargado.
3. Deja los valores por defecto y pulsa **Importar**.
4. Inicia la máquina virtual.
5. Inicia sesión con `alumno` / `alumno` o conéctate por SSH:
   ```bash
   ssh -p 2222 alumno@127.0.0.1
   ```
