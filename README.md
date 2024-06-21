# First ReactJS - Docker

- ReactJS
- Docker - (Docker Desktop)
- Vite.js

# RUN - PROJECT
- `npm install`
- `npm run dev` (Vite.js)

# RUN - DOCKER
## Build the Docker Image

Once you have cloned the repository, navigate to the project directory and build the Docker image using the following command:

### Development Mode
```
docker build -t reactjs/convert-suhu:dev -f Dockerfile .
```

### Preview Mode
```
docker build -t reactjs/convert-suhu:pre -f Dockerfile.pre .
```

### Production Mode
```
docker build -t reactjs/convert-suhu:prod -f Dockerfile.prod .
```

## Run the Docker Container

After successfully building the Docker image, you can run the container in different modes:

### Development Mode

To run the container in development mode, use the following command:

```
docker run -d -p 5000:5000 reactjs/convert-suhu:dev
```

The application will now be running in a Docker container with hot-reloading enabled. You can access it at `http://localhost:5000`.

### Preview Mode

To run the container in preview mode, use the following command:

```
docker run -d -p 4000:4000 reactjs/convert-suhu:pre
```

The application will now be running in a Docker container with optimized production-like settings. You can access it at `http://localhost:4000`.

### Production Mode

To run the container in production mode, use the following command:

```
docker run -d -p 3000:3000 reactjs/convert-suhu:prod 
```

The application will now be running in a Docker container with production settings. You can access it at `http://localhost:3000`.

# NOTES: Lưu Ý: Khi Project có những thay đổi mới thì phải build lại theo mục "Build the Docker Image" để hiển thị đúng nội dung Project mới nhất.
