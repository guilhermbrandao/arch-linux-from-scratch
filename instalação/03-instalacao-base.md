# Instalação do Sistema Base

## Objetivo
Instalar os pacotes essenciais do Arch Linux.

### Comando utilizado
```
pacstrap /mnt base linux linux-firmware
```
### Resultado 

<img width="1293" height="806" alt="1-intalacao-base" src="https://github.com/user-attachments/assets/5f4a57e7-3d32-4b4b-becb-321d5d76eb6d" />


- Apenas esperar instalar e verificar se ocorre algum erro.

### Explicação

- base: estrutura básica do sistema
- linux: kernel do sistema operacional
- linux-firmware: firmwares necessários para hardware


### Aprendizado

O pacstrap instala os pacotes diretamente no sistema montado em /mnt, criando a base do novo sistema operacional.

## Geração do fstab

### Comando utilizado
```
genfstab -U /mnt >> /mnt/etc/fstab
```

### Resultado 

<img width="616" height="176" alt="2-instalacao-base" src="https://github.com/user-attachments/assets/27a4acbc-a886-4cd5-bbc1-eb29fe8ba0bc" />


### Explicação
O fstab define quais partições serão montadas automaticamente durante a inicialização do sistema.

- genfstab = gera automaticamente o arquivo
- -U	  = usa UUID dos discos
- /mnt	= sistema instalado
- ">>"  = adiciona conteúdo no arquivo
- /mnt/etc/fstab	= arquivo de configuração
- UUID  = identificador único da partição (Em vez de usar: /dev/sda1, o Linux usa algo mais confiável: UUID=8f2a...)

### Aprendizado
O uso de UUID torna a identificação das partições mais confiável e evita problemas caso o nome dos discos mude.

## Fonte
Arch Linux Wiki -- 
man pages:
```
man pacstrap
man genfstab
```
