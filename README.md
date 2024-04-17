# Doom en Raspberry Pi Pico IWG-101
Como correr Doom64 en Raspberry Pi pico
1.-Descargar los archivos necesarios en el siguiente link:
https://www.dropbox.com/scl/fi/qs54mlor0b0l0ub41dog2/picodoom.rar?rlkey=dojpd0vgtn756uu4eg8v3kjxi&dl=0
2.-Mantener botón "BOOTSEL", mientras conecta con cable microusb la Raspberry Pi Pico al PC
3.-Copiar archivo "doom_tiny.uf2" al directorio de la Raspberry(RPI-RP2)
4.-La raspberry se reiniciará, así que hay que desconectarla y conectarla denuevo(teniendo en cuenta el paso 2, mantener botón "BOOTSEL")
4.-Arrastrar carpeta "picodoom" en el directorio: "C:\"
5.-Abrir cmd de windows(Windows+R, "cmd") y escribir "cd/picodoom", con esto se entrará al directorio de la carpeta movida en el paso anterior(4)
6.-Escribir "picotool load -v -t bin doom1.whx -o 0x10040000", esto va a escribir el contenido del firmware adicional a la memoria de la Raspberry
