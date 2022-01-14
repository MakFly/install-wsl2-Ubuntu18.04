# Installation du wsl 2 sous w10 / w11
1. Installer le WSL en rentrant cette commande en tant qu’administrateur dans le PowerShell
=> dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

2. Activer la fonctionnalité facultative « Plateforme de machine virtuelle » pour pouvoir utiliser le WSL 2 permettant d’avoir un noyau linux virtualisé :
=> dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

3. Redémarrer l'ordinateur pour terminer l'installation du WSL et mettre à jour vers le wsl2
=> wsl --set-default-version 2

3. Vous allez probablement voir ce message apparaître dans le terminal : « WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel« . Cela indique que vous devez suivre le lien pour télécharger et exécuter un fichier pour installer un noyau linux accessible au WSL 2. Puis, réexécutez la commande pour définir le WSL 2 comme version par défaut.

4. Installation la version 18.04 d'ubuntu puis du windows terminal

5. Faire la mise a jour du system ubuntu avec les commandes suivantes:
=> sudo apt-get update && apt-get upgrade

6. Installation de php : 
=> sudo apt-get install php ( Warning: Par défaut à ce jour, il installe la version 7.4 de php )
Pour passer à la version 8.0 ou 8.1 suivre le tutoriel suivant : https://php.watch/articles/php-8.0-installation-update-guide-debian-ubuntu
Bien prendre aussi les modules php pour une compatibilité de votre environnement docker si vous en avez un

7. Installation de docker :
=> https://doc.ubuntu-fr.org/docker

8. Installation de composer : 
=> https://www.digitalocean.com/community/tutorials/how-to-install-and-use-composer-on-ubuntu-20-04-fr

9. Installation de symfony-cli :
 echo 'deb [trusted=yes] https://repo.symfony.com/apt/ /' | sudo tee /etc/apt/sources.list.d/symfony-cli.list
 sudo apt update
 sudo apt install symfony-cli
