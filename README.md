# Instituto São João Bosco — Site

Site institucional do Instituto São João Bosco (Brasília/DF).

## Estrutura de Pastas

```
site/
├── index.html                  # Página principal
├── projetos.html               # Página de projetos (grid de cards)
├── README.md                   # Este arquivo
│
├── assets/
│   ├── css/
│   │   └── style.css           # Estilos globais do site
│   ├── js/
│   │   └── main.js             # Scripts: menu, animações, modal, admin
│   └── images/
│       ├── logo/
│       │   ├── logo-horizontal.png
│       │   └── logo-vertical.png
│       ├── hero/
│       │   └── hero-principal.webp
│       └── background/
│           ├── missao-bg.webp
│           ├── grafismo.webp
│           └── Frame-*.webp
│
├── projetos/
│   ├── data/
│   │   └── index.json          # Metadados de todos os projetos (lido pelo JS)
│   ├── pages/                  # HTML de cada projeto (carregado no modal)
│   │   ├── tapetes.html
│   │   ├── corte-costura.html
│   │   ├── reforco-escolar.html
│   │   ├── tampinhas-lacres.html
│   │   ├── workshop-compota.html
│   │   └── workshop-bolachas.html
│   └── thumbnails/             # Imagens de capa dos cards
│       ├── tapetes.webp
│       └── ...
│
└── admin/
    └── index.html              # Painel administrativo (senha: isjb2025)
```

## Como adicionar um novo projeto

1. Crie o arquivo HTML do projeto em `projetos/pages/<slug>.html`
2. Coloque a imagem de capa em `projetos/thumbnails/<slug>.webp`
3. Adicione uma entrada no arquivo `projetos/data/index.json`:

```json
{
  "slug": "nome-do-projeto",
  "titulo": "Nome do Projeto",
  "resumo": "Breve descrição exibida no card.",
  "status": "ativo",
  "statusLabel": "Em andamento",
  "local": "Brasília / DF",
  "capa": "projetos/thumbnails/nome-do-projeto.webp"
}
```

> **Status disponíveis:** `ativo` · `breve` · `realizado`

Também é possível usar o **Painel Admin** (`admin/`) para gerar o HTML automaticamente.

## Tecnologias

- HTML5 + CSS3 puro (sem frameworks)
- JavaScript vanilla (sem dependências)
- Fontes: Google Fonts — Poppins + Roboto
