Title: Installation sous Windows

Avec CCVPNGUI (recommandé, simple)
-------------

CCVPNGUI est fait pour CCrypto VPN et contient tout ce qu'il faut. Téléchargez et lancez juste :  
<https://dl.ccrypto.org/ccvpngui/releases/ccvpngui-1.0.0-1.exe>
[(sig)](https://dl.ccrypto.org/ccvpngui/releases/ccvpngui-1.0.0-1.exe.asc)

À l'installation, il vous sera proposé d'installer une icône sur le bureau.  
Vous aurez ensuite à faire un clic-droit sur l'icône dans la zone de notification,
puis "Connecter".  
Une fenêtre s'affichera pour vous informer de la progression, vous pouvez la fermer
à n'importe quel moment et le VPN restera connecté.

C'est open-source et basé sur [LVPNGUI](https://github.com/PacketImpact/lvpngui/).

---

Avec OpenVPN GUI (avancé)
----------------

1. Téléchargez le Windows Installer d'OpenVPN sur 
    [OpenVPN.net](http://openvpn.net/index.php/open-source/downloads.html)  
    et installez OpenVPN.

2. Dans [votre compte](/account/config), téléchargez le fichier de configuration (.ovpn)
    et copiez le dans `C:\Program Files\OpenVPN\config\`.
    Si vous avez téléchargé plusieurs fichiers dans une archive, extrayez l'archive dans
    `C:\Program Files\OpenVPN\config\`

3. Démarrez `OpenVPN GUI` *en tant qu'Administrateur*. Vous pouvez le trouver sur le bureau ou
    dans le menu Démarrer.  
    Une fois démarré, vous devriez le voir dans la zone de notification.
    Faites un clic droit dessus, et choisissez `Connect`.

4. Une fenêtre de log OpenVPN devrait s'ouvrir et montrer la progression.
    Si il y a une erreur, elle y sera affichée et vous pourrez lire
    [la page d'auto-diagnostic](/page/self-diagnosis).
    Si votre problème n'est pas résolu, [contactez le support](/tickets/).

5. Si la connexion s'est bien passée, l'icone OpenVPN devrait devenir verte.  
    Vous êtes alors connecté et pouvez profiter de votre connexion sécurisée.


#### Enregistrer les identifiants
Vous pouvez faire qu'OpenVPN enregistre votre nom d'utilisateur et votre mot de
passe, pour ne pas avoir à l'entrer à chaque connexion.  
Créez un fichier texte "ccrypto_creds.txt" contenant votre nom sur la
première ligne, et votre mot de passe sur la deuxième, comme ceci:

    JackSparrow
    s0mep4ssw0rd

Déplacez-le ensuite dans `C:\Program Files\OpenVPN\config\`, avec le fichier
ccrypto.ovpn que vous avez téléchargé plus tôt.

Ouvrez ccrypto.ovpn avec un éditeur de texte (Bloc-notes, Notepad++, ...)
et ajouter une ligne à la fin:

    auth-user-pass ccrypto_creds.txt

Pour finir, redémarrez OpenVPN GUI et connectez vous : il ne devrait plus vous
demander votre mot de passe.

