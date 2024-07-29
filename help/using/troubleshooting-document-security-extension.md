---
title: Dépannage d’AEM Document Security Extension for Microsoft Office
description: Si vous rencontrez des problèmes lors de l’installation, de la configuration ou de l’utilisation d’AEM Document Security Extension for Microsoft Office, suivez les instructions figurant dans ce document.
uuid: 61001ca8-a25a-4879-98ac-563a6eb126e7
contentOwner: khsingh
content-type: reference
topic-tags: using
discoiquuid: bdc3f174-e417-4d3e-b3af-972cdcc10133
exl-id: 98f24032-0774-47f8-bcc5-1ee37b417833
source-git-commit: 3b6a686966fb8d006bed8cc4a4bf5eebe0dfb030
workflow-type: ht
source-wordcount: '284'
ht-degree: 100%

---

# Dépannage d’AEM Document Security Extension for Microsoft Office{#troubleshooting-aem-document-security-extension-for-microsoft-office}

## Dépannage des problèmes d’installation et de configuration {#troubleshootinginstallationandconfiguration}

Si vous rencontrez des problèmes pour installer et configurer l’extension AEM Document Security pour Microsoft Office, assurez-vous que vous avez soigneusement suivi les instructions figurant dans la section « Avant l’installation » de l’article [Installation](installing-configuring-aemdsext.md).

Si vous avez effectué l’installation et la configuration conformément à la documentation, consultez les sections suivantes qui abordent des problèmes similaires à ceux que vous rencontrez.

### Document Security Extension ne se charge pas lors du chargement des applications Microsoft Office. {#document-security-extension-fails-to-load-for-microsoft-office-applications}

La propriété LoadBehavior dans le registre Windows spécifie le comportement d’exécution du plug-in Document Security. Si la propriété LoadBehavior est définie sur 3, tous les plug-ins sont chargés automatiquement. Avant d’installer l’extension Document Security pour Microsoft Office, assurez-vous que la valeur de la propriété LoadBehavior est définie sur 3.

1. Effectuez une sauvegarde du registre Windows avant d’y apporter des modifications. Pour obtenir des instructions détaillées, consultez la section [Modifier le registre Windows](https://learn.microsoft.com/fr-fr/troubleshoot/windows-server/performance/windows-registry-advanced-users).
1. Dans l’éditeur de registre, accédez à HKEY_CURRENT_USER\Software\Microsoft\Office\Word\Addins\Adobe.DRMIntegration.WordAddin ou HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Word\Addins\Adobe.DRM.
1. Définissez la valeur de la propriété **LoadBehavior** sur 3.

1. Fermez l’éditeur du registre.

Pour plus d’informations sur LoadBehavior, consultez l’article [Entrées du registre pour les modules complémentaires VSTO](https://learn.microsoft.com/fr-fr/visualstudio/vsto/registry-entries-for-vsto-add-ins?view=vs-2022&amp;redirectedfrom=MSDN#LoadBehavior).

## Dépannage des tâches d’administration {#admintasks}

Cette section aborde les problèmes qui pourraient survenir avec votre installation d’AEM Document Security Extension.

### Les applications Microsoft Office ne se lancent pas correctement après l’installation de Document Security Extension {#microsoft-office-applications-dont-start-smoothly-on-installing-document-security-extension}

Pour garantir un démarrage correct des applications Office sur un ordinateur doté de l’extension Document Security et de McAfee VirusScan avec l’option Analyse à l’accès activée, désactivez l’option Protection contre le débordement de la mémoire tampon dans la console McAfee VirusScan.
