# Parte 3. Interpretación de comandos

## 1. Analiza

### Planteamiento
```bash
git status
git add README.md
git commit -m "Actualiza documentación"
git push
```

### Mi respuesta
- git status: muestra el estado del repositorio y dice que archivos estan cambiados.
- git add README.md: agrega el archivo README.md a la etapa de preparacion.
- git commit -m "Actualiza documentación": guarda los cambios con un mensaje descriptivo.
- git push: sube esos cambios a GitHub.

### Explicación
Git status sirve para ver que esta pasando en el proyecto. git add prepara los archivos que se quieren guardar. git commit crea un punto de guardado en el historial. git push publica esos cambios en el repositorio remoto para que todos los puedan ver.

## 2. Identifica qué falta

### Caso A
```bash
Modificar archivo
↓
git add .
↓
?
↓
git push
```

### Mi respuesta
Falta hacer git commit -m "mensaje".

### Explicación
Primero se preparan los archivos con git add ., pero eso no guarda el cambio. Para guardar el cambio hay que hacer commit y despues ya se puede hacer push.

### Caso B
```bash
Repositorio GitHub
↓
?
↓
Repositorio local
```

### Mi respuesta
Se usa git clone URL_del_repositorio.

### Explicación
Con git clone yo descargo una copia del repositorio remoto a mi computadora para poder trabajar en ella.

### Caso C
```bash
Repositorio remoto actualizado
↓
?
↓
Repositorio local actualizado
```

### Mi respuesta
Se usa git pull.

### Explicación
git pull trae los cambios que ya existian en GitHub y los actualiza en el repositorio local para que quede sincronizado.
