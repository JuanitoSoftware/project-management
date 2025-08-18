# 💬 Unified Chat Widget + TTS - Ficha Técnica  

**Desarrollado por JuanitoSoftware&Games – 2025**  

**Licencia:** Uso No Comercial  

---

## 🧾 Descripción  

**Unified Chat Widget** es una aplicación para **OBS** que unifica en tiempo real los mensajes de chat de **Twitch, YouTube y Kick** en un único widget web.  
Está desarrollada en **Node.js** con servidor **Express + WebSocket**, e integra un sistema de **Text-to-Speech (TTS)** opcional basado en **Python** y la librería `TTS` para locución automática de mensajes.  

👉 Ideal para streamers que buscan **centralizar la interacción** de sus chats en una sola ventana y añadir **voz sintetizada** a los mensajes en pantalla.  

---

## 🛠️ Características principales  

- 🌐 Unificación de chats de **Twitch, YouTube y Kick**.  
- 💻 Widget **HTML** para incrustar en **OBS** como fuente de navegador.  
- 🔄 Comunicación en tiempo real mediante **WebSocket**.  
- 🗂️ Historial de mensajes persistente en `messages/latest.json`.  
- 🗣️ Sistema **TTS en español** mediante servidor **Flask + TTS.api**.  
- 🎛️ **Comandos de control desde chat:**  
  - `/TTS_ON` → Activar locución (solo admins autorizados).  
  - `/TTS_OFF` → Desactivar locución.  
- 🔒 Lista de **administradores autorizados** para controlar TTS.  
- 🚫 Ignora comandos y prefijos especiales (`/`, `!`) para evitar lecturas innecesarias.  
- ⚡ Compatible con **Windows, Linux y macOS**.  

---

## 🗃️ Estructura de archivos  

