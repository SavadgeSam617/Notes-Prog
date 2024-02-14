
### File system
| Path | description |
| ---- | ---- |
| / | La racine |
| /bin | contient des executables, la plupart des commandes que vous utilisez. |
| /boot | contient le noyau vmlinuz et les fichiers de démarrage. |
| /dev | contient les fichiers spéciaux pour accéder aux périphériques (devices). |
| /etc | contient les fichiers de configuration du système et des applications. |
| /etc/X11 | paramétrage du serveur X |
| /etc/sysconfig | configuration des périphériques |
| /etc/cron | planificateur de tâches |
| /etc/skel | création des profils par défaut des utilisateurs |
| /home | contient les répertoires des utilisateurs. |
| /lib | les bibliothèques et les modules du noyau. |
| /mnt | c’est là que seront montés les systèmes de fichiers éjectables. |
| /opt | pour l’installation de certaines applications. |
| /root | le home de root. |
| /sbin | les exécutables nécessaires à l’administration du système donc utilisés principalement par root. |
| /tmp | pour les fichiers temporaires, tout le monde peut écrire dedans. |
| /usr | répertoire général des applications. |
| /var | c’est dans ce répertoire que l’on trouve les logs et l’aide au débogage. |
| /proc | contient entre autres choses, la liste des processus en cours et une image de la RAM (kcore). |
Le chemin Absolut **COMMENCE TOUJOURS** par un `/`
Le chemin relatif **COMMENCE JAMAIS** par `/`
Le `.` est le répertoire courant
Le `..` est le répertoire parent
Le `home/[user]` le répertoire personnel

