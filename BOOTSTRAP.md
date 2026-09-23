
### Bootstrap a development pore-scale repo

Run **one command at a time**, edit as needed, replace `git@` with `https://` if you are not a developer:

```bash
mkdir apps
cd apps
git init
git clone git@github.com:difizix/image3kit.git
(cd image3kit && git remote add digi git@github.com:DigiPorFlow/image3kit.git)
git clone git@github.com:difizix/pnmkit
git clone git@github.com:difizix/porgui
git clone git@github.com:aliraeini/xpm.git || git clone git@github.com:difizix/xpm
git submodule add ./image3kit image3kit
git submodule add ./pnmkit pnmkit
git submodule add ./porgui porgui
git submodule add ./xpm xpm
git commit -m "bootstrap porsim" -a
```
