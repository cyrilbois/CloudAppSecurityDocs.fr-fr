---
title: "Configuration requise du réseau Cloud App Security | Microsoft Docs"
description: "Cette rubrique décrit les adresses IP et les ports à ouvrir pour fonctionner avec Cloud App Security."
keywords: 
author: rkarlin
ms.author: rkarlin
manager: mbaldwin
ms.date: 8/27/2017
ms.topic: get-started-article
ms.prod: 
ms.service: cloud-app-security
ms.technology: 
ms.assetid: 4de606f2-a09e-4e48-a578-e223de8b5e69
ms.reviewer: reutam
ms.suite: ems
ms.openlocfilehash: dac230e191c7c2d8159a2f373e6ef939fdd841a4
ms.sourcegitcommit: c3fda43ef6fe0d15f0eb9ea23a6f245bad8c371b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2017
---
# <a name="network-requirements"></a>Configuration requise pour le réseau

Cette rubrique fournit une liste de ports et d’adresses IP que vous devez autoriser et ajouter à la liste verte pour qu’ils fonctionnent avec Cloud App Security. 


## <a name="portal-access"></a>Accès au portail

Pour accéder au portail, il est nécessaire d’ajouter les adresses IP suivantes à la liste verte de votre pare-feu pour fournir l’accès au portail Cloud App Security :  
  
104.42.231.28  


## <a name="app-connector-access"></a>Accès au connecteur d’application

Pour que Cloud App Security puissent accéder à certaines applications tierces, vous devrez peut-être ajouter les adresses IP suivantes à la liste verte pour permettre à Cloud App Security de collecter les journaux et de fournir un accès pour la console Cloud App Security :  
  
104.209.35.177  
13.91.98.185 40.118.211.172 13.93.216.68 13.91.61.249 13.93.233.42 13.64.196.27 13.64.198.97 13.64.199.41 13.64.198.19

> [!NOTE]
>Vous verrez peut-être ces adresses IP dans les journaux d’activité du fournisseur, car Cloud App Security effectue des actions de gouvernance et des analyses à partir de ces adresses IP. 
  

## <a name="siem-agent-and-log-collector"></a>Agent SIEM et collecteur de journaux

Pour permettre à Cloud App Security de se connecter à votre agent SIEM et au collecteur de journaux Cloud App Security de s’exécuter, vous devez ouvrir le :

- Port sortant 443 sur 104.42.231.28

## <a name="external-dlp-integration"></a>Intégration DLP externe

Pour que Cloud App Security envoie des données via votre stunnel à votre serveur ICAP, ouvrez le pare-feu DMZ aux adresses IP externes utilisées par Cloud App Security avec un numéro de port source dynamique. 

1.  Adresses sources : elles doivent figurer sur la liste verte, comme ci-dessus pour les applications tierces du connecteur d’API
2.  Port TCP source : dynamique
3.  Adresse(s) de destination : une ou deux adresses IP du stunnel connecté au serveur ICAP externe
4.  Port TCP de destination : comme défini dans votre réseau

> [!NOTE] 
> Par défaut, le numéro de port du stunnel a la valeur 11344. Vous pouvez le remplacer par un autre port si nécessaire, mais n’oubliez pas de noter le nouveau numéro de port.



  
## <a name="see-also"></a>Voir aussi  
[Activités quotidiennes pour protéger votre environnement cloud](daily-activities-to-protect-your-cloud-environment.md)   
[Pour obtenir un support technique, visitez la page de support assisté Cloud App Security.](http://support.microsoft.com/oas/default.aspx?prid=16031)   
[Les clients Premier peuvent également choisir Cloud App Security directement depuis le portail Premier.](https://premier.microsoft.com/)  
  

   