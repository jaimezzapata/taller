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

3. **Componentización y manejo de datos**:
   - El código debe estar dividido de forma clara y reutilizable (por ejemplo: `components/Header.jsx`, `components/Footer.jsx`, `components/Card.jsx`, `pages/...`, `data/...`).
   - En el proceso de componentización deben **crear la data, objetos o arreglos necesarios** (por ejemplo, en archivos `src/data/...`) para renderizar dinámicamente las *cards* y demás elementos repetitivos mediante `props` o `import/export` y `.map()`, evitando duplicar código JSX.

---

## Configuración Inicial de Git (Obligatoria antes de trabajar)

Si **no estás en tu PC personal**, asegúrate de limpiar credenciales anteriores y configurar tu identidad en Git antes de hacer commits o subir cambios:

1. **Limpiar credenciales guardadas (Windows, Git Bash y VS Code):**
   - **Administrador de credenciales de Windows:** Abre el *Panel de control > Cuentas de usuario > Administrador de credenciales > Credenciales de Windows* y elimina cualquier credencial previa relacionada con `git:` o `github.com`.
   - **Desde Git Bash / terminal:** Puedes limpiar la caché o desactivar el asistente de credenciales para evitar que use una cuenta anterior:
     ```bash
     git credential-manager delete https://github.com o git config --global credential.helper "". Ensayar con cual de las dos funciona
     ```
   - **En Visual Studio Code (VSC):** Si hay una sesión iniciada de otra persona, haz clic en el ícono de **Cuentas (perfil)** en la barra lateral inferior izquierda y selecciona **Cerrar sesión** (*Sign Out*) en GitHub antes de autenticar tu propia cuenta.
2. **Configurar tu nombre y correo de Git:**
   ```bash
   git config --global user.name "Tu Nombre Completo" o "Usaurio de GitHub"
   git config --global user.email "tu-correo@ejemplo.com"
   ```
3. **Verificar la configuración:**
   ```bash
   git config --list
   ```
   Con esto garantizas que tus commits y `push` queden registrados correctamente con tu cuenta.

---

## Flujo de Versionamiento en Git (Estricto)

Se evaluará el seguimiento ordenado del repositorio siguiendo exactamente estos pasos:

1. **Rama `master` (Proyecto base + `README.md` detallado):**
   - En tu proyecto base de React creado con Vite, el archivo `README.md` debe contener **tu información personal muy detallada** (nombre completo, documento, ficha, correos, teléfono, usuario de GitHub, diseño asignado y una breve presentación).
   - Todo esto se debe crear en la rama `master`, guardar (`git commit`) y **subir a GitHub** (`git push -u origin master`) antes de crear otras ramas.
   - **No** se debe subir el código de la migración directamente a `master`.

2. **Rama `develop` (Copia fiel — NO se modifica):**
   - Una vez guardado y subido `master` con tu `README.md` detallado, crea la rama `develop` como una **copia fiel de `master`** y súbela a GitHub:
     ```bash
     git checkout -b develop
     git push -u origin develop
     ```
   - **En `develop` NO se modifica nada**; debe quedar intacta como espejo de `master`.

3. **Rama `feature/<nombre>` (Desarrollo de la solución):**
   - Desde `develop`, crea una rama con el prefijo `feature/` más el nombre que quieras ponerle (por ejemplo `feature/migracion-memphis` o `feature/solucion-taller`):
     ```bash
     git checkout develop
     git checkout -b feature/nombre-que-quieras
     ```
   - Trabaja toda la migración en esta rama (o en ramas `feature/...` independientes si divides por partes) y **sube cada rama a GitHub** (`git push -u origin feature/nombre-que-quieras`).
   - **IMPORTANTE — NO hacer PR ni merge:** **No** realices Pull Request (PR) ni *merge* hacia `develop` ni hacia `master`. Todas las ramas (`master`, `develop` y `feature/...`) deben quedar **quietas e independientes** en GitHub para su revisión.

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

## Información del Estudiante (Plantilla para tu `README.md` en `master`)

> *(En tu proyecto base de React, completa estos datos de forma **muy detallada** en la rama `master`, haz commit y súbela a GitHub antes de crear `develop`)*

- **Nombre completo:**
- **Documento de identidad:**
- **Ficha:** 
- **Programa de formación:**  
- **Correo personal:** 
- **Usuario / Enlace de GitHub:** 
- **Diseño asignado:**
- **Sobre mí / Perfil:**


---

## Rúbrica de Evaluación (100 Puntos)

| Criterio | Peso | Excelente (100%) | Aceptable (60%) | Por mejorar (0–30%) |
|---|---:|---|---|---|
| **1. Stack y Fidelidad Visual** *(Vite + React + Tailwind)* | **20 pts** | Proyecto creado con Vite + React, Tailwind instalado como dependencia (sin CDN) y respeta fielmente el diseño asignado (colores planos sin degradados, header/footer fijos, secciones). | Usa Vite + React y Tailwind, pero presenta diferencias visuales notables, degradados o problemas de diseño. | No usa Vite + React, usa Tailwind por CDN o no corresponde al diseño asignado. |
| **2. Enrutamiento (React Router v6.4+)** | **20 pts** | Navegación 100% funcional con `React Router v6.4+` (`createBrowserRouter` / `RouterProvider`), sin recargas de página ni enlaces rotos. | La navegación funciona parcialmente o usa una versión/API anterior a v6.4. | No implementa enrutamiento o la navegación no funciona. |
| **3. Componentización y Data** | **25 pts** | Código modular en componentes reutilizables (`Header`, `Footer`, `Card`, `pages`, etc.) y uso de archivos de data (objetos/arreglos con `.map()` y `props`). | Componentiza algunas partes, pero deja bloques grandes sin separar o *hardcodea* las cards sin usar arreglos/objetos. | Todo el código está en un solo archivo (`App.jsx`) sin componentización ni manejo de data. |
| **4. Flujo Git y Convención de Commits** | **25 pts** | `master` solo con el proyecto base + `README.md` muy detallado; `develop` copia fiel intacta; desarrollo en rama `feature/...` independiente subida a GitHub (sin PR ni merge); commits con prefijos `docs:`, `chore:`, `feature:`. | Cumple la mayoría de ramas o commits, pero modificó `develop`, hizo merge/PR o faltaron prefijos en algunos commits. | No respeta la estructura de ramas, subió todo a `master` o no usó convención de commits. |
| **5. README Detallado y Entrega** | **10 pts** | `README.md` completo con toda la información personal detallada en `master` y repositorio enviado puntualmente al finalizar la jornada a `jzapata@sena.edu.co`. | Información personal incompleta en el `README.md` o entrega con observaciones menores. | No incluye datos personales en el `README.md` o no envió el repositorio al correo indicado. |
