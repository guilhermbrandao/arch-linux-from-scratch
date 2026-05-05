# Particionamento do Disco

## Objetivo
Preparar o disco para instalação do sistema operacional.

## Identificação do disco

### Comando utilizado

```
lsblk 
```

### Resultado

- <img width="567" height="108" alt="4-particionamento" src="https://github.com/user-attachments/assets/bec9c98b-4d13-418d-8b8e-c7f7bf6602b8" />

### Análise do resultado 'lsblk

sda - 20.7G - disk (onde vamos instalar)

loop0 - sistema livre 

sr0 - ISO do Arch 

#### importante 
- tudo oque fazer no 'sda' vai apagar os dados dele.
- no meu caso estou usando VM. 

### Aprendizado
Identifiquei o disco onde o sistema será instalado.
