# Installation de GNS3, VMware Workstation et Images de Routeurs  

## Introduction  
Ce document compile les captures d'écran fournies pour détailler visuellement le processus d'installation de GNS3, de VMware Workstation, ainsi que des images de routeurs. Les captures d'écran utilisées sont situées dans le chemin  

---

## 1. Paramètres de la Machine Virtuelle (VMware Workstation)  
![Paramètres de la machine virtuelle](C:\Users\Wendy Colas\TD\image\image (1).png)  

---

## 2. Configuration de la VM pour GNS3  
![Configuration de la VM pour GNS3](C:\Users\Wendy Colas\TD\image\image (2).png)  

---

## 3. Écran de Bienvenue de l'installation de GNS3  
![Écran de Bienvenue de GNS3](C:\Users\Wendy Colas\TD\image\image (3).png)  

---

## 4. Choix du dossier dans le Menu Démarrer  
![Choix du dossier dans le menu démarrer](C:\Users\Wendy Colas\TD\image\image (4).png)  

---

## 5. Choix de l'emplacement d'installation de GNS3  
![Choix de l'emplacement d'installation](C:\Users\Wendy Colas\TD\image\image (5).png)  

---

## 6. Avancement de l'installation de GNS3  
![Progression de l'installation](C:\Users\Wendy Colas\TD\image\image (6).png)  

---

## 7. Sélection des options de simulation  
![Options de simulation](C:\Users\Wendy Colas\TD\image\image (7).png)  

---

## 8. Création d'un nouveau template (Appliance)  
![Création d'un nouveau template](C:\Users\Wendy Colas\TD\image\image (8).png)  

---

## 9. Installation de l'appliance Cisco 1700 - Étape 1  
![Installation Cisco 1700 - Étape 1](C:\Users\Wendy Colas\TD\image\image (9).png)  

---

## 10. Installation de l'appliance Cisco 1700 - Étape 2  
![Installation Cisco 1700 - Étape 2](C:\Users\Wendy Colas\TD\image\image (10).png)  

---

## 11. Installation de l'appliance Cisco 1700 - Étape 3  
![Installation Cisco 1700 - Étape 3](C:\Users\Wendy Colas\TD\image\image (11).png)  

---

## 12. Importation des fichiers nécessaires pour Cisco 1700  
![Importation des fichiers nécessaires](C:\Users\Wendy Colas\TD\image\image (12).png)  

---

## 13. Sélection du fichier d'image pour Cisco 1700  
![Sélection du fichier d'image pour Cisco 1700](C:\Users\Wendy Colas\TD\image\image (13).png)  

---

## 14. Finalisation de l'installation de Cisco 1700  
![Finalisation de l'installation de Cisco 1700](C:\Users\Wendy Colas\TD\image\image (14).png)  

---

## 15. Instructions après l'installation de Cisco 1700  
![Instructions après l'installation de Cisco 1700](C:\Users\Wendy Colas\TD\image\image (15).png)  

---

## 16. Interface post-installation de GNS3  
![Interface de GNS3](C:\Users\Wendy Colas\TD\image\image (16).png)  

---  

# Reproduction de la Topologie et Configuration du Routeur et des PCs

## Configuration Réseau

### 1. Configuration du Routeur
Voici les étapes effectuées pour configurer le routeur :
- Activation de l'interface `FastEthernet` :

- Vérification de l'image IOS chargée et des erreurs de compatibilité.

**Capture d'écran :**
![Configuration du routeur](C:\Users\Wendy Colas\TD\image\image (17).png)

### 2. Paramètres des PCs
Les PCs ont été configurés avec les adresses IP suivantes :
- **PC1** : 192.168.1.2/24
- **PC2** : 192.168.1.3/24

Les paramètres DNS ont été mis à jour pour permettre la résolution des noms de domaine si nécessaire.

**Capture d'écran PC1 :**
![Configuration de PC1](C:\Users\Wendy Colas\TD\image\image (18).png)

**Capture d'écran PC2 :**
![Configuration de PC2](C:\Users\Wendy Colas\TD\image\image (19).png)

### 3. Test de Connectivité
Les tests de ping ont été effectués entre les PCs et le routeur pour confirmer la connectivité.

**Capture d'écran des tests de connectivité :**
![Tests de connectivité 1](C:\Users\Wendy Colas\TD\image\image (20).png)

**Capture d'écran des tests de connectivité 2 :**
![Tests de connectivité 2](C:\Users\Wendy Colas\TD\image\image (21).png)

---

# Reproduction de la topologie et configuration du routeur et des PCs

---

## Topologie du réseau
Voici une représentation visuelle de la topologie mise en place :

![Topologie réseau](C:\Users\Wendy Colas\TD\image\image (23).png)

---

## Configuration du routeur
### Interface FastEthernet0/0
- **IP Address** : 192.168.1.1/24
- **Status** : Active
- **Commandes** :
    ```bash
    interface FastEthernet0/0
    ip address 192.168.1.1 255.255.255.0
    no shutdown
    ```

### Interface FastEthernet0/1
- **IP Address** : 192.168.2.1/24
- **Status** : Active
- **Commandes** :
    ```bash
    interface FastEthernet0/1
    ip address 192.168.2.1 255.255.255.0
    no shutdown
    ```

![Configuration du routeur](C:\Users\Wendy Colas\TD\image\image (24).png)

---

## Configuration des PCs
### PC1
- **IP Address** : 192.168.1.2/24
- **Gateway** : 192.168.1.1
- **Commandes** :
    ```bash
    set pc1 ip 192.168.1.2 255.255.255.0 192.168.1.1
    ```

![Configuration PC1](C:\Users\Wendy Colas\TD\image\image (25).png)

### PC2
- **IP Address** : 192.168.2.2/24
- **Gateway** : 192.168.2.1
- **Commandes** :
    ```bash
    set pc2 ip 192.168.2.2 255.255.255.0 192.168.2.1
    ```

![Configuration PC2](C:\Users\Wendy Colas\TD\image\image (26).png)

### PC3
- **IP Address** : 192.168.2.3/24
- **Gateway** : 192.168.2.1
- **Commandes** :
    ```bash
    set pc3 ip 192.168.2.3 255.255.255.0 192.168.2.1
    ```

![Configuration PC3](C:\Users\Wendy Colas\TD\image\image (27).png)

### PC4
- **IP Address** : 192.168.2.4/24
- **Gateway** : 192.168.2.1
- **Commandes** :
    ```bash
    set pc4 ip 192.168.2.4 255.255.255.0 192.168.2.1
    ```

![Configuration PC4](C:\Users\Wendy Colas\TD\image\image (28).png)

---

## Tests de connectivité
- **PC1 vers Routeur** :
    - Commande : `ping 192.168.1.1`
    - Résultat : [Inclure les résultats ou le résumé]

- **PC2 vers Routeur** :
    - Commande : `ping 192.168.2.1`
    - Résultat : [Inclure les résultats ou le résumé]

---

## Conclusion
Ce td m'a permis de me familiariser avec le logiciel gns3 ainsi qu'avec vmware workstation.

---


