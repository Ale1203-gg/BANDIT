# BANDIT

## ¿Qué es OverTheWire - Bandit?  

OverTheWire es una plataforma de **wargames** diseñada para mejorar habilidades en **seguridad informática** y **Linux**.  
El juego **Bandit** es ideal para principiantes que quieren aprender a usar la terminal de Linux, comandos de seguridad y manipulación de archivos.  

 **Objetivo:** Acceder a cada nivel utilizando **SSH**, leer archivos ocultos y resolver desafíos de seguridad.  

---

##  Acceder al Nivel 0  

Para empezar, necesitas conectarte vía **SSH** al servidor de OverTheWire.  

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
**Contraseña Inicial:** `bandit0`  

**Explicación:**  
- `bandit0`  Usuario del primer nivel.  
- `bandit.labs.overthewire.org`  Servidor de OverTheWire.  
- `-p 2220` Especifica el puerto **2220** (en lugar del 22 por defecto).  

Si la conexión es exitosa, verás la terminal del servidor.  

---

##  Bandit Nivel 0 → Nivel 1  

Para avanzar al siguiente nivel, debes encontrar la contraseña en un archivo llamado `readme`.  

```bash
ls
cat readme
```

**Explicación:**  
- `ls`  Lista los archivos en el directorio.  
- `cat readme` Muestra el contenido del archivo.  

La contraseña obtenida te permitirá acceder al **nivel 1**:  

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```

Cuando pida la contraseña, ingresa la que encontraste en `readme`.  

---

##  Bandit Nivel 1  Nivel 2  

En este nivel, la contraseña está en un archivo oculto llamado `-`. Para visualizarlo y leer su contenido, usa:  

```bash
ls -a
cat ./-
```

 **Explicación:**  
- `ls -a`  Muestra archivos ocultos.  
- `cat ./-`  Usa `./` para evitar errores con nombres de archivo que parecen comandos.  

Copia la contraseña y úsala para acceder al nivel 2.  

```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
```

---

##  Consejos Generales para Avanzar  

- Usa `ls -a` para ver archivos ocultos.  
- `cat` muestra el contenido de archivos.  
- `cd` para cambiar de directorio.  
- `file` para saber el tipo de archivo.  
- `strings` extrae texto legible de archivos binarios.  
- `find / -name "archivo"` busca archivos en el sistema.  
- `grep` ayuda a buscar texto dentro de archivos.  

---
