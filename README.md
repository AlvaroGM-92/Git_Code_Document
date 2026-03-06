# 📚 Guía rápida de Git y GitHub

## Conceptos básicos

* **Working Directory** → Archivos en tu carpeta de trabajo.
* **Staging Area** → Archivos preparados para hacer commit.
* **Commit** → Instantánea del proyecto guardada en el repositorio local.
* **Push** → Subir commits al repositorio remoto.

---

# Inicializar repositorio

Crear repositorio local:

```bash
git init
```

---

# Añadir archivos al staging

Añadir todos los archivos:

```bash
git add .
```

Añadir un archivo específico:

```bash
git add archivo.txt
```

---

# Ver estado del repositorio

```bash
git status
```

---

# Quitar archivos del staging

```bash
git rm --cached archivo.txt
```

---

# Crear commit

```bash
git commit -m "Mensaje descriptivo"
```

---

# Conectar con GitHub

Añadir repositorio remoto:

```bash
git remote add origin URL
```

Ver repositorios remotos configurados:

```bash
git remote -v
```

---

# Subir cambios al repositorio remoto

```bash
git push origin main
```

La primera vez pedirá iniciar sesión en GitHub.

---

# Historial de commits

Ver historial completo:

```bash
git log
```

Versión resumida:

```bash
git log --oneline
```

Salir del historial:

```
q
```

---

# Diferencias entre archivos

Ver cambios no añadidos al staging:

```bash
git diff
```

Ver cambios añadidos al staging:

```bash
git diff --staged
```

---

# Restaurar cambios

Restaurar todos los archivos al último commit:

```bash
git restore .
```

Restaurar un archivo concreto:

```bash
git restore archivo.txt
```

Quitar archivo del staging:

```bash
git restore --staged archivo.txt
```

---

# Volver atrás en commits

Mantener cambios en staging:

```bash
git reset --soft HEAD~1
```

Mantener cambios fuera del staging:

```bash
git reset --mixed HEAD~1
```

Eliminar cambios:

```bash
git reset --hard HEAD~1
```

Volver a un commit concreto:

```bash
git reset --hard ID_COMMIT
```

---

# Ramas (Branches)

Ver ramas:

```bash
git branch
```

Crear una rama nueva:

```bash
git branch nueva-rama
```

Cambiar de rama:

```bash
git switch rama
```

Crear y cambiar a una rama nueva:

```bash
git switch -c nueva-rama
```

---

# Merge (Unir ramas)

Moverse a la rama destino:

```bash
git switch main
```

Unir otra rama:

```bash
git merge rama-feature
```

Cancelar un merge:

```bash
git merge --abort
```

---

# Eliminar ramas

Eliminar rama fusionada:

```bash
git branch -d rama
```

Eliminar rama forzadamente:

```bash
git branch -D rama
```

---

# Clonar repositorio

Clonar repositorio:

```bash
git clone URL
```

Clonar en la carpeta actual:

```bash
git clone URL .
```

---

# Sincronizar con GitHub

Actualizar repositorio local:

```bash
git pull origin main
```

Traer cambios sin fusionarlos:

```bash
git fetch
```

---

# Flujo típico de trabajo

```bash
git add .
git commit -m "mensaje"
git push origin main
```

---

# .gitignore

Archivo para evitar subir archivos innecesarios al repositorio.

Ejemplo:

```
node_modules
.env
*.log
```

---

# Pull Request (GitHub)

1. Hacer **push** de los cambios.
2. En GitHub pulsar **Compare & Pull Request**.
3. Crear la **Pull Request**.
4. Revisar cambios.
5. Pulsar **Merge Pull Request**.

---

# Fork (Open Source)

**Fork** → Copia de un repositorio en tu cuenta de GitHub.

Flujo de trabajo:

1. Hacer **Fork** del repositorio.
2. Clonar el fork en local.
3. Realizar cambios.
4. Hacer **Push** al fork.
5. Crear **Pull Request** al repositorio original.
