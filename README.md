# Atividade 4 - Cabeçalho compartilhado

Projeto da disciplina Desenvolvimento Web I - DSM, desenvolvido com Node.js e Express.

## Estrutura principal

```text
app/
├── server/
│   ├── main.js
│   └── partials/
│       └── header.html
├── public/
│   ├── assets/
│   │   ├── css/
│   │   └── images/
│   ├── pages/
│   │   ├── 1dsm.html
│   │   ├── 2dsm.html
│   │   ├── 3dsm.html
│   │   ├── 4dsm.html
│   │   ├── 5dsm.html
│   │   └── 6dsm.html
│   └── index.html
├── package.json
└── README.md
```

## Como executar

1. Instale o Node.js (versão compatível com `import.meta.dirname`).
2. Abra o terminal na pasta do projeto.
3. Execute `npm install`.
4. Execute `npm start`.
5. Acesse `http://localhost:3000`.

## O que foi implementado

- Cabeçalho único em `server/partials/header.html`, contendo logos DSM, FATEC e CPS, título do curso e menu dos seis semestres.
- Marcador `<!-- shared-header -->` nas sete páginas HTML.
- Motor de visualização HTML configurado com `app.engine("html", ...)`.
- Leitura dos arquivos com `readFile` e codificação UTF-8.
- Inclusão do cabeçalho com `replace()`.
- Rotas configuradas com `res.render()`.
- Arquivos estáticos preservados em `/assets`.
- Resposta HTTP 404 preservada para rotas inexistentes.

## Rotas

- `/` - Página inicial
- `/1dsm` até `/6dsm` - Páginas dos semestres
