---
title: Qu’est-ce que Cloud App Security ? | Microsoft Docs
description: Cette rubrique décrit Cloud App Security et comment il fonctionne.
keywords: ''
author: rkarlin
ms.author: rkarlin
manager: mbaldwin
ms.date: 4/22/2018
ms.topic: article
ms.prod: ''
ms.service: cloud-app-security
ms.technology: ''
ms.assetid: d46756b1-7dd8-4190-9799-3a97688f1266
ms.reviewer: reutam
ms.suite: ems
ms.openlocfilehash: c8fb1c11fb522b826f7106798f2583e5fa4c6be6
ms.sourcegitcommit: 45311f2cafef79483e40d971a4c61c7673834d96
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2018
---
*S’applique à : Microsoft Cloud App Security*


# <a name="what-is-microsoft-cloud-app-security"></a>Qu’est-ce que Microsoft Cloud App Security ?

> [!NOTE]
> Pour plus d’informations sur la Gestion de la sécurité avancée et Cloud App Security dans Office 365, consultez [Bien démarrer avec la Gestion de la sécurité avancée](https://support.office.com/article/Get-started-with-Advanced-Management-Security-d9ee4d67-f2b3-42b4-9c9e-c4529904990a).

Si le passage au cloud offre davantage de flexibilité aux employés et réduit les coûts informatiques, il introduit également une nouvelle complexité et de nouveaux défis pour le maintien de la sécurité de votre organisation. Pour tirer le meilleur parti des applications cloud, une équipe informatique doit trouver le juste équilibre entre la prise en charge des accès et la conservation du contrôle pour protéger les données critiques.  

Cloud App Security est un composant essentiel de la pile Microsoft Cloud Security. Il s’agit d’une solution complète qui permet à votre organisation de tirer pleinement parti de la promesse des applications cloud tout en vous permettant de conserver le contrôle grâce à une meilleure visibilité de l’activité. Elle renforce également la protection des données critiques des applications cloud. Avec des outils permettant de découvrir l’informatique fantôme, d’évaluer les risques, d’appliquer des stratégies, d’examiner les activités et de stopper les menaces, votre organisation peut passer plus tranquillement au cloud tout en conservant le contrôle des données critiques. 

## <a name="the-cloud-app-security-framework"></a>Infrastructure de Cloud App Security  

- **Cloud Discovery** : découvrez toute les utilisations du cloud dans votre organisation, notamment la génération de rapports et le contrôle de l’informatique fantôme, et l’évaluation des risques.
    
- **Protection des données** : surveillez et contrôlez vos données dans le cloud grâce à une visibilité, à l’application de stratégies DLP, à la gestion des alertes et aux investigations. 
    
- **Protection contre les menaces** : détectez les utilisations anormales et les incidents de sécurité. Utiliser l’analyse des comportements et des outils d’investigation avancés pour réduire les risques, et définissez des stratégies et des alertes pour obtenir un contrôle maximal sur le trafic cloud réseau.

## <a name="architecture"></a>Architecture  

Cloud App Security intègre une visibilité à votre cloud :  

-   En utilisant Cloud Discovery pour mapper et identifier votre environnement cloud et les applications cloud que votre organisation utilise.
-   En approuvant ou non des applications de votre cloud.  
-   En utilisant des connecteurs d’application faciles à déployer qui tirent parti des API du fournisseur, ce qui permet une visibilité et une gouvernance des applications auxquelles vous vous connectez.  
-   En utilisant une protection de proxy pour obtenir une visibilité en temps réel et contrôler l’accès et les activités effectuées au sein de vos applications cloud.
-   En vous permettant un contrôle continu via la définition et l’optimisation permanente de stratégies.  

![Schéma de l’architecture Cloud App Security](./media/proxy-architecture.png)  

### <a name="data-retention--compliance"></a>Conservation des données et conformité

Cloud App Security est officiellement certifié avec la conformité Microsoft pour ISO, HIPAA, CSA STAR, les clauses contractuelles types de l'Union européenne et plus encore. Pour consulter la liste complète des certifications, accédez à la page des [offres de conformité Microsoft](https://go.microsoft.com/fwlink/?linkid=842039) et sélectionnez Cloud App Security.  

Quand Cloud App Security exécute une inspection du contenu, la confidentialité des données est respectée. Le contenu du fichier n’est pas stocké dans la base de données Cloud App Security. Seules les métadonnées des enregistrements de fichiers et les violations qui ont été identifiées sont stockées dans la base de données Cloud App Security. Pour plus d’informations sur la rétention des données, consultez notre [politique de confidentialité](http://go.microsoft.com/fwlink/?LinkId=512132) et le [Microsoft Trust Center](https://www.microsoft.com/TrustCenter/Privacy/You-are-in-control-of-your-data).
Cloud App Security conserve les données comme suit : 
 
- Journal d’activité : 180 jours 
- Données de découverte : 90 jours 
- Alertes : 180 jours 

Une fois que les données sont collectées à partir de ces sources, Cloud App Security exécute un moteur de détection d’anomalie heuristique sophistiqué qui établit le profil de votre environnement et vous avertit des activités anormales par rapport à la base de référence apprise, ce qui vous donne une visibilité plus grande dans votre environnement cloud. Vous pouvez configurer une stratégie dans Cloud App Security et l’utiliser pour protéger tout ce qui se trouve dans votre environnement cloud.  

### <a name="cloud-discovery"></a>Cloud Discovery  

Cloud Discovery utilise vos journaux de trafic pour découvrir et analyser dynamiquement les applications cloud utilisées dans votre organisation. Pour créer un rapport d’instantané sur l’utilisation du cloud de votre organisation, vous pouvez charger manuellement les fichiers journaux à partir de vos pare-feu ou de vos proxys pour une analyse. Pour configurer des rapports en continu, utilisez les collecteurs de journaux de Cloud App Security pour transférer régulièrement vos journaux.  

Pour plus d’informations sur Cloud Discovery, voir [Configurer Cloud Discovery](set-up-cloud-discovery.md).

### <a name="sanctioning-and-unsanctioning-an-app"></a>Approbation et non-approbation d’une application  

Vous pouvez utiliser Cloud App Security pour approuver/ne pas approuver des applications dans votre organisation en utilisant le *catalogue d’applications cloud*. L’équipe d’analystes Microsoft dispose d’un catalogue fourni et en constante évolution de plus de 15 000 applications cloud, classées et évaluées selon les normes du secteur. Vous pouvez utiliser le catalogue d’applications cloud pour évaluer les risques pour vos applications cloud selon les certifications réglementaires, les normes du secteur et les bonnes pratiques. Vous pouvez ensuite personnaliser les scores et les pondérations des différents paramètres selon les besoins de votre organisation. À partir de ces scores, Cloud App Security vous indique le degré de risque lié à une application en fonction de plus de 60 facteurs de risque susceptibles d’affecter votre environnement.  

### <a name="app-connectors"></a>Connecteurs d’application  
Les connecteurs d’application utilisent les API des fournisseurs d’application cloud pour intégrer le cloud Cloud App Security à d’autres applications cloud. Les connecteurs d’application étendent le contrôle et la protection. Ils vous donnent aussi accès aux informations directement à partir des applications cloud, pour une analyse par Cloud App Security.  

Pour connecter une application et étendre la protection, l’administrateur de l’application autorise Cloud App Security à accéder à l’application. Ensuite, Cloud App Security récupère les journaux d’activité de l’application et analyse les données, les comptes et le contenu cloud. Cloud App Security peut appliquer des stratégies, détecter des menaces et appliquer des actions de gouvernance pour résoudre les problèmes.  

Cloud App Security utilise les API fournies par le fournisseur cloud. Chaque application a ses propres limitations de framework et d’API. Cloud App Security fonctionne avec les fournisseurs d’applications pour optimiser l’utilisation des API et garantir des performances optimales. Compte tenu des différentes limitations que les applications imposent sur les API (comme les limitations, les limites d’API et les fenêtres d’API de décalage temporel dynamique), les moteurs de Cloud App Security utilisent la capacité autorisée. Certaines opérations, comme l’analyse de tous les fichiers dans le locataire, nécessitent une grande quantité d’API et sont donc réparties sur une période plus longue. Il est normal que certaines stratégies s’exécutent pendant plusieurs heures ou jours.  

### <a name="proxy-protection"></a>Protection de proxy
Le proxy Cloud App Security vous propose les outils dont vous avez besoin pour obtenir une visibilité et un contrôle en temps réel de l’accès et des activités effectuées au sein de votre environnement cloud. Avec le proxy, vous pouvez protéger votre organisation : 
-   Éviter les fuites de données en bloquant les téléchargements avant qu’ils se produisent
-   Définir des règles qui forcent le chiffrement des données stockées dans le cloud et téléchargées à partir du cloud
-   Obtenir une visibilité sur les points de terminaison non protégés afin de surveiller les opérations réalisées sur les appareils non gérés
-   Contrôler l’accès depuis des réseaux hors entreprise ou des adresses IP à risque

### <a name="policy-control"></a>Contrôle des stratégies  

Vous pouvez utiliser des stratégies pour définir le comportement de vos utilisateurs dans le cloud. Utilisez des stratégies pour détecter des comportements à risques, des violations, ou des points de données et des activités suspectes dans votre environnement cloud. Si nécessaire, vous pouvez utiliser des stratégies pour intégrer des processus de correction de façon à réduire complètement les risques. Plusieurs types de stratégies sont en corrélation avec les différents types d’informations que vous voulez collecter sur votre environnement cloud et les types d’actions correctives que vous pouvez entreprendre.  

## <a name="related-videos"></a>Vidéos connexes
- [Rejoindre la communauté sur la sécurité](https://channel9.msdn.com/Shows/Microsoft-Security/Join-the-Security-Community)

## <a name="see-also"></a>Voir aussi  

Découvrez les concepts de base dans [Bien démarrer avec Cloud App Security](getting-started-with-cloud-app-security.md).    

Les clients Premier peuvent également choisir Cloud App Security directement depuis le [portail Premier](https://premier.microsoft.com/).   