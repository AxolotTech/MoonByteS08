[Regresar a index](/README.md)
# Configuracioens MoonByte Rev 4 Base

MoonByte base tiene algunas formas de configurarse de acuerdo a la necesidad, por lo que aquí se explicarán las fucniones de los jumpers y cómo usarlos

## Selección de voltaje para el `MicroMod`
### <span style="color:red">Esta acción puede dañar el `MicroMod`, proceda con cuidado</span>

Algunos microcontroladores pueden trabajar tanto a 5V cómo 3.3V, los `MicroMods` tienen un método para poder definir automáticamente que voltaje es el que van a usar, pero también el usuario puede definir esta alimentación, se explica en la siguiente tabla

| Jumper | Posición | Descripción |
| :------: | :--------: | :-----------: |
|H9|Centro -> Auto|El `MicroMod` decide el voltaje de alimentación <span style="color:green">es lo más recomendable</span>
|H9|Centro -> Manual|Se usa el Voltaje definido en "H11" <span style="color:yellow">seleccionar antes de colocar el `MicroMod`</span>|
|H11|Centro -> 5V|El `MicroMod` estará alimentado a 5V <span style="color:red">No todos los microcontroladores soportan 5V revisar datasheet</span>|
|H11|Centro -> 3.3V|El `MicroMod` estará alimentado a 3.3V|


## Conexión serial
Para poder habilitar la conexión serial del `MicroMod` al programador se deben colocar los jumpers de "H13" verticalmente del centro hacía el letrero "UART"

## Conexiones puerto LCD
El puerto LCD está mapeado de la siguiente manera

| Pin MoonByte | Pin LCD | Funcion        | Habilitado |
| ------------ | ------- | -------------- | ---------- |
| PTF0         | D0      | Datos          | Conectado  |
| PTF1         | D1      | Datos          | Conectado  |
| PTF2         | D2      | Datos          | Conectado  |
| PTF3         | D3      | Datos          | Conectado  |
| PTF4         | D4      | Datos          | Conectado  |
| PTF5         | D5      | Datos          | Conectado  |
| PTF6         | D6      | Datos          | Conectado  |
| PTF7         | D7      | Datos          | Conectado  |
| PTG0         | RS      | RegisterSelect | Conectado  |
| PTG1         | EN      | Enable         | Conectado  |
| PTG2         | R/W     | __Read__/Write | Jumper     |
| PTG3         | LED     | Backlight      | Jumper     |

En caso de que el `MicroMod` colocado no cuente con estos puertos, se pueden usar Jumpers a la conexión física del puerto para conectar los puertos disponibles

Para manejar el contraste se debe mover el potenciometro R54

## Led RGB
El led RGB está mapeado al puerto C PTC0, PTC1 Y PTC2 respectivamente, se puede deconectar quitando los Jumpers

## Tira Led
La tira de 8 leds está conectada al puerto B PTB0-PTB7, se pueden desconectar inhabilitando los switches

## Push Buttons
Los PushButtons están conectados al del PTA0 al PTA3, Se pueden inhabilitar desconectado los switches

### <span style="color:yellow">Advertencia:</span>
El PushButton 0 comparte pin PTA0 con el led integrado en el MicroMod, esto no genera un fallo en si mismo pero debe tomarse en cuenta al diseñarse firmware