---
layout: post
title:  "UD01-05 : Configuración dun Servidor Web Local e Redirección de Dominios"
date:   2023-09-27 19:11:33 +0200
categories: UD01 linux
---

# Práctica: Configuración dun Servidor Web Local e Redirección de Dominios

#### Obxectivos:

-   Aprender a instalar e configurar un servidor web local usando
    Apache.

-   Entender como modificar o arquivo hosts para redirixir dominios.

#### Pasos:

1.  **Instalar Apache**:

    -   Abre o terminal e executa o seguinte comando para instalar
        Apache:

    <!-- -->

    -   sudo apt-get install apache2

2.  **Comprobar a Instalación de Apache**:

    -   Abre o teu navegador web e vai a `http://localhost`. Deberías
        ver a páxina predeterminada de Apache.

3.  **Crear unha Páxina Web Simples**:

    -   Crea un arquivo chamado `index.html` no teu escritorio e engade
        o seguinte contido:

    <!-- -->

    -   <!DOCTYPE html>
            <html>
            <head>
              <title>Benvido ao Meu Servidor Web Local</title>
            </head>
            <body>
              <h1>Hola Mundo!</h1>
            </body>
            </html>

    <!-- -->

    -   Mover o arquivo `index.html` ao directorio raíz do servidor web:

    <!-- -->

    -   sudo mv ~/Desktop/index.html /var/www/html/

4.  **Modificar o Arquivo Hosts**:

    -   Abre o arquivo hosts con permisos de administrador:

    <!-- -->

    -   sudo nano /etc/hosts

    <!-- -->

    -   Engade a seguinte liña ao final do arquivo:

    <!-- -->

    -   127.0.0.1 fakegoogle.com

5.  **Probar a Redirección**:

    -   Garda e pecha o arquivo hosts.

    -   Abre o teu navegador web e vai a `http://fakegoogle.com`.
        Deberías ver a túa páxina web simple.

6.  **Reverter os Cambios** (opcional):

    -   Se desexas revertir os cambios, simplemente elimina a liña que
        engadiches ao arquivo hosts e elimina o arquivo `index.html` do
        directorio `/var/www/html/`.


