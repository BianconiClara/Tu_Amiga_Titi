# 🌱 Tu_Amiga_Titi

## Autores
**Avril Ogas** y **Clara Bianconi**

---

## 📝 Descripción del Proyecto

**"Tu Amiga Titi"** es una planta interactiva diseñada como una mascota electrónica que combina automatización y personalización mediante tecnología Arduino. Fue desarrollada como proyecto final para la materia **Laboratorio I (LAB I)**.

Sus funciones principales incluyen:

### 💧 Sistema de Riego Inteligente
- Sensor de humedad que mide el estado del suelo.
- Activa automáticamente una bomba de agua si la planta necesita ser regada.
- Emite sonidos que informan si la planta está seca o ha sido regada en exceso.

### ☀️ Detección de Iluminación
- Sensor de luz que detecta niveles de luminosidad.
- Informa al usuario si la planta necesita más o menos luz, sugiriendo reubicación.

### 🎤 Interacción por Voz
- Comandos básicos: `"Hola"`, `"Chau"`, `"¿Cómo estás?"`.
- Reacción visual en pantalla LCD con expresiones según el estado de la planta.

### 📱 Configuración desde Aplicación Móvil
- App desarrollada en **App Inventor**.
- Ajuste de parámetros como humedad e iluminación óptima.
- Consulta del estado, comandos y notificaciones en tiempo real.

🔍 **Objetivo:** Automatizar el cuidado de plantas y convertirlo en una experiencia divertida, accesible e interactiva para todo tipo de usuario.

---

## 🧰 Tecnologías Utilizadas

- 🔌 Placa **Arduino Mega 2560**
- 💻 **Arduino IDE**
- 📱 **App Inventor**
- 🎨 **Tinkercad** y **Autodesk** para diseño electrónico y 3D

---

## 📂 Contenido del Repositorio
1-Documentos
```
* Anteproyecto 
* Informe del proyecto
* Presentacion PowerPoint 
* Video Tutorial
```
2-APP
```
* Archivo .aia de "APP Inventor"
* Código en bloques de la APP
```
3-Arduino
```
*Código en C++
```
4-Diseño 3D
```
* Diseño 3D Titi
    + obj.mtl
    + tinker.obj
```
5-Diseño Electrónico
```
* Diseño Electronico
    + diseño del circuito electronico-AutoDesk
    + diseño electronico titi.brd
    + diseño electronico-editado
    + diseño electronico-tinkercard
```
# 🛠️ Guía de instalación

Para la correcta instalación del prototipo **"Tu Amiga Titi"**, es necesario seguir los pasos detallados a continuación para asegurar la correcta conexión y configuración de los componentes. Apóyese en los recursos provistos en la documentación (video tutorial) y en el diseño electrónico (esquemático editado).

---

## 1. 📁 Recursos Adicionales

Aprovechá los recursos proporcionados para facilitar el proceso de instalación:

- 🎥 **Video tutorial**: Consulta el video para una explicación visual de cada paso.
- 📄 **Esquemático del diseño electrónico**: Verificá las conexiones siguiendo el esquema editado.

---

## 2. 🔌 Conexiones de Hardware

### 🔹 Paso 1: Configuración Inicial
- Colocá la placa **Arduino Mega** en un lugar seguro, usando una protoboard para evitar cortocircuitos.
- Conectá la placa a tu computadora por USB o una fuente de alimentación adecuada.

### 🔹 Paso 2: Mini Bomba de Agua
- Ubicá la mini bomba en un recipiente con agua.
- Conectá una manguera desde la salida hacia la maceta.
- Asegurate de que esté completamente sumergida.
- Conexión eléctrica:
  - `VCC` y `GND` al módulo de control (relé o transistor).
  - Módulo conectado al Arduino Mega para control desde el software.

### 🔹 Paso 3: Pantalla LCD 20x4 con I2C
- Conectá la pantalla al módulo I2C.
- Conexiones:
  - `VCC`: 5V en Arduino Mega
  - `GND`: GND en Arduino Mega
  - `SDA`: Pin 20
  - `SCL`: Pin 21

### 🔹 Paso 4: Sensor de Humedad
- Insertalo en la tierra de la planta.
- Conexiones:
  - `VCC`: 5V
  - `GND`: GND
  - `Signal`: A0

### 🔹 Paso 5: Sensor Táctil Capacitivo TTP223
- Colocalo donde el usuario pueda acceder fácilmente.
- Conexiones:
  - `VCC`: 5V
  - `GND`: GND
  - `Signal`: D2

### 🔹 Paso 6: Sensor de Luz
- Ubicá el sensor en una zona con buena luz ambiental.
- Conexiones:
  - `VCC`: 5V
  - `GND`: GND
  - `Signal`: A1

### 🔹 Paso 7: Módulo DFPlayer Mini
- Conectalo al **Serial1** del Arduino Mega.
- Conexiones:
  - `VCC`: 5V
  - `GND`: GND
  - `TX`, `RX`: Pines TX1 y RX1
- Conectá un altavoz al DFPlayer (respetá la polaridad).

### 🔹 Paso 8: Módulo Bluetooth HC-06
- Conectalo al **Serial2** del Arduino Mega.
- Conexiones:
  - `VCC`: 5V
  - `GND`: GND
  - `RX`: TX2
  - `TX`: RX2
- Asegurá firmemente todas las conexiones.

---

## 3. 💻 Configuración de Software

### Paso 1: Verificación de Conexiones
Antes de cargar el código:
- Revisá instalación de bomba, sensores y módulos.
- Confirmá conexiones firmes y según el esquema.

### Paso 2: Carga del Código
1. Abrí el **Arduino IDE**.
2. Cargá el sketch del proyecto:
   - Seleccioná la placa **Arduino Mega 2560**.
   - Elegí el puerto correcto.
   - Compilá y subí.
3. Observá que los componentes funcionen correctamente.

---

## 4. 📱 Configuración de la Aplicación Móvil

### 🔗 Descarga e instalación
Descargá la aplicación desde el siguiente enlace:

📥 [ENLACE PARA DESCARGAR LA APP](https://drive.google.com/drive/folders/1TEbHYMsClE_ovuQ5bpBkStJ184czhBTf?usp=sharing)

### 🔄 Emparejamiento Bluetooth
- Activá Bluetooth en el celular.
- Emparejá con el módulo HC-06.
- Confirmá la conexión en la aplicación.
- Configurá las funciones interactivas desde la app.

---

## 5. ✅ Validación Final

### 🔎 Pruebas funcionales
- Verificá funcionamiento de la bomba cuando baja la humedad.
- Observá lecturas en pantalla LCD.
- Probá la interacción táctil.
- Confirmá el sonido emitido por el DFPlayer Mini.

### ⚙️ Ajustes finales
- Corregí cualquier error en la instalación o el código.
- ¡Y listo! Tu prototipo **"Tu Amiga Titi"** estará completamente operativo.

---
