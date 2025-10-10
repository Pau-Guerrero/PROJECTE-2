# GUIA T03

## INSTAL.LACIÓ DISC DUR
Primer de tot, he instal·lat el disc dur a la màquina virtual.

![Configuracio e instal.lacio del disc dur](img/image1.png)


## CANVIAR LA CONTRASENYA
En engegar la màquina, premem el botó Shift i s’obrirà aquest menú. Després, triem la segona opció: “Advanced options for Zorin”.

![Primer menu de zorin](img/image2.png)

Ara s’obrirà aquest menú, on seleccionarem la segona opció: “Zorin, with Linux 6.8.0-85-generic (recovery mode)”.

![Segona menu de zorin](img/image3.png)

Ara s’obrirà aquest menú i triarem l’opció que diu “root”.

![Menu de root](img/image4.png)

Ara posarem “mount -rw -o remount /” per poder canviar la contrasenya.

![Primera comanda de linux](img/image5.png)

Ara utilitzarem la comanda passwd miquel per canviar la contrasenya de l’usuari miquel.

![Comanda per canviar la contrasenya](img/image6.png)

Una vegada canviat la contrasenya reinciciarem la maquina y al inciciar sesio posarem la contrasenya feta

![Iniciar sesio](img/image7.png) ![Escritori de Zorin](img/image8.png)

## FORTIFICAR L'ACCES AL GRUB

Ara posem la comanda de “grub-mkpasswd-pbdf2” per generar el hash de la contrasenya

![Comanda per generar el hash de la contrasenya](img/image10.png)

Per reforçar l’accés al GRUB, escriurem la comanda: sudo nano /etc/grub.d/40_custom.

![Comanda per entrar a l'arxiu](img/image9.png)


En executar aquesta comanda s’obrirà la pantalla on introduirem aquestes dues línies. 
set superusers="miquel"
password_pbkdf2 miquel hash_de_la_contrasenya

![Codi que canvia el arxiu](img/image11.png)

I després, per actualitzar el GRUB, escriurem sudo update-grub.

![Comanda per actualitzar el GRUB](img/image12.png)
