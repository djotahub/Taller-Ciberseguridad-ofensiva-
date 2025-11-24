Taller de Ciberseguridad Ofensiva

> **Material oficial del curso práctico dictado en la Facultad de Informática de la Universidad Nacional de La Plata (UNLP), organizado en colaboración con el Club de Programación.**

[![UNLP](https://img.shields.io/badge/UNLP-Facultad%20de%20Inform%C3%A1tica-0055a0?style=flat-square&logo=university&logoColor=white)](https://www.info.unlp.edu.ar/) [![Club de Programación](https://img.shields.io/badge/Comunidad-Club%20de%20Programaci%C3%B3n-7b16ff?style=flat-square&logo=discord&logoColor=white)](https://linktr.ee/clubdeprogramacion) [![YouTube Qb1t](https://img.shields.io/badge/YouTube-Canal%20Oficial-red?style=flat-square&logo=youtube&logoColor=white)](https://www.youtube.com/@Qb1t) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square&logo=opensource&logoColor=white)](https://opensource.org/licenses/MIT)

---

## 📖 Sobre el Taller

Este repositorio centraliza todos los recursos, laboratorios, diapositivas y material de apoyo utilizados durante el **Taller de Introducción a la Ciberseguridad Ofensiva**.

El objetivo de estas jornadas fue brindar una formación práctica e intensiva sobre las metodologías de **Hacking Ético** y **Penetration Testing**, diseñadas para introducir a los estudiantes en el rol de Red Team, construyendo una base sólida desde los fundamentos hasta la explotación avanzada y el reporte profesional.

---

## 🎯 Temario Abarcado (10 Módulos)

El taller se estructuró en 10 módulos progresivos que cubren el ciclo de vida de un pentest:

### 🟢 Fundamentos
* **Módulo 1: Linux para Hackers (Parte 1):** Manejo esencial de terminal, permisos y sistema de archivos.
* **Módulo 2: Linux para Hackers (Parte 2):** Procesos, redes en Linux, scripting básico en Bash y herramientas esenciales.
* **Módulo 3: Redes para Ciberseguridad:** Protocolos TCP/IP, análisis de tráfico, segmentación y servicios comunes.
* **Módulo 4: Metodologías de Pentesting:** Estándares de industria (PTES, OWASP), ética y fases de un ataque.

### 🟡 Reconocimiento y Enumeración
* **Módulo 5: Análisis de Vulnerabilidades e Intro al Reconocimiento:** OSINT, escaneo pasivo, escaneo activo con Nmap y detección de servicios.

### 🔴 Explotación y Post-Explotación
* **Módulo 6: Explotación de Infraestructura:** Uso de Metasploit Framework, payloads y ataques de fuerza bruta (Hydra).
* **Módulo 7: Escalada de Privilegios (Linux):** Vectores comunes de escalada local: binarios SUID, Kernel Exploits (ej. DirtyCOW), tareas programadas y NFS.
* **Módulo 8: Hacking Web (Server-Side):** OWASP Top 10 práctico: Inyección SQL, Command Injection, LFI/RFI, uso de Burp Suite.
* **Módulo 9: Hacking Web (Client-Side):** Ataques de Cross-Site Scripting (XSS) y robo de sesiones.
* **Módulo 10 (Bonus): Del Laboratorio al Mundo Real:** Evasión de defensas (AV/EDR/WAF), introducción a la informática forense y redacción de informes profesionales.

---

## 📂 Estructura del Repositorio

```plaintext
.
├── 📘 Recursos/       # Diapositivas, guías teóricas y material de referencia (Cheatsheets).
├── 🧪 Laboratorios/   # Guías paso a paso para las prácticas en entornos controlados (VMs).
├── 💻 Scripts/        # Exploits y herramientas personalizadas (Python/Bash) usadas en clase.
└── 📸 Capturas/       # Screenshots de apoyo y soluciones de ejemplo.
```


## 🛠️ Requisitos Previos

Para seguir los laboratorios y utilizar los scripts, se recomienda contar con el siguiente entorno:

- **Software de Virtualización:** 🖥️ VirtualBox o VMware Player/Workstation.
    
- **Máquina Virtual de Atacante:** 🐉 Kali Linux, Parrot OS o similar.
    
- **Máquinas Virtuales Víctima:** (Ej. Metasploitable 2, DVWA) según se indique en cada guía de laboratorio.
    
- **Conocimientos Básicos:** Manejo de terminal Linux y nociones fundamentales de redes (IP, puertos, servicios).
    

---

## 🚀 Comenzando

Para obtener una copia local de todo el material, clona este repositorio en tu máquina:


```
git clone https://github.com/djotahub/Taller-Ciberseguridad-ofensiva-.git
cd Taller-Ciberseguridad-ofensiva-
```

Te recomendamos revisar primero la carpeta `📘 Recursos/` para tener el contexto teórico antes de pasar a los `🧪 Laboratorios/`.

---

## 👨‍🏫 Instructor

Este taller fue diseñado y dictado por:

* **David Jeferson (Qb1t)**

    [![GitHub](https://img.shields.io/badge/-GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/djotahub) [![YouTube](https://img.shields.io/badge/-YouTube-FF0000?style=flat-square&logo=youtube&logoColor=white)](https://www.youtube.com/@Qb1t) [![LinkedIn](https://img.shields.io/badge/-LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/david-jeferson)

> *Material creado con fines educativos para la comunidad académica.*
---

## 🤝 Organización

Este taller fue posible gracias a la colaboración entre:

* [![Facultad de Informática - UNLP](https://img.shields.io/badge/Facultad%20de%20Inform%C3%A1tica-UNLP-0055a0?style=flat-square&logo=university&logoColor=white)](https://www.info.unlp.edu.ar/)
* [![Club de Programación](https://img.shields.io/badge/Comunidad-Club%20de%20Programaci%C3%B3n-7b16ff?style=flat-square&logo=discord&logoColor=white)](https://www.youtube.com/@ClubDeProgramacionUNLP/videos)
    

---

## 📄 Licencia

Este material se distribuye bajo la licencia **MIT**. Eres libre de utilizarlo, modificarlo y compartirlo con fines educativos, dando el crédito correspondiente.
