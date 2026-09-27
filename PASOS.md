# Cómo publicar este sitio

El repositorio local ya está inicializado y con el primer commit hecho. Falta crearlo en
GitHub y empujarlo.

## 1. Crear el repositorio vacío en GitHub

En <https://github.com/new>, con la cuenta **FinochioAdrian**:

- **Repository name:** `FinochioAdrian.github.io` — exactamente así, respetando mayúsculas
- **Public**
- **No** tildar «Add a README file», ni `.gitignore`, ni licencia — tiene que quedar vacío
- Create repository

## 2. Empujarlo

Abrí una terminal en esta carpeta y pegá esto. Git te va a pedir autenticarte la primera vez
(se abre el navegador, o te pide usuario y token personal).

```bash
git remote add origin https://github.com/FinochioAdrian/FinochioAdrian.github.io.git
git push -u origin main
```

Si te dice que `origin` ya existe:

```bash
git remote set-url origin https://github.com/FinochioAdrian/FinochioAdrian.github.io.git
git push -u origin main
```

## 3. Verificar que Pages esté activo

En el repositorio → **Settings** → **Pages**. Para un sitio de usuario debería decir
«Your site is live at https://finochioadrian.github.io/». Si no, poné:

- **Source:** Deploy from a branch
- **Branch:** `main` · carpeta `/ (root)` · Save

La primera publicación tarda uno o dos minutos. Después, cada `git push` actualiza el sitio.

## 4. Comprobar

- <https://finochioadrian.github.io/> → el perfil
- <https://finochioadrian.github.io/aplicaciones.html> → las ocho aplicaciones
- <https://finochioadrian.github.io/cv/CV-Adrian-Finochio.pdf> → el CV

## Para actualizar más adelante

```bash
git add .
git commit -m "describí acá qué cambiaste"
git push
```

## Qué hacer con el portafolio viejo

`finochioadrian.github.io/MiPortafolio` sigue online con la versión de hace tres años. Una vez
que este sitio esté funcionando, conviene decidir: reemplazar el contenido de ese repositorio
por una redirección a la raíz, o archivarlo. Mientras siga como está, es lo primero que
encuentra quien te busca por nombre.
