# Taller: Migración de Diseño Web a React + Vite

> **IMPORTANTE — LEER ANTES DE EMPEZAR:**
> - **Trabajo individual:** Este taller debe realizarse de manera **100% individual**.
> - **Lectura previa obligatoria:** Lee completamente este `README.md` antes de iniciar, ya que aquí se encuentran todas las instrucciones de trabajo, arquitectura y control de versiones.
> - **Entrega:** El repositorio con la solución debe enviarse **finalizando la jornada** al correo SENA: **jzapata@sena.edu.co**.

## Objetivo
Migrar el diseño HTML/Tailwind asignado (**Memphis**, **Pop Art** o **Brutalismo**) a una aplicación moderna en **React**, aplicando buenas prácticas de componentización, enrutamiento y control de versiones estricto en Git.

---

## Requisitos Técnicos

1. **Stack obligatorio**:
   - El proyecto debe crearse **únicamente** utilizando **Vite + React** (`npm create vite@latest`).
   - Mantener Tailwind CSS (como dependencia, nada de CDN) y la fidelidad visual del diseño asignado (colores planos, sin degradados, header y footer fijos, y estructura visual).

2. **Enrutamiento (React Router v6.4+)**:
   - La navegación entre secciones/vistas debe ser completamente funcional utilizando **React Router versión 6.4 o superior** (ej. `createBrowserRouter` + `RouterProvider`).
   - Los enlaces del `Header` y botones de navegación deben funcionar correctamente sin recargar la página.

3. **Componentización**:
   - El código debe estar dividido de forma clara y reutilizable (por ejemplo: `components/Header.jsx`, `components/Footer.jsx`, `components/Card.jsx`, `pages/...`).

---

## Configuración Inicial de Git (Obligatoria antes de trabajar)

Si **no estás en tu PC personal**, asegúrate de limpiar credenciales anteriores y configurar tu identidad en Git antes de hacer commits o subir cambios:

1. **Limpiar credenciales guardadas (Windows, Git Bash y VS Code):**
   - **Administrador de credenciales de Windows:** Abre el *Panel de control > Cuentas de usuario > Administrador de credenciales > Credenciales de Windows* y elimina cualquier credencial previa relacionada con `git:` o `github.com`.
   - **Desde Git Bash / terminal:** Puedes limpiar la caché o desactivar el asistente de credenciales para evitar que use una cuenta anterior:
     ```bash
     git credential-manager delete https://github.com
     git config --global credential.helper ""
     ```
   - **En Visual Studio Code (VSC):** Si hay una sesión iniciada de otra persona, haz clic en el ícono de **Cuentas (perfil)** en la barra lateral inferior izquierda y selecciona **Cerrar sesión** (*Sign Out*) en GitHub antes de autenticar tu propia cuenta.
2. **Configurar tu nombre y correo de Git:**
   ```bash
   git config --global user.name "Tu Nombre Completo"
   git config --global user.email "tu-correo@ejemplo.com"
   ```
3. **Verificar la configuración:**
   ```bash
   git config --list
   ```
   Con esto garantizas que tus commits y `push` queden registrados correctamente con tu cuenta.

---

## Flujo de Versionamiento en Git (Estricto)

Se evaluará el seguimiento ordenado del repositorio siguiendo estas reglas:

1. **Rama `master`**:
   - Debe contener **únicamente** el archivo `README.md` con la **información personal** de cada integrante (nombre completo, código/identificación, correo y diseño asignado).
   - **No** se debe subir código fuente del proyecto directamente a `master`.

2. **Rama `develop`**:
   - Una vez configurado `master` con el `README.md`, se debe crear la rama `develop` como una **copia fiel de `master`**:
     ```bash
     git checkout -b develop
     ```

3. **Ramas por cada funcionalidad o actualización**:
   - Por cada nueva característica, componente, configuración o actualización, se debe crear una rama **desde `develop`**:
     ```bash
     git checkout develop
     git checkout -b feature/nombre-de-la-funcionalidad
     ```
   - Al finalizar cada tarea, integrar los cambios nuevamente hacia `develop`.

---

## Convención de Commits

Todos los commits deben utilizar uno de los siguientes prefijos según el tipo de cambio:

- **`docs:`** Cambios en documentación o en el `README.md`.
  - *Ejemplo:* `docs: agregar información personal en README`
- **`chore:`** Configuración inicial, instalación de dependencias, ajustes de Vite/Tailwind o mantenimiento.
  - *Ejemplo:* `chore: inicializar proyecto con vite, react y tailwind`
- **`feature:`** Implementación de componentes, rutas, vistas o nuevas funcionalidades.
  - *Ejemplo:* `feature: implementar enrutador con react-router v6.4`
  - *Ejemplo:* `feature: crear componentes Header y Footer fijos`

---

## Tabla de Asignación de Ejercicios

Busca tu **número de documento** para conocer el diseño que te corresponde migrar a React + Vite:

| N° | Documento | Diseño Asignado | Archivo Base |
|---:|-----------|-----------------|--------------|
| 1 | `1020106633` | Memphis (Centro Médico) | `memphis.html` |
| 2 | `1147934543` | Pop Art (Festival BOOM!) | `popart.html` |
| 3 | `1079359161` | Brutalismo (Monolito Arq) | `brutalismo.html` |
| 4 | `1000754763` | Memphis (Centro Médico) | `memphis.html` |
| 5 | `1027807516` | Pop Art (Festival BOOM!) | `popart.html` |
| 6 | `1025653094` | Brutalismo (Monolito Arq) | `brutalismo.html` |
| 7 | `1025885618` | Memphis (Centro Médico) | `memphis.html` |
| 8 | `1023593393` | Pop Art (Festival BOOM!) | `popart.html` |
| 9 | `1031941416` | Brutalismo (Monolito Arq) | `brutalismo.html` |
| 10 | `1020457824` | Memphis (Centro Médico) | `memphis.html` |
| 11 | `1052838240` | Pop Art (Festival BOOM!) | `popart.html` |
| 12 | `1129806057` | Brutalismo (Monolito Arq) | `brutalismo.html` |
| 13 | `1152450955` | Memphis (Centro Médico) | `memphis.html` |
| 14 | `1023527752` | Pop Art (Festival BOOM!) | `popart.html` |
| 15 | `1015074323` | Brutalismo (Monolito Arq) | `brutalismo.html` |
| 16 | `1025655679` | Memphis (Centro Médico) | `memphis.html` |
| 17 | `1035520611` | Pop Art (Festival BOOM!) | `popart.html` |

---

## Información del Estudiante

> *(Completar en la rama `master` antes de crear `develop`)*

- **Nombre completo:** 
- **Documento / Código:** 
- **Correo:** 
- **Diseño asignado:** *(Memphis / Pop Art / Brutalismo)*
