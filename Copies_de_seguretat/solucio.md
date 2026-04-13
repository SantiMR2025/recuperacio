Perfecto 👍  
Aquí tienes una **GUÍA TÉCNICA COMPLETA en MARKDOWN**, **lista para que solo tengas que ir pegando las capturas de pantalla**, adaptada a **FP Grado Medio (SMX)**, **Windows 11**, y **Cobian Backup**, cumpliendo el enunciado.

👉 Puedes **copiar y pegar tal cual** en un editor Markdown (VS Code, Typora, GitHub, Moodle, etc.).

***

# 📘 Guía técnica – Copias de seguridad con Cobian Backup

## 1. Datos de la actividad

*   **Ciclo formativo:** Sistemas Microinformáticos y Redes (SMX)
*   **Curso:** 2º
*   **Módulo:** 0226 – Seguridad Informática
*   **Sistema operativo:** Windows 11
*   **Software de copias:** Cobian Backup
*   **Tipo de actividad:** Recuperación y restauración de copias de seguridad

***

## 2. Objetivo de la práctica

El objetivo de esta práctica es aprender a:

*   Crear copias de seguridad completas, incrementales y diferenciales
*   Programar tareas automáticas de backup
*   Verificar los logs de ejecución
*   Restaurar archivos de forma parcial y completa

***

## 3. Entorno de trabajo

*   Sistema Windows 11 funcionando correctamente
*   Usuario con carpeta **Documentos**
*   Disco de destino configurado como **RAID 1**
*   Cobian Backup instalado y ejecutándose en segundo plano

***

## 4. Ejercicio 1 – Backup completo

### 4.1 Creación de la carpeta y archivos

Se crea la carpeta **Dades** dentro de **Documentos** y los siguientes archivos de texto:

*   file1.txt
*   file2.txt
*   file3.txt
*   file4.txt
*   file5.txt

Cada archivo contiene el texto indicado en el enunciado.

📸 **Captura 1 – Carpeta Dades y archivos creados**

    ruta/de/la/captura1.png

***

### 4.2 Creación de la tarea de backup completo

Se crea una nueva tarea en Cobian Backup con las siguientes características:

*   Tipo de copia: Completa
*   Origen: Carpeta Dades
*   Destino: Disco RAID 1
*   Programación: Fecha y hora concreta

📸 **Captura 2 – Configuración de la tarea de backup completo**

    ruta/de/la/captura2.png

***

### 4.3 Verificación del backup

Se comprueba que la copia se ha ejecutado correctamente mediante el archivo de log.

📸 **Captura 3 – Log de backup completo realizado correctamente**

    ruta/de/la/captura3.png

***

## 5. Ejercicio 2 – Backup incremental

### 5.1 Creación de la tarea incremental

Se crea una nueva tarea con:

*   Tipo de copia: Incremental
*   Frecuencia: Cada 5 minutos
*   Origen: Carpeta Dades
*   Destino: Disco RAID 1

📸 **Captura 4 – Configuración tarea incremental**

    ruta/de/la/captura4.png

***

### 5.2 Modificación de archivos (paso 2)

Los cambios se realizan en bloques, esperando 5 minutos entre ellos para permitir la ejecución del backup incremental.

#### Primer bloque de cambios

*   Añadir línea al file1
*   Añadir línea al file2

📸 **Captura 5 – Modificación file1 y file2**

    ruta/de/la/captura5.png

***

#### Segundo bloque de cambios

*   Renombrar file3 a file33
*   Eliminar file5

📸 **Captura 6 – Renombrado y borrado de archivos**

    ruta/de/la/captura6.png

***

#### Tercer bloque de cambios

*   Vaciar el contenido de file4
*   Añadir una nueva línea en file2

📸 **Captura 7 – Últimas modificaciones**

    ruta/de/la/captura7.png

***

### 5.3 Verificación de las copias incrementales

Se revisa el archivo de log para comprobar que se han ejecutado varias copias incrementales y que cada una recoge solo los cambios realizados.

📸 **Captura 8 – Log de copias incrementales**

    ruta/de/la/captura8.png

***

## 6. Ejercicio 3 – Restauración parcial

### 6.1 Restauración del archivo file5

El archivo se restaura copiándolo manualmente desde la copia de seguridad completa hasta la carpeta Dades.

📸 **Captura 9 – Restauración de file5**

    ruta/de/la/captura9.png

***

### 6.2 Restauración de la primera versión de file1

Se recupera la versión inicial del archivo desde la copia completa.

📸 **Captura 10 – Restauración file1 versión original**

    ruta/de/la/captura10.png

***

## 7. Ejercicio 4 – Restauración completa

Se elimina completamente la carpeta Dades y posteriormente se restaura desde la copia completa.

📸 **Captura 11 – Carpeta Dades eliminada**

    ruta/de/la/captura11.png

📸 **Captura 12 – Carpeta Dades restaurada**

    ruta/de/la/captura12.png

***

## 8. Ejercicio 5 – Copia diferencial comprimida

Se crea una nueva tarea diferencial:

*   Compresión ZIP
*   Protección con contraseña
*   Programación: Viernes a las 23:30

📸 **Captura 13 – Configuración copia diferencial comprimida**

    ruta/de/la/captura13.png

***

## 9. Ejercicio 6 – Copia comprimida y cifrada

Se configura una copia comprimida y cifrada de la carpeta **imagenes**, programada cada 12 horas.

📸 **Captura 14 – Copia cifrada de imágenes**

    ruta/de/la/captura14.png
