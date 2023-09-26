# Ajout d'un volume LVM sur proxmox  

**Dans Virtualbox, sur le contrôleur SATA existant, après avoir créé un autre disque dur de type vmdk** 

**Création du volume logique**   

**La commande _fdisk -l /dev/sdc_ pour voir les informations sur le disque**  
**Création du volume physique avec _pvcreate /dev/sdc_**  
**Vérification de la création du volume avec _pvdisplay /dev/sdc_**  
**Création du volume group vg1 avec la commande _vgcreate vg1 /dev/sdc_**  
**Création du volume logique vl-dd2 avec la commande _lvcreate -n vl-dd2 -L 40G vg1_**   
**Formatage en ext4 du volume logique avec la commande _mkfs.ext4 /dev/vg1/vl-dd2_** 

![image](https://github.com/techerbeatrice/ajout_volume_LVM_proxmox/assets/138071140/4122081a-2d8b-4cfa-94fb-55ba8bf97f66)

![image](https://github.com/techerbeatrice/ajout_volume_LVM_proxmox/assets/138071140/b6f78dfb-59e3-48d4-aed6-ed18df036470)

![image](https://github.com/techerbeatrice/ajout_volume_LVM_proxmox/assets/138071140/23c0ea73-3084-468e-aca7-1c0586551e97)

![image](https://github.com/techerbeatrice/ajout_volume_LVM_proxmox/assets/138071140/8eddd621-491d-421c-a90b-0ed6109e69ff)




