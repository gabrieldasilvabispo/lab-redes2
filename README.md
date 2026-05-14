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

### Estrutura do Site

Pasta padrão do IIS: ````C:\inetpub\wwwroot````

O que fica nessa pasta?

Arquivos do site:

index.html
imagens
CSS
JavaScript

### Publicando um Site
````
Pegar:
HTML
imagens
arquivos do projeto

Ir em: C:\inetpub\wwwroot

Remover arquivos padrão do IIS

Colocar:

index.html
imagens
restante do projeto
````
### Configurar DNS para o Site
````
Gerenciador do Servidor
DNS
Botão direito no servidor
Gerenciar DNS

Criar Zona

Botão direito: Zona de Pesquisa Direta

Selecionar: Nova Zona
````
### Criar Registro Host (A)
Dentro da zona criada
````
Área branca → botão direito
Novo Host (A ou AAAA)

Nome: www

Endereço IP: 192.168.17.10
````

## Hospedar Mais de Um Site

### Criar Novo Site
````
Criar pasta

Colocar arquivos HTML:

index.html
imagens
CSS
JS
````

### Adicionar Site no IIS
````
Gerenciador do Servidor
Ferramentas
Gerenciador dos Serviços de Informações da Internet (IIS)
Expandir servidor
Botão direito em:
Sites
Adicionar Site
````
Configuração`:
````
Nome do site

Caminho físico: C:\inetpub

Nome do Host: www.xxxxxx.tec
````







 











