FROM node:alpine

# Create the app directory and set ownership
RUN mkdir -p /usr/src/node-app && chown -R node:node /usr/src/node-app

# Set the working directory
WORKDIR /usr/src/node-app

# Copy package.json and yarn.lock into the container
COPY package*.json ./

# Switch to the node user
USER node

# Install dependencies
RUN npm install

# Copy the application files and set ownership
COPY --chown=node:node . .

# Expose port 4000
EXPOSE 4000

# Command to run the app (assuming an app entry file like index.js)
CMD ["npm", "start"]
