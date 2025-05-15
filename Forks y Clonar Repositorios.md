## Forks y Clonar Repositorios 

**¿Qué es un Fork?**  
Un *fork* es una copia de un repositorio que se crea en tu cuenta de GitHub. Sirve para proponer cambios al proyecto original sin modificarlo directamente.

**¿Cuándo usarlo?**  
- Para contribuir a proyectos donde no tienes permiso directo.  
- Para trabajar en tu versión personal de un repositorio.  
- Para hacer pruebas sin afectar el original.

---

### 🚀 ¿Cómo hacer un Fork?

1. Ve al repositorio que quieres copiar.  
2. Haz clic en el botón **“Fork”** en la esquina superior derecha.  
3. GitHub lo copiará a tu cuenta.  

> 💡 **Tip rápido:** tras forkar, puedes renombrar tu fork en **Settings → Repository name** para diferenciarlo mejor.

---

### 🖥️ ¿Cómo clonar el repositorio a tu PC?

1. En tu repositorio fork, haz clic en **“Code”** y copia la URL (HTTPS o SSH).  
2. Abre tu terminal o Git Bash y ejecuta:
   ```bash
   git clone https://github.com/tu-usuario/nombre-del-repo.git
   cd nombre-del-repo
   ```
3. (Opcional) Configura tu nombre de usuario y email si aún no lo has hecho:
   ```bash
   git config --global user.name "Tu Nombre"
   git config --global user.email "tu@correo.com"
   ```

---

### 🔄 Mantener tu Fork sincronizado

Cuando el proyecto original avanza y quieres traer esos cambios a tu fork:

```bash
# 1. Añade el remoto upstream (repositorio original)
git remote add upstream https://github.com/propietario-original/nombre-del-repo.git

# 2. Descarga las ramas y commits del upstream
git fetch upstream

# 3. Fusiona los cambios en tu main
git checkout main
git merge upstream/main

# 4. Sube los cambios a tu fork en GitHub
git push origin main
```
