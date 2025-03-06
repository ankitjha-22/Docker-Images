# Use official Node.js image as the base image
FROM node:16-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json (or yarn.lock) to the container
COPY package*.json ./
# If you're using Yarn, replace the above line with:
# COPY yarn.lock ./

# Install dependencies
RUN npm install
# If you're using Yarn, replace the above line with:
# RUN yarn install

# Copy the rest of the application files
COPY . .

# Build the Remix application for production
RUN npm run build
# If you're using Yarn, replace the above line with:
# RUN yarn build

# Expose the port Remix app will run on
EXPOSE 3000

# Start the Remix application
CMD ["npm", "run", "start"]
# If you're using Yarn, replace the above line with:
# CMD ["yarn", "start"]
