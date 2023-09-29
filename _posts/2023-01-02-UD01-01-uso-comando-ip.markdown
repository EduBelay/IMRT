---
layout: post
title:  "UD01-01 :  Uso do comando ip en Ubuntu (VirtualBox)"
date:   2023-09-27 19:11:33 +0200
categories: UD01
---
# Práctica: Uso do comando ip en Ubuntu (VirtualBox)
O comando ip é unha ferramenta para administrar interfaces de rede e rutas en sistemas Linux. Nesta práctica, aprenderás a usar diferentes opcións deste comando en Ubuntu, ten en conta que o nome da interface de rede pode ser diferente aos exemplos indicados. 

# Exercicio 1: Mostrar todas as interfaces de rede
Explicación: Para ver todas as interfaces de rede dispoñibles na túa máquina virtual, podes usar o comando ip.

Comando:
```bash
ip addr show
```


Solución: Este comando mostrará unha lista de todas as interfaces de rede xunto coas súas direccións IP asignadas.

# Exercicio 2: Mostrar a táboa de rutas
Explicación: A táboa de rutas é esencial para determinar por onde enviaránse os paquetes de rede.
Comando:
```bash
ip route show
```

Solución: Este comando mostrará a táboa de rutas do sistema.

# Exercicio 3: Engadir unha nova dirección IP a unha interface
Explicación: Se queres engadir unha nova dirección IP a unha interface, podes facelo co comando ip. VirtualBox utiliza direccións IP no rango 10.0.2.x por defecto para as máquinas virtuais.
Comando:
```bash
ip addr add 10.0.2.15/24 dev eth0
```
Solución: Este comando asignará a dirección IP 10.0.2.15 á interface eth0.

# Exercicio 4: Eliminar unha dirección IP dunha interface
Explicación: Para eliminar unha dirección IP dunha interface, usa o comando ip.
Comando:
```bash
ip addr del 10.0.2.15/24 dev eth0
```

Solución: Este comando eliminará a dirección IP 10.0.2.15 da interface eth0.
# Exercicio 5: Activar ou desactivar unha interface de rede
Explicación: Podes activar ou desactivar unha interface de rede usando o comando ip.
Comando (activar):
```bash
ip link set eth0 up
```

Comando (desactivar):
```bash
ip link set eth0 down
```
Solución: O primeiro comando activará a interface eth0, mentres que o segundo a desactivará.