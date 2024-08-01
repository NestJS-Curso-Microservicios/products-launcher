# Proyecto Microservicios

Este proyecto contiene múltiples microservicios que interactúan entre sí utilizando NATS como sistema de mensajería.

## Requisitos Previos

Antes de correr el proyecto, asegúrate de tener instalados los siguientes componentes:

- Docker
- Docker Compose
- Node.js (versión 14 o superior)
- npm (versión 6 o superior)

## Configuración del Entorno

1. Clona el repositorio:
   ```sh
   git clone https://github.com/tu-usuario/tu-repositorio.git
   cd tu-repositorio
   ```
   
2. Instala las dependencias de los microservicios:
   ```sh
    npm install
    ```
   
3. Crea un archivo `.env` en la raíz del proyecto con la siguiente información:
    ```sh
    NATS_URL=nats://nats:4222
    ```
   
## Ejecución

Para correr los microservicios, ejecuta el siguiente comando:
   ```sh
   docker-compose up --build
   ```

## Detener la Ejecución

Para detener los microservicios, presiona `Ctrl + C` en la terminal donde se están ejecutando y luego ejecuta el siguiente comando:
   ```sh
   docker-compose down
   ```



### Pasos para crear los Git Submodules


1. Crear un nuevo repositorio en GitHub
2. Clonar el repositorio en la máquina local
3. Añadir el submodule, donde `repository_url` es la url del repositorio y `directory_name` es el nombre de la carpeta donde quieres que se guarde el sub-módulo (no debe de existir en el proyecto)
```
git submodule add <repository_url> <directory_name>
```
4. Añadir los cambios al repositorio (git add, git commit, git push)
   Ej:
```
git add .
git commit -m "Add submodule"
git push
```
5. Inicializar y actualizar Sub-módulos, cuando alguien clona el repositorio por primera vez, debe de ejecutar el siguiente comando para inicializar y actualizar los sub-módulos
```
git submodule update --init --recursive
```
6. Para actualizar las referencias de los sub-módulos
```
git submodule update --remote
```


## Importante
Si se trabaja en el repositorio que tiene los sub-módulos, **primero actualizar y hacer push** en el sub-módulo y **después** en el repositorio principal.

Si se hace al revés, se perderán las referencias de los sub-módulos en el repositorio principal y tendremos que resolver conflictos.



## Licencia

Distribuido bajo la licencia MIT. Ver `LICENSE` para más información.
