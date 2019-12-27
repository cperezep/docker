FROM node:8

COPY ["package.json", "package-lock.json", "/usr/src/"]
# [<ubicacion de los archivos a copiar>, <destino donde van a quedar los archivos copiados>]
WORKDIR /usr/src
# es similar al comando cd, WORKDIR <entrar en la siguiente ruta>
RUN npm install
# RUN ejecuta el comando npm install
COPY [".", "/usr/src/"]
# Copiar los demás archivos de la node app (docker cachea lo que ya tiene por lo tanto mejora el rendimiento al hacer las builds)
EXPOSE 3000
# le indica al contenedor el puerto por el cual va a salir o exponer el contenedor, es el mismo puerto por donde esta escuchando node
CMD ["npm", "run", "start"]
# ejecuta el comando node index.js el cual levanta el servidor de express