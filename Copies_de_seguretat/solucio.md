# Guía técnica – Copias de seguridad con Cobian Backup

***

## 1. Objetivo de la práctica

El objetivo de esta práctica es aprender a:

*   Crear copias de seguridad completas, incrementales y diferenciales
*   Programar tareas automáticas de backup
*   Verificar los logs de ejecución
*   Restaurar archivos de forma parcial y completa

***

## 2. Ejercicio 1 – Backup completo

### 2.1 Creación de la carpeta y archivos

Se crea la carpeta **Dades** dentro de **Documentos** y los siguientes archivos de texto:

*   file1.txt
*   file2.txt
*   file3.txt
*   file4.txt
*   file5.txt

Cada archivo contiene el texto indicado en el enunciado.


![img](img/0006.png)
![img](img/0001.png)
![img](img/0002.png)
![img](img/0003.png)
![img](img/0004.png)
![img](img/0005.png)
***

### 2.2 Creación de la tarea de backup completo

Se crea una nueva tarea en Cobian Backup con las siguientes características:

*   Tipo de copia: Completa
*   Origen: Carpeta Dades
*   Destino: Disco RAID 1
*   Programación: Fecha y hora concreta

![img](img/0008.png)
![img](img/0009.png)
![img](img/0010.png)
![img](img/0011.png)

***

### 2.3 Verificación del backup

Se comprueba que la copia se ha ejecutado correctamente mediante el archivo de log.

![img](img/0012.png)

***

## 3. Ejercicio 2 – Backup incremental

### 3.1 Creación de la tarea incremental

Se crea una nueva tarea con:

*   Tipo de copia: Incremental
*   Frecuencia: Cada 5 minutos
*   Origen: Carpeta Dades
*   Destino: Disco RAID 1


![img](img/0013.png)
![img](img/0014.png)

***

### 3.2 Modificación de archivos (paso 2)

Los cambios se realizan en bloques, esperando 5 minutos entre ellos para permitir la ejecución del backup incremental.


*   Añadir línea al file1
*   Añadir línea al file2
*   Renombrar file3 a file33
*   Eliminar file5
*   Vaciar el contenido de file4
*   Añadir una nueva línea en file2

![img](img/0015.png)

***

## 4. Ejercicio 3 – Restauración parcial

### 4.1 Restauración del archivo file5

El archivo se restaura copiándolo manualmente desde la copia de seguridad completa hasta la carpeta Dades.

📸 **Captura 9 – Restauración de file5**

![img](img/0016.png)
![img](img/0017.png)

***

### 4.2 Restauración de la primera versión de file1

Se recupera la versión inicial del archivo desde la copia completa.

![img](img/0018.png)

***

## 5. Ejercicio 4 – Restauración completa

Se elimina completamente la carpeta Dades y posteriormente se restaura desde la copia completa.

![img](img/0021.png)
![img](img/0022.png)
![img](img/0023.png)
![img](img/0024.png)
![img](img/0025.png)

***

## 6. Ejercicio 5 – Copia diferencial comprimida

Se crea una nueva tarea diferencial:

*   Compresión ZIP
*   Protección con contraseña
*   Programación: Viernes a las 23:30

![img](img/0026.png)
![img](img/0027.png)
![img](img/0028.png)

***

## 7. Ejercicio 6 – Copia comprimida y cifrada

Se configura una copia comprimida y cifrada de la carpeta **imagenes**, programada cada 12 horas.

![img](img/0029.png)
![img](img/0030.png)
![img](img/0031.png)
![img](img/0032.png)
