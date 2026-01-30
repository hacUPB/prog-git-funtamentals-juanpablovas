# ¿Qué es un archivo .gitignore?

Un archivo **.gitignore** es un archivo de texto que le dice a Git qué archivos o carpetas NO debe rastrear ni subir al repositorio.

Es básicamente la lista de “cosas que Git debe ignorar”.

## ¿Para qué sirve?

Sirve para evitar subir al repositorio archivos que:

- 🔒 Contienen información sensible (contraseñas, tokens, .env)
- 🧱 Se generan automáticamente (logs, builds, binarios)
- 💻 Dependen de tu entorno local (configuraciones del IDE, cachés)
- 🗑️ No aportan nada al código fuente

Ejemplos típicos:

- node_modules/  
- .env  
- .log  
- .idea/  
- dist/  

## ¿Qué hace exactamente?
Cuando Git ve un archivo que coincide con una regla del .gitignore:

❌ No lo agrega con git add  
❌ No lo sube al repositorio  
❌ No muestra cambios de ese archivo en git status  
⚠️ Ojo importante:  
Si un archivo ya fue agregado al repositorio antes, el .gitignore NO lo deja de rastrear automáticamente.