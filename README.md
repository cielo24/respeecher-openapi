# Respeecher API Documentation

This is a non-official OpenAPI specification based on the official [Respeecher API Documentation](https://docs.respeecher.com/).

**NOTE:** Cielo24 has no affiliation with Respeecher. This repository is periodically updated as a kindness to others who have shown interest in it. Therefore, this exists to provide an easy way to access and contribute with the project, nothing more.

## Generating Client Code

While there are multiple ways to generate client code from the OpenAPI specification, we strongly encourage the use of Docker. Docker simplifies the setup process, ensuring that the only requirement on your machine is Docker itself. This method also provides a consistent environment that minimizes issues related to dependencies or platform-specific configurations.

To generate client code using Docker, please follow the command below, replacing `LANGUAGE` with your target programming language:

```shell
docker run --rm \
  -v ${PWD}:/local openapitools/openapi-generator-cli generate \
  --package-name=respeecher \
  -i /local/respeecher.yml \
  -g LANGUAGE \
  -o /local/respeecher-LANGUAGE
```

The `LANGUAGE` parameter can be any of the supported languages by the OpenAPI Generator, such as:

> ada, android, csharp, dart, go, java, kotlin, php, python, ruby, scala, swift5, typescript, and more.

For a comprehensive list of supported languages, refer to the [OpenAPI Generator documentation](https://openapi-generator.tech/docs/generators/).

## Pre-generated Clients

For convenience, we provide pre-generated client libraries for some programming languages:

- [Python 3](https://github.com/cielo24/respeecher-python)
