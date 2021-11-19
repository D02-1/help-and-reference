# Setup SSH key 


:point_right:[GitHub docs-generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

1. im Terminal eingeben mit deiner email => `$ ssh-keygen -t ed25519 -C "your_email@example.com"`\
(die email, welche bei GitHub hinterlegt ist, siehe: `git config --global --list`)

---
**danach, bei den folgenden prompts, einfach Enter:**

- Enter file in which to save the key (/home/dci/.ssh/id_ed25519):\
- Enter passphrase (empty for no passphrase):\
- Enter same passphrase again: 

---
2. im terminal eingeben => `$ eval "$(ssh-agent -s)"`
3. im terminal eingeben => `$ ssh-add ~/.ssh/id_ed25519`
4. im terminal eingeben => `cat ~/.ssh/id_ed25519.pub`

nun sollte ein ssh key im Terminal ausgegeben werden, kopiere diesen und hinterlege diesen auf deinem GitHub Konto, wie folgt:\

- gehe auf settings 
- SSH and GPG keys 
- drücke auf new SSH key 
- gebe einen title ein und kopiere den ssh key ins key feld

<img src="ssh-github.png" alt="ssh-github" width="60%"> 

