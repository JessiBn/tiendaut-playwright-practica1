# Entrega de Práctica 1 TiendaUT

## Archivos
- `tests/errores-intencionales.spec.ts`: laboratorio E1-E8 que falla a propósito; ejecutar solo para documentar.
- `tests/nuevas-pruebas.spec.ts`: tres pruebas nuevas requeridas.
- `public/catalogo.html` y `public/logo.svg`: sitio corregido.
- `.github/workflows/playwright.yml`: pipeline original, con exclusión del laboratorio y reporte como artefacto.

## Verificación en tu computadora
```powershell
npm ci
npx playwright install
npm run lint
npm run test:chromium -- --update-snapshots=missing
npx playwright test --grep-invert @laboratorio --update-snapshots=missing --repeat-each=5
```

Revisa resultados y guarda capturas; NO se ha comprobado desde esta sesión que el navegador y GitHub Actions funcionen en tu computadora. La primera ejecución de la prueba visual puede generar una referencia propia de tu sistema.

## GitHub
1. Crea un repositorio vacío nuevo en GitHub.
2. En la carpeta raíz del proyecto: `git init`, `git add .`, `git commit -m "Practica 1 TiendaUT"`, `git branch -M main`.
3. Ejecuta `git remote add origin URL_DEL_REPOSITORIO` y `git push -u origin main`.
4. Abre GitHub > Actions > Playwright Tests y espera el check verde.
5. Abre el run > Artifacts > `playwright-report`. Adjunta esa captura y enlace.

## Documentación
Completa la bitácora DOCX facilitada en el chat con nombres y enlaces. Adjunta evidencia de ejecución y trazas. No presentar las correcciones como verificadas hasta correr la suite.
