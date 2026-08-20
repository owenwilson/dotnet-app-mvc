# dotnet-app-mvc

## setup

```sh
mkdir dotnet-app-mvc && cd dotnet-app-mvc
```

```sh
dotnet new globaljson --sdk-version 8.0.424
```

```sh
dotnet new mvc
```

## ci-cd

```sh
dotnet restore
```

- This flag prevents the dependencies from being restored again, assuming that `dotnet restore` was previusly run.

```sh
dotnet build --configuration Release --no-restore
```

```sh
dotnet test --configuration Release --no-build --collect:"XPlat Code Coverage"
```

```sh
dotnet publish --configuration Release --no-build --output ./publish
```

## references

- check out [api rest with dotnet core](https://medium.com/nbellocam-es/creando-una-api-rest-con-asp-net-core-desde-cero-fc58924395fd)
