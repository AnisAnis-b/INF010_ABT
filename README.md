#  Déploiement d'une VM Linux sur Azure avec Ansible

Ce projet Ansible permet de déployer **une machine virtuelle Linux sur Microsoft Azure** avec un réseau complet :
- ✅ **Resource Group**  
- ✅ **Virtual Network (VNet) et Subnet**  
- ✅ **Adresse IP publique**  
- ✅ **Network Security Group (NSG) avec accès SSH**  
- ✅ **Interface Réseau (NIC)**  
- ✅ **Machine Virtuelle Linux (Ubuntu)**  
- ✅ **Connexion SSH avec clé publique ou mot de passe**  
- ✅ **Résumé du déploiement avec adresse IP publique et commande SSH**  

---

## 📌 **Prérequis**

Avant d'exécuter ce playbook, assurez-vous d'avoir :

1️⃣ **Un compte Azure actif**  
2️⃣ **Azure CLI installé et authentifié** :
   az login

3️⃣ **Un environnement Ansible fonctionnel avec les modules Azure :
pipx inject ansible ansible[azure] azure-cli**

4️⃣ **Un fichier inventory.ini contenant** :

[localhost]
localhost ansible_connection=local

5️⃣ **Une clé SSH générée sur votre machine locale** :

ssh-keygen -t rsa -b 2048 -f ~/.ssh/id_rsa -q -N ""

## 📌 **Utilisation**:
ansible-playbook -i inventory.ini deploy-vm-azure-interactif.yml

Le script vous demandera plusieurs informations, par exemple :

Nom du Resource Group: MonRG

Région Azure (ex: westeurope, eastus, etc.) [westeurope]: (voir fichier region codes.txt)

Nom du Virtual Network: MonVNet

Nom du Subnet: MonSubnet

Nom de l'IP Publique: MonPublicIP

Nom du Network Security Group (NSG): MonNSG

Nom de l'Interface Réseau: MonNIC

Nom de la Machine Virtuelle: MonVM

Taille de la VM (ex: Standard_B1s, Standard_D2s_v3) [Standard_B1s]: Standard_D2s_v3   (voir fichier Taille Vm.txt)

Nom de l'Utilisateur Admin: monuser

Mot de passe Administrateur: ********

Chemin de la clé SSH publique [~/.ssh/id_rsa.pub]: 


## 📌 **Crédits**

Développé par ANIS-FLORENT-THIERRY

Date : Janvier 2025
