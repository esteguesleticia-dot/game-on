# 🍦 Desafio Contábil Flor de Baunilha

Jogo educativo em dupla para revisar conceitos de Contabilidade (Plano de Contas, Débito e Crédito, Lançamentos Contábeis, Razonetes, Demonstrações Contábeis e Conceitos Fundamentais), baseado no e-book *"Você sabe como a Contabilidade organiza as empresas?"* (PUCPR / Sistematização de Informações Contábeis).

Feito em **HTML + CSS + JavaScript puro**, tudo em **um único arquivo `index.html`** (sem dependências externas, sem pastas, sem caminhos relativos) — para evitar qualquer problema de CSS/JS não carregando em serviços de deploy (GitHub Pages, Vercel, Netlify, etc.).

## ▶️ Como jogar

1. Abra `index.html` no navegador (ou acesse o link publicado).
2. Clique em **"Começar Desafio"**.
3. Cada jogador escolhe um personagem (avatar) e digita seu nome.
4. Os jogadores se revezam respondendo 6 perguntas por rodada — a cada nova partida as perguntas mudam e a ordem de quem começa a responder também se alterna.
5. Cada resposta correta vale **10 pontos**.
6. Ao final, o jogador com mais pontos é declarado vencedor e pode salvar sua pontuação no **Ranking da Turma**.

## 📁 Estrutura de arquivos

```
desafio-contabil/
├── index.html   # tudo em um arquivo: HTML + CSS + JS (banco de perguntas incluso)
└── README.md
```

Como é um único arquivo HTML autossuficiente, basta subir **esse arquivo** para qualquer serviço de hospedagem estática — não há risco de link quebrado de CSS/JS.

## 🚀 Publicando

### GitHub Pages
1. Crie um repositório no GitHub.
2. Suba o arquivo `index.html` (e o `README.md`, opcional) para a raiz do repositório.
3. Vá em **Settings → Pages**.
4. Em **Source**, selecione a branch `main` e a pasta `/ (root)`.
5. Em alguns minutos o jogo estará em `https://SEU_USUARIO.github.io/NOME_DO_REPOSITORIO/`.

### Vercel
1. Crie um novo projeto e importe o repositório (ou arraste a pasta com o `index.html`).
2. **Não defina build command nem output directory** — é um site estático puro. Se a Vercel pedir um *Framework Preset*, selecione **"Other"**.
3. Deploy. Pronto.

## ✏️ Como editar as perguntas

Abra `index.html` e procure por `const QUESTION_BANK = [` (dentro da tag `<script>`). Cada pergunta segue este formato:

```js
{
  topic: "Plano de Contas",
  question: "Texto da pergunta?",
  options: ["Opção A", "Opção B", "Opção C", "Opção D"],
  correctIndex: 0 // posição da resposta correta no array "options" (0 = primeira)
}
```

Você pode adicionar quantas perguntas quiser — o jogo sorteia 6 por rodada automaticamente e evita repetir as últimas usadas.

## 🏆 Ranking da Turma

O ranking é salvo localmente no navegador (`localStorage`), permitindo comparar resultados de diferentes partidas jogadas no mesmo computador/navegador. É possível limpar o ranking a qualquer momento na tela "Ranking da Turma".

> **Observação:** como o armazenamento é local (por navegador), para um ranking compartilhado entre vários computadores da turma seria necessário um backend (ex: Google Sheets via API, Firebase, etc.) — não incluído nesta versão simples.

## 🎨 Paleta de cores

Inspirada no design do e-book da Flor de Baunilha:
- Vinho escuro `#8E2E52`
- Rosa médio `#B05C7E`
- Rosa claro `#E7B9C9`
- Dourado baunilha `#C9A36A`
- Creme `#FBF1E6`

## 🧠 Objetivo pedagógico

Promover a revisão dos conteúdos de Sistematização de Informações Contábeis, estimular o raciocínio lógico, a tomada de decisão e a aprendizagem colaborativa por meio da gamificação, com base no estudo de caso da empresa fictícia **Flor de Baunilha**.
