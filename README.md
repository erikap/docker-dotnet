# docker-dotnet

Tooling for using the [.Net Core docker](https://hub.docker.com/r/microsoft/dotnet/) and [.Net Core Tools](https://docs.microsoft.com/en-us/dotnet/articles/core/tools/) in a reproducable way. Inspired by [docker-ember](https://github.com/madnificent/docker-ember).

## Prerequisites
Enable user-namespaces in Docker such that volumes are mounted with the right privileges. See [here](http://www.jrslv.com/docker-1-10/#usernamespacesindocker) for some basic info.

## Commands
The arguments you need to pass to the Docker run command for it to be useful are too cumbersome, hence we've created scripts to help you out. Run them at the root of your project.

### dtns

`dtns` launches your application

    # No nonsense application
    dtns
    # Application in a subfolder
    dtns -s My.Sub.Application

### dtni

`dtni` is an interactive command that helps you install dependencies and run any other dotnet command. It can ask you questions and you can provide interactive answers.

    # Install dependencies
    dtni dotnet restore

### omnisharp

`omnisharp` starts an [Omnisharp Docker container](https://github.com/erikap/docker-dotnet/tree/master/omnisharp).