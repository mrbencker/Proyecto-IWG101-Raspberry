# Doom en Raspberry Pi Pico IWG-101

Como correr Doom64 en Raspberry Pi pico

#Parte Firmware

1.-Descargar los archivos necesarios en el siguiente link:
https://www.dropbox.com/scl/fi/qs54mlor0b0l0ub41dog2/picodoom.rar?rlkey=dojpd0vgtn756uu4eg8v3kjxi&dl=0

2.-Mantener botón "BOOTSEL", mientras conecta con cable microusb la Raspberry Pi Pico al PC

3.-Copiar archivo "doom_tiny.uf2" al directorio de la Raspberry(RPI-RP2)
![imagen](https://github.com/mrbencker/raspberry/assets/167112129/e97b6e39-465e-4e10-98f6-1a4f021fdf71)


4.-La raspberry se reiniciará, así que hay que desconectarla y conectarla denuevo(teniendo en cuenta el paso 2, mantener botón "BOOTSEL")

5.-Arrastrar carpeta "picodoom" en el directorio: "C:\"

![imagen](https://github.com/mrbencker/raspberry/assets/167112129/901830e1-0802-498b-972e-570cd091fd0e)


6.-Abrir cmd de windows(Windows+R, "cmd") y escribir "cd/picodoom", con esto se entrará al directorio de la carpeta movida en el paso anterior(4)

![imagen](https://github.com/mrbencker/raspberry/assets/167112129/347ed38c-afed-4f38-b72a-76acfd307864)


7.-Escribir "picotool load -v -t bin doom1.whx -o 0x10040000", esto va a escribir el contenido del firmware adicional a la memoria de la Raspberry

![imagen](https://github.com/mrbencker/raspberry/assets/167112129/2cea99b8-7d58-4fbf-a282-bfee94582a2e)

********Acá es donde saldrá un error de drivers**********

![image](https://github.com/mrbencker/raspberry/assets/167112129/8f9ecb8a-a898-43cc-8ae2-431d217d01ec)

8.- Instalar Zadig USB driver installer: https://zadig.akeo.ie/#google_vignette

9.-Abrir el programa e instalar drivers en el puerto RP2 BOOT(Interface 1)

![image](https://github.com/mrbencker/raspberry/assets/167112129/645793ff-dd3d-4756-84e0-a9969afd95a0)

10.-Nuevamente, hacer el paso 7(escribir "picotool load -v -t bin doom1.whx -o 0x10040000" en cmd cd/picodoom)

*Acá es donde termina la instalación del firmware a la Raspberry*

#Parte instalación hardware
![WhatsApp Image 2024-05-15 at 11 02 27 AM](https://github.com/mrbencker/raspberry/assets/167112129/f8db5971-c208-415c-bb2d-6b2b89cd22d2)

-hicimos uso de una pantalla LCD de 2,4 pulgadas.

![WhatsApp Image 2024-05-15 at 11 02 27 AM(2)](https://github.com/mrbencker/raspberry/assets/167112129/bc39b82e-7e1c-44b6-ac74-263cc497e6bd)
![image](https://github.com/mrbencker/raspberry/assets/167332513/17a9f618-b195-4558-be8a-c7cc9b298479)

-Con ayuda de este tipo de imagen conectamos los cables correspondientes de la raspberry en la protoboard a la pantalla.

![WhatsApp Image 2024-05-15 at 11 02 28 AM](https://github.com/mrbencker/raspberry/assets/167112129/05359b35-9c22-446f-a387-f6d8f39b5a19)
![WhatsApp Image 2024-05-15 at 11 02 28 AM(1)](https://github.com/mrbencker/raspberry/assets/167112129/822f8927-ae88-4ee3-9961-e1d1a279cb6e)
![WhatsApp Image 2024-05-15 at 11 02 27 AM(1)](https://github.com/mrbencker/raspberry/assets/167112129/da14a1c2-6f82-4e12-befc-b4e32643c49e)

-Conectado todo a la pantalla y con el DOOM instalado ya en la raspberry, la pantalla emula el juego de manera correcta, solo falta la instalación de los botones.
**CONEXIÓN DE BOTONES**
El juego necesita de 7 botones para funcionar, los cuales estarán conectados en los siguientes puertos de la raspberry:


Lista de conexiones de botones:

-GP5  Abajo

-GP6  Derecha

-GP8  Izquierda

-GP9  Arriba

-GP4  Menú

-GP2  A

-GP3  B

Estos estarán conectados 
![stock-pictures2f14152fpcb20una20cara205x7-1](https://github.com/mrbencker/raspberry/assets/167112129/fca9b98a-cfa1-47f7-a541-85040bef6a9f)
-Placa (5x7)[cm] PCB
