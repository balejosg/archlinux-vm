# Arch Linux VM para VirtualBox

Máquina virtual oficial de Arch Linux configurada y empaquetada en formato `.ova` para uso educativo.

## 🚀 Descarga
Puedes descargar el archivo `.ova` listo para importar en VirtualBox desde la página web o directamente desde Releases:

* 🌐 **Página Web / GitHub Pages**: [https://balejosg.github.io/archlinux-vm/](https://balejosg.github.io/archlinux-vm/)
* 📦 **Descarga directa (.ova, ~599 MB)**: [ArchLinux.ova](https://github.com/balejosg/archlinux-vm/releases/download/v1.0.0/ArchLinux.ova)

---

## 🔑 Credenciales y Configuración

| Parámetro | Valor |
| :--- | :--- |
| **Usuario** | `alumno` |
| **Contraseña** | `alumno` |
| **Permisos** | Administrador completo (`sudo`) |
| **SSH** | Habilitado (`sshd`) |
| **Port Forwarding SSH** | Puerto anfitrión `2222` ➡️ Puerto VM `22` |
| **Guest Additions** | `virtualbox-guest-utils` preinstalado |
| **Disco** | 40 GB dinámico |
| **RAM recomendada** | 2048 MB (2 GB) |

---

## 📖 Instrucciones de instalación

1. Descarga el archivo `ArchLinux.ova`.
2. Abre **VirtualBox**.
3. Haz doble clic en el archivo descargado (o ve a **Archivo** > **Importar servicio virtualizado** en VirtualBox).
4. Pulsa en **Importar**.
5. Inicia la máquina virtual.
6. Inicia sesión con `alumno` / `alumno`.
