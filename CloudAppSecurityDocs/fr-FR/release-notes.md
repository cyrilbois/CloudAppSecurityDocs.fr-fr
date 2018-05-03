---
title: Nouveautés de Cloud App Security | Microsoft Docs
description: Cette rubrique est mise à jour fréquemment pour vous informer des nouveautés de la dernière version de Cloud App Security.
keywords: ''
author: rkarlin
ms.author: rkarlin
manager: mbaldwin
ms.date: 4/22/2018
ms.topic: article
ms.prod: ''
ms.service: cloud-app-security
ms.technology: ''
ms.assetid: d418ef3d-76ee-45d5-b5ae-21346e5239a3
ms.reviewer: reutam
ms.suite: ems
ms.openlocfilehash: f5c1d986648aef00b605f32d5c0a986d316604ed
ms.sourcegitcommit: d43a0f5c17e1961348dcbf315120046bb83305c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
*S’applique à : Microsoft Cloud App Security*


# <a name="whats-new-with-microsoft-cloud-app-security"></a>Nouveautés de Microsoft Cloud App Security

## <a name="cloud-app-security-release-121"></a>Cloud App Security version 121
Publication : 22 avril 2018

-   La préversion publique du **contrôle d’application d’accès conditionnel (anciennement appelé Proxy Cloud App Security)** a été enrichie de fonctionnalités qui approfondissent la visibilité et le contrôle de diverses applications. Vous pouvez à présent créer une stratégie de session avec un filtre *Type d’activité*, pour surveiller et bloquer un éventail d’activités propres à l’application. Ce nouveau filtre augmente les fonctionnalités existantes de contrôle de téléchargement de fichiers pour vous fournir un contrôle total sur les applications de votre organisation. Il fonctionne avec l’accès conditionnel Azure Active Directory pour offrir une visibilité en temps réel et un contrôle des sessions utilisateur présentant un risque (par exemple, les sessions avec des collaborateurs B2B ou des utilisateurs d’appareils non gérés). Pour plus d’informations, consultez [Stratégies de session](session-policy-aad.md).
-   Lancement progressif : les **stratégies de détection d’anomalie de Cloud App Security ont été améliorées** de sorte à inclure deux nouveaux types de détection des menaces : l’activité de ransomware et l’activité des utilisateurs en fin de contrat. Cloud App Security a étendu ses capacités de détection de ransomware à la détection d’anomalie pour garantir une couverture plus complète contre les attaques de ransomware complexes. Fort de notre expertise en recherche dans la sécurité visant à identifier les modèles comportementaux qui reflètent des activités de ransomware, Cloud App Security assure une protection complète et solide. L’activité des utilisateurs en fin de contrat vous permet de surveiller les comptes des utilisateurs en fin de contrat, qui ont été peut-être été déprovisionnés des applications d’entreprise, mais qui, dans de nombreux cas, conservent toujours l’accès à certaines ressources de l’entreprise. Pour plus d’informations, consultez [Obtenir instantanément une détection d’anomalie et une analytique comportementale](anomaly-detection-policy.md).


## <a name="cloud-app-security-release-120"></a>Cloud App Security version 120
Publication : 8 avril 2018

-   Pour Office 365 et Azure AD, nous développons progressivement la possibilité de détecter les applications internes en tant qu’activités de compte d’utilisateur effectuées par les applications Office 365 et Azure AD (internes et externes). Cela vous permet de créer des stratégies qui vous avertissent si une application effectue des activités inattendues et non autorisées. 
-   Lors de l’exportation d’une liste d’autorisations d’application au format csv, des champs supplémentaires, comme l’éditeur, le niveau d’autorisation et l’utilisation de la Communauté, sont ajoutés pour vous aider dans le processus d’investigation et de conformité.
-   L’application connectée ServiceNow a été améliorée pour que les activités de service interne ne soient plus enregistrées comme ayant été effectuées par « Invité » et ne déclenchent plus d’alertes fausses positives. Ces activités sont maintenant représentées par N/A comme toutes les autres applications connectées.


## <a name="cloud-app-security-release-119"></a>Cloud App Security version 119
Date de publication : 18 mars 2018

-   La page des plages d’adresses IP contient les adresses IP intégrées qui sont découvertes par Cloud App Security. Cela inclut les adresses IP des services cloud identifiés, comme Azure et Office 365, ainsi que le flux de Threat Intelligence qui enrichit automatiquement les adresses IP avec des informations sur les adresses IP risquées connues. 
-   Lorsque Cloud App Security tente d’exécuter une action de gouvernance sur un fichier, mais échoue parce que le fichier est verrouillé, il retente automatiquement l’action de gouvernance. 

## <a name="cloud-app-security-release-118"></a>Cloud App Security version 118
Date de publication : 4 mars 2018

- Vous pouvez désormais tirer parti de la découverte du Shadow IT de Microsoft Cloud App Security et des fonctions de surveillance de vos propres applications personnalisées propriétaires. La nouvelle possibilité d’ajouter des applications personnalisées à Cloud Discovery vous permet de surveiller l’utilisation des applications et d’être averti des modifications apportées au modèle d’utilisation. Pour plus d’informations, consultez [Protection de vos applications personnalisées](cloud-discovery-custom-apps.md). Cette fonctionnalité est déployée progressivement.

- Les pages **Paramètres** du portail Cloud App Security ont été repensées. La nouvelle conception consolide toutes les pages de paramètres et intègre une fonctionnalité de recherche et un design amélioré. 

- Cloud Discovery prend désormais en charge les pare-feu Barracuda F-Series et Barracuda F-Series Firewall Web Log Streaming.

- La fonctionnalité de recherche dans les pages Utilisateur et Adresse IP permet maintenant la saisie semi-automatique, ce qui facilite vos recherches.

- Vous pouvez désormais effectuer des actions en bloc dans les pages Exclure des entités et Exclure une adresse IP. Vous pouvez ainsi sélectionner plus facilement plusieurs utilisateurs, groupes ou adresses IP, et les exclure de l’analyse dans le cadre de la solution Cloud Discovery de votre organisation. 

## <a name="cloud-app-security-release-117"></a>Cloud App Security version 117
Date de publication : 20 février 2018

-   L’intégration approfondie de Cloud App Security avec Azure Information Protection vous permet désormais de protéger des fichiers dans G Suite. Cette fonctionnalité en préversion publique vous permet d’analyser et de classifier des fichiers dans G Suite, et d’appliquer automatiquement des étiquettes Azure Information Protection pour la protection. Pour plus d’informations, consultez [Intégration d’Azure Information Protection](azip-integration.md).

-   Cloud Discovery prend désormais en charge [Digital Arts i-FILTER](http://www.daj.jp/en/products/if/).

-   Le tableau des agents SIEM inclut désormais plus de détails pour faciliter la gestion.

## <a name="cloud-app-security-release-116"></a>Cloud App Security version 116
Date de publication : 4 février 2018
- La stratégie de détection d’anomalie de Cloud App Security a été améliorée grâce à de nouvelles **détections basées sur des scénarios**, notamment les activités de type Voyage impossible, les échecs de tentatives de connexion multiples et les activités provenant d’adresses IP suspectes. Les nouvelles stratégies sont automatiquement activées et fournissent une solution de détection des menaces prête à l’emploi pour votre environnement cloud. En outre, les nouvelles stratégies exposent davantage de données à partir du moteur de détection de Cloud App Security afin d’accélérer le processus d’investigation, et contiennent des menaces permanentes. Pour plus d’informations, consultez [Obtenir instantanément une détection des anomalies et une analytique comportementale](https://docs.microsoft.com/en-us/cloud-app-security/anomaly-detection-policy).

- Déploiement progressif : Cloud App Security met désormais en corrélation les utilisateurs et leurs comptes dans les applications SaaS. Cela vous permet d’examiner facilement toutes les activités d’un utilisateur, dans toutes ses différentes applications SaaS corrélées, peu importe l’application ou le compte qu’il a utilisé.  

-   Déploiement progressif : Cloud App Security prend désormais en charge plusieurs instances de la même application connectée. Si vous utilisez plusieurs instances, par exemple, Salesforce (une pour le service commercial et une autre pour le département marketing), vous pourrez les connecter à la fois à Cloud App Security et les gérer à partir de la même console pour créer des stratégies granulaires et obtenir une investigation plus approfondie. 

- Les analyseurs de Cloud Discovery prennent désormais en charge deux formats de point de contrôle supplémentaires, XML et KPC.



## <a name="cloud-app-security-release-115"></a>Cloud App Security version 115
Publiée le 21 janvier 2018

- Cette version offre une meilleure expérience lors de la sélection de dossiers spécifiques dans les stratégies de fichier. Vous pouvez désormais facilement afficher et sélectionner plusieurs dossiers à inclure dans une stratégie. 
- Dans la page **Applications découvertes** : 
  - La fonctionnalité de balisage en bloc vous permet d’appliquer des balises personnalisées (en plus des balises approuvées et non approuvées). 
  - Lorsque vous **générez un rapport d’adresses IP** ou **générez un rapport d’utilisateurs**, les rapports exportés incluent désormais les informations sur le trafic provenant d’applications approuvées non approuvées. 
- Vous pouvez maintenant demander à l’équipe Microsoft Cloud App Security un nouveau connecteur d’application API directement depuis le portail, dans la page **Connecter une application**. 


## <a name="cloud-app-security-release-114"></a>Cloud App Security version 114
Publiée le 7 janvier 2018

- À compter de la version 114, nous allons progressivement déployer la possibilité de créer et d’enregistrer des requêtes personnalisées dans les pages du journal d’activité et des applications découvertes. Les requêtes personnalisées vous permettent de créer des modèles de filtre qui peuvent être réutilisés pour des examens approfondis. De plus, des **requêtes suggérées** ont été ajoutées pour fournir des modèles d’examen prédéfinis permettant de filtrer vos activités et vos applications découvertes. Les **requêtes suggérées** incluent des filtres personnalisés pour identifier les risques comme les activités d’emprunt d’identité, les activités d’administrateur, les applications de stockage cloud non conformes présentant des risques, les applications d’entreprise avec un chiffrement faible et les risques de sécurité. Vous pouvez utiliser les **requêtes suggérées** comme point de départ, les modifier comme vous le souhaitez, puis les enregistrer en tant que nouvelle requête. Pour plus d’informations, consultez [Filtres d’activité et requêtes](activity-filters-queries.md) et [Filtres d’application découverte](discovered-app-queries.md).
 
- Vous pouvez désormais vérifier l’état actuel du service Cloud App Security en accédant à [status.cloudappsecurity.com](https://status.cloudappsecurity.com) ou directement à partir du portail en cliquant sur **Aide**>**État du système**. 
 


## <a name="see-also"></a>Voir aussi  

Pour obtenir une description des versions antérieures à celles répertoriées ici, consultez [Versions précédentes de Microsoft Cloud App Security](release-note-archive.md).

[Les clients Premier peuvent également choisir Cloud App Security directement depuis le portail Premier.](https://premier.microsoft.com/)  
  
  