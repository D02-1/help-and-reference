# Setup SSH key 


:point_right:[GitHub docs-generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

:woman_technologist: 1. im Terminal eingeben mit deiner email => `$ ssh-keygen -t ed25519 -C "your_email@example.com"`\
(die email, welche bei GitHub hinterlegt ist, siehe: `git config --global --list`)

---
**danach, bei den folgenden prompts, einfach Enter:**

- Enter file in which to save the key (/home/dci/.ssh/id_ed25519):
- Enter passphrase (empty for no passphrase):
- Enter same passphrase again: 

---
:woman_technologist: 2. im terminal eingeben => `$ eval "$(ssh-agent -s)"`
:woman_technologist: 3. im terminal eingeben => `$ ssh-add ~/.ssh/id_ed25519`
:woman_technologist: 4. im terminal eingeben => `cat ~/.ssh/id_ed25519.pub`

---
nun sollte ein ssh key im Terminal ausgegeben werden, kopiere diesen und hinterlege diesen auf deinem GitHub Konto, wie folgt:

Beispiel::point_right: ssh-ed25519 AAAAC4NzaC1lZDI1NTE5AAAAIDUskq6niRTVtwsrWocBxlabsCGE4BKiZY50QY5Gh0HY your_email@example.com

:diamonds: gehe auf dein GitHub Profil
:diamonds: gehe auf settings 
:diamonds: SSH and GPG keys 
:diamonds: drücke auf new SSH key 
:diamonds: gebe einen title ein und kopiere den ssh key ins key feld

<img src="ssh-github.png" alt="ssh-github" width="80%"> 

