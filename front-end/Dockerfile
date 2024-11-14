#           NOT TESTED YET
FROM node:20-alpine
LABEL authors="XIONdevel, Anya-ctrl"
# Set the working directory
WORKDIR /usr/src/app
# Copy package.json and install dependencies
COPY package.json .
RUN npm install
# Copy the rest of the application code
COPY . .
# Expose the port the app runs on
EXPOSE 3000
# Start the Node.js application
CMD ["npm", "start"]
