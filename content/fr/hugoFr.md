# Qu'est-ce qu'Hugo
Hugo est un framework moderne de création de sites Web à usage général. Il entre dans la catégorie des nouveaux générateurs de sites statiques, basés sur l'architecture dynamique JAMstack et entièrement écrits en Go. Il a été initialement créé par Steve France en 2013.
# Facilité
Dans ce tutoriel nous allons installer Hugo

Nous allons l'installer dans sa version étendue, qui comprend son programme de base et quelques fonctionnalités supplémentaires qui peuvent être utiles
Installer Hugo sous Linux
Vérifiez si Snap est installé

Pour installer Hugo sur Linux, nous allons utiliser le gestionnaire de packages Snap. Pour cette raison, la première chose que nous allons faire est de vérifier si nous avons installé ce gestionnaire, pour cela nous utiliserons la commande suivante :

```version instantanée
```


Celui-ci devrait nous répondre avec le message suivant :

```cliquer 2.55.3+22.04
snapd 2.55.3+22.04
série 16
Ubuntu 22.04
noyau 5.15.0-48-générique
```

Dans ce cas, cela signifie que Snap est installé. Ensuite, nous pouvons commencer l'installation.
Installez le paquet hugo-extended

À l'aide du gestionnaire Snap, nous allons installer le package hugo-extended.
```
snap installer hugo --channel=extended
```
Installer Hugo sous Windows

Il va falloir accéder à la page d'Hugo et aller dans les téléchargements.

Une fois ici, nous téléchargerons la dernière version qui a un nom au format hugo_extended_x.x.x_windows-amd64.zip où x.x.x correspondra à la version.

Ce zip contiendra le CMS, mais l'installation devra se faire manuellement.

Nous allons extraire le zip et pour plus de facilité nous déplacerons le fichier Hugo.exe résultant vers le chemin C:\Hugo\bin que nous allons créer.

Une fois que nous l'avons, dans le moteur de recherche Windows, nous accéderons à Modifier les variables d'environnement système en y recherchant.

Une fenêtre appelée Propriétés système s'ouvrira et dans celle-ci, nous cliquerons à nouveau sur Variables d'environnement.

Dans la liste qui nous montrera nous chercherons la variable PATH, et à la fin nous ajouterons ';C:\Hugo\bin'.

Avec ce redémarrage du système, nous aurons hugo installé et accessible dans notre système.
Installer Hugo sur macOS

Si nous ne l'avons pas déjà installé, nous installerons le gestionnaire de paquets brew avec la commande suivante

```ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
Une fois installé, nous utiliserons cette commande pour installer Hugo.
``` brew install hugo
```
Création du site avec Hugo
Création du site

Suite au tutoriel précédent, Hugo devrait déjà être installé sur notre système.

Maintenant pour créer un site avec le CMS nous allons utiliser les commandes :
# ATTENTION CES COMMANDES DOIVENT ÊTRE EFFECTUÉES DEPUIS NOTRE UTILISATEUR HABITUEL, JAMAIS DEPUIS SUDO

```hugo nouveau site nom du site
cd nom du site
```
Notre site est déjà créé, mais pour le moment il n'est pas fonctionnel. Pour que cela fonctionne, nous devons d'abord trouver un thème à utiliser.
Installer un thème sur le site

À titre d'exemple, je vais utiliser le thème PaperMod, mais il y en a beaucoup sur Internet que nous pouvons utiliser. Pour installer le thème ce que nous allons faire dans ce cas (chaque thème peut avoir sa propre méthode d'installation, mais la plupart sont ainsi)

```echo "theme = 'hugo-PaperMod'" >> config.toml
thèmes de CD
#Clonez ou téléchargez dans ce dossier le thème qui nous plaît.
git clone https://github.com/adityatelange/hugo-PaperMod
# Nous entrons dans le dossier de notre thème
cd hugo-PaperMod
# Nous supprimons le dossier .git de ce thème afin qu'il ne nous cause pas de problèmes
#lors du téléchargement de notre page
rm -rf .git
```
 

Avec cela, nous aurons le thème installé et nous pourrons démarrer notre site en utilisant

```hugo-serveur
```
Après l'avoir démarré, la commande renverra une URL dans laquelle nous pourrons voir notre site pendant que ce serveur est activé.
Créer des articles dans Hugo

Pour créer des articles dans Hugo, nous devons aller dans le dossier de contenu, et à l'intérieur du dossier de publication, nous pouvons commencer à les écrire au format MarkDown ou MD en abrégé.

Au moment où nous écrivons ceci, il sera ajouté au site et visible sur notre serveur local.
Ci-dessous, je laisse un lien vers une vidéo pour mieux comprendre comment se passe l'installation
{{<youtube tPP-P289BbY>}}