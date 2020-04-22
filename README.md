# [Oh My Fish][oh-my-fish] custom package repo
This repository contains a list of public Fish packages that can be installed by name using Oh My Fish. The goal of this repo is to maintain a discoverable index of quality Fish packages that can easily be maintained by the Fish community.

## Repository format
Packages are referenced in the repository using property files located in the `packages/` directory. The actual code of each package is stored in separate, individual Git repositories maintaned by the package mantainer themselves. This keeps control of the package in the owner's hands, but still allows easy sharing of the package.

The name of each property file indicates the package name, and the various properties in the file describe the package and how it can be installed. These are the properties currently used:

- `type`: The type of package. Can be `plugin` or `theme`.
- `repository`: A cloneable Git URL to the package source repository.
- `maintainer`: The name and email of the maintainer of the package.
- `description`: A short description of the package.

## Submitting a package
Want to add your own package to the public repository? First, make a fork of this Git repository. Then create a package description file inside the `packages/` directory. The file name should be the name of your package without any file extensions, and should contain at least these properties:

```
type = plugin
repository = YOUR-PACKAGE-URL
maintainer = YOUR-NAME <YOUR-EMAIL>
description = YOUR-PACKAGE-DESCRIPTION
```

Be sure to use a cloneable Git URL for your package. If your package is a theme, use `type = theme` instead.

[fish]: http://fishshell.com
