# Problema: No bootable device

## Situação
Após remover a ISO do Arch Linux e iniciar a VM, foi exibida a mensagem:
"No bootable option or device was found."

<img width="1021" height="839" alt="01-troubleshooting" src="https://github.com/user-attachments/assets/cdc2d282-b2f0-420e-a451-74037f626dad" />


## Causa
O sistema operacional já estava instalado, porém o bootloader ainda não havia sido configurado.
O disco virtual existe. 
O Arch está instalado.
Mas o sistema ainda não tem bootloader.

## Aprendizado
O bootloader é responsável por localizar e iniciar o kernel do sistema operacional durante o boot.

UEFI tentou iniciar: VBOX HARDDISK.

 Mas não encontrou:
 
- GRUB
- systemd-boot
- EFI loader
  
Então o firmware falou: Não sei como iniciar esse sistema.
