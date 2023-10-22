**Exercicio 1 : Dada a notación CDIR nos seguintes casos calcula a máscara de rede en decimal separada por octetos.**

|**CDIR**|**Resposta**|
| :- | :- |
|(a) /24|<p></p><p></p>|
|(b) /16|<p></p><p></p>|
|(c) /8|<p></p><p></p>|
|(d) /14|<p></p><p></p>|

**Exercicio 2 : Dada as seguintes máscaras de rede en octetos obtén o seu equivalente en notación CDIR.  Todas as respostas deben ser explicadas e que permitan comprobar a dedución da mesma.**

** 

|**Máscara de rede**|**Resposta**|
| :- | :- |
|(e) 255.255.255.248|<p></p><p></p>|
|(f) 255.255.128.0|<p></p><p></p>|
|(g) 255.255.252.0|<p></p><p></p>|
|(h) 255.255.255.0|<p></p><p></p>|
|(i) 240.0.0.0|<p></p><p></p>|
|(j) 254.0.0.0|<p></p><p></p>|


**Exercicio 3 : Calcula a dirección de rede nos seguintes casos:**

1) **192.168.128.15/29**







1) **10.11.12.13/25**




<b>Exercicio 4 : Cal é o numero máximo de equipos nas seguintes redes. Recorda que o número de equipos pódese calcular tendo en conta “o número de 0 que temos na máscara de rede” e que lle chamaremos “n”. Logo o nº de equipos = 2<sup>n</sup> -2 .</b>

**Nota:**

- **recorda que unha máscara de rede como moito ten 32 bits.**



|**Máscara de rede**|**Nº de ceros**|**Nº de equipos**|
| :- | :- | :- |
|<p>(k) /8</p><p></p>|||
|(l) 255.255.255.248|<p></p><p></p>||
|(m) 255.255.128.0|<p></p><p></p>||
|(n) 255.255.252.0|<p></p><p></p>||
|(o) 255.255.255.0|<p></p><p></p>||
|(p) 240.0.0.0|<p></p><p></p>||
|(q) 254.0.0.0|<p></p><p></p>||
|(r) /18||<p></p><p></p>|
|(s) /29||<p></p><p></p>|


# SOLUCIÓN

**Exercicio 1 : Dada a notación CDIR nos seguintes casos calcula a máscara de rede en decimal separada por octetos.**

|**CDIR**|**Resposta**|
| :- | :- |
|(a) /24|<p>A notación CDIR /24 significa que os primeiros 24 bits da máscara de rede están en "1" e os últimos 8 bits están en "0".</p><p></p><p>Máscara de rede en decimal separada por octetos: **255.255.255.0**</p><p></p>|
|(b) /16|<p>A notación CDIR /16 significa que os primeiros 16 bits da máscara de rede están en "1" e os últimos 16 bits están en "0".</p><p></p><p>Máscara de rede en decimal separada por octetos: **255.255.0.0**</p><p></p>|
|(c) /8|<p></p><p>Máscara de rede en decimal separada por octetos: **255.0.0.0**</p><p></p><p></p>|
|(d) /14|<p></p><p>Máscara de rede en decimal separada por octetos: **255.252.0.0**</p><p></p><p></p>|

**Exercicio 2 : Dada as seguintes máscaras de rede en octetos obtén o seu equivalente en notación CDIR.  Todas as respostas deben ser explicadas e que permitan comprobar a dedución da mesma.**

** 

|**Máscara de rede**|**Resposta**|
| :- | :- |
|(e) 255.255.255.248|<p>Para converter esta máscara a notación CDIR, primeiro debemos contar os bits "1" na máscara. 255.255.255.248 en binario é **11111111.11111111.11111111.11111000**, o que significa que hai 29 bits "1" en total.</p><p></p><p>**Notación CDIR equivalente: /29**</p>|
|(f) 255.255.128.0|<p>En binario, esta máscara é 11111111.11111111.10000000.00000000, o que significa que hai 17 bits "1" en total.</p><p></p><p>Notación CDIR equivalente: /17</p>|
|(g) 255.255.252.0|<p>En binario, esta máscara é **11111111.11111111.11111100.00000000**, o que significa que hai 22 bits "1" en total.</p><p></p><p>Notación **CDIR equivalente: /22**</p><p></p>|
|(h) 255.255.255.0|<p>En binario, esta máscara é 11111111.11111111.11111111.00000000, o que significa que hai 24 bits "1" en total.</p><p></p><p>Notación CDIR equivalente: /24</p><p></p>|
|(i) 240.0.0.0|<p>En binario, esta máscara é 11110000.00000000.00000000.00000000, o que significa que hai 4 bits "1" en total.</p><p></p><p>Notación CDIR equivalente: /4</p><p></p>|
|(j) 254.0.0.0|<p>En binario, esta máscara é **11111110.00000000.00000000.00000000**, o que significa que hai 7 bits "1" en total.</p><p></p><p>Notación CDIR equivalente: **/7**</p><p></p>|


**Exercicio 3 : Calcula a dirección de rede nos seguintes casos:**

1) **192.168.128.15/29**


|<p>Para calcular a dirección de rede, simplemente facemos un AND lóxico entre a dirección IP e a máscara de rede. A dirección IP en binario é 11000000.10101000.10000000.00001111, e a máscara de rede en binario é 11111111.11111111.11111111.11111000.</p><p></p><p>Realizando un AND lóxico:<br>192\.168.128.15</p><p>255\.255.255.248</p><p>-----------------------------</p><p>192\.168.128.8</p><p>**A dirección de rede é 192.168.128.8.**</p><p></p>|
| :- |


1) **10.11.12.13/25**

|<p>A dirección IP en binario é 00001010.00001011.00001100.00001101, e a máscara de rede en binario é 11111111.11111111.11111111.10000000.</p><p></p><p>Realizando un AND lóxico:</p><p></p><p>10\.11.12.13</p><p>255\.255.255.128</p><p>-----------------------------</p><p>10\.11.12.0</p><p></p><p>**A dirección de rede é 10.11.12.0.**</p>|
| :- |






<b>Exercicio 4 : Cal é o numero máximo de equipos nas seguintes redes. Recorda que o número de equipos pódese calcular tendo en conta “o número de 0 que temos na máscara de rede” e que lle chamaremos “n”. Logo o nº de equipos = 2<sup>n</sup> -2 .</b>

**Nota:**

- **recorda que unha máscara de rede como moito ten 32 bits.**
- **Para calcular o número máximo de equipos en cada rede, primeiro debemos contar o número de bits "0" na máscara de rede (n).**



|**Máscara de rede**|**Nº de ceros**|**Nº de equipos**|
| :- | :- | :- |
|<p>(k) /8</p><p></p>|24|2 <sup>24</sup> - 2 = 16.777.214|
|(l) 255.255.255.248|<p>3</p><p></p>|2^3 - 2 = 6|
|(m) 255.255.128.0|<p>15</p><p></p>|2^15 - 2 = 32,766|
|(n) 255.255.252.0|<p>10</p><p></p>|2^10 - 2 = 1,022|
|(o) 255.255.255.0|<p>8</p><p></p>|` `2^8 - 2 = 254|
|(p) 240.0.0.0|<p>4</p><p></p>|` `2^4 - 2 = 14|
|(q) 254.0.0.0|<p>7</p><p></p>|2^7 - 2 = 126|
|(r) /18|14|<p>2^14 - 2 = 16,382</p><p></p>|
|(s) /29|3|<p>2^3 - 2 = 6</p><p></p>|


