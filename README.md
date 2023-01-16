# SIEMAzure_HoneyPot

SIEM para monitorar uma VM HoneyPot com Azure.

Eu desativei todas as proteções de firewall, para que a máquina ficasse exposta a rede, e então começasse a sofrer ataques.

Sistema de log com classificação de: Origem, destino, username, país, estado, longitude, altitude, label e timestamps.

![image](https://user-images.githubusercontent.com/122818447/212739064-dc3655c9-4853-4066-b325-fddb5a405b5a.png)


VM utilizada como honeypot da azure:

![image](https://user-images.githubusercontent.com/122818447/212739670-d7feb666-6c6f-4334-9567-2887350dc191.png)

Este PowerShell script registra todas as tentativas falhas de login no HoneyPot, pega uma chave API do site IPGeolocation.io, que detecta a localização de um IP.

![image](https://user-images.githubusercontent.com/122818447/212740533-493f06fb-7435-4c48-b50c-10d31ee89550.png)

Com essas informações, é possível utilizar o Microsoft Sentinel para criar um mapa dos ataques.

![image](https://user-images.githubusercontent.com/122818447/212740994-19aaee78-778b-4bca-b5af-7f9bf12e7706.png)
(States=United States)

Página de overview do Microsoft Sentinel da vm, é possível verificar quantos logs ao todo foram registrados do script:

![image](https://user-images.githubusercontent.com/122818447/212742609-c4a8adb8-2374-4ef9-b17c-ea54b0faa370.png)

*Créditos:
Projeto feito com Josh Madakor, utilizei o script PowerShell disponibilizado por ele.* 

