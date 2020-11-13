# How to start the swagger server.

first pull the image:

```t
docker pull swaggerapi/swagger-ui
```

Then create the server:

```t
docker run -d --name vistracks-swagger-server-1.0.0 -p 8085:8080 BASE_URL=/VistracksSwagger -e SWAGGER_JSON=/Swagger/vistracks-swagger.yaml -v /Swagger:/Swagger swaggerapi/swagger-ui
```