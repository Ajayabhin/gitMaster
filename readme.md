# Git master

## check Installation
``` bash
git version
```

## Global Configs
``` bash 
git config --global user.name "ourname"
git config --global user.email "our github email "
```

- To check configs

`
git config --global --list
`

## (optional) Adding ssh Keys 

``` bash
ssh-keygen -t ed25519 -C "our github email"
#save file as ~/.ssh/id_ed25519_gh

#now save the pub key contents to github ssh keys
cat ~/.ssh/id_ed25519_gh

#now create a ssh config 
nano ~/.ssh/config

```

## add these inside config
`
Host github.com
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_ed25519_gh
    IdentitiesOnly yes
`

then

``` bash

git config --global url."git@github.com:".insteadOf "https://github.com"

ssh github.com

```