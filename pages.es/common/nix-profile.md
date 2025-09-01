# nix profile

> Instala, actualiza y quita paquetes de perfiles de Nix.
> Más información: <https://nix.dev/manual/nix/2.30/command-ref/new-cli/nix3-profile>.

- Instala unos paquetes desde nixpkgs al perfil predeterminado:

`nix profile add {{nixpkgs#pkg1 nixpkgs#pkg2 ...}}`

- Instala un paquete desde un flake en GitHub a un perfil específico:

`nix profile add {{github:dueño/repositorio/paquete}} --profile {{./ruta/al/directorio}}`

- Lista los paquetes instalados actualmente en el perfil predeterminado:

`nix profile list`

- Quita un paquete instalado desde nixpkgs del perfil predeterminado, por nombre:

`nix profile remove {{legacyPackages.x86_64-linux.pkg}}`

- Actualiza paquetes en el perfil predeterminado a la versión más reciente disponible:

`nix profile upgrade`

- Revierte (cancela) la acción más reciente en el perfil predeterminado:

`nix profile rollback`
