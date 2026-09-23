
To bootstrap a development pore-scale git repository, run the following commands.
Edit as appropriate, e.g. 
* replace `GITBASE=git@github.com:` with `GITBASE=https://github.com/` if you haven't added your SSH public key to github.
* replace `GITBASE=git@github.com:` with `GITBASE=ssh://git@localhost:27032/` to recreate from a local, or ssh-forwarded, Gitea server at localhost:27032

```bash
mkdir apps; cd apps
GITBASE=git@github.com:
git clone ${GITBASE}DigiPorFlow/image3kit.git
(cd image3kit && git remote add dfz ${GITBASE}difizix/image3kit.git && git fetch dfz/main)
git clone ${GITBASE}difizix/pnmkit.git
git clone ${GITBASE}difizix/porgui.git
git clone ${GITBASE}aliraeini/xpm.git || git clone ${GITBASE}difizix/xpm.git # replace aliraeini with your user name in github or gitea

# Having above git repositories as git submodules helps keeping track of changes
git submodule add ./image3kit image3kit
git submodule add ./pnmkit pnmkit
git submodule add ./porgui porgui
git submodule add ./xpm xpm
git commit -m "bootstrap digiporflow-related apps" -a
```

And/or open the apps folder in your favorite IDE and ask LLMs to guide you further.
