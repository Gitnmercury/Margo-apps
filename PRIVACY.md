# Confidentialité et données

**En résumé : tout reste sur votre PC et votre tablette. Rien n'est envoyé à l'auteur, sauf le message que vous décidez vous-même d'envoyer par « Contactez-nous ».**

## Ce que le logiciel ne fait pas

- Aucune collecte de données, aucun compte, aucun cloud.
- Aucune télémétrie, aucune statistique d'usage.
- Aucun appel réseau automatique vers Internet. « Vérifier les mises à jour » ouvre seulement la
  page de téléchargement dans votre navigateur, à votre demande.

## Échanges avec la tablette

Le logiciel ne communique qu'avec votre tablette reMarkable, branchée en USB (adresse locale
10.11.99.1), par SSH et, si elle est activée, par l'interface web USB de la tablette.

## Clé SSH

Au premier lancement, une clé de connexion est générée sur votre PC :
`%USERPROFILE%\.ssh\id_rm` (clé privée) et `id_rm.pub` (clé publique, copiée sur la tablette).
La clé privée ne quitte jamais votre PC.

## Mot de passe de la tablette

S'il est mémorisé, il est chiffré :

- sous Windows avec DPAPI : seul votre compte Windows, sur ce PC, peut le déchiffrer ;
- sous Linux (version Python) : scellé avec l'identifiant de la machine, dans un fichier
  accessible à votre seul compte.

Il est stocké dans `%APPDATA%\Margo\settings.json` (application Windows) ou
`~/.margo.json` (version Python). « Aide › Oublier le mot de passe mémorisé » l'efface.

## Sauvegardes

Les sauvegardes `.rmbak` sont chiffrées sur votre PC. Ni le logiciel ni l'auteur ne détiennent de
copie de leurs clés.

## Journaux de diagnostic

« Aide › Exporter les journaux de diagnostic » crée un fichier texte local, que vous seul décidez de
transmettre. Il contient : version et build du logiciel, version de Windows et d'OpenSSH, état de la
connexion, réglages d'affichage, derniers messages d'état et erreurs.

Il **ne contient jamais** : mot de passe (même chiffré), clé SSH, clé de sauvegarde, contenu ou noms
de vos documents.

## Contactez-nous

« Aide › Contactez-nous » (Je rencontre un bogue, Donner mon avis, Poser une question) prépare un message dans **votre** messagerie.
Margo n'envoie rien elle-même : vous relisez le message et vous cliquez sur Envoyer, ou vous fermez la fenêtre. Tout est facultatif.

Le message contient ce que vous avez écrit, vos étoiles et vos images si vous en joignez, votre adresse seulement si vous la saisissez (elle est alors aussi jointe, **chiffrée**, au code technique : seul l'auteur peut la lire avec sa clé privée, et la fenêtre vous le dit avant l'envoi), et des
informations techniques sans donnée personnelle, sous la forme d'un code court (par exemple `MG1-S2R4C3E3T1U1D1M2N1-V1.1.18`) que la fenêtre
vous explique en clair avant l'envoi : système, mémoire, cœurs du processeur et largeur d'écran par tranches, thème, type de licence, type
de document concerné (PDF, EPUB, carnet…), modèle de tablette et mode de connexion (USB ou Wi-Fi), version de Margo. Il ne contient jamais :
nom de fichier ou de document, adresse de la tablette, mot de passe, clé, chemin de votre dossier personnel. Pour un bogue, un rapport lisible
du même contenu s'ajoute. Un avis demande ces informations techniques (la case est cochée d'office) ; un bogue ou une question peuvent s'en passer.
Ce que vous envoyez est utilisé pour traiter votre retour, et pour cela seulement.

## Contact

apps@ohtna.fr - Anthony BELKACEM EI
