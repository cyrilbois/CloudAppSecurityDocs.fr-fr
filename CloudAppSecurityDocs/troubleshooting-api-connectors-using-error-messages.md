---
title: "Résolution des problèmes des connecteurs API à l’aide de messages d’erreur | Documentation Microsoft"
description: "Cette rubrique fournit une liste de messages d’erreur relatifs aux connecteurs API ainsi que des solutions recommandées pour chacun."
keywords: 
author: rkarlin
ms.author: rkarlin
manager: mbaldwin
ms.date: 10/15/2016
ms.topic: article
ms.prod: 
ms.service: cloud-app-security
ms.technology: 
ms.assetid: 4b6ac04a-4653-4c4a-bd6f-5926743475cc
ms.reviewer: reutam
ms.suite: ems
translationtype: Human Translation
ms.sourcegitcommit: ed4ea71b24767d3602d40894d1cbac7447bcd8a2
ms.openlocfilehash: 61492a0126bff93c2a61d5d1317784ca96687df7


---

# <a name="troubleshooting-api-connectors-using-error-messages"></a>Résolution des problèmes des connecteurs API à l’aide de messages d’erreur
|Message d’erreur|Application correspondante|Description|Solution|
|----|----|----|----|
|HttpRequestFailure: 400 Requête incorrecte retourné par le serveur : {"error":{"code":"AF20012","message":"L’ID de client spécifié (emplacement de Tenant_ID) est configuré de façon incorrecte dans le système."|Office 365 |Aucune licence Office 365 attribuée n’a été trouvée. |Attribuez au moins une licence Office 365 à votre client.| 
|AuthFatalFailureException: com.box.boxjavalibv2.exceptions.BoxServerException: {"error":"invalid_grant","error_description":"Jeton d’actualisation non valide"}|Box|Le jeton d’actualisation Box n’est pas valide|Suivez le processus pour reconnecter Box à Cloud App Security.|
|BoxRestException: Échec de l’analyse de la réponse.|Box|Erreur interne|Cliquez à nouveau sur le lien Tester maintenant pour tester la connexion à Box.|
|ContextManagerServiceException: com.adallom.adalib.httputils.exceptions.TokenRefreshException: {"error":"invalid_grant","error_description":"Jeton d’actualisation non valide"}'|Box|Le jeton d’actualisation Box n’est pas valide|Suivez le processus pour reconnecter Box à Cloud App Security.|
|BoxServerException: L’utilisateur ne peut pas accéder à cette fonctionnalité sans avoir une entreprise|Box|Le compte Box n’est pas un compte d’entreprise.|Mettez à niveau votre licence Box vers la version d’entreprise de Box, puis suivez le processus pour reconnecter Box à Cloud App Security.|
|BoxServerException: Non autorisé - Autorisation impossible avec ce service|Box|L’administrateur Box a supprimé l’application Cloud App Security dans Box.|Suivez le processus pour reconnecter Box à Cloud App Security.|
|HttpRequestFailure: 401 Non autorisé retourné par le serveur|Okta|Le jeton Okta n’est pas valide.|Suivez le processus pour reconnecter Okta à Cloud App Security.|
|IOException:|Okta|Erreur interne|Contactez le support technique|
|HttpRequestFailure: 404 Non trouvé retourné par le serveur|Okta|Erreur interne|Contactez le support technique|
|SocketTimeoutException: Expiration du délai d’attente de lecture|Salesforce|Erreur interne|Cliquez à nouveau sur le lien Tester maintenant pour tester la connexion à Salesforce.|
|HttpRequestFailure: 400 Requête incorrecte retourné par le serveur|Salesforce|La connexion à Salesforce n’a pas été établie ou a expiré.|Suivez le processus pour reconnecter Salesforce à Cloud App Security.|
|HttpRequestFailure: 401 Non autorisé retourné par le serveur|Office 365|Problème interne|Cliquez à nouveau sur le lien Tester maintenant|
|TokenRefreshException: {"error":"invalid_grant","error_description":"AADSTS70002: Erreur de validation des informations d’identification. AADSTS70008: Le jeton d’actualisation ou le code d’autorisation fourni a expiré. Envoyez une nouvelle demande d’autorisation interactive pour cet utilisateur et cette ressource.|Office 365|Jeton expiré|Suivez le processus pour reconnecter Office 365 à Cloud App Security.|
|SocketTimeoutException: Expiration du délai d’attente de lecture|Office 365|Erreur interne|Cliquez à nouveau sur le lien Tester maintenant|
|NullPointerException|Office 365|Erreur interne|Contactez le support technique|
|IgniteException|Office 365|Le domaine ou l’utilisateur ne sont pas valides|Réinitialisez vos paramètres et suivez le processus pour reconnecter Office 365 à Cloud App Security.|
|ContextManagerServiceException: com.adallom.adalib.httputils.exceptions.TokenRefreshException: {"error":"invalid_grant","error_description":"AADSTS70002: Erreur de validation des informations d’identification. AADSTS70008: Le jeton d’actualisation ou le code d’autorisation fourni a expiré. Envoyez une nouvelle demande d’autorisation interactive pour cet utilisateur et cette ressource.|Office 365|Le domaine ou l’utilisateur ne sont pas valides|Réinitialisez vos paramètres et suivez le processus pour reconnecter Office 365 à Cloud App Security.|
|HttpRequestFailure: 400 Requête incorrecte retourné par le serveur|Office 365|Erreur interne|Cliquez à nouveau sur le lien Tester maintenant dans quelques minutes et, s’il ne fonctionne pas, suivez le processus pour reconnecter Office 365 à Cloud App Security.|
|GoogleJsonResponseException: 401 Non autorisé|Google Apps|Accès refusé. Vous n’êtes pas autorisé à lire les enregistrements d’activité. L’utilisateur avec lequel vous vous connectez à Google Apps doit être un utilisateur administrateur.|Suivez le processus pour reconnecter Google Apps à Cloud App Security à l’aide d’un compte d’administrateur.|
|GoogleJsonResponseException: 403 Interdit|Google Apps|Problème d’exécution de l’API Google Apps.|Si vous venez de déployer le connecteur d’applications Cloud App Security pour Google Apps, vérifiez les éléments suivants : si vous avez cliqué sur Illimité, assurez-vous que votre compte Google Apps est vraiment illimité. Dans le cas contraire, réexécutez le connecteur d’applications et désélectionnez l’option pour un compte illimité. Vérifiez que les étendues que vous avez définies lors de l’installation sont correctes. S’il ne s’agit pas d’un nouveau déploiement et que cette erreur s’affiche, vous avez peut-être atteint la limite d’API pour aujourd’hui et les événements Google Apps seront renouvelés demain.|
|TokenResponseException: 400 Requête incorrecte|Google Apps|La connexion à Google Apps n’a pas été établie ou a expiré.|Suivez le processus pour reconnecter Google Apps à Cloud App Security.|
|RuntimeException: com.adallom.adalib.httputils.exceptions.HttpRequestFailure: 403 Interdit retourné par le serveur|ServiceNow|Les autorisations sont incorrectes|Suivez le processus pour reconnecter ServiceNow à Cloud App Security à l’aide d’un compte d’administrateur.|
|HttpRequestFailure: 401 Non autorisé retourné par le serveur|Exchange Online|L’utilisateur ou le mot de passe sont incorrects|Vérifiez que le nom d’utilisateur et le mot de passe sont corrects, et suivez le processus pour reconnecter Exchange Online à Cloud App Security.|
|HttpRequestFailure: 404 Non trouvé retourné par le serveur|Exchange Online|L’utilisateur que vous utilisez pour vous connecter à Exchange Online ne dispose pas d’une boîte aux lettres principale dans Exchange Online (par exemple, un utilisateur qui n’existe pas dans Azure AD ou un utilisateur qui existe dans Azure AD, mais ne dispose pas d’une licence Exchange Online).|Suivez le processus pour reconnecter Exchange Online à Cloud App Security à l’aide d’un nouveau compte d’administrateur.|
|NullPointerException|AWS|Erreur interne|Contactez le support technique|
|HttpRequestFailure: 500 Erreur interne au serveur retourné par le serveur|Toutes les applications|Une erreur s’est produite dans l’application.|Vérifiez l’état de l’application|
|Le service a expiré|Toutes les applications|Un délai d’attente a été détecté dans la connexion entre Cloud App Security et l’application. Un problème au niveau de l’application peut en être la cause.|Réessayez ultérieurement.|

## <a name="see-also"></a>Voir aussi  
[Activités quotidiennes pour protéger votre environnement cloud](daily-activities-to-protect-your-cloud-environment.md)   
[Pour obtenir un support technique, visitez la page de support assisté Cloud App Security.](http://support.microsoft.com/oas/default.aspx?prid=16031)   
[Les clients Premier peuvent également choisir Cloud App Security directement depuis le portail Premier.](https://premier.microsoft.com/)  
  
  


<!--HONumber=Oct16_HO4-->

