# Svelte + prettier + Vim

-   this repository is a minimal template to get started with svelte
-   configured to make prettier for svelte work exactly like in vscode
-   this repository is cloned from [sveltejs/template](https://github.com/sveltejs/template).

# Installation

```
clone https://github.com/revoltez/vimSvelte my-project
cd my-project
npm i
npm run dev
```
if you are using vite or svelteKit, simply copy `prettier.config.cjs`, and add ` prettier prettier-plugin-svelte` with your favorite package manager 

ex: `npm i -D prettier prettier-plugin-svelte`

# vim/neovim configuration

-   you need to have the following plugins added to your vimrc or init.vim in case you are using neovim

```
Plug 'neoclide/coc.nvim', {'branch': 'release'}
Plug 'prettier/vim-prettier'
// syntax highlighting for lots of languages
Plug 'sheerun/vim-polyglot'
Plug 'codechips/coc-svelte', {'do': 'npm install'}
Plug 'evanleck/vim-svelte'

let g:coc_global_extensions = ['coc-json', 'coc-eslint', 'coc-tsserver']
```

-   configure prettier :

```
autocmd BufWritePre *.svelte,*.js,*.jsx,*.html,*.mjs,*.ts,*.tsx,*.json,*.graphql,*.md,*.yaml, PrettierAsync

```
