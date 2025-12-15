# Proyecto de Mecatrónica: Segway Monkey

<img width="465" height="602" alt="segway monkey 1" src="https://github.com/user-attachments/assets/12e261b9-75cd-4628-8131-d64283edf006" />

![foto 1 }](https://github.com/user-attachments/assets/2ec3a501-20fe-44b8-a479-3b68b29c4abe)

## Integrantes: Julio Dufflocq, Bruno Giannetti, Francisca Henríquez y Tomás Wityk.
## Este repositorio fue creado para recopilar todos los archivos asociados al proyecto de robot autobalancín realizado para el ramo ME4250-1 Mecatrónica en la Facultad de Ciencias Físicas y Matemáticas de la Universidad de Chile por el GRUPO 1.

## Índice: 
### 1) Descripción del proyecto
### 2) Carpeta de archivos CAD
### 3) Carpeta de componentes y materiales
### 4) Carpeta de código
### 5) Carpeta de diagramas electrónicos
### 6) Carpeta de registros audiovisuales
(Para este proyecto no se usaron referencias externas a las recomendaciones del eequipo docente. No nos basamos en ningún proyecto de internet ni ocupamos papers académicos sobre el tema.)

## 1) Descripción del proyecto
Aquí podrán encontrar los archivos tipo .f3d, .f3z y .stl ocupados para diseñar e imprimir las diferentes piezas de nuestro robot-mono autobalancín. Escogimos darle al proyeto una estética de chimpancé sobre un Scooter Segway pues nos pareció gracioso y ad-hoc al robot autobalancín ya que los scooters marca Segway ocupan esta tecnología para balancearse.

## 2) Carpeta CAD
El siguiente link es de los archivos CAD que se usaron ([Carpeta CAD](https://github.com/TomasWityk/Proyecto-Mecatronica/tree/c9919a96ce4f7ce4c64e0028fc4ff8c7a873124e/Proyecto%20Mecatronica%20Grupo%201))

## 3) Carpeta de componentes y materiales


## 4) Carpeta de código
**Diagrama de conexiones**
![foto 1 }](Diagrama Conexiones.png)

El sistema eléctrico del robot atobalancín se alimenta a partir de una batería principal, la cual se conecta inicialmente a un interruptor general. Este interruptor permite energizar o desenergizar el sistema completo de manera segura. Desde el interruptor, la alimentación se distribuye hacia los drivers de los motores mediante la entrada de potencia (Power In), proporcionando la energía necesaria para el accionamiento de los motores paso a paso NEMA 17.

Los drivers de motor cumplen una doble función dentro del sistema. Por una parte, reciben la señal de control proveniente del Arduino Uno y suministran la corriente adecuada a los motores. Por otra parte, entregan una salida regulada de 5 V, la cual se utiliza para alimentar simultáneamente la placa Arduino, permitiendo así un funcionamiento integrado del sistema sin requerir una fuente de alimentación adicional para la electrónica de control.

El control de los motores se realiza a través de las señales digitales STEP y DIR de cada driver, las cuales se conectan directamente a pines digitales del Arduino Uno. La señal STEP determina la cantidad y velocidad de los pasos del motor, mientras que la señal DIR define el sentido de giro. De esta forma, el Arduino es capaz de controlar con precisión el movimiento de los motores en función de la señal de control generada por el algoritmo de balanceo.

El sensor de inclinación GY-521 se alimenta directamente desde la salida de 5 V del Arduino Uno. La comunicación entre el sensor y el microcontrolador se realiza mediante el protocolo I\textsuperscript{2}C, utilizando los pines SDA y SCL, los cuales se encuentran asociados a los pines analógicos del Arduino. A través de esta interfaz, el sensor transmite la información de aceleración y velocidad angular necesaria para estimar el ángulo de inclinación del robot.

Finalmente, todas las conexiones de referencia eléctrica (GND) del sistema —incluyendo batería, drivers, Arduino y sensor— se encuentran unidas en un mismo punto común. Esta conexión a tierra compartida es fundamental para garantizar una correcta referencia de voltaje, reducir ruidos eléctricos y asegurar la estabilidad del sistema de control.

**Diagrama de sistema de control**
![foto 1 }](Diagrama Conexiones (1).png)

El sistema implementado corresponde a un sistema de control en lazo cerrado para un robot autobalanceante. El ángulo de inclinación es medido mediante un sensor GY-521, el cual entrega información de aceleración y velocidad angular. Estos datos son procesados por un Arduino Uno, donde se implementa un controlador PID encargado de generar la señal de control. Dicha señal es enviada a los drivers HW-135, que alimentan los motores NEMA 17, permitiendo corregir la inclinación del robot y mantener el equilibrio.

## 5) Carpeta de diagramas electrónicos


## 6) Carpeta de registros audiovisuales
En el siguiente link podrán acceder a la carpeta con los registros audiovisuales del proyecto:
([Carpeta registros audiovisuales](https://github.com/TomasWityk/Proyecto-Mecatronica/tree/d7f582911d95c63d2b97696b3192d372937d1184/Registros%20audiovisuales%20Segway%20Monkey))

