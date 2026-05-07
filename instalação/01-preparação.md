# Preparação do Ambiente

## Verificação do modo de boot

### Comando utilizado

- ```bash
  ls /sys/firmware/efi


### Resultado
ls: cannot access '/sys/firmware/efi': No such file or directory

Diretório não encontrado

- <img width="575" height="86" alt="particionamento2" src="https://github.com/user-attachments/assets/883c7a42-3817-4a14-bf09-0563dcd27277" />

Interpretação:
Sistema iniciado em modo BIOS (Legacy)

Decisão:
Optado por reiniciar instalação utilizando UEFI para seguir padrão atual, empresas usam isso hoje em dia.

### resultado 2

depois de configurar o VirtualBox (exemplos na pasta "configuração.md") 

utilizei mesmo comando e obtive esse resultado abaixo: 

O sistema foi iniciado em UEFI.

- <img width="686" height="105" alt="3-particionamento" src="https://github.com/user-attachments/assets/6ac279a5-d287-4701-a360-6ce02df26093" />

### Oque são os arquivos/pastas
- efivars: variáveis do boot do firmware
- fw_vendor: fabricante do firmware
- runtime: serviços do firmware em execução
- config_table: tabelas de configuração do sistema



## Sincronização de horário e teste de conectividade da rede.

### Comando utilizado
```
ping google.com
timedatectl set-ntp true
timedatectl status
```

### Resultado

-<img width="754" height="316" alt="teste-rede-horario" src="https://github.com/user-attachments/assets/b59101bb-fb15-404f-b0e8-3dc354fd42c7" />



### Interpretação
O sistema está com o horário sincronizado automaticamente via NTP e conectado a rede.

### Aprendizado
A sincronização garante funcionamento correto do sistema e evita erros com pacotes. Analisar se teve ping de rede e se está sincronizado data e hora.



### Fonte 
Arch Linux Wiki - Installation Guide
```
man timedatectl
```
