# GIT: Guía de Referencia

## Referencias

### git init

Inicia el espacio de trabajo (workspace) de un repositorio.

Sintaxis:

```bash
git init
```

Ejemplo:

```bash
mkdir mi-proyecto
cd mi-proyecto
git init
```

Aplicación:

Se utiliza al comenzar un proyecto nuevo para que Git pueda rastrear los cambios de los archivos.

---

### git config

Permite editar las variables que modifican el comportamiento del repositorio en los distintos ámbitos: --local, --global, --system.

Sintaxis:

```bash
git config [opciones] <clave> <valor>
```

Ejemplo:

```bash
git config --global user.name "Juan Pérez"
git config --global user.email "juan@example.com"
```

Ver configuración actual:

```bash
git config --list
```

Aplicación:

Configurar la identidad del desarrollador para que los commits registren correctamente el autor de los cambios.

---

### git status

Muestra el estado actual (status) del repositorio.

Sintaxis:

```bash
git status
```

Ejemplo:

```bash
git status
```

Aplicación:

Verificar qué archivos han sido modificados antes de crear un commit.

---

### git add

Agrega cambios al área de preparación (staging area).

Sintaxis:

```bash
git add <archivo>
```

o

```bash
git add .
```

Ejemplo:

```bash
git add README.md
```

Agregar todos los archivos modificados:

```bash
git add .
```

Aplicación:

Seleccionar los cambios que formarán parte del próximo commit.

---

### git commit

Registra cambios en el repositorio sobre la rama actual.

Sintaxis:

```bash
git commit -m "mensaje"
```

Ejemplo:

```bash
git commit -m "Agrega página principal"
```

Aplicación:

Guardar un punto de control en la historia del proyecto para poder revisar o recuperar cambios posteriormente.

---

### git branch

Permite administrar ramas (branches).

Listar ramas:

```bash
git branch
```

Crear una rama:

```bash
git branch desarrollo
```

Ejemplo:

```bash
git branch feature-login
```

Aplicación:

Desarrollar una nueva funcionalidad sin afectar la rama principal del proyecto.

---

### git switch

Permite cambiar entre ramas.

Sintaxis:

```bash
git switch <rama>
```

Ejemplo:

```bash
git switch feature-login
```

Crear y cambiar a una nueva rama:

```bash
git switch -c feature-login
```

Aplicación:

Moverse entre diferentes líneas de desarrollo dentro del mismo repositorio.

---

### git log

Muestra el historial de commits de la rama actual.

Sintaxis:

```bash
git log
```

Ejemplo:

```bash
git log --oneline
```

Salida ejemplo:

```text
a1b2c3d Agrega autenticación
e4f5g6h Commit inicial
```

Aplicación:

Revisar cuándo y por qué se realizaron cambios en el proyecto.

---

### git clone

Clona un repositorio remoto en la máquina local.

Sintaxis:

```bash
git clone <url>
```

Ejemplo:

```bash
git clone https://github.com/usuario/proyecto.git
```

Aplicación:

Obtener una copia local de un proyecto existente para colaborar o analizar su código.

---

### git remote

Administra repositorios remotos asociados al repositorio local.

Ver remotos configurados:

```bash
git remote -v
```

Agregar un remoto:

```bash
git remote add origin https://github.com/usuario/proyecto.git
```

Aplicación:

Conectar el repositorio local con plataformas como GitHub, GitLab o Bitbucket.

---

### git fetch

Descarga información y cambios desde el repositorio remoto sin fusionarlos.

Sintaxis:

```bash
git fetch
```

Ejemplo:

```bash
git fetch origin
```

Aplicación:

Consultar cambios realizados por otros desarrolladores antes de decidir cuándo integrarlos.

---

### git push

Envía commits locales al repositorio remoto.

Sintaxis:

```bash
git push
```

Ejemplo:

```bash
git push -u origin main
```

Aplicación:

Publicar cambios para que el resto del equipo pueda acceder a ellos.

---

### git pull

Obtiene y fusiona los cambios del repositorio remoto en la rama actual.

Sintaxis:

```bash
git pull
```

Ejemplo:

```bash
git pull origin main
```

Aplicación:

Actualizar la copia local del proyecto con los cambios más recientes del equipo.

---

## Flujo de trabajo básico

```bash
# Crear repositorio
git init

# Revisar estado
git status

# Agregar cambios
git add .

# Crear commit
git commit -m "Primer commit"

# Crear rama de trabajo
git switch -c develop

# Revisar historial
git log --oneline

# Asociar repositorio remoto
git remote add origin https://github.com/usuario/proyecto.git

# Publicar cambios
git push -u origin main

# Actualizar cambios remotos
git pull origin main

# Fusion de ramas
git merge ticket/001

```
