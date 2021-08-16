FROM adoptopenjdk/openjdk8:alpine-jre
RUN mkdir /magma
WORKDIR /magma/
COPY ./mods/ ./mods/
COPY ./plugins/ ./mods/
COPY ./magma-1.12.2-server.jar .
COPY ./server.properties .
COPY ./eula.txt .
COPY ./bukkit.yml .
COPY ./spigot.yml .
COPY ./paper.yml .
COPY ./magma.yml .



CMD Java -jar magma-1.12.2-server.jar