# Doom en Raspberry Pi Pico IWG-101

Como correr Doom64 en Raspberry Pi pico

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

  
