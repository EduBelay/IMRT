---
layout: post
title:  "UD01-03 :  Configuración de rede"
date:   2023-09-27 19:11:33 +0200
categories: UD01
---
#  Configuración de Rede en VirtualBox:
**1. PC01:**

* Tarxeta 1:
  * Vai a "Configuración" -> "Rede" -> "Adaptador 1".
  * Selecciona "NAT" como o tipo de conexión.
* Tarxeta 2:
  * Vai a "Configuración" -> "Rede" -> "Adaptador 2".
  * Selecciona "Rede Interna" como o tipo de conexión e asigna un nome á rede interna, por exemplo, "RedeInterna".

**2. PC02:**

* Tarxeta 1:
  * Vai a "Configuración" -> "Rede" -> "Adaptador 1".
  * Selecciona "Rede Interna" como o tipo de conexión e usa o mesmo nome de rede interna que asignaches no PC01, "RedeInterna".

#  Configuración de IP estática en PC01 e PC02:
## PC01:

* Abre un terminal e edita o arquivo de configuración de rede:
  
  ```sudo nano /etc/netplan/*.yaml```

* Agrega a seguinte configuración:
 ```bash
network:
  version: 2
  ethernets:
    enp0s3:  # Nome do dispositivo da tarxeta 1
      dhcp4: yes
    enp0s8:  # Nome do dispositivo da tarxeta 2
      dhcp4: no
      addresses: [192.168.0.1/24]
 ```

 * Garda e pecha o arquivo, e aplica a configuración:
 
   ```sudo netplan apply ```

## PC02: 
* Abre un terminal e edita o arquivo de configuración de rede:  ```sudo nano /etc/netplan/*.yaml ```

 * Agrega a seguinte configuración:

 ```bash
network:
  version: 2
  ethernets:
    enp0s3:  # Nome do dispositivo da tarxeta 1
      dhcp4: no
      addresses: [192.168.0.2/24]
      routes:             #antigamente >> gateway4:
        - to: default
          via: 192.168.10.1
      nameservers:
        addresses: [8.8.8.8, 8.8.4.4]

 ```

 * Garda e pecha o arquivo, e aplica a configuración:
 ```sudo netplan apply ```

# Verificación de conectividade en ambos equipos

 * No PC01 verifica que tes conectividade co PC02
  
    ```ping 192.168.0.2 ```

 * No PC02 verifica que tes conectividade co PC01
  
    ```ping 192.168.0.1 ```

