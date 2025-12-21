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
