---
layout: post
title:  "UD01-06 : Redireccion DNS /etc/host"
date:   2023-09-27 19:11:33 +0200
categories: UD01 linux
---

## **Práctica: Redirección de Dominios sen Servidor Local**
### **Obxectivos:**
- Aprender a redirixir un dominio a outro usando o arquivo hosts.
- Entender como funciona a redirección de dominios a nivel local.

### Material:
1. Computadora
1. Sistema Operativo baseado en Linux (e.g., Ubuntu, Xubuntu)
1. Editor de Texto (e.g., Nano, Gedit)
1. Terminal
1. Navegador Web
1. Python 3
1. Permisos de Administrador
1. Conexión a Internet (opcional)


### <a name="pasos"></a>**Pasos:**
1. **Modificar o Arquivo Hosts**:
   - Abre o terminal.
   - Abre o arquivo hosts con permisos de administrador:

     sudo nano /etc/hosts
   - Engade a seguinte liña ao final do arquivo:

     127.0.0.1 edu.xunta.gal
2. **Crear unha Páxina Web Simples**:
   - Crea un arquivo chamado index.html no teu escritorio e engade o seguinte contido:

     <!DOCTYPE html>
     **<html>**
     **<head>**
     **<meta** **http-equiv**="refresh" **content**="0; url=http://praza.gal" **/>**
     **<title>**Redirección a Praza.gal**</title>**
     **</head>**
     **<body>**
     **</body>**
     **</html>**
3. **Servir a Páxina Web Simples**:
   - Podes usar Python para servir a túa páxina web simple. Abre o terminal e navega ao directorio onde está o arquivo index.html:

     cd ~/Desktop
   - Agora executa o seguinte comando para servir a túa páxina web:

     python3 -m http.server 80
4. **Probar a Redirección**:
   - Abre o teu navegador web e vai a <http://edu.xunta.gal>. Deberías ser redirixido a <http://praza.gal>.
5. **Reverter os Cambios (opcional)**:
   - Se desexas revertir os cambios, simplemente elimina a liña que engadiches ao arquivo hosts.
   - Para deter o servidor web, volta ao terminal e preme Ctrl + C.


