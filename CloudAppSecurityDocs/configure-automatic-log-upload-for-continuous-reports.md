---
title: Configurer le chargement automatique des journaux pour des rapports continus | Documentation Microsoft
description: "Cette rubrique fournit des informations sur le chargement de journaux pour créer des rapports Cloud Discovery automatiques."
keywords: 
author: rkarlin
ms.author: rkarlin
manager: mbaldwin
ms.date: 10/15/2016
ms.topic: article
ms.prod: 
ms.service: cloud-app-security
ms.technology: 
ms.assetid: c4123272-4111-4445-b6bd-2a1efd3e0c5c
ms.reviewer: reutam
ms.suite: ems
translationtype: Human Translation
ms.sourcegitcommit: ed4ea71b24767d3602d40894d1cbac7447bcd8a2
ms.openlocfilehash: 9672336d69f19875d160eb414bf3ca2c525692e1


---

# <a name="configure-automatic-log-upload-for-continuous-reports"></a>Configurer le chargement automatique des journaux pour des rapports continus
Avant de configurer la collecte de fichiers journaux automatique, vérifiez que votre journal correspond au type attendu de journal pour vous assurer que Cloud App Security peut analyser votre fichier spécifique. 

## <a name="technical-requirements"></a>Spécifications techniques
- Hyperviseur : HyperV ou VMware
- Espace disque : 250 Go
- Processeur : 2
- RAM : 4 Go 
- Paramètres du pare-feu : 
- Autoriser le collecteur de journaux à recevoir le trafic FTP et Syslog entrant
- Autoriser le collecteur de journaux à lancer le trafic sortant sur le portail (par exemple, contoso.cloudappsecurity.com) sur le port 443

  
## <a name="set-up-automatic-log-file-collection"></a>Configurer la collecte de fichiers journaux automatique  
  
Les collecteurs de journaux vous permettent d’automatiser facilement le chargement manuel des journaux de votre réseau. Le collecteur de journaux s’exécute sur votre réseau et reçoit les journaux par le biais de Syslog ou FTP. Chaque journal est automatiquement traité, compressé et transmis au portail. Les journaux FTP sont chargés sur Cloud App Security une fois que le fichier a terminé le transfert FTP vers le collecteur de journaux et, pour les journaux Syslog, le collecteur de journaux écrit les journaux reçus sur disque toutes les 20 minutes, puis charge le fichier sur Cloud App Security.  La machine virtuelle du collecteur de journaux est disponible pour Hyper-V (format VHD) et l’hyperviseur VMware (format OVF). Elle nécessite 250 Go d’espace disque, 2 processeurs et 4 Go de RAM. 
     
  
     The log collector VHD image can be downloaded and run on Azure servers.  
  
2.  Accédez à la page des paramètres de chargement automatisé :  
    Dans le portail Cloud App Security, cliquez sur l’icône des paramètres ![icône des paramètres](./media/settings-icon.png "settings icon"), sur **Paramètres Cloud Discovery**, puis sélectionnez l’onglet **Charger les journaux automatiquement**.  
  
3.  Pour chaque pare-feu ou proxy à partir desquels vous voulez charger des journaux, créez une source de données correspondante :  
  
    1.  Cliquez sur **Ajouter une source de données**.  
  
    2.  **Nommez** votre proxy ou pare-feu.  
  
    3.  Sélectionnez l’appareil dans la liste **Source**.  
  
    4.  Comparez votre journal à l’exemple de format de journal attendu. Si votre format de fichier journal ne correspond pas à cet exemple, vous devez ajouter votre source de données en tant qu’**Autre**.  
  
    5.  Affectez à l’option **Type de récepteur** la valeur **FTP** ou **Syslog**.  
  
         Pour **Syslog**, choisissez **UDP** ou **TCP**.  
  
    6.  Répétez ce processus pour chaque pare-feu ou proxy dont les journaux peuvent être utilisés pour détecter le trafic sur votre réseau.  
  
4.  Accédez à l’onglet **Collecteurs de journaux** en haut.  
  
    1.  Cliquez sur **Ajouter un collecteur de journaux**.  
  
    2.  Donnez un **nom** au collecteur de journaux.  
  
    3.  Sélectionnez toutes les **sources de données** que vous voulez connecter au collecteur, puis cliquez sur **Mettre à jour**.  
  
         > [!NOTE] 
       > Copiez le contenu de l’écran, car vous aurez besoin des informations lors de la configuration du collecteur de journaux pour communiquer avec Cloud App Security. Si vous avez sélectionné Syslog, ces informations vont inclure des informations sur le port utilisé par l’écouteur Syslog pour écouter.
         
![sources de données de découverte](./media/discovery-data-sources.png)
> [!NOTE] 
         > Un seul collecteur de journaux peut gérer plusieurs sources de données.
  
4.  **Téléchargez** une nouvelle machine virtuelle de collecteur de journaux en cliquant sur Hyper-V ou VMWare et décompressez le fichier en utilisant le mot de passe que vous avez reçu dans le portail.  
  
## <a name="set-up-your-virtual-machine-in-hyperv"></a>Configurez votre machine virtuelle dans Hyper-V :  
  
1.  Ouvrez le Gestionnaire Hyper-V.  
  
2.  Sélectionnez **Nouveau**, puis **Machine virtuelle** et cliquez sur **Suivant**.  
  
             ![discovery hyperv virtual machine](./media/discovery-hyperv-virtual-machine.png "discovery hyperv virtual machine")  
  
3.  Fournissez un **nom** à la nouvelle machine virtuelle, par exemple, CloudAppSecurityLogCollector01, puis cliquez sur **Suivant**.  
  
4.  Sélectionnez **Génération 1**, puis cliquez sur **Suivant**.  
  
5.  Affectez à la **mémoire de démarrage** la valeur **4 096 Mo**.  
        
6. Cochez **Use Dynamic Memory (Utiliser la mémoire dynamique)** pour cette machine virtuelle et cliquez sur **Suivant**.  
  
7.  Si disponible, choisissez la **connexion** réseau et cliquez sur **Suivant**.  
  
8.  Choisissez **Utiliser un disque dur virtuel existant** et sélectionnez le fichier .**vhd** qui était inclus dans le fichier Zip que vous avez téléchargé.  
  
9.  Cliquez sur **Suivant** , puis sur **Terminer**.  
  
             The machine will be added to your Hyper-V environment.  
  
9. Cliquez sur la machine dans le tableau **Machines virtuelles** et cliquez sur **Démarrer**.   
  
10. Connectez-vous à la machine virtuelle du collecteur de journaux pour déterminer si une adresse DHCP lui a été attribuée : cliquez sur la machine virtuelle, puis sélectionnez **Connect** (Connecter). Vous devez voir l’invite de connexion. Si vous voyez une adresse IP, vous pouvez vous connecter à la machine virtuelle à l’aide d’un outil Terminal Server/SSH.  Si vous ne voyez pas une adresse IP, connectez-vous en utilisant les outils de connexion Hyper-V/VMWare avec les informations d’identification que vous avez copiées quand vous avez créé le collecteur de journaux ci-dessus. Vous pouvez modifier le mot de passe et configurer la machine virtuelle en exécutant la commande suivante
```
sudo network_config
```
> [!NOTE]
> La machine virtuelle est préconfigurée pour obtenir une adresse IP d’un serveur DHCP. Si vous avez besoin de configurer des adresses IP statiques, une passerelle par défaut, un nom d’hôte, des serveurs DNS et NTPS, vous pouvez utiliser l’utilitaire **network_config** ou effectuer les modifications manuellement.


À ce stade, votre collecteur de journaux doit être connecté à votre réseau et en mesure d’atteindre le portail Cloud App Security.  

## <a name="log-in-and-import"></a>Connexion et importation 
La première fois que vous vous connectez au collecteur de journaux et importez sa configuration à partir du portail, procédez comme suit. 

1.  Connectez-vous au collecteur de journaux via SSH, à l’aide des informations d’identification d’administrateur interactives qui vous ont été fournies dans le portail. (S’il s’agit de votre première connexion à la console, vous devrez modifier le mot de passe et vous reconnecter après la modification. Si vous utilisez une session Terminal Server, vous devrez peut-être la redémarrer. )
2.  Exécutez l’utilitaire de configuration de collecteur avec le jeton d’accès fourni quand vous avez créé le collecteur de journaux. 

```
sudo collector_config <access token>
```

3. Entrez le domaine de la console, par exemple :

```
contoso.portal.cloudappsecurity.com
```

Il est disponible à partir de l’URL qui s’affiche après la connexion au portail Cloud App Security. 
 

4. Entrez le nom du collecteur de journaux à configurer, par exemple :

**CloudAppSecurityLogCollector01** ou **NewYork** à partir de l’image ci-dessus.
 
8.  Importez la configuration du collecteur de journaux à partir du portail, comme suit :  
  
      1.  Connectez-vous au collecteur de journaux via SSH, à l’aide des informations d’identification d’administrateur interactives qui vous ont été fournies dans le portail.  
  
       2.  Exécutez l’utilitaire de configuration de collecteur avec le jeton d’accès fourni dans la commande **sudo collector_config \<jeton d’accès>**  
  
             Entrez le domaine de la console, par exemple :  
  
             **contoso.portal.cloudappsecurity.com ** 
  
             Entrez le nom du collecteur de journaux à configurer, par exemple :  
  
             **CloudAppSecurityLogCollector01**  
  
5.  Configurez vos pare-feu réseau et proxys pour exporter régulièrement les journaux vers le port Syslog dédié du répertoire FTP selon les instructions données dans la boîte de dialogue, par exemple :  
  
     `London Zscaler - Destination path: 614`  
  
     `SF Blue Coat - Destination path: \\CloudAppSecurityCollector01\BlueCoat\`  
  
6.  Utiliser le journal de gouvernance pour vérifier que les journaux sont régulièrement chargées vers le portail.  
  
## <a name="log-collector-performance"></a>Performances du collecteur de journaux
Le collecteur de journaux peut gérer correctement une capacité allant jusqu’à 50 Go par heure.

Les principaux goulots d’étranglement dans le processus de collecte des journaux sont les suivants :
* Bande passante réseau : votre bande passante réseau détermine la vitesse de chargement des journaux.
* Performances d’E/S de la machine virtuelle allouées par votre service informatique : détermine la vitesse à laquelle les journaux sont écrits sur le disque du collecteur de journaux.

Le collecteur de journaux dispose d’un mécanisme de sécurité intégré qui surveille le débit auquel les journaux arrivent et le compare au débit de chargement. En cas de congestion, le collecteur de journaux commence à supprimer des fichiers journaux. Si votre configuration dépasse généralement 50 Go par heure, il est recommandé de diviser le trafic entre plusieurs collecteurs de journaux.


<!--HONumber=Oct16_HO4-->

