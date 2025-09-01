# nix profile

> Install, update and remove packages from Nix profiles.
> More information: <https://nix.dev/manual/nix/2.30/command-ref/new-cli/nix3-profile>.

- Install some packages from nixpkgs into the default profile:

`nix profile add {{nixpkgs#pkg1 nixpkgs#pkg2 ...}}`

- Install a package from a flake on GitHub into a custom profile:

`nix profile add {{github:owner/repo/pkg}} --profile {{./path/to/directory}}`

- List packages currently installed in the default profile:

`nix profile list`

- Remove a package installed from nixpkgs from the default profile, by name:

`nix profile remove {{legacyPackages.x86_64-linux.pkg}}`

- Upgrade packages in the default to the latest available versions:

`nix profile upgrade`

- Rollback (cancel) the latest action on the default profile:

`nix profile rollback`
