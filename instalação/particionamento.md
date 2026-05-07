# Particionamento do Disco

## Objetivo
Preparar o disco para instalação do sistema operacional.

## Identificação do disco

### Comando utilizado

```
lsblk 
```

### Resultado

<img width="567" height="108" alt="4-particionamento" src="https://github.com/user-attachments/assets/bec9c98b-4d13-418d-8b8e-c7f7bf6602b8" />

### Análise do resultado 'lsblk

sda - 20.7G - disk (onde vamos instalar)

loop0 - sistema livre 

sr0 - ISO do Arch 

#### importante 
- tudo oque fazer no 'sda' vai apagar os dados dele.
- no meu caso estou usando VM. 

### Aprendizado
Identifiquei o disco onde o sistema será instalado.

## Formatação do disco 
Agora precisa criar o sistema de arquivos para o Linux usar.

### Comandos utilizado 
```
mkfs.fat -F32 /dev/sda1
mkfs.ext4 /dev/sda2
```
oque esses comandos fazem:

mkfs → “make filesystem” (criar sistema de arquivos)
FAT32 - usado no boot UEFI - compatível com firmware
ext4 - padrão do Linux

### Resultado 

<img width="669" height="235" alt="1-formatação" src="https://github.com/user-attachments/assets/48ce5a8b-5b86-4eb8-b3f3-bce2741dd46d" />


## Montagem das partições

### Comandos utilizados
```
mount /dev/sda2 /mnt
mkdir /mnt/boot
mount /dev/sda1 /mnt/boot
```

### Resultado

<img width="495" height="162" alt="1-montagem" src="https://github.com/user-attachments/assets/cea45014-9b8f-4aae-962e-68ee58fa6e87" />


Partições montadas corretamente em /mnt e /mnt/boot.

### Aprendizado
A montagem conecta as partições ao sistema, permitindo a instalação do sistema operacional.

#### Fonte
Arch Linux Wiki → Installation Guide (Mount the file systems) -- 
man pages:
```
man mkfs
man mkfs.ext4
man mount
```













