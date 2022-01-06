# Born2BeRoot

# *LISTE COMMANDE*

- apt-get = installation de package
- su - = passer en mode root 
- su <username> = se connecter a un user
- compgen -u = afficher la liste des user
- compgen -g = afficher la liste des groupes
- getent group = afficher la liste des groupes, + user correspondants
- userdel --remove = remove le user ET son dossier /home ET le groupe auxquel il appartient 
- adduser <username> = add un user
- getent passwd <username> = check si le user est bien cree
- systemctl status ssh = check SSH status
(depuis le terminal) - ssh <username>@<ip-address> -p 4242 = se connecter via une autre machine
- sudo visudo = ouvrir la config sudo
- sudo nano /etc/login.defs = config de passwd
- sudo nano /etc/pam.d/common-password = exigences mot de passe
- sudo crontab -u root -e = config de crontab
- ss -tnulp = check les ports
- sudo nano /etc/ssh/sshd_config
- sudo ufw status numbered = check ufw status
- sudo ufw delete <number> = delete la regle du nombre en question
- sudo ufw allow (nbr du port) = ajouter une nouvelle regle pour un port 
- hostnamectl = check current hostname
- hostnamectl set-hostname <nouveau-nom> = set un nouveau nom de hostname + ne pas oublier de changer le fichier contenant les hosts en faisant un "sudo nano /etc/hosts"
- usermod -a -G examplgegroup exampleusername = ajouter un user dans un groupe specifique
- groupadd <nomdugroupe> = creer un groupe
- fdisk -l = pour voir la partition du disk sur la vm
- head -n 2 /etc/os-release = regarder la version de la vm


---------------

# *EXPLICATION DEFENSE*

- Difference entre apt et aptitude = aptitude est un package manager plus puissant et complet (apt est seulement une commande tandis que aptitude est un groupement d'utilisation d'apt, et possede une interface graphique).

- LVM = Logical Volume Manager : Ca sert a gerer des disques durs partitionnes 

- Uncomplicated Firewall = Un programme informatique qui est un pare-feu simple d'utilisation.

- Difference entre CentOS et Debian = Debian est open-source, alors que CentOS est dirige par une entreprise, et il est concu a un usage professionnel pour les entreprises, tandis que Debian est plus facile pour debuter, et pour installer des interfaces utilisateurs (par exemple zsh).

- Difference entre AppArmor et SELinux = Ce sont tous les deux des logiciels de securite pour Linux. SELinux est plus dur a installer car extremement pousse (developpe par la NSA, par des cracks, pour des cracks), contrairement a AppArmor qui est plus facile a utiliser.

- Pourquoi utiliser cette politique de mot de passe ? : Elle est extremement securisee, mais chiante pour l'utilisateur car il faut le changer souvent, sans pour autant qu'il ressemble a l'ancien

- Sudo = Sudo veut dire "Super User DO", c'est une commande qui permet d'executer n'importe quelle autre commande sans restrictions. (en tant que root).

- SSH = Secure Shell. C'est un protocole qui permet a des utilisateurs d'acceder de maniere securise a des networks pas securises (via des cles de chiffrement les fameuses cles ssh).



