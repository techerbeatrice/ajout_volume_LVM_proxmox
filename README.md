# Ajout d'un volume LVM sur proxmox  

**Dans Virtualbox, sur le contrôleur SATA existant, après avoir créé un autre disque dur de type vmdk** 

**Création du volume logique**   

**La commande _fdisk -l /dev/sdc_ pour voir les informations sur le disque**  
**Création du volume physique avec _pvcreate /dev/sdc_**  
**Vérification de la création du volume avec _pvdisplay /dev/sdc_**  



**Création du volume group vg1 avec la commande _vgcreate vg1 /dev/sdc_**  
**Création du volume logique vl-dd2 avec la commande _lvcreate -n vl-dd2 -L 90G vg1_**   
**Formatage en ext4 du volume logique avec la commande _mkfs.ext4 /dev/vg1/vl-dd2_** 

__________


![image](https://github.com/techerbeatrice/ajout_volume_LVM_proxmox/assets/138071140/e54deb89-35f3-4e68-9738-bd6741193239)

![image](https://github.com/techerbeatrice/ajout_volume_LVM_proxmox/assets/138071140/ae9fa946-bae2-4025-9082-a085dc1cd66c)


