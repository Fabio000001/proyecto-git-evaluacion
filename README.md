### 1. Cuestionario teórico
1. **¿Qué problema resuelve un sistema de control de versiones?**

Permite gestionar y registrar los cambios realizados en archivos a lo largo del tiempo, facilitando la recuperación de versiones anteriores y el trabajo colaborativo sin pérdida de información.
2. **Diferencia entre:**
    - Control de versiones local
    - Centralizado
    - Distribuido
El control local guarda el historial únicamente en la computadora del usuario; el centralizado utiliza un servidor único que almacena el repositorio principal; el distribuido permite que cada usuario tenga una copia completa del repositorio con todo su historial.
3. **¿Por qué Git es considerado un sistema distribuido?**
Porque cada clon del repositorio contiene todo el historial y permite trabajar de forma independiente, incluso sin conexión a internet.
4. **¿Qué significa que Git trabaje con instantáneas y no con diferencias de archivos?**
Significa que Git guarda una imagen completa del estado de los archivos en cada commit, en lugar de almacenar solo los cambios entre versiones.
5. **Ventajas principales de Git frente a otros sistemas de control de versiones**
Git es rápido, permite trabajar sin conexión, ofrece mayor seguridad del historial y facilita el manejo de ramas y fusiones.
### 2. Creación del proyecto
**Explica brevemente: Al ejecutar el comando git init ¿Qué carpeta oculta aparece? ¿Para qué sirve?**
Al ejecutar el comando git init se crea una carpeta oculta llamada .git, la cual sirve para almacenar toda la información interna que Git necesita para gestionar el repositorio, como el historial de cambios, las ramas, la configuración, el área de preparación (staging) y los punteros a los commits; esta carpeta es esencial, ya que sin ella el proyecto dejaría de ser un repositorio Git.
### 3. Estados de los archivos
**Clasifica cada archivo según su estado:**
- No rastreado
- Preparado
- Confirmado
README.md (No rastreado)
notas.txt (No rastreado)
### 4. Área de preparación (staging area)
**Explica: ¿Qué archivos están en staging? ¿Cuál no?**
En el área de preparación (staging) está el archivo README.md, el archivo notas.txt sigue en estado no rastreado (untracked).
### 5. Primer commit
**¿Qué guarda Git exactamente en un commit?**
Un commit guarda una instantánea del estado completo del proyecto en ese momento, junto con metadatos como el autor, la fecha, un identificador único (hash) y una referencia al commit anterior.
**¿Por qué es importante el mensaje del commit?**
El mensaje del commit es importante porque describe claramente qué cambios se realizaron y por qué, facilitando la comprensión del historial del proyecto y el trabajo colaborativo.
### 6. Historial de cambios
**¿Qué información muestra cada commit?**
Cada commit muestra un identificador único (hash), la referencia de la rama (HEAD), el nombre y correo del autor, la fecha y hora en que se realizó el cambio y el mensaje que describe qué se modificó.
**¿Qué es el hash?**
El hash es una cadena alfanumérica única generada mediante una función criptográfica que identifica de forma inequívoca a un commit y a su contenido.
**¿Por qué el historial es inmutable?**
El historial es inmutable porque cada commit depende criptográficamente del commit anterior mediante su hash, por lo que cualquier modificación alteraría toda la cadena y sería detectada por Git.
### 6. Conexión local–remoto
**¿Qué es origin?**
origin es el nombre por defecto que se le da al repositorio remoto, es decir, la referencia al servidor donde se aloja el proyecto (por ejemplo, en GitHub, GitLab o Bitbucket).
**¿Qué significa -u?**
La opción -u (o --set-upstream) establece una relación entre la rama local y la rama remota, permitiendo que en adelante se puedan usar comandos como git push o git pull sin especificar el nombre del remoto y la rama.
### 7. Creación de ramas
**¿Qué representa una rama en Git?**
Una rama en Git representa una línea independiente de desarrollo que apunta a una serie de commits, permitiendo trabajar en nuevas funcionalidades, correcciones o experimentos sin afectar la rama principal.
**¿Por qué Git las crea tan rápido?**
Git crea las ramas muy rápido porque internamente solo son punteros ligeros a commits, no copias completas de los archivos, lo que hace que su creación y manejo sea casi inmediato.
<<<<<<< HEAD

=======
### 8. Fusión de ramas
**¿Qué tipo de merge se ha producido?**
Se ha producido un merge fast-forward, en el que Git simplemente avanzó el puntero de la rama actual hasta el último commit de la rama desarrollo sin crear un commit de fusión.
**¿Por qué no hubo conflictos (si es el caso)?**
No hubo conflictos porque la rama actual no tenía cambios propios que divergieran de desarrollo, por lo que Git pudo aplicar los commits de forma directa y automática.
### 9. Protección de rama main en repositorio remoto
**Describe brevemente las opciones más relevantes disponibles al proteger una rama, incluyendo al menos:**
- **Obligación de usar Pull Requests:** Impide hacer commits directos sobre la rama protegida y obliga a que todos los cambios se integren mediante una Pull Request.
- **Requerimiento de revisiones antes de fusionar:** Exige que uno o más revisores aprueben los cambios antes de que puedan fusionarse en la rama protegida.
- **Restricción de quién puede aprobar los cambios:** Permite definir usuarios o equipos específicos que tienen permiso para aprobar las Pull Requests, aumentando el control y la seguridad.
- **Descartar las aprobaciones de solicitudes obsoletas cuando se suban nuevos commits:** Hace que las aprobaciones previas se invaliden si se añaden nuevos commits, obligando a una nueva revisión del código actualizado.
**Indica qué opción de revisión es la más adecuada para esta práctica.**
La opción más adecuada es requerir revisiones antes de fusionar, configurando al menos una aprobación.
**Justifica la elección teniendo en cuenta que se trata de un proyecto educativo individual / académico.**
Aunque el proyecto sea individual, requerir revisiones ayuda a simular un entorno profesional real, fomenta buenas prácticas y evita errores accidentales en la rama main, incluso si la revisión la realiza el propio autor desde otra rama.
**Explica la diferencia entre:**
- **Requerir revisiones:** Obliga a que una Pull Request sea revisada y aprobada antes de poder fusionarse, aumentando el control y la calidad del código.
- **No requerir revisiones:** Permite fusionar directamente los cambios sin aprobación previa, lo que es más rápido pero reduce el control y aumenta el riesgo de errores.
**Describe y demuestra la secuencia correcta de pasos para modificar la rama main cuando está protegida:**
>>>>>>> desarrollo

## Autor: Fabio Acosta Fuentes
## Fecha: 21/12/2025
## Descripción breve del proyecto:
Introducción a Git y GitHub (Capítulos 1, 2 y 3 de Pro Git)