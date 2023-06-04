# We need node 16. I found node:16.20.0 on Docker Hub
FROM node:16.20.0

EXPOSE 5000

WORKDIR /usr/src/app

# Copy all of the source code
COPY . .

#Check npm install
RUN node -v && npm -v

# Install all packages
RUN npm install

# Build static files
RUN npm run build

# Install npm package serve
RUN npm install -g serve

# Command to serve the project
CMD ["serve", "-s", "-l", "5000", "build"]
