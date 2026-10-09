# Parte 4. Conceptos

## 1. Explica la diferencia entre Git y GitHub.

### Respuesta
Git es un sistema de control de versiones distribuido que permite registrar el historial de cambios de un proyecto en tu computadora. GitHub es una plataforma en línea que aloja repositorios Git y facilita la colaboración, revisión y publicación del código.

### Explicación
Git se utiliza localmente para versionar y gestionar cambios. GitHub se usa como servicio remoto para compartir proyectos, trabajar en equipo, revisar pull requests y mantener repositorios accesibles desde Internet.

## 2. Explica para qué sirve .gitignore.

### Respuesta
`.gitignore` sirve para indicar a Git qué archivos o carpetas no deben seguirse ni subirse al repositorio.

### Explicación
Esto es útil para excluir archivos temporales, carpetas de entorno virtual, archivos compilados, credenciales o datos locales que no deberían publicarse. En este proyecto, por ejemplo, se excluye `.venv/` porque es local y puede recrearse fácilmente.

## 3. Explica por qué .venv no debe almacenarse normalmente en GitHub.

### Respuesta
Porque `.venv` contiene un entorno virtual local con dependencias instaladas y configuraciones específicas del equipo.

### Explicación
Cada persona puede tener una versión diferente de Python, paquetes y librerías. Mantener `.venv` en GitHub aumenta el tamaño del repositorio, genera archivos redundantes y puede causar conflictos entre entornos. Por eso se debe excluir con `.gitignore` y regenerarse con `requirements.txt`.

## 4. Explica para qué sirve requirements.txt.

### Respuesta
`requirements.txt` sirve para registrar las dependencias del proyecto y sus versiones.

### Explicación
Permite que otra persona pueda instalar exactamente lo necesario ejecutando `pip install -r requirements.txt`. Esto hace que el entorno sea reproducible y facilita la colaboración y el despliegue.

## 5. Explica la diferencia entre Stage, Commit y Push.

### Respuesta
- Stage: prepara archivos para ser incluidos en el siguiente commit.
- Commit: guarda una instantánea del proyecto con un mensaje descriptivo.
- Push: envía los commits locales al repositorio remoto en GitHub.

### Explicación
El flujo típico es: editar archivos → `git add` (stage) → `git commit` (guardar cambios localmente) → `git push` (publicar en GitHub). Cada paso cumple una función distinta en el flujo de versionado.

## 6. Explica por qué un repositorio puede tener varios commits antes de realizar un push.

### Respuesta
Porque mientras un desarrollador trabaja, puede hacer varios cambios y guardar cada uno como un commit antes de decidir publicarlos en GitHub.

### Explicación
Los commits representan puntos de guardado del historial local. Es normal hacer varios commits para documentar avances, corregir errores o agrupar cambios antes de subirlos al remoto. El push solo publica ese conjunto de commits hacia GitHub en el momento que se decide.
