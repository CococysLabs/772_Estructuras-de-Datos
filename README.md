# 772_Estructuras-de-Datos_Ejemplos
Contenido, ejemplos y recursos del curso de Estructuras de Datos (EDD).

## 📁 Contenido

Cada ciclo contiene el material del curso organizado según la estructura original del profesor/catedrático.

| Ciclo | Estado |
| --- | --- |
| [Ciclo-2024-Primer-Semestre](Ciclo-2024-Primer-Semestre) | Archivado |
| [Ciclo-2024-Segundo-Semestre](Ciclo-2024-Segundo-Semestre) | Archivado |
| [Ciclo-2025-Primer-Semestre](Ciclo-2025-Primer-Semestre) | Archivado |
| [Ciclo-2025-Segundo-Semestre](Ciclo-2025-Segundo-Semestre) | Archivado |
| [Ciclo-2026-Primer-Semestre](Ciclo-2026-Primer-Semestre) | Restringido |
| [Ciclo-2026-Segundo-Semestre](Ciclo-2026-Segundo-Semestre) | En curso |

## 📥 Clonar

Esta sección es únicamente para descargar el contenido de un ciclo específico sin traer el repositorio completo.

```bash
git clone --filter=blob:none --sparse https://github.com/CococysLabs/772_Estructuras-de-Datos_Ejemplos.git nombre-carpeta
cd nombre-carpeta
git sparse-checkout set Ciclo-xxxx-xxxx-Semestre
```

Donde:

- `nombre-carpeta` es el nombre que tendrá la carpeta descargada en tu computadora.
- `Ciclo-xxxx-xxxx-Semestre` es el ciclo específico que deseas descargar (por ejemplo, `Ciclo-2025-Primer-Semestre`).

---

## 📌 Guía de Trabajo para Tutores Auxiliares

¡Bienvenido/a al equipo de tutores! Para garantizar el correcto orden del material, este repositorio utiliza restricciones por directorio mediante el archivo `CODEOWNERS` y permisos asignados al **Team de Tutores**.

### 🚨 Políticas de Permisos y Edición

1. **Pertenencia al Team:** Eres parte del equipo asignado a este repositorio con permisos para subir cambios a la carpeta del ciclo vigente ubicada en la rama `main`.
2. **Restricción de Rutas:** El archivo `.github/CODEOWNERS` protege los ciclos anteriores y otras carpetas del curso. **Únicamente se te permitirá hacer push o cambios sobre la carpeta correspondiente al ciclo actual.**
3. **Descarga Selectiva:** Para evitar descargar carpetas pesadas de ciclos pasados, es **obligatorio** utilizar el flujo de *sparse-checkout* detallado a continuación.

### 🚀 Flujo de Trabajo Paso a Paso

1. Sigue esta secuencia exacta de comandos en tu terminal para descargar exclusivamente la carpeta de trabajo asignada:

    ```bash
    # 1. Clonar el repositorio sin descargar archivos completos
    git clone --no-checkout https://github.com/CococysLabs/772_Estructuras-de-Datos_Ejemplos.git

    cd 772_Estructuras-de-Datos_Ejemplos

    # 2. Habilitar sparse-checkout en modo cono
    git sparse-checkout init --cone

    # 3. Indicar únicamente la carpeta que necesita trabajar el tutor
    git sparse-checkout set Ciclo-2026-Segundo-Semestre/Ejemplos

    # 4. Descargar solo esa carpeta en la rama main
    git checkout main
    ```

2. Agrega tus códigos de ejemplo, guías o material didáctico dentro de la carpeta descargada:

    `Ciclo-2026-Segundo-Semestre/Ejemplos/`

3. Guarda tus cambios localmente creando un commit explicativo:

    ```bash
    git add .
    git commit -m "feat: agregar ejemplo de [DESCRIPCION] para el ciclo 2026-Segundo-Semestre"
    ```

4. Envía tus cambios directamente a la rama principal:

    ```bash
    git push origin main
    ```

    > **Nota:** Si por error intentas modificar o eliminar archivos fuera de la carpeta `Ciclo-2026-Segundo-Semestre/Ejemplos`, la plataforma rechazará el `push` debido a las reglas de propiedad configuradas en `CODEOWNERS`.

---

## 📁 Estructura del Repositorio

```text
772_Estructuras-de-Datos_Ejemplos/
├── .github/
│   └── CODEOWNERS                       <-- Configuración de permisos
├── Ciclo-2024-Primer-Semestre/          <-- Protegido por CODEOWNERS
├── Ciclo-2024-Segundo-Semestre/         <-- Protegido por CODEOWNERS
├── Ciclo-2025-Primer-Semestre/          <-- Protegido por CODEOWNERS
├── Ciclo-2025-Segundo-Semestre/         <-- Protegido por CODEOWNERS
├── Ciclo-2026-Primer-Semestre/          <-- Protegido por CODEOWNERS
└── Ciclo-2026-Segundo-Semestre/
    └── Ejemplos/                        <-- 🎯 Tu carpeta de trabajo asignada
        └── .gitkeep
```

## 📧 Contacto

- Email: computacion.cococys@gmail.com
- Organización: [CococysLabs](https://github.com/CococysLabs)
