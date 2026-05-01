# Base image
FROM node:18

# Create a folder inside the container
WORKDIR /app

# Copy files
COPY app/ .

# Expose port
EXPOSE 3000

# Command to run the app
CMD ["node", "app.js"]