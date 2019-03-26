# Pack NuGet package

```bash
mono .paket/paket.exe pack --template src/Be.Vlaanderen.Basisregisters.Templates/paket.template dist
```

# Install local NuGet package

```bash
dotnet new -i dist/Be.Vlaanderen.Basisregisters.Templates.1.0.0.nupkg
```

# Uninstall the template

```bash
dotnet new -u Be.Vlaanderen.Basisregisters.Templates
```

# Check the available template parameters

```bash
dotnet new be-registry -h
```

# Check what a template would install

```bash
dotnet new be-registry --dry-run
```

# Create a new registry

```bash
dotnet new be-registry -n UserRegistry -aggregate User
The template "Basisregisters Vlaanderen Registry" was created successfully.
```

# All in one packaging & installing

```bash
rm -rf dist/; \
mono .paket/paket.exe pack --template src/Be.Vlaanderen.Basisregisters.Templates/paket.template dist; \
dotnet new -u Be.Vlaanderen.Basisregisters.Templates; \
dotnet new -i dist/Be.Vlaanderen.Basisregisters.Templates.1.0.0.nupkg;
```