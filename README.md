#GPM

Group Package installation and tracking for debian/ubuntu package manager

##Instalation
Ensure that you have Python installed, place `gpm` script in some of your `PATH` folders, for ex: `/usr/local/bin`
Add execute flag `chmox +x /usr/local/bin/gpm`

Create json file in `/etc/gpm.json` with your apt packages, for ex:

```json
{
  "packages":{
    "nodejs": {"group": "dev"},
    "gnome-core": {"group": "desktop"}
  }
}

```

Run `gpm install` to install all packages or `gpm install --group dev` to install packages from certain group. 

See `gpm -h` or `gpm <command> -h` for additional info.

```
usage: gpm <command> [<args>]

  Possible gpm commands are:
     add        Add new package to gpm.json and run installation
     remove     Remove package from gpm.json and run uninstalation
     list       List of all packages and their groups
     install    install all packages from gpm.json
     uninstall  uninstall all packages from gpm.json
```
