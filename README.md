# Guia de Java (MkDocs)

## Executar en local
```bash
pip install -r requirements.txt
mkdocs serve        # http://127.0.0.1:8000/
```

## Pujar a GitHub i desplegar
```bash
git init
git add .
git commit -m "Primer commit"
git branch -M main
git remote add origin https://github.com/EL_TEU_USUARI/guia-java.git
git push -u origin main

mkdocs gh-deploy    # crea/actualitza la branca gh-pages
```
Després, a GitHub: **Settings → Pages → Branch: gh-pages**.
