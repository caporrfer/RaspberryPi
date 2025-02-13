# Servidor de Minecraft en Raspberry Pi 🛠️🎮

Bienvenido a este repositorio, donde documentaré paso a paso cómo montar un servidor de Minecraft de forma sencilla en una Raspberry Pi. Si quieres jugar con amigos sin complicaciones, este proyecto es para ti. 🚀

## 📌 Objetivo
Facilitar la instalación y configuración de un servidor de Minecraft en una Raspberry Pi, optimizando su rendimiento y permitiendo el acceso de jugadores externos sin necesidad de abrir puertos.

## 📋 Requisitos
Antes de comenzar, asegúrate de contar con lo siguiente:
- Una **Raspberry Pi** (preferiblemente Raspberry Pi 4 o superior)
- Una tarjeta microSD de **al menos 16GB** (se recomienda 32GB+)
- **Sistema operativo Raspberry Pi OS** instalado
- **Conexión a Internet**
- Acceso por **SSH o terminal**
- **Java instalado** (para servidores Java Edition)

## 🚀 Pasos de instalación
1. **Actualizar el sistema**
   ```bash
   sudo apt update && sudo apt upgrade -y
   ```
2. **Instalar Java** (necesario para Minecraft Java Edition)
   ```bash
   sudo apt install openjdk-17-jre -y
   ```
3. **Descargar el servidor de Minecraft**
   ```bash
   wget https://launcher.mojang.com/v1/objects/<versión_del_servidor>.jar -O minecraft_server.jar
   ```
4. **Ejecutar el servidor por primera vez**
   ```bash
   java -Xms512M -Xmx2G -jar minecraft_server.jar nogui
   ```
5. **Aceptar los términos de uso**
   ```bash
   echo "eula=true" > eula.txt
   ```
6. **Configurar el servidor (opcional)**
   - Editar `server.properties` para ajustar las configuraciones deseadas.

7. **Ejecutar el servidor definitivamente**
   ```bash
   java -Xms512M -Xmx2G -jar minecraft_server.jar nogui
   ```

## 🌍 Acceder desde el exterior (sin abrir puertos)
Para permitir que tus amigos jueguen sin abrir puertos, puedes utilizar **ZeroTier** o **Ngrok** para establecer una conexión segura.

## 📌 Notas adicionales
- Es recomendable ejecutar el servidor dentro de `tmux` o `screen` para evitar que se cierre cuando cierras la sesión SSH.
- Puedes automatizar el inicio del servidor al encender la Raspberry Pi con un servicio `systemd`.

## 📜 Licencia
Este proyecto está bajo la licencia **MIT**, por lo que puedes utilizarlo y modificarlo libremente. 😊

---

¡Espero que este tutorial te ayude a montar tu propio servidor de Minecraft en Raspberry Pi! 🎮🔥
