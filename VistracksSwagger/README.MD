# How to start the swagger server.

first pull the image:

```t
docker pull swaggerapi/swagger-ui
```

Then create the server:

```t
docker run -d --name "vistracks-swagger-server-1.0.0" -p 8085:8080 -e BASE_URL=/VistracksSwagger -e SWAGGER_JSON=/Swagger/vistracks-1.0.0.yaml -v /home/XRSDEV.LOCAL/kelby.stine/VistracksSwagger:/Swagger swaggerapi/swagger-ui
```

How to get to the swagger server:

http://xrsdev-lin86b.xrsdev.local:8085/VistracksSwagger/
