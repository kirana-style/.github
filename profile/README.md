<h1 align="center">Kirana</h1>

<p align="center"><b>Write objects. Read classes. Ship CSS.</b><br>Light through every line of your styles.</p>

<p align="center"><a href="https://kirana.style">kirana.style</a> · <a href="https://kirana.style/docs">Docs</a> · <a href="https://kirana.style/blog">Blog</a></p>

CSS-in-JS with a Rust engine of its own. Start with plain style objects and grow into tokens and
themes; Kirana compiles them into one small, atomic stylesheet at native speed, turns mistakes into
compile errors, and shows every element's CSS on its line in your editor.

```tsx
import { css } from "@kirana-style/core"

const styles = {
  card: css({ display: "grid", gap: "1rem", padding: "1rem" }),
}

export const Card = () => <article sx={styles.card} /> // ▦ grid · gap 1rem · p 1rem
```

## The ecosystem

**The compiler.** A Rust engine on [oxc](https://oxc.rs), with a WASI build that writes the same
bytes where no native one runs. It reads typed style objects at build time and writes one layered,
atomic stylesheet: one rule per distinct declaration, shared by every element that uses it.
45 diagnostics catch what used to fail silently, and the `kirana` command builds, checks, traces and
migrates (`init`, `dev`, `build`, `check`, `trace`, `analyze`, `doctor`, `export`, `migrate`, `lsp`).

**Authoring.** `@kirana-style/core`: `css`, `recipe`, `relation`, `select`, `defineTokens`,
`defineTheme`, `keyframes` and more, all compiled away. Styles merge per property instead of
colliding, and a parent styles its children without overriding their own styles. Start with plain
objects; add tokens, themes, recipes and the ready-made scales of `@kirana-style/preset-scales` when
your design system grows.

**Frameworks.** `sx` compiles in React, Preact, Solid, Qwik, Vue, Svelte, Astro, Angular and Ember,
with guides for Next.js, React Router, TanStack Start, Gatsby, Nuxt, SvelteKit and Meteor. Server
templates read the same class map in Laravel, Symfony, Rails, Phoenix and AdonisJS.

**Bundlers.** Vite, Rolldown, webpack, Rspack and Rsbuild, Parcel, Bun and esbuild, plus PostCSS and
Jest.

**Editors.** The language server writes each element's CSS at the end of its line, draws the box
model on hover and says which entry wins and why. VS Code, Cursor, Windsurf and Antigravity share one
extension, with a Style Inspector and Style Fold; Zed, Neovim and Helix get the same server.

**Linters.** 11 rules read from the compiler itself, for Oxlint, ESLint and Biome.

**Coding agents.** Agent skills, `llms.txt`, `llms-full.txt` and a markdown twin of every docs page.

## Where it is published

| Registry | Package |
| --- | --- |
| npm | `@kirana-style/*` (20 packages) and `kirana-style`, the command line |
| RubyGems | `kirana` |
| Hex | `kirana` |
| Packagist | `kirana-style/kirana` (also as `kirana/kirana`) |
| VS Code Marketplace · Open VSX | `kirana-style.kirana` |
| Zed | Kirana |

## Repositories

- [`kirana`](https://github.com/kirana-style/kirana): the compiler, the packages, the editor
  extensions, the helpers for server templates and the documentation site.
- [`kirana-php`](https://github.com/kirana-style/kirana-php): a read-only mirror of the PHP helper,
  for Packagist.

## Status

Kirana is in development and not released yet. The first release will be announced on
[kirana.style](https://kirana.style).

Contact: hello@kirana.style · Security: see the [security policy](https://github.com/kirana-style/.github/blob/main/SECURITY.md)
