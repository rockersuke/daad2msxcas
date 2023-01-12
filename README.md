Daad2MsxCas
***********

English docs below.

Daad2MsxCas versión 1.0 211003 (c) 2020-21 Pedro Fernández

Crea ficheros .cas para emuladores de MSX a partir de bases de datos de aventuras DAAD compiladas para MSX.

Uso
===

Usar: "python daad2msxcas.py -h" en una línea de comados o power-shell para ver las opciones.

El script requiere como argumento un fichero creado con el compilador del DAAD "DC" para MSX (opción -m4) y generará como salida un fichero con el mismo nombre y la extensión ".cas" con la aventura lista para jugarse en un emulador de MSX.

Ej:

python daad2msxcas.py aventura.ddb

Esta orden creará un fichero "aventura.cas" listo para usarse.

Opcionalmente se puede indicar (opción -scr) un fichero para usar como pantalla de carga que debe ser un fichero SCR de ZX Spectrum.

Opcionalmente también se puede indicar (opción -mdg) un fichero de gráficos vectoriales de DAAD para MSX. Éstos se obtienen a partir de las bases de datos gráficas de Spectrum (ficheros .SDG) convirtiéndolas con la utilidad de MS-DOS "DSM.COM" incluida en las utilidades gráficas del DAAD.
Si no se especificase ninguno, daad2msxcas generará internamente un fichero de gráficos en blanco con la información mínima indispensable (básicamente el juego de caracteres por defecto en DAAD).

Opciones
========

- -scr fichero opcional para usar como pantalla de carga (SCR de Spectrum).
- -mdg fichero opcional con gráficos de MSX convertidos desde Spectrum.
- -h Muestra ayuda.
- -v Modo verboso.
- -e Usar intérprete inglés.

Observaciones sobre los ficheros SDG de Spectrum.
=================================================

Para una óptima conversión de ficheros .SDG de Spectrum a .MDG de MSX se recomienda crear los primeros con la utilidad DG para Spectrum en su versión A02D incluida en el fichero disk26.mgt (imagen de disco de 3,5" para unidad disciple de Spectrum) que viene en la descarga original del DAAD. Esta versión es la única que garantiza la compatibilidad con el el programa DSM.COM de conversión a MSX.

La versión A03+3 de DG incluida en el disco DISK33.DSK (imagen de disco de 3" para Spectrum +3) además de tener un bug, utiliza por defecto un sistema de compresión interna incompatible con el programa de conversión.

En caso de tener ya hechos unos gráficos de Spectrum con esta última, existe un script de Python para descomprimirlos. Contactar conmigo en caso de necesidad.

Historia
========

- **1.0 211003**

 -  Cambiado el IM 2 por un IM 1 en el intérprete inglés. Ahora los juegos en inglés no se cuelgan en MSX2. Por qué eso no sucedía con el intérprete español sigue siendo un misterio.


Daad2MsxCas
***********

Daad2MsxCas version 1.0 211003 (c) 2020-21 Pedro Fernández

Creates .cas files for MSX emulators from DAAD adventure databases compiled to MSX.

Usage
=====

Use "python daad2msxcas.py -h" in a commnd line window or power-shell to see the options.

The script requires as argument a file created with DAAD compiler "DC" targetting MSX (option -m4) and will output a file with the same name and a ".cas" extension with the adventure ready to be played in a MSX emulator.

Example:

python daad2msxcas.py advent.ddb

This will create a file "advent.cas" ready to be used.

Optionally you can indicate (-scr option) a file to be used as a loading screen which must be a valid Spectrum SCR screen file.

Also optionalyy you can indicate (-mdg option) a file with MSX DAAD vector graphics. This is obtained from Spectrum graphic databases (.SDG files) converted through the MS-DOS utility "DSM.COM" included among DAAD graphic tools.
If no MDG file is specified daad2msxcas will internally generate a blank graphics file with the minimal required information (basically the default DAAD character set).

Options
=======

- -scr optional file to use as loading screen (Spectrum SCR file).
- -mdg optional file with MSX graphics converted from Spectrum.
- -h shows help.
- -v verbose mode.
- -e use english interpreter.

Some notes about Spectrum SDG graphics.
=======================================

For an optimal SDG to MDG file conversion it's recommended creating the former with the DG Spectrum utility version A02D found inside the DISK26.mgt file (3,5" disk image file for an Spectrum Disciple disk unit) included in DAAD's original download. This is the only version proven to work nicely with the DSM.COM conversion tool.

DG version A03+3 included in DISK33.DSK (3" disk image for the Spectrum +3), apart from being buggy, uses as defualt an internal compression system incompatible with the DSM.COM conversion program.

In case you 've got already some Spectrum graphics made with this last one, there's available a python script to uncompress them. Contact with me if needed!

History
=======

- **1.0 211003**

 - Replaced IM 2 with IM 1 in english terp. Now english games don't crash in MSX2. Why this didn't happened with the spanish terp is still unknown.
