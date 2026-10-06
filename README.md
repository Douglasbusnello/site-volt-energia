# Watt In Energia — site institucional

Site de uma página (single-file, sem build) apresentando a Watt In Energia: instalação, operação e manutenção de carregadores de carro elétrico em Santa Catarina, com simulador de retorno e três modelos de parceria (investimento próprio, aluguel de equipamento, loja investe/nós operamos).

Todo o HTML, CSS e JavaScript estão em `index.html` — não há dependências de build, framework ou backend. As únicas chamadas externas são as fontes do Google Fonts (Archivo, Instrument Sans, JetBrains Mono).

## Como visualizar localmente

Basta abrir o arquivo no navegador:

```bash
open index.html        # macOS
xdg-open index.html    # Linux
start index.html       # Windows
```

Ou suba um servidor simples (recomendado, evita restrições de `file://` em alguns navegadores):

```bash
python3 -m http.server 8000
# depois acesse http://localhost:8000
```

## Publicar no GitHub Pages

1. Crie o repositório no GitHub e suba este conteúdo (veja o passo a passo abaixo).
2. No GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**.
3. Escolha a branch `main` e a pasta `/ (root)`.
4. Salve. Em alguns minutos o site fica disponível em `https://<seu-usuario>.github.io/<nome-do-repo>/`.
5. Para um domínio próprio, adicione um arquivo `CNAME` na raiz com o domínio (ex.: `wattinenergia.com.br`) e configure o DNS do domínio apontando para o GitHub Pages.

## O que ainda é uma demonstração

- **Formulário de contato**: funciona na tela (valida nome e e-mail), mas não envia para lugar nenhum ainda. Precisa de um backend ou serviço de formulário (Formspree, Netlify Forms, um endpoint próprio) para receber os contatos de verdade.
- **Painel do parceiro** (gráfico de barras na seção de tecnologia): usa dados fictícios, só para ilustrar como o relatório mensal se parece.
- **Simulador de retorno**: os números são calculados no navegador a partir dos valores que o visitante digita; as premissas (tarifa, custo de energia, repasse) são as mesmas do modelo financeiro do projeto, mas devem ser revisadas periodicamente.

## Estrutura

```
.
├── index.html   # site completo (HTML + CSS + JS)
└── README.md
```
