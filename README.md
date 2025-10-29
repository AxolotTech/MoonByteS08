# MoonByteS08

### Index de archivos
* [Esquemático MoonByteS08](/docs/Schematics/MoonByte/readme.md)
* [Esquemático MicroMods](/docs/Schematics/MicroMods/readme.md)
* [Binarios Disponibles](/Bin/)
* [Configuraciones MoonByte Base](/docs/MoonByte%20Configs/readme.md)

### ¿Que es MoonByte S08?
MoonByte S08 es una tarjeta de desarrollo diseñada para poder realizar protoipos de manera sencilla con la familia me microcontroladores HCS08 de NXP/Freescale.

Tiene algunas particularidades que la hacen diferente a otras tarjetas de desarrollo:

* Los puertos estan mapeados siempre en el mismo sitio, sin importar el MCU que se coloque
* Se puede intercambiar el MCU en tarjeta mediante el accesorio "MicroMod"
* Todos los accesorios integrados pueden desconectarse de los pines designados, y así mismo se pueden conectar a los pines que se deseen
* Se puede seleccionar manualmente el voltaje de alimentación del MCU, o que el accesorio "MicroMod" se encargue de decidir que voltaje requiere
* Puerto LCD integrado para manejo de Displays LCD
* OSBDM integrado para carga de firmware y debug con USB C
* Conexión serial mediante el USB C
* Soporta hasta 28V de entrada entregando 5V@2A y 3.3V@1.5A

![MoonByte Top View](/img/MoonByteView.png)

### ¿Que es un MicroMod?

Un MicroMod es un módulo extraible de la tarjeta MoonByte, su funcion es crear el mapeo de los pines del MCU para que siempre se puedan tener los puertos conectados en el mismo lugar, por lo que los GPIOs siempre se encontrarán en el mismo header de pines sin importar cual MCU se coloque

Los MicroMods contienen un led embebido conectado directamente al pin PTA0, y un led que indica que se está energizando correctamente

MicroMod de MC9S08QExxx

![MicroMod QE](/img/MicroMod_QE.png)

MicroMod de MC9S08QGxx - MC9S08PBxx

![MicroMod GQ PB](/img/MicroMod_QG_PB.png)