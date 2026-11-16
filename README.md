# Margo

Gérez la bibliothèque de votre tablette reMarkable 1 ou 2 depuis Windows ou Linux, par USB.
Aucun compte, aucun cloud, aucune télémétrie : tout reste sur votre PC et votre tablette. Rien n'est envoyé à l'auteur, sauf le message que vous décidez d'envoyer vous-même depuis « Contactez-nous ».

**[Télécharger la dernière version](https://github.com/Gitnmercury/Margo-apps/releases/latest)**

Projet indépendant, ni affilié, ni approuvé, ni sponsorisé par reMarkable AS.

## Aperçu

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="captures/03-bibliotheque-sombre.png">
    <img src="captures/03-bibliotheque-clair.png" alt="Bibliothèque d'une reMarkable 2 dans Margo : dossiers, recherche, import, export et aperçu" width="860">
  </picture>
</p>

<p align="center"><em>La bibliothèque de la tablette, en thème clair ou sombre selon votre réglage GitHub.<br>
Captures réalisées avec des noms de dossiers et de livres d'exemple.</em></p>

<p align="center">
  <img src="captures/00-installeur.png" alt="Assistant d'installation de Margo : bienvenue et déclaration d'usage particulier" width="560">
</p>

<p align="center"><em>La première installation, sans droit administrateur. L'assistant reconnaît aussi une installation existante<br>
(y compris l'ancienne rM Desktop) et propose de la mettre à jour.</em></p>

<p align="center">
  <img src="captures/01-installation.png" alt="Copie des fichiers avec une astuce" width="330">
  <img src="captures/02-installation-terminee.png" alt="Installation terminée" width="330">
</p>

<p align="center"><em>Pendant la copie, quelques astuces défilent ; puis Margo se lance.</em></p>

<p align="center">
  <img src="captures/08-demarrage.png" alt="Écran de démarrage de Margo : « Bienvenue sur Margo, reMarkable 2 détectée »" width="330">
</p>

<p align="center"><em>Au premier lancement : l'écran d'accueil, puis la détection de la tablette branchée en USB.</em></p>

<p align="center">
  <img src="captures/06-guide-demarrage.png" alt="Guide de démarrage de Margo : brancher, connecter une fois, importer, sauvegarder" width="420">
  <img src="captures/07-contactez-nous.png" alt="Aide, Contactez-nous : bogue, avis ou question, tout est facultatif" width="420">
</p>

<p align="center"><em>Le menu Aide : guide de démarrage et « Contactez-nous ». Rien ne part sans votre clic sur Envoyer.</em></p>

<p align="center">
  <img src="captures/04-mode-veille.png" alt="Mode veille de Margo : une tablette avec un petit cœur et le message « Je fais une petite pause »" width="760">
</p>

<p align="center"><em>Après une minute sans activité, l'application se met en veille avec un petit cœur qui respire.<br>
Un mouvement de souris la réveille.</em></p>

<p align="center">
  <img src="captures/05-tablette-deconnectee.png" alt="Margo quand la tablette est débranchée : « Tablette déconnectée, branche la reMarkable avec le câble USB-C »" width="760">
</p>

<p align="center"><em>Quand la tablette est débranchée, l'application le dit gentiment.<br>
La fenêtre se réactive toute seule dès que le câble est rebranché.</em></p>

## Fonctions

- Parcourir la bibliothèque de la tablette, rechercher, prévisualiser.
- Importer PDF, EPUB, Word et images (conversion en PDF et OCR à la demande), par glisser-déposer.
- Exporter, renommer, épingler, supprimer (corbeille), créer des dossiers ; sélection multiple.
- Exporter les carnets manuscrits.
- Lire les premières pages d'un livre EPUB, sans autre logiciel.
- Ajouter ses propres modèles de page (agenda, quadrillage…) sur la tablette.
- Sauvegarde chiffrée de la tablette.
- Image de l'écran de veille de la tablette ; connexion par Wi-Fi possible (l'USB reste prioritaire).
- Aide › Contactez-nous : bogue, avis ou question, préparés dans votre messagerie (Margo n'envoie rien elle-même).
- Thèmes clair, sombre et automatique.

## Prérequis

- Windows 10 (version 2004 ou plus) ou Windows 11, avec OpenSSH (installé par défaut) ;
  ou Linux avec Python 3.10 ou plus (Ubuntu 22.04, Debian 12 ou plus récent).
- Une reMarkable 1 ou 2, branchée en USB.
- Le mot de passe de la tablette (Réglages > Aide > À propos > Copyrights et licences), saisi une
  seule fois au premier lancement.
- Testé sur reMarkable 2, logiciel 3.28.0.172.

## Installation sous Windows

1. Téléchargez `install_margo.exe` dans la [dernière version](https://github.com/Gitnmercury/Margo-apps/releases/latest).
2. Lancez-le et suivez l'assistant. Aucun droit administrateur n'est demandé, rien n'est téléchargé.
   Il vous demande de confirmer l'usage particulier (gratuit, à titre privé) ; pour un usage professionnel,
   le bouton « Licence entreprise » indique comment demander une licence.
3. Au premier lancement, branchez la tablette en USB et saisissez son mot de passe (une seule fois).

Windows peut afficher « Windows a protégé votre ordinateur » : l'installeur est signé avec un
certificat personnel de l'auteur, que Windows ne connaît pas encore. Cliquez sur « Informations
complémentaires », puis « Exécuter quand même ». Vous pouvez vérifier le fichier avec son
empreinte SHA-256, indiquée dans chaque version.

Désinstallation : menu Démarrer > Margo > Désinstaller, ou Paramètres > Applications.

Margo est le nouveau nom de rM Desktop : si l'ancienne version est installée, l'assistant la remplace,
reprend vos réglages et supprime l'ancien dossier et les anciens raccourcis.

## Installation sous Linux (Ubuntu, Debian, Linux Mint…)

1. Téléchargez `margo_<version>_all.deb` dans la [dernière version](https://github.com/Gitnmercury/Margo-apps/releases/latest).
2. Dans un terminal, depuis le dossier du téléchargement :

   ```
   sudo apt install ./margo_*_all.deb
   ```

   `apt` installe aussi ce qui manque (Python, Tkinter, OpenSSH).
3. Lancez « Margo » depuis le menu des applications, ou `margo` dans un terminal.

Fonctions en option : aperçu des pages PDF (`sudo apt install python3-fitz`), OCR
(`tesseract-ocr tesseract-ocr-fra`), conversion Word (`libreoffice-writer`).

Désinstallation : `sudo apt remove margo`. Le paquet remplace l'ancien `rm-desktop` (ancien nom de Margo).

## Noms

Margo s'appelait rM Desktop jusqu'à la version 1.1.0. Les fichiers des anciennes versions (`install_remarkable.exe`,
`rm-desktop_1.1.0_all.deb`) gardent leur ancien nom. L'installation de Margo reprend l'ancienne installation et vos réglages.

## Licence et confidentialité

Libre d'utilisation, sous réserve, pour les particuliers à titre privé. Sans accord écrit, il ne peut être vendu,
loué, intégré à une offre payante, redistribué en dehors de cette page, modifié pour être diffusé, ni utilisé à titre professionnel
ou par une entreprise, une administration ou une association (licence entreprise : [licence@ohtna.fr](mailto:licence@ohtna.fr)).
Voir [LICENSE.md](LICENSE.md), [PRIVACY.md](PRIVACY.md) et [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

Le code source n'est pas publié. Le paquet Linux contient la version Python de l'application sous
forme lisible : la même licence s'y applique.

## Auteur et contact

Margo est créé et maintenu par Anthony BELKACEM, pour son entreprise individuelle
Anthony BELKACEM EI.

Pour les questions générales et le support : [apps@ohtna.fr](mailto:apps@ohtna.fr)

Pour les demandes de licence, d'autorisation d'utilisation, de partenariat ou de prestation :
[licence@ohtna.fr](mailto:licence@ohtna.fr)
