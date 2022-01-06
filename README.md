# Born2BeRoot

# *LISTE COMMANDE*

- apt-get = installation de package
- su - = passer en mode root 
- su "username" = se connecter a un user
- compgen -u = afficher la liste des user
- compgen -g = afficher la liste des groupes
- getent group = afficher la liste des groupes, + user correspondants
- userdel --remove = remove le user ET son dossier /home ET le groupe auxquel il appartient 
- adduser "username" = add un user
- getent passwd "username" = check si le user est bien cree
- systemctl status ssh = check SSH status
(depuis le terminal) - ssh "username"@"ip-address" -p 4242 = se connecter via une autre machine
- sudo visudo = ouvrir la config sudo
- sudo nano /etc/login.defs = config de passwd
- sudo nano /etc/pam.d/common-password = exigences mot de passe
- sudo crontab -u root -e = config de crontab
- ss -tnulp = check les ports
- sudo nano /etc/ssh/sshd_config
- sudo ufw status numbered = check ufw status
- sudo ufw delete "number" = delete la regle du nombre en question
- sudo ufw allow (nbr du port) = ajouter une nouvelle regle pour un port 
- hostnamectl = check current hostname
- hostnamectl set-hostname "nouveau-nom" = set un nouveau nom de hostname + ne pas oublier de changer le fichier contenant les hosts en faisant un "sudo nano /etc/hosts"
- usermod -a -G examplgegroup exampleusername = ajouter un user dans un groupe specifique
- groupadd "nomdugroupe" = creer un groupe
- lsblk = pour voir la partition du disk sur la vm
- head -n 2 /etc/os-release = regarder la version de la vm


---------------

# *EXPLICATION DEFENSE*

- Difference entre apt et aptitude = aptitude est un package manager plus puissant et complet (apt est seulement une commande tandis que aptitude est un groupement d'utilisation d'apt, et possede une interface graphique).

- LVM = Logical Volume Manager : Ca sert a gerer des disques durs partitionnes 

- Uncomplicated Firewall = Un programme informatique qui est un pare-feu simple d'utilisation.

- Difference entre CentOS et Debian = CentOs est open-source mais appartient a Linux. C'est destine aux entreprises. Debian est developpe a partir d'autres sources open-source. C'est developpe par des independant. CentOS est plus populaire que Debian. Debian a plus de packet que CentOS tandis que CentOS supporte moins d'architectures (organisation du systeme, les relations entre les elementss etc..). Ils sont en revanche tous les deux utilises.

- Apparmor = C'est un logiciel de securite, qui permet d'appliquer des restrictions a des logiciels notamment (par exemple interdire a un logiciel d'acceder a un certain dossier sans pour autant modifier le fonctionnement de l'application).

- Pourquoi utiliser cette politique de mot de passe ? : Elle est extremement securisee, mais chiante pour l'utilisateur car il faut le changer souvent, sans pour autant qu'il ressemble a l'ancien

- Sudo = Sudo veut dire "Super User DO", c'est une commande qui permet d'executer n'importe quelle autre commande sans restrictions. (en tant que root).
Exemple : si un logiciel se veut malveillant ou bien pour l'utilisateur d'acceder a des dossiers dont il n'est pas autorise.

- SSH = Secure Shell. C'est un protocole qui permet a des utilisateurs d'acceder de maniere securise a des networks pas securises (via des cles de chiffrement les fameuses cles ssh). Toutes les transactions de donnees sont cryptees.

- La commande sed = Cette commande permet d'appliquer un certain nombre de commandes sur un fichier puis d'en afficher le resultat (sans modification du fichier de départ) sur la sortie standard.

- La commande awk = Cette commande permet d'appliquer certaines actions sur un fichier en fonction de differentes expressions entre les accolades.

- La commande grep = Permet de faire des recherches de chaines de caracteres dans un flux de texte.

- Partition de disque dur = Division virtuelle du disque dur. Cela permet d'accelerer l'acces aux donnees. Deux systemes d'exploitations ne peuvent pas cohabiter sur la meme partition. Ca peut aussi servir de roue de secours si le systemme d'exploitation tombe en panne, sseule la partition de l'os sera concernee.