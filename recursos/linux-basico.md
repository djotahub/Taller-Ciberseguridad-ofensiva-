# 🐧 Linux Básico para Ciberseguridad (Clases 1 y 2)

Este cheatsheet reúne los comandos esenciales  de  las clases 1 y 2, **con aplicación directa en análisis forense, pentesting y administración segura**.  

---

## 📍 Navegación y Orientación

| Comando | Sintaxis | Explicación | Uso en Ciberseguridad |
|---------|----------|-------------|------------------------|
| **pwd** | `pwd` | Muestra el directorio actual. | Evita ejecutar comandos destructivos en la carpeta equivocada. |
| **ls** | `ls`, `ls -la` | Lista archivos. Con `-la` muestra ocultos y detalles. | Identificar backdoors ocultos (ej. `.malware`), revisar permisos. |
| **cd** | `cd /ruta` | Cambia de directorio (absoluto o relativo). | Explorar `/var/log` (logs), `/etc` (configs), `/tmp` (archivos temporales maliciosos). |
| **tree** | `tree /ruta` | Representa directorios en árbol. | Útil para mapear un servidor web comprometido. |

---

## 📂 Creación y Gestión de Archivos

| Comando | Sintaxis | Explicación | Uso en Ciberseguridad |
|---------|----------|-------------|------------------------|
| **mkdir** | `mkdir carpeta`, `mkdir -p ruta/sub` | Crea directorios. | Preparar entorno de análisis o sandbox. |
| **touch** | `touch archivo.txt` | Crea archivo vacío o actualiza fecha de modificación. | Verificar o simular ataques de *timestomping*. |
| **cp** | `cp origen destino`, `cp -r dir/ destino/` | Copia archivos o directorios. | Clonar logs antes de analizarlos (mantener integridad forense). |
| **mv** | `mv origen destino` | Mueve o renombra archivos. | Poner binarios sospechosos en cuarentena. |
| **rm** | `rm archivo`, `rm -rf dir/` | Elimina archivos/carpetas. **Irreversible.** | Borrar scripts maliciosos en `/tmp`. Siempre confirmar con `pwd`. |

---

## 📖 Lectura e Inspección de Archivos

| Comando | Sintaxis | Explicación | Uso en Ciberseguridad |
|---------|----------|-------------|------------------------|
| **cat** | `cat archivo` | Muestra contenido completo. | Leer `.bash_history` y configs alteradas. |
| **less** | `less archivo` | Visualiza archivo grande, navegación interactiva. | Examinar logs extensos sin perder info. |
| **more** | `more archivo` | Visualiza archivo, solo hacia adelante. | Revisión rápida de registros. |
| **head** | `head -n 20 archivo` | Muestra primeras n líneas. | Revisar cabecera de logs/configs. |
| **tail** | `tail -n 50 archivo` | Muestra últimas n líneas. | Ver actividad reciente de un log. |
| **tail -f** | `tail -f archivo` | Sigue archivo en tiempo real. | Monitorear ataques de fuerza bruta en `auth.log`. |

---

## ✍️ Edición de Archivos

| Comando | Sintaxis | Explicación | Uso en Ciberseguridad |
|---------|----------|-------------|------------------------|
| **nano** | `nano archivo` | Editor de texto simple en terminal. | Modificar configs seguras (`sshd_config`, `crontab`). |
| **vi/vim** | `vim archivo` | Editor avanzado. | Ampliamente usado en servidores remotos. |

---

## 🔑 Permisos y Propiedades

| Comando | Sintaxis | Explicación | Uso en Ciberseguridad |
|---------|----------|-------------|------------------------|
| **ls -l** | `ls -l archivo` | Muestra permisos, dueño, grupo, tamaño. | Detectar permisos débiles o SUID sospechosos. |
| **chmod (simbólico)** | `chmod u+x archivo` | Cambia permisos con letras. | Dar permisos de ejecución a un script de prueba. |
| **chmod (numérico)** | `chmod 755 archivo` | Cambia permisos con valores octales (r=4,w=2,x=1). | Configurar binarios seguros (ej. scripts web). |
| **chown** | `chown usuario:grupo archivo` | Cambia dueño/grupo de un archivo. | Reasignar archivos de servicios (ej. `www-data`). |
| **chgrp** | `chgrp grupo archivo` | Cambia grupo propietario. | Ajustar control de acceso compartido. |
| **whoami** | `whoami` | Muestra usuario actual. | Confirmar si conseguiste escalada de privilegios. |
| **groups** | `groups usuario` | Muestra grupos a los que pertenece un usuario. | Detectar acceso privilegiado oculto. |

---

## ⚡ Extra: Comandos útiles en forense y pentesting

| Comando | Sintaxis | Explicación | Uso en Ciberseguridad |
|---------|----------|-------------|------------------------|
| **history** | `history` | Lista comandos ejecutados. | Ver huellas del atacante en la terminal. |
| **which** | `which comando` | Muestra ruta de un comando. | Detectar binarios falsos en el PATH. |
| **file** | `file archivo` | Identifica tipo de archivo. | Confirmar si un binario es ELF o un script camuflado. |
| **find** | `find / -name archivo` | Busca archivos por nombre/propiedades. | Ubicar webshells o archivos recientes. |
| **grep** | `grep "cadena" archivo` | Busca texto en archivos. | Buscar IOC (IPs, hashes, URLs) en logs. |

---

📌 **Tips de seguridad en terminal**:  
- Usá **rutas absolutas** en entornos comprometidos → `/bin/ls` en lugar de `ls`.  
- Siempre revisá permisos (`ls -l`) antes de manipular archivos críticos.  
- Con `history` y `tail -f /var/log/auth.log` podés reconstruir gran parte de la actividad de un atacante.  

---
by Qb1t:.
