# Laboratorio 2 – Análisis de Protocolos de la Capa de Aplicación

Este repositorio contiene las capturas de tráfico en formato **.pcap** y el informe en **PDF** correspondientes al **Laboratorio 2 de Infraestructura de Comunicaciones (ISIS-3204, Universidad de los Andes)**.  
El objetivo del laboratorio fue analizar distintos protocolos de la capa de aplicación, identificando su comportamiento en la red, los puertos utilizados, las capas involucradas y aspectos de seguridad.

---

## 📂 Contenido del repositorio

- `Laboratorio 2 Grupo 7.pdf` → Informe completo con análisis de cada protocolo, capturas de Wireshark y conclusiones.  
- Archivos `.pcap` con las capturas realizadas:
  - `Ping_DNS_IP.pcap` – Prueba de conectividad hacia servidor DNS.  
  - `Ping_FTP_IP.pcap` – Prueba de conectividad hacia servidor FTP.  
  - `Ping_WEB_IP.pcap` – Prueba de conectividad hacia servidor WEB (por IP).  
  - `Ping_WEB.pcap` – Prueba de conectividad hacia servidor WEB (por URL).  
  - `FTP_download.pcap` – Descarga de archivo desde servidor FTP.  
  - `FTP_upload.pcap` – Subida de archivo al servidor FTP.  
  - `HTTP_view.pcap` – Tráfico de navegación HTTP.  
  - `HTTPS_view.pcap` – Tráfico de navegación HTTPS en distintos sitios.  
  - `YouTube_view.pcap` – Tráfico capturado al navegar y comentar en YouTube.  
  - `VoIP_view.pcap` – Tráfico de una llamada VoIP (SIP, SDP, RTP).  
  - `RTMP_view.pcap` – Tráfico de una transmisión RTMP en vivo.  

---

## 📑 Protocolos analizados

- **DNS (UDP/53)** – Resolución de nombres, consultas tipo A, caché.  
- **FTP (TCP/21 y TCP/20, SFTP TCP/22)** – Transferencia de archivos, comandos RETR/STOR, diferencias entre subida y descarga, limitaciones de seguridad.  
- **HTTP (TCP/80)** – Peticiones GET y respuestas en texto plano.  
- **HTTPS (TCP/443)** – Tráfico cifrado mediante TLS, confidencialidad y protección de datos.  
- **VoIP (SIP UDP/5060, SIP-TLS TCP/5061, RTP en puertos UDP dinámicos)** – Establecimiento de llamadas con SIP, negociación de parámetros con SDP y transmisión de audio en RTP.  
- **RTMP (TCP/1935, RTMPT en HTTP/80 o HTTPS/443)** – Handshake y transmisión de audio/video confiable en streaming.  

---

## 🔐 Seguridad

- Protocolos como **HTTP** y **FTP** transmiten en texto plano, exponiendo credenciales e información sensible.  
- **HTTPS**, **SIPS** y **SFTP** garantizan confidencialidad mediante **TLS/SSH**.  
- VoIP puede mejorar su seguridad con **SRTP** para cifrar medios.  
- RTMP, aunque confiable sobre TCP, depende de encapsulación en puertos estándar (80/443) para atravesar restricciones de red.

---

## 👥 Autores

- David Quiroga – 202310820  
- Nicolás González – 202310041  
- Samuel Rodríguez Torres – 202310140  

---

## 📌 Notas

- Los archivos `.pcap` pueden abrirse con [Wireshark](https://www.wireshark.org/).  
- Para reproducir los experimentos, se recomienda limpiar cachés DNS y cerrar aplicaciones que generen tráfico extra antes de iniciar capturas.  
