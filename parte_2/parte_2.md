# Parte 2. Comprensión del flujo colaborativo

## 1. Flujo colaborativo

### Planteamiento
Supón que quieres colaborar con el repositorio de otro desarrollador. Ordena y explica los siguientes elementos: Push, Fork, Pull Request, Clone, Merge, Commit, Review, Branch y Modificar archivos. Agrega cualquier operación que consideres necesaria.

### Mi respuesta
El flujo normal seria asi:

1. Fork: crear una copia del repositorio original en mi cuenta de GitHub.
2. Clone: bajar esa copia a mi computadora.
3. Branch: crear una rama para trabajar sin dañar la rama principal.
4. Modificar archivos: hacer cambios en el proyecto.
5. Commit: guardar los cambios con un mensaje descriptivo.
6. Push: subir la rama a mi fork.
7. Pull Request: pedir que revisen los cambios.
8. Review: el dueño del proyecto revisa el codigo.
9. Merge: si todo esta bien, integrar esos cambios al repositorio principal.
10. Sync Fork: actualizar mi fork si el repositorio original tuvo cambios nuevos.

### Explicación
Este flujo sirve para que varias personas trabajen al mismo tiempo sin romper el proyecto. Cada uno hace cambios en su propia rama y luego pide que revisen su trabajo. Cuando se aprueba, los cambios se juntan al proyecto principal.

## 2. Fork y Clone

### Planteamiento
Analiza la afirmación: “Clone crea una copia del proyecto dentro de mi cuenta de GitHub”. Indica si es correcta y explica la diferencia entre Fork y Clone.

### Mi respuesta
No, esa afirmacion no es correcta. Clone no crea una copia dentro de mi cuenta de GitHub, sino que descarga una copia del repositorio a mi computadora.

### Explicación
Fork es una copia del repositorio en GitHub, dentro de mi cuenta personal. Clone es cuando yo descargo esa copia a mi equipo para trabajar. En pocas palabras, fork se hace en GitHub y clone se hace localmente.

## 3. Pull Request

### Planteamiento
Supón que realizaste Fork, Clone, Branch, Modificar, Commit y Push. Responde: ¿los cambios ya forman parte del repositorio original? ¿Qué debe ocurrir para incorporarlos?

### Mi respuesta
No, esos cambios aun no forman parte del repositorio original. Solo estan en mi fork y en mi rama.

### Explicación
Para que el proyecto original los acepte, tengo que abrir un Pull Request desde mi rama hacia la rama principal del repositorio original. Ahí el dueño del proyecto revisa y si aprueba hace el Merge. Solo entonces los cambios pasan a formar parte del repositorio principal.

## 4. Request Changes

### Planteamiento
El propietario revisa tu Pull Request y selecciona Request Changes. Explica qué debes hacer, si necesitas crear otro Pull Request y qué ocurre cuando realizas nuevamente push.

### Mi respuesta
Debo corregir los cambios que me pidieron, hacer nuevos commits en la misma rama y hacer push otra vez.

### Explicación
Cuando se usa Request Changes, el PR aun no se acepta. Yo tengo que arreglar lo que dijo el propietario y volver a subir los cambios. El Pull Request se actualiza automaticamente con ese nuevo push. No siempre hace falta crear otro PR si sigo trabajando en la misma rama.

## 5. Merge y repositorio local

### Planteamiento
Un Pull Request fue aceptado y se realizó Merge en GitHub. Sin embargo, el repositorio local del propietario no contiene los cambios. Explica por qué sucede y qué operación debe realizarse.

### Mi respuesta
Porque el merge se hizo en GitHub y no en el equipo local. El historial local sigue viejo.

### Explicación
Para actualizar el repositorio local, el propietario tiene que hacer git fetch y luego git pull o git pull origin main. Eso trae los cambios del repositorio remoto a su computadora.

## 6. Sync Fork

### Planteamiento
Tu Fork fue creado varios días atrás y el repositorio original recibió nuevos commits. Explica qué herramienta utilizarías, qué repositorio se actualiza y qué diferencia existe entre Sync Fork y git pull.

### Mi respuesta
Yo usaría Sync Fork en GitHub para actualizar mi fork con los cambios del repositorio original.

### Explicación
Lo que se actualiza es mi fork, no el repositorio principal. El repositorio original no cambia por mi accion, solo sus colaboradores hacen pushes. La diferencia es que Sync Fork se hace en GitHub y git pull se hace en la computadora para traer los cambios del remoto al proyecto local.
