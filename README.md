# pizzafarm

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

### Docker Image: Pull the App Image 
```
docker pull dennisdavid/pizzafarm:latest
```
## Run the App in a Docker Container 
You can view the app on your host browser on port 8081
```
docker run -it -p 8081:80 --rm --name pizzafarm  dennisdavid/pizzafarm
```
