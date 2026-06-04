# NFT Preview Card Component

## Identità

Progetto statico **Frontend Mentor** — HTML5 + CSS3 (Flexbox) + Vanilla JS.  
Nessun package manager, nessuna dipendenza, nessun build step. Apri `index.html` nel browser.

**⚠ Vietato**: TypeScript, JSX, React, Tailwind. Questo è solo HTML+CSS+JS vanilla.

## File guida

| File             | Cosa contiene                                                |
| ---------------- | ------------------------------------------------------------ |
| `style-guide.md` | Colori HSL, font, dimensioni layout del challenge originale. |

## Debito tecnico

| #  | Criticità                               | Dove                                                 | Fix proposto                                                              |
| -- | --------------------------------------- | ---------------------------------------------------- | ------------------------------------------------------------------------- |
| #2 | Overlay hover via JS con event listener | `index.html` script + classi `.img-active`/`.active` | Sostituire con CSS `:hover` + `opacity`/`transition`                      |
| #3 | Centratura icona: `margin: 41%`         | `style.css` `.icon-view`                             | Flexbox su `.img-active` (`justify-content: center; align-items: center`) |
| #4 | Dimensioni card fisse (250×430px)       | `style.css` `.card-bg`                               | `max-width` + media query (375px/1440px style-guide)                      |
| #5 | `console.log` di debug                  | `index.html` script                                  | Rimuovere                                                                 |
| #6 | Variabili poco descrittive              | `element`, `imgActive` nel JS                        | Rinominare                                                                |
| #7 | Colori duplicati in chiaro              | `style.css`                                          | Variabili CSS `:root`                                                     |
| #8 | `<h3>` per titolo principale card       | `index.html`                                         | Valutare `<h1>` (pagina standalone)                                       |

## Git workflow

- **Lingua commit**: italiano, prefix **Conventional Commits** (`feat:`, `fix:`, `docs:`, `chore:`, `refactor:`, `test:`)
- **Divieto**: commit su `main`. Creare branch da `main`: `git checkout -b <tipo>/<nome>`
- **Atomicità**: `git add <file_specifico>`, mai `git add .` o `git commit -am`
- **PR**: template in `.github/pull_request_template.md`

## CI/CD

- `release-please` su push a `main` — genera release e CHANGELOG automaticamente
- `opencode` attivabile da commenti PR/issue con `/oc` o `/opencode`

## Comandi

```sh
# Aprire in browser (Windows)
start index.html

# Formattazione (se Prettier installato globalmente)
prettier --write .
```
