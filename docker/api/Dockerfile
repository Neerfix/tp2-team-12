#import depuis Docker hub
FROM node:10

#Création du repertoire de l'application
WORKDIR /home/nodejs/app
RUN chown -R node:node /home/nodejs/app

#Permet l'installation des librairies listés au sein du fichier composer.json
COPY package*.json ./
RUN npm install
COPY . .

#Permet d'exposer le port pour Doker
EXPOSE 8080

#execute le lancement du serveur node
CMD ["npm","start"]

