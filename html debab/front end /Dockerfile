# Use Node.js 
FROM node:16-alpine

#Set the working Directory 
WORKDIR /app

# #Copy package file
COPY package*.json ./

# INSTALL DEPENDENCIES 
RUN npm install 

#Copy app source code 
COPY . .

#build react app
RUN npm run build 

#EXPOSE PORT 3000
EXPOSE 3000

#SERVE react app

CMD ["npx", "serve", "-s", "build"]