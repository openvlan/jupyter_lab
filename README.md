# jupyter_lab
Docker Compose Jupiter data science

## Requerimientos Previos:
.- Docker
.- Docker Compose
.- Si no se tiene docker compose y si unicamente docker se puede abrir CMD en Windows o la consola en Linux y Mac e ingresar el siguiente comando:

## Para instalar con Docker Compose en Linux o Mac
```bash
chmod +x installJupyterLab.sh
./installJupyterLab.sh
```

## Para instalar con Docker Compose en Windows

```bash
installJupyter.bat
```

## Para usar directamente con docker sin docker-compose

```bash
docker run --rm -p 10000:8888 -e JUPYTER_ENABLE_LAB=yes -v "${PWD}":/home/jovyan/work jupyter/datascience-notebook
```

## Se explican los parametros
    .- run -> crea un contenedor
    .- -p -> le indica localmente el puerto en la maquina host y luego de los dos puntos el puerto en el contenedor. Se podrá acceder a traves del puerto 10000 en este caso
    .- -e JUPYTER_ENABLE_LAB=yes habilita LAB ya que esta imagen tiene mas cosas
    -V monta un directorio dentro del contenedor, esto permite ver los archivos que se pongan en este directorio en dentro del contenedor
    .- El último parametro es la imagen que se usa para crear este contenedor

## Repositorio Original
[Link en github](https://github.com/jupyter/docker-stacks)