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

## git remotes multiples

- default github

```sh
origin	git@github.com:user/app-mvc.git (fetch)
origin	git@github.com:user/app-mvc.git (push)
```

- add azure repos example

```sh
git remote add azure git@ssh.dev.azure.com:v3/user/app-mvc/app-mvc
```

```sh
git remote -v

azure	git@ssh.dev.azure.com:v3/user/app-mvc/app-mvc (fetch)
azure	git@ssh.dev.azure.com:v3/user/app-mvc/app-mvc (push)
origin	git@github.com:user/app-mvc.git (fetch)
origin	git@github.com:user/app-mvc.git (push)
```

- test push azure

```sh
git push azure main
```

## references

- check out [api rest with dotnet core](https://medium.com/nbellocam-es/creando-una-api-rest-con-asp-net-core-desde-cero-fc58924395fd)
