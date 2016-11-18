# Omnisharp docker

Docker to run an [Omnisharp server](https://github.com/OmniSharp/omnisharp-server).

## Starting the Omnisharp server

```bash
docker run --rm -p 2000:2000 -v $PWD:/app erikap/omnisharp-server
```

or use the [omnisharp](https://github.com/erikap/docker-dotnet) command.

## Configuration
The Omnisharp server can be configured by setting environment variables on the Docker container. The following options are available:
* LOG_LEVEL: log level of the Omnisharp server. Default: `Debug`. Must be one of `Silent`, `Quiet`, `Debug`, `Verbose`.

