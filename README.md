# CatRunner Releases

Repositorio **publico de distribucion** de CatRunner. El codigo fuente vive en
un repositorio privado; aqui se publican los instaladores oficiales.

## Instalar con un solo comando (Windows)

```powershell
irm https://github.com/CarlosVeraAvelino/CatRunner-releases/releases/latest/download/install.ps1 | iex
```

El script descarga `CatRunner-Setup.exe` (instalador autocontenido: no
requiere Node ni permisos de administrador), verifica su SHA-256 y lo instala
en modo silencioso.

## Instalacion manual

Descarga `CatRunner-Setup.exe` desde la [pagina de
releases](https://github.com/CarlosVeraAvelino/CatRunner-releases/releases) y
ejecutalo.

## Verificacion

Cada release incluye `CatRunner-Setup.exe.sha256` con el hash del
instalador. Comprueba asi:

```powershell
Get-FileHash .\CatRunner-Setup.exe -Algorithm SHA256
```

---

Los releases se generan automaticamente desde el repositorio privado al
pushear una etiqueta `v*` (workflow `release.yml`).