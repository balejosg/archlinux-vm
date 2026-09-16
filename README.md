# Arch Linux VM para VirtualBox (Edición Especial DAM 1 - Tutor IA)

Máquina virtual oficial de Arch Linux configurada específicamente para el módulo de **Programación de 1º de DAM (Desarrollo de Aplicaciones Multiplataforma)**. Diseñada para trabajar de forma sincronizada con **IntelliJ IDEA** en el equipo anfitrión y actuar como un **tutor pedagógico de IA** que guía el aprendizaje sin resolver las tareas por el alumno.

## 🚀 Descarga
Puedes descargar el archivo `.ova` listo para importar en VirtualBox desde la web oficial o directamente desde GitHub Releases:

* 🌐 **Página Web / GitHub Pages**: [https://balejosg.github.io/archlinux-vm/](https://balejosg.github.io/archlinux-vm/)
* 📖 **Caso de Estudio (Cómo se hizo con IA)**: [https://balejosg.github.io/archlinux-vm/como-se-hizo.html](https://balejosg.github.io/archlinux-vm/como-se-hizo.html)
* 📦 **Descarga directa (.ova, ~1.7 GB)**: [ArchLinux.ova (v1.3.0)](https://github.com/balejosg/archlinux-vm/releases/download/v1.3.0/ArchLinux.ova)

---

## 🔑 Credenciales y Configuración

| Parámetro | Valor |
| :--- | :--- |
| **Usuario** | `alumno` |
| **Contraseña** | `alumno` |
| **Permisos** | Administrador completo (`sudo`) |
| **Java Toolchain** | **OpenJDK 21 LTS** (`java`, `javac`) y **Apache Maven 3.9** |
| **Herramientas de Análisis** | `ripgrep` (`rg`), `fd`, `tree` |
| **Carpeta compartida Host** | Preconfigurada en `/home/alumno/trabajo` |
| **Localización** | España (`es_ES.UTF-8`, zona horaria `Europe/Madrid`) |
| **Teclado** | Español (`KEYMAP=es`, distribución X11 `es`) |
| **SSH** | Habilitado (`sshd`) en puerto anfitrión `2222` |
| **Guest Additions** | `virtualbox-guest-utils` activo |

---

## 🎓 Entorno Pedagógico DAM 1

### 1. Rol de "Tutor Socrático" Preconfigurado
Los agentes (`agy` y `opencode`) vienen preconfigurados con directrices docentes obligatorias (`AGENTS.md`):
* **No hacen la tarea por el alumno:** Proporcionan pistas progresivas y preguntas guía para estimular el razonamiento algorítmico.
* **Explicación didáctica de excepciones:** Desglosan errores comunes de Java (`NullPointerException`, `IndexOutOfBoundsException`, fallos de compilación) explicando el "por qué" y cómo evitarlos.
* **Estándares de Código DAM:** Exigen buenas prácticas de POO (atributos privados, `getters`/`setters`, convenciones Java, Javadoc).
* **Adaptación al temario:** Priorizan algoritmos tradicionales antes que abstracciones complejas.

### 2. Estructura de Contexto en `~/trabajo`
```text
~/trabajo/
├── proyectos/             <-- Proyectos desarrollados con IntelliJ IDEA en el host
├── examenes-anteriores/   <-- Enunciados y exámenes de cursos previos para dar contexto al agente
├── apuntes/               <-- Guías y teoría en PDF o Markdown
├── CRITERIOS_EVALUACION.md<-- Criterios y rúbricas docentes leídos por el agente
├── AGENTS.md              <-- Reglas del rol pedagógico del agente
└── LEEME.txt              <-- Resumen de uso rápido para el alumno
```

---

## 📁 Cómo vincular tu carpeta local de trabajo

1. En VirtualBox: **Dispositivos ➡️ Carpetas compartidas ➡️ Preferencias...**
2. Añade (+) tu carpeta local (donde guardas tus proyectos de IntelliJ).
3. Nombre de la carpeta: **`trabajo`**
4. Marca: **Automontar** y **Hacer permanente**.
5. Al arrancar la VM se montará sola en `~/trabajo` (o escribe `montar-trabajo` en la terminal).

---

## 💡 ¿Cómo se creó esta máquina y este proyecto con un Agente?

Todo este proyecto (la descarga de la imagen oficial, la configuración de la VM, la web en GitHub Pages, la release y el rol pedagógico) fue generado íntegramente mediante una conversación en lenguaje natural con un agente de IA.

Puedes ver la transcripción real y las instrucciones paso a paso para reproducirlo desde cualquier Linux aquí:
👉 **[Ver el Caso de Estudio Completo](https://balejosg.github.io/archlinux-vm/como-se-hizo.html)**

### Resumen rápido para reproducirlo:
1. **En tu Linux (Host)**: Asegúrate de tener instalado `virtualbox` y `git`.
2. **Elige tu agente**:
   * **Opción A (Antigravity CLI)**: `paru -S antigravity-cli` y ejecuta `agy`.
   * **Opción B (OpenCode - 100% Libre y Gratuito)**: `curl -fsSL https://opencode.ai/install | bash` y ejecuta `opencode`.
3. **Pega la primera petición**:
   > *«quiero que me prepares una vm con arch para Virtualbox. Debe tener un usuario de tipo sudo y un servidor ssh. el usuario será alumno:alumno»*
