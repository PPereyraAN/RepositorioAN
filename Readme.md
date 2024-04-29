# Introducción a Git

Git es un sistema de control de versiones distribuido ampliamente utilizado en el desarrollo de software para el seguimiento de cambios en archivos y coordinación de trabajo entre múltiples personas en proyectos colaborativos. Proporciona un historial completo de cambios, facilita la colaboración entre desarrolladores y permite la gestión eficiente de proyectos de cualquier tamaño.

Algunas de las razones por las que Git es importante en el desarrollo de software son:

**Historial de cambios**: Git mantiene un historial completo de todos los cambios realizados en el código, lo que permite a los desarrolladores revisar y volver a versiones anteriores si es necesario.

**Colaboración**: Git facilita la colaboración entre equipos de desarrollo al permitir que varios desarrolladores trabajen en el mismo proyecto de manera simultáneamente y fusionen sus cambios de manera eficiente.

**Ramas (branches)**: Git permite a los desarrolladores trabajar en diferentes ramas de desarrollo de forma independiente, lo que facilita la implementación de nuevas características o la corrección de errores sin afectar la rama principal del proyecto.

## Conceptos básicos de Git:

**Repositorio**: Un repositorio Git es un directorio que contiene todos los archivos y carpetas de un proyecto, así como el historial de cambios asociado.

**Commits**: Un commit en Git representa un conjunto de cambios realizados en el código fuente en un momento determinado. Cada commit tiene un mensaje descriptivo que indica los cambios realizados.

**Ramas (branches)**: Las ramas en Git son versiones paralelas del repositorio que permiten a los desarrolladores trabajar en características o correcciones de errores de manera independiente.

**Fusiones (merges)**: Una fusión en Git combina los cambios realizados en una rama con otra rama, lo que permite integrar nuevas características o correcciones de errores en la rama principal del proyecto.

## Instalación de Git

Para instalar Git en tu sistema, seguí estos pasos:

1. **Windows:** Descarga el instalador desde el sitio web oficial de Git: [Git Downloads](https://git-scm.com/downloads) y sigue las instrucciones de instalación.
   
2. **macOS:** Instala Git utilizando Homebrew ejecutando el siguiente comando en la terminal:

    ```bash
    brew install git
    ```

3. **Linux:** En la mayoría de las distribuciones de Linux, Git está disponible en los repositorios de paquetes. Puedes instalarlo utilizando el gestor de paquetes de tu distribución.

## Configuración de Git

Después de instalar Git, es importante configurar tu nombre de usuario y dirección de correo electrónico, que se utilizarán para identificar tus contribuciones a los proyectos.

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu_correo@example.com"
```

## Git Clone

El comando **git clone** se utiliza para crear una copia local de un repositorio remoto existente. Esta copia incluirá todos los archivos, ramas y el historial de commits del repositorio remoto.

### **Sintaxis:**
```bash
git clone <URL_del_repositorio_remoto> [<nombre_directorio_local>]
```
-**<URL_del_repositorio_remoto>:** La URL del repositorio remoto que deseas clonar. Puede ser una URL HTTPS o SSH.

-**[<nombre_directorio_local>]:** (Opcional) El nombre de la carpeta en la que deseas clonar el repositorio. Si no se especifica, Git creará un directorio con el mismo nombre que el repositorio remoto.

### **Ejemplo:**

```bash
git clone https://github.com/ejemplo/repo.git
```

## Git Pull

El comando **git pull** se utiliza para recuperar cambios desde un repositorio remoto y fusionarlos automáticamente en tu rama actual. Básicamente, git pull es equivalente a ejecutar git fetch seguido de git merge.

### **Sintaxis:**
```bash
git pull <remote> <branch>
```

### Git Add

El comando **git add** se utiliza para agregar cambios al área de preparación en Git. Esto significa que los cambios realizados en los archivos se preparan para ser incluidos en el próximo commit.

#### Sintaxis:

```bash
git add <nombre_del_archivo>
git add .
```
-**<nombre_del_archivo>:** El nombre del archivo que deseas agregar al área de preparación. Puedes especificar múltiples archivos separándolos por espacios. También puedes utilizar un punto (.) para agregar todos los archivos modificados y eliminados al área de preparación.

### Git Commit

El comando **git commit** se utiliza para guardar los cambios realizados en el área de preparación en el repositorio Git local. Cada commit representa una instantánea de los archivos en el repositorio en un momento específico, junto con un mensaje descriptivo que explica los cambios realizados.

#### Sintaxis:

```bash
git commit -m "Mensaje del commit"
```

### Git Push

El comando `git push` se utiliza para subir los cambios realizados en el repositorio local al repositorio remoto correspondiente. Esto actualiza el historial de commits en el repositorio remoto con los cambios realizados en el repositorio local.

#### Sintaxis:

```bash
git push <nombre_remoto> <nombre_rama>
```

-**<nombre_remoto>:** Especifica el nombre del repositorio remoto al que deseas enviar los cambios.

-**<nombre_rama>:** Especifica el nombre de la rama que deseas enviar al repositorio remoto.

### **Ejemplo:**

```bash
git push origin main
```
Este comando envía los cambios de la rama "main" del repositorio local al repositorio remoto llamado "origin".

```bash
git push -u origin main
```
Este comando envía los cambios de la rama "main" del repositorio local al repositorio remoto llamado "origin" y configura la rama local "main" para realizar un seguimiento de la rama remota "main". Después de configurar el upstream, en futuros pushes, puedes simplemente ejecutar **git push** sin especificar la rama remota y local, y Git realizará el push a la rama remota correspondiente automáticamente.


# Crear un Repositorio en GitHub y Vincularlo con un Repositorio Local

## 1. Crear un Repositorio en GitHub

- Ingresar a  [GitHub](https://github.com/) e iniciar sesión.
- Hacer clic en el signo más (+) en la esquina superior derecha y seleccioná "New repository" (Nuevo repositorio).
- Completar la información del repositorio, como el nombre, la descripción y la visibilidad.
- Hacer clic en "Create repository" (Crear repositorio) para crear el repositorio en GitHub.

## 2. Inicializar un Repositorio Local

Abrir la terminal o línea de comandos y navegar al directorio donde se va a crear tu repositorio.

```bash
git init
```

## 3. Vincular el Repositorio Local con el Repositorio Remoto y Subir tus Cambios

- Copiar la URL del repositorio creado en GitHub.
- En la terminal, dentro del directorio de tu repositorio local, ejecutar el siguiente comando para agregar la URL del repositorio remoto:

```bash
git remote add origin https://github.com/PPereyraAN/PruebaRepositorios.git
```

## 4. Subir tus Cambios al Repositorio Remoto
Una se vinculó el repositorio local con el remoto, se envian los cambios al repositorio remoto ejecutando el siguiente comando:

```bash
git push -u origin master
```
# Git Branches

Una rama en Git es una línea de desarrollo independiente que permite trabajar en nuevas funcionalidades, arreglos de errores o experimentos sin afectar el código principal.

#### Crear una nueva rama:

```bash
git branch <nombre_rama>
```
#### Cambiar a una rama existente:

```bash
git checkout <nombre_rama>
```

#### Listar todas las ramas:

```bash
git branch
```
#### Eliminar una rama:

```bash
git branch -d <nombre_rama>
```
#### Fusionar ramas:

```bash
git merge <nombre_rama>
```
