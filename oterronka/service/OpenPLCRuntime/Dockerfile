FROM ubuntu:latest
#Clonar el repositorio de OpenPLC:
RUN [ "executable" ]h git clone https://github.com/thiagoralves/OpenPLC_v3.git
RUN cd OpenPLC_v3```[_{{{CITATION{{{_1{1.4 Installing OpenPLC Runtime on Linux – Autonomy](https://autonomylogic.com/docs/installing-openplc-runtime-on-linux-systems/)
#Construir la imagen Docker:
RUN docker build -t openplc-docker .```[_{{{CITATION{{{_2{Docker container for OpenPLC Server - GitHub](https://github.com/jpaffrath/docker-openplc)
#Ejecutar el contenedor Docker:
#RUN docker run --name plc -d -p 8080:8080 -p 502:502 -v /PATH/TO/SCRIPT:/home/openplc/scripts openplc-docker```[_{{{CITATION{{{_2{Docker container for OpenPLC Server - GitHub](https://github.com/jpaffrath/docker-openplc)- Asegúrate de reemplazar `/PATH/TO/SCRIPT` con la ruta a tus scripts de OpenPLC[_{{{CITATION{{{_2{Docker container for OpenPLC Server - GitHub](https://github.com/jpaffrath/docker-openplc).

#abrir un navegador para acceder al interfaz de openplc runtime

# Instalar las dependencias
RUN apt-get update && apt-get install -y \
    xvfb \
    chromium-browser \
    && rm -rf /var/lib/apt/lists/*

# Crear un script para iniciar el navegador
RUN echo '#!/bin/bash\n' \
    'export DISPLAY=:99\n' \
    'Xvfb :99 -screen 0 1024x768x16 &\n' \
    'chromium-browser --no-sandbox --disable-gpu "$@"\n' \
    > /usr/local/bin/start-browser && chmod +x /usr/local/bin/start-browser

# Comando para abrir una URL específica
CMD ["start-browser", "http://localhost:8080"]
# Construir la imagen Docker
RUN docker build -t navegador-con-url
# Ejecutar el contenedor Docker
#RUN docker run --rm navegador-con-url





