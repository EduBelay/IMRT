---
layout: post
title:  "UD01-03 : Configuración da Tarxeta de Rede en Dúas Máquinas Virtuais en VirtualBox con Xubuntu"
date:   2023-09-27 19:11:33 +0200
categories: UD01
---


##  Configuración da Tarxeta de Rede en Dúas Máquinas Virtuais en VirtualBox con Xubuntu

Para configurar a tarxeta de rede en dúas máquinas virtuais en VirtualBox cun sistema operativo Xubuntu, podes seguir os seguintes pasos. Os pasos serán similares nas dúas máquinas virtuais. Vou asumir que desexas configurar unha conexión de rede estática entre as dúas máquinas:

### Crear as Máquinas Virtuais en VirtualBox:
1. Crea dúas máquinas virtuais en VirtualBox e instala Xubuntu en ambas.

### Configurar a Rede en VirtualBox:
1. Nas configuracións de cada máquina virtual, vai a "Rede" e selecciona "Adaptador 1".
2. Escolle "Rede interna" ou "Rede de host único" segundo a túa preferencia.


### Iniciar as Máquinas Virtuais:
1. Inicia as dúas máquinas virtuais e abre un terminal en cada unha delas.


### Identificar o Nome do Dispositivo de Rede:
1. Executa o seguinte comando para identificar o nome do dispositivo de rede:
2. Busca a liña que contén "enp0s3" ou algo semellante. Este é o nome do teu dispositivo de rede.


### Editar o Arquivo de Configuración de Rede:
1. Abre o arquivo de configuración de rede usando o editor de texto nano (ou calquera outro editor de texto que prefiras):
2. Agrega ou modifica a seguinte configuración no arquivo, substituíndo "enp0s3" polo nome do teu dispositivo de rede e asignando un enderezo IP estático diferente para cada máquina (por exemplo, 192.168.1.2 e 192.168.1.3):
3. Garda e pecha o arquivo.


### Aplicar a Configuración de Rede:
1. Aplica a nova configuración de rede executando o seguinte comando:
### Verificar a Configuración:
1. Verifica que a configuración se aplicou correctamente executando novamente o comando ip a.
### Probar a Conexión:
1. Podes probar a conexión entre as dúas máquinas pingeando o enderezo IP da outra máquina desde cada unha delas:
2. Repite os pasos 4 a 8 na outra máquina virtual, asegurándote de asignar un enderezo IP estático diferente. Así terás configurada a tarxeta de rede nas dúas máquinas virtuais en Xubuntu e poderás comunicarte entre elas.

```bash 

ping 192.168.1.3

sudo netplan apply

network:
`  `version: 2
`  `ethernets:
`    `enp0s3:
`      `dhcp4: no
`      `addresses: [192.168.1.2/24]
`      `routes: 
`        `- to: default
`          `via: 192.168.1.1
`      `nameservers:
`        `addresses: [8.8.8.8, 8.8.4.4]

sudo nano /etc/netplan/\*.yaml

ip a
```