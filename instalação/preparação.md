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

### Pastas
- efivars: variáveis do boot do firmware
- fw_vendor: fabricante do firmware
- runtime: serviços do firmware em execução
- config_table: tabelas de configuração do sistema



