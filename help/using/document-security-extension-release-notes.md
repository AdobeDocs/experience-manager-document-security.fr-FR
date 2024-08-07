---
title: AEM Document Security for Microsoft Office – Notes de mise à jour
description: Lisez les notes de mise à jour avant d’installer AEM Document Security 6.2 Extension for Microsoft Office.
uuid: f6ab73d4-ac4e-4fff-9bb8-917b75401653
content-type: reference
topic-tags: installing
discoiquuid: c9342c28-8289-4831-a613-4bc03431f557
exl-id: 582f10bb-60d2-46ed-b81d-5818a040edc6
source-git-commit: 3b6a686966fb8d006bed8cc4a4bf5eebe0dfb030
workflow-type: ht
source-wordcount: '1010'
ht-degree: 100%

---

# AEM Document Security for Microsoft Office – Notes de mise à jour{#aem-document-security-for-microsoft-office-release-notes}

## Nouveautés dans AEM Document Security for Microsoft Office {#whats-new-in-aem-document-security-for-microsoft-office}

* **Prise en charge d’Office 2019** : Document Security Extension for Microsoft Office prend dorénavant Microsoft Office 2019 en charge. Son fonctionnement avec les applications Microsoft Office 2019 installées dans le cadre d’Office 365 est également prévu.

>[!NOTE]
>
>Le document utilise les termes suivants de manière interchangeable :
>
>* Adobe Experience Manager Document Security pour Microsoft Office
>* Extension Adobe Experience Manager Document Security pour Microsoft Office
>* Extension Document Security pour Microsoft Office

## Installation et configuration d’AEM Document Security Extension for Microsoft Office {#installing-and-configuring-aem-document-security-extension-for-microsoft-office}

Cette version de Document Security Extension for Microsoft Office est compatible avec les modules complémentaires Adobe LiveCycle Rights Management ES2 et versions ultérieures, et Document Security pour AEM Forms.

Consultez les informations présentées dans ce document avant d’installer AEM Document Security Extension for Microsoft Office. Pour des instructions d’installation détaillées, consultez l’article [Installation et configuration de l’extension AEM Document Security pour Microsoft Office](installing-configuring-aemdsext.md).

## Problèmes résolus {#fixed-issues}

* Affichage vertical des chaînes et ajout des sauts de ligne erronés au contenu. (CQ-4201054)

## Problèmes connus {#known-issues}

### Plug-ins tiers non pris en charge {#third-party-plug-ins-not-supported}

AEM Document Security Extension pour Microsoft Office ne fonctionne pas avec les plug-ins tiers. Désinstallez tous les plug-ins tiers de Microsoft Office avant d’installer l’extension Document Security pour Microsoft Office.

### Options de menu désactivées dans Microsoft Word, Excel et PowerPoint {#disabled-menu-options-in-microsoft-word-excel-and-powerpoint}

AEM Document Security Extension for Microsoft Office est doté de fonctionnalités de protection intégrées pour protéger les documents, les feuilles de calcul et les présentations. Cela désactive certaines des options des menus d’Excel, Word et PowerPoint.

### Restrictions pour Microsoft Office 2013, 2016 et 2019 {#restrictions-for-microsoft-office}

Dans Microsoft Office, les options suivantes ne sont pas disponibles lors d’une session protégée :

* Microsoft Office 2016 ou Microsoft Office 2019

   * Fichier > Enregistrer sous
   * Fichier > Historique
   * Fichier > Partager
   * Fichier > Exporter
   * Fichier > Publier
   * Fichier > Compte
   * Fichier > Infos > Protéger le document/le classeur/la présentation > Chiffrer par un mot de passe
   * Fichier > Infos > Protéger le document > Ajouter une signature numérique
   * Fichier > Infos > Protéger le document > Marquer comme final
   * L’option de partage est située en haut à droite

* Microsoft Office 2013

   * Fichier > Enregistrer sous
   * Fichier > Partager
   * Fichier > Exporter
   * Fichier > Compte
   * Fichier > Infos > Protéger le document/le classeur/la présentation > Chiffrer par un mot de passe
   * Fichier > Infos > Protéger le document > Ajouter une signature numérique
   * Fichier > Infos > Protéger le document > Marquer comme final

### Ouverture d’un document protégé à partir de SharePoint Server {#opening-a-protected-document-from-sharepoint-server}

Pour ouvrir un document protégé dans l’extension Document Security pour Microsoft Office à partir de SharePoint Server, ouvrez d’abord le programme Microsoft Office associé (Word, Excel ou PowerPoint), sans quoi le document risque de ne pas s’ouvrir. Un message d’erreur vous indique d’installer le plug-in approprié. Il est donc recommandé d’ouvrir le programme Microsoft Office associé avant d’ouvrir un document protégé dans Document Security Extension for Microsoft Office à partir de SharePoint Server.

(Facultatif) Il est recommandé de vider votre dossier de cache avant d’ouvrir un document protégé dans Document Security Extension for Microsoft Office à partir de SharePoint Server.

Lorsque vous ouvrez un document protégé à partir de SharePoint Server, toutes les autorisations du document sont désactivées, quelle que soit la politique appliquée.

### Application d’une politique avec un filigrane dynamique à Microsoft Excel 2013, Microsoft Excel 2016 et Microsoft Excel 2019 sans qu’aucune imprimante ne soit installée {#apply-a-policy-with-a-dynamic-watermark-to-microsoft-excel-microsoft-excel-and-microsoft-excel-file-with-no-printer-installed}

L’application d’une politique avec filigrane dynamique à des fichiers Excel 2013, 2016 ou 2019 sur un ordinateur sans imprimante installée entraîne l’erreur suivante : « Erreur interne lors de l’application du filigrane dynamique ». Cette erreur s’affiche également lorsque vous ouvrez de nouveau le fichier protégé. Le filigrane n’est pas appliqué et n’est pas visible depuis Afficher > Mise en page.

### Désactivation de la prévention de l’exécution des données Windows pour les applications Office prises en charge {#disable-windows-data-execution-prevention-for-supported-office-applications}

Il est recommandé de désactiver le paramètre Windows Data Execution Prevention (DEP) lors de l’utilisation des applications Document Security Extension for Microsoft Office.

### Les fichiers Microsoft Office partagés ne peuvent pas être protégés à l’aide de Document Security Extension. {#shared-microsoft-office-files-cannot-be-protected-using-document-security-extension}

Quand vous protégez un fichier Microsoft Office partagé à l’aide de Document Security Extension, une erreur se produit et le fichier partagé n’est pas sécurisé.

### Démarrage des applications Office sur un ordinateur contenant Document Security Extension for Microsoft Office et McAfee VirusScan {#starting-office-applications-on-a-machine-containing-document-security-extension-for-microsoft-office-and-mcafee-virusscan}

Pour garantir un démarrage correct des applications Office sur un ordinateur doté de Document Security et de McAfee VirusScan avec l’option Analyse à l’accès activée, désactivez l’option Protection contre le débordement de la mémoire tampon dans la console de McAfee VirusScan.

### Installer Document Security Extension for Microsoft Office sur un ordinateur doté de Microsoft Office dans une langue non prise en charge {#installing-document-security-extension-for-microsoft-office-on-a-machine-with-an-unsupported-microsoft-office-language}

Avant d’installer Document Security Extension for Microsoft Office sur un ordinateur où une application Microsoft Office est installée dans une langue non prise en charge, vous devez ouvrir l’application Office au moins une fois.

### Le bouton Synchronisation hors connexion est activé même lorsque l’utilisateur ne dispose pas d’autorisations hors connexion {#synchronize-offline-button-is-enabled-even-when-a-user-does-not-have-offline-permissions}

Le bouton de synchronisation pour un accès hors connexion est disponible, même lorsque l’utilisateur ne dispose pas d’autorisations hors connexion pour le document. Toutefois, ce bouton est inopérant.

### Pas de prise en charge des versions d’évaluation de Microsoft Office {#no-support-for-trial-versions-of-microsoft-office}

L’extension Document Security pour Microsoft Office ne prend pas en charge les versions d’évaluation de Microsoft Office. Avant d’installer l’extension, assurez-vous que vous avez installé une copie autorisée de Microsoft Office et que celle-ci est activée.

### Impossible d’ouvrir des fichiers Microsoft Office protégés {#unable-to-open-a-protected-microsoft-office-files}

Si la vue protégée de Microsoft Office est activée, Rights Management Extension ne peut pas ouvrir les fichiers Microsoft Excel (XLS, XLSX) et Microsoft PowerPoint (PPT) protégés depuis un emplacement distant.

### Les cellules du document Microsoft Excel contenant une image ou une couleur d’arrière-plan, s’affichent sur le filigrane {#cells-of-microsoft-excel-document-containing-an-image-or-background-color-appear-on-top-of-watermark}

Si une cellule d’un document Excel comporte une image ou une couleur d’arrière-plan et qu’un filigrane dynamique est appliqué, l’image ou la couleur recouvre le filigrane. Cet exemple montre que le filigrane est recouvert par l’image ou la couleur d’arrière-plan de la cellule.

### Problème d’utilisation avec plusieurs certificats {#usability-issue-with-multiple-certificates}

Si plusieurs certificats sont présents sur l’ordinateur client et que l’utilisateur ou l’utilisatrice annule la boîte de dialogue de sélection du certificat, la boîte de dialogue s’affiche à nouveau. L’utilisateur ou l’utilisatrice doit annuler la boîte de dialogue deux fois.

### Microsoft PowerPoint permet de modifier les documents protégés. {#microsoft-powerpoint-allows-editing-protected-documents}

Lors d’une tentative de modification d’un document protégé, Microsoft PowerPoint affiche le message « Vous n’avez pas l’autorisation de modifier ce document. Vous ne pouvez pas enregistrer vos modifications. » Après la fermeture du message, les utilisateurs et les utilisatrices peuvent continuer à ajouter du texte ou à modifier le document. Toutefois, les modifications apportées aux documents protégés ne sont pas enregistrées.

Le comportement indiqué ci-dessus se manifeste dans PowerPoint 2013, PowerPoint 2016 et PowerPoint 2019.
