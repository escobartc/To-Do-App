# Original Dockerfile for running the application

FROM node:14-alpine3.14

# Install production dependencies
RUN apk update \
    && apk add --no-cache python2 g++ make 

WORKDIR /app

# Copy application code
COPY . .

# Install production dependencies
RUN yarn install --production

# Expose the port on which your application runs
EXPOSE 3000

# Command to start the application
CMD ["node", "src/index.js"]
