# Saltstack Masterless Template

**Utilisation du template**

1/ Installer Virtualbox.

2/ Installer Vagrant.

3/ Installer le plugin vagrant-vbguest.

4/ Installer le plugin vagrant-salt.

5/ Configurer le chemin absolu vers le dossier *etc/salt/srv* (variable **config.vm.synced_folder** du fichier *Vagrantfile*).

6/ Configurer l'IP de la VM (si nécessaire, variable **config.vm.network** du fichier *Vagrantfile*).

7/ Démarrer la VM : `vagrant up`