# Laboratorio de redes 02 - Integração usando Windows server + Debian firewall 

## Configurar Windows para usar o Debian
````
No Windows:

Botão direito no ícone de rede
Configurações de Rede e Internet
Configurações avançadas de rede
Ethernet → Editar
````
### Configurar IPv4:
````
IP: 192.168.17.10
MÁSCARA:255.255.255.0
GATEWAY:192.168.17.1
DNS:192.168.17.10
````
### Configurar DNS no Windows Server
````
Configurações de rede
Adaptador (ex: NICGABRIELBISPO)
IPv4 → Propriedades
Configurar DNS - Exemplo: 192.168.17.10
````
## Configurar Encaminhador DNS
````
Gerenciador do Servidor
DNS
Botão direito no servidor
Propriedades
Aba: Encaminhadores
Configurar

Desmarcar: “Usar dicas de raiz...”
Remover DNS inválidos

Adicionar: 192.168.17.1
````
Debian vira saída DNS da rede

### Verificar DHCP
````
No DHCP:
IPv4
Escopo
Opções de escopo
````
Conferir:

- Gateway → termina em 1

- DNS → termina em 10

## Configurar WEB SERVER NO Windows Server

### Instalar IIS
````
Gerenciar
Servidor Web(IIS)
````
### Configurar WEB SERVER
````
Disco local(C:)

Windows

INETPUB

WWWROOT

Colocar o arquivo HTML la dentro
````
### Adicionar mais sites
````
No servidor clicar em IIs

Botão direito no servidor: Gerenciador do serviços de informações da internet(IIS)

Botão direito em SITES: Adicionar site
````




