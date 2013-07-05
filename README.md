# SaltStack Masterless Template

**Utilisation du template**

1/ Installer [Virtualbox](https://www.virtualbox.org/wiki/Downloads).

2/ Installer [Vagrant](http://downloads.vagrantup.com).

3/ Installer le plugin vagrant-vbguest.

`vagrant plugin install vagrant-vbguest`

4/ Installer le plugin vagrant-salt (https://github.com/saltstack/salty-vagrant).

`vagrant plugin install vagrant-salt`

5/ Configurer le chemin absolu vers le dossier *etc/salt/srv* (variable **config.vm.synced_folder** du fichier *Vagrantfile*).

6/ Configurer l'IP de la VM (si nécessaire, variable **config.vm.network** du fichier *Vagrantfile*).

7/ Démarrer la VM : `vagrant up`.

**Approvisionnement**

Votre machine virtuelle est prête. Elle sera approvisionnée automatiquement à chaque démarrage avec les outils décrits dans le fichier *etc/salt/srv/state/base/common/init.sls*.

Vous pouvez exécuter un approvisionnement manuel en exécutant la commande `vagrant provision` (ou `vagrant ssh` pour vous connecter à la VM, puis `sudo salt-call state.highstate`).

**C'est à vous !**

[http://docs.saltstack.com/topics/tutorials/walkthrough.html](http://docs.saltstack.com/topics/tutorials/walkthrough.html)