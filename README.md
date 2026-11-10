# 🎮 Biblioteca de prompts

Guarda tus prompts en categorías y subcategorías, con icono, copiado en un clic y estilo gamer.
Todo es un solo archivo (`index.html`), sin dependencias.

- Para modificar algo (agregar, editar, eliminar) pide la clave. Por defecto es `1234`; se cambia en `const KEY` dentro de `index.html`.
- Los datos viven en el navegador (localStorage) y, si lo configuras, también se copian solos a `data/prompts.json` de este repositorio.

## 1. Subir el proyecto a GitHub
1. Crea un repositorio nuevo en https://github.com/new (por ejemplo `biblioteca-prompts`).
2. Sube estos archivos: `index.html`, `README.md`, `.nojekyll` y la carpeta `data/`.
   Con la terminal:
   ```
   git init
   git add .
   git commit -m "Biblioteca de prompts"
   git branch -M main
   git remote add origin https://github.com/TU_USUARIO/biblioteca-prompts.git
   git push -u origin main
   ```

## 2. Ponerlo en línea (GitHub Pages)
1. En el repositorio: **Settings → Pages**.
2. En *Build and deployment* elige **Deploy from a branch**, rama `main`, carpeta `/ (root)`, y guarda.
3. En uno o dos minutos tendrás tu página en `https://TU_USUARIO.github.io/biblioteca-prompts/`.

## 3. Copia automática independiente del navegador
1. Crea un token en **GitHub → Settings → Developer settings → Personal access tokens → Fine-grained tokens**.
   - *Repository access*: solo este repositorio.
   - *Permissions → Contents*: **Read and write**.
2. Abre tu página, pulsa **☁️ Respaldo**, escribe la clave, y completa usuario, repositorio, rama (`main`) y token.
3. Desde ahí, cada cambio se sube solo a `data/prompts.json` (el icono muestra ⏳ subiendo, ✅ listo o ⚠️ error).
   Al abrir la página en otro navegador o equipo, con el mismo token, se descargan tus prompts.

Sin token, la página igual muestra en modo lectura lo que haya en `data/prompts.json`.

## Qué tener en cuenta
- **Repositorio público = prompts públicos.** Cualquiera podría leer `data/prompts.json`. GitHub Pages en repositorios privados requiere un plan de pago.
- La clave `1234` es una barrera visual: está en el código y no es seguridad real.
- El token queda guardado en el navegador donde lo escribas. Usa uno limitado a este repositorio y bórralo si dejas de usar ese equipo.
- Si editas desde dos equipos a la vez, gana el cambio más reciente.
- Además, **⬇ Exportar / ⬆ Importar** te deja guardar y restaurar un archivo `.json` a mano.
