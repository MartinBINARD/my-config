# Cheat Sheet Git

## Global config
```
git config --global user.name "Jean Dupont"
git config --global user.email jean.dupont@protonmail.com
it config --global color.ui auto
```

## Key génration
```
ssh-keygen -t ed25519 -f ~/.ssh/id_ed25519 -C "your-email@exemple.com"
```

## Ssh agent config
```
eval "$(ssh-agent -s)"

ssh-add ~/.ssh/id_ed25519
```

## Configuration of ssh file
```
# GitHub
Host github.com
    HostName github.com
    PreferredAuthentications publickey
    IdentityFile ~/.ssh/id_ed25519_hub

# GitLab
Host gitlab.com
    HostName gitlab.com
    PreferredAuthentications publickey
    IdentityFile ~/.ssh/id_ed25519_lab
```

## Copy public key
```
cat ~/.ssh/id_ed25519_lab.pub | clip
```

## Check connexions
```
ssh -T git@github.com
ssh -T git@gitlab.com
```