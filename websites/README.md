# Website workshop

In this workshop we will make a professional website using [zola](https://www.getzola.org/).

## To install zola on Mac or Linux:

Please follow the official instructions [here](https://www.getzola.org/documentation/getting-started/installation/).

## To install zola on Windows:

First [install the windows powershell](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows?=powershell-7.2#msi). Select the x64 version (not the x86 version).

Next install Scoop (using the newly installed powershell) using:

```sh
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```

followed by

```sh
irm get.scoop.sh | iex
```

Once that has run test that it installed ok by typing in the powershell:

```sh
zola
```

It should show the version number on the first line if all went well.
