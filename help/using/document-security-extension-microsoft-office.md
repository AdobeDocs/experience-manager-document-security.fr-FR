---
title: Présentation d’AEM Document Security Extension pour Microsoft® Office
description: À l’aide de l’extension Document Security pour Microsoft® Office, vous pouvez appliquer des paramètres de confidentialité prédéfinis à vos fichiers Microsoft® Office.
uuid: a5428c50-fae3-4823-9e6f-0f5306e7248f
content-type: reference
topic-tags: using
discoiquuid: cf93f9f5-1fb6-4909-815e-0ffb8c6ea6d1
exl-id: 3e07c031-3f88-4bde-bdb3-b136ef5f9527
source-git-commit: 3b6a686966fb8d006bed8cc4a4bf5eebe0dfb030
workflow-type: ht
source-wordcount: '1248'
ht-degree: 100%

---

# Présentation d’AEM Document Security Extension for Microsoft® Office{#introduction-to-aem-document-security-extension-for-microsoft-office}

Adobe® Experience Manager Document Security Extension for Microsoft® Office garantit que seules les personnes autorisées ont accès à vos fichiers Word, Excel et PowerPoint contenant votre propriété intellectuelle. À l’aide de Document Security Extension for Microsoft® Office, vous pouvez appliquer des paramètres prédéfinis de confidentialité à vos fichiers.

L’extension Document Security pour Microsoft® Office améliore LiveCycle Rights Management et Document Security pour Adobe Experience Manager Forms. Elle protège les fichiers Office et permet aux utilisateurs et aux utilisatrices autorisés d’accéder à des fichiers protégés par une politique, conformément aux paramètres de confidentialité définis.

## Protection de la propriété intellectuelle à l’aide de Document Security {#how-document-security-protects-intellectual-property}

Document Security garantit que seules les personnes autorisées peuvent utiliser les fichiers contenant votre propriété intellectuelle. Grâce à Document Security, vous pouvez protéger les fichiers en appliquant des politiques de confidentialité. Une *politique* recense des informations telles que les paramètres de confidentialité et la liste de personnes utilisatrices autorisées. Les paramètres spécifiés dans une politique déterminent dans quelle mesure un destinataire peut utiliser un fichier auquel vous appliquez cette politique. Vous pouvez par exemple indiquer si les destinataires peuvent imprimer ou copier du texte ou enregistrer des modifications.

Les administrateurs et les utilisateurs de Document Security créent des politiques. Les administrateurs créent des politiques organisationnelles accessibles à tous les utilisateurs autorisés. Les administrateurs ou coordinateurs de politiques peuvent également créer des groupes de politiques appelés *jeux de politiques* mis à la disposition d’un sous-ensemble d’utilisateurs. Les utilisateurs peuvent créer leurs propres politiques, qu’eux seuls peuvent utiliser. Les administrateurs et les administratrices, les coordinateurs et les coordinatrices de jeux de politiques et les utilisateurs et les utilisatrices créent des politiques à l’aide des pages web de Document Security.

Bien qu’elles soient stockées dans Document Security, vous pouvez appliquer les politiques à des fichiers dans Word, Excel ou PowerPoint. Lorsque vous appliquez une politique à un fichier, les informations qu’il contient sont protégées par les paramètres de confidentialité spécifiés dans cette politique. Lorsque vous distribuez le fichier protégé par une politique, seules les personnes destinataires autorisées peuvent accéder à son contenu.

En utilisant une politique pour protéger un fichier, vous maintenez un contrôle continu sur ce document, même après sa distribution. Vous pouvez contrôler les événements afin d’effectuer un suivi de quand et comment les personnes destinataires utilisent votre fichier. Vous pouvez également apporter des modifications à la politique, empêcher des utilisateurs et des utilisatrices de continuer à accéder au fichier et modifier la politique associée au fichier.

## Fonctionnement des politiques {#how-policies-work}

Les politiques contiennent des informations sur les utilisateurs et utilisatrices autorisés et les paramètres de confidentialité à appliquer à la propriété intellectuelle. Document Security reconnaît les utilisateurs et les utilisatrices inclus dans une liste LDAP ou Active Directory liée. Il s’agit également de personnes qui ont été invitées à s’inscrire auprès de Document Security ou pour lesquelles l’administrateur a créé un compte.

Les paramètres de confidentialité d’une politique déterminent comment les destinataires peuvent utiliser les fichiers protégés par cette politique. Par exemple, les politiques indiquent si les destinataires peuvent imprimer des fichiers, copier du contenu dans d’autres fichiers ou enregistrer des modifications dans des fichiers protégés. Les politiques peuvent également spécifier différents paramètres de confidentialité pour divers utilisateurs.

Lorsque vous appliquez une politique à un fichier, les informations qu’il contient sont protégées par les paramètres de confidentialité spécifiés dans cette politique. Si vous distribuez le fichier, Document Security peut authentifier les destinataires qui tentent de l’ouvrir et autoriser l’accès en fonction des privilèges spécifiés dans la politique.

Après l’application d’une stratégie à un fichier, les paramètres de confidentialité de la stratégie peuvent être modifiés à tout moment. Cela vous permet d’ajouter ou de supprimer des utilisateurs et des utilisatrices autorisés ou de modifier leurs privilèges après la réception du fichier. La politique appliquée au fichier peut être modifiée. De plus, l’accès au fichier peut être révoqué, de manière que toute personne disposant d’une copie du fichier ne puisse plus l’ouvrir.

Si l’utilisation hors connexion est autorisée par la politique, les destinataires peuvent également utiliser les fichiers protégés par la politique hors connexion (sans liaison avec Internet ou le réseau) pendant la période spécifiée dans la politique.

## Fonctionnement des fichiers protégés par une politique {#how-policy-protected-files-work}

Pour qu’un utilisateur ou une utilisatrice puisse ouvrir et utiliser des fichiers Word, Excel et PowerPoint protégés par une politique, celle-ci doit inclure l’utilisateur ou l’utilisatrice comme destinataire. Ou bien, elle doit autoriser un accès anonyme. L’utilisateur ou l’utilisatrice doit également avoir installé l’extension Document Security pour Microsoft® Office. Pour remettre un fichier protégé par une politique à une personne qui ne dispose pas de l’extension Document Security pour Microsoft® Office, vous pouvez lui fournir une copie du logiciel. Vous pouvez également lui indiquer comment le télécharger à partir de votre site web. Si vous ne disposez pas du programme d’installation, vous pouvez le télécharger à partir de la [page des téléchargements](https://experienceleague.adobe.com/fr/docs/experience-manager-document-security/using/download-installer).

Lorsqu’un utilisateur ou une utilisatrice tente d’ouvrir un fichier protégé par une politique, l’extension Document Security pour Microsoft® Office se connecte à Document Security pour authentifier cet utilisateur ou cette utilisatrice. Si Document Security est configuré pour contrôler l’utilisation des fichiers, l’utilisateur voit une notification indiquant que l’utilisation des fichiers est contrôlée. Document Security détermine les autorisations de fichiers à accorder à l’utilisateur, qui peut ensuite utiliser le fichier en fonction des paramètres de politique, dans les conditions suivantes :

* indéfiniment ou pendant la période de validité spécifiée dans la politique ;
* jusqu’à ce que l’administrateur ou la personne ayant appliqué la politique révoque l’accès au fichier ou modifie la politique.

  Si la personne qui a appliqué la stratégie la modifie ou révoque l’accès au fichier, les autorisations de la personne utilisatrice concernant le fichier sont modifiées ou supprimées même si elle dispose déjà du fichier. Si le fichier lui-même a été révoqué, une URL peut être fournie à la personne utilisatrice pour obtenir une copie mise à jour.

  Si la politique autorise l’accès hors ligne, les utilisateurs et les utilisatrices peuvent ouvrir des fichiers protégés par une politique sans connexion Internet ou sans connexion réseau pendant la période d’ouverture hors connexion spécifiée. Lorsque la période d’ouverture hors connexion se termine, l’utilisateur ou l’utilisatrice doit se connecter et se synchroniser avec Document Security, ce qui démarre une nouvelle période d’ouverture.

  Si la politique autorise l’accès hors ligne, les utilisateurs et les utilisatrices peuvent ouvrir des fichiers protégés par une politique sans connexion Internet ou sans connexion réseau pendant la période d’ouverture hors connexion spécifiée. Les événements tels que les tentatives d’ouverture du nouveau fichier sont également contrôlés et enregistrés comme pour le fichier original.

## Utiliser Document Security pour protéger vos fichiers {#using-document-security-to-protect-your-files}

Vous pouvez utiliser des stratégies pour protéger vos fichiers dans différentes situations.

Par exemple, une entreprise de fabrication accepte les offres de fournisseurs qui proposent des pièces pour un nouveau produit. L’entreprise de fabrication doit fournir aux entreprises candidates les informations exclusives pour finaliser leurs offres. Le fabricant utilise Document Security pour protéger les fichiers par le biais d’une politique qui permet aux candidats d’ouvrir les fichiers et d’afficher les informations. Cependant, les candidats ne peuvent pas modifier, imprimer ni copier les fichiers et les personnes dépourvues de l’autorisation nécessaire ne peuvent pas ouvrir les fichiers.

Après avoir accepté une offre, le fabricant met à jour la politique afin d’accorder à la personne à l’origine de cette offre les autorisations nécessaires pour imprimer, copier et enregistrer les modifications en local. Le fabricant supprime également les personnes dont les offres n’ont pas été acceptées, révoquant ainsi leur autorisation d’ouvrir les fichiers.

En travaillant avec l’entreprise candidate retenue, les ingénieurs et ingénieures de l’entreprise de fabrication modifient certaines des spécifications de conception contenues dans les dossiers. Pour publier les nouvelles spécifications, le fabricant révoque l’accès à certains fichiers et publie de nouvelles versions. Lorsque les ingénieurs de l’entreprise retenue tentent d’ouvrir le fichier, un message s’affiche indiquant que l’accès au fichier a été révoqué. Le message contient une URL permettant de télécharger une nouvelle version du fichier.

## Informations supplémentaires {#additional-information}

Pour en savoir plus sur Document Security d’AEM, consultez les ressources présentées dans le tableau ci-dessous :

<table >
 <tbody>
  <tr>
   <th><p>Pour obtenir des informations sur</p> </th>
   <th><p>Voir</p> </th>
  </tr>
  <tr>
   <td><p>Aide destinée à l’administration d’AEM Forms</p> </td>
   <td><p><a href="https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/forms/administrator-help/get-started/configure-general-aem-forms-settings">Aide à l’administrateur</a> ou, dans les pages administratives de Document Security, cliquez sur le lien Aide dans le coin supérieur droit d’une page.</p> </td>
  </tr>
  <tr>
   <td><p>Mises à jour des correctifs, notes techniques et informations supplémentaires sur cette version du produit.</p> </td>
   <td><p><a href="https://experienceleague.adobe.com/fr?support-solution=General&amp;support-tab=home&amp;lang=fr#support">Support technique d’Experience Cloud</a></p> </td>
  </tr>
 </tbody>
</table>
