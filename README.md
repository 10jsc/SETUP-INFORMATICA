# SETUP INFORMÁTICA — Landing Page

Landing page minimalista de revenda de hardware (clone limpo da Cel Infor):
zero JavaScript, zero CDN, zero fontes externas. Só HTML + CSS + imagens locais.

## Estrutura

```
site/
├── index.html   ← página gerada (não editar à mão)
├── style.css    ← CSS próprio, paleta da Cel Infor (#293f4e, #1598c9, #13b918, #ffb648)
├── assets/      ← logo e 41 fotos de produto (redimensionadas: máx. 600px / q.80)
├── produto/     ← 41 páginas de descrição geradas (uma por produto)
└── README.md
```

## Como atualizar (preços, produtos, textos)

A página é **gerada** pelo script `../build.py`, que lê `../produtos.json`
(`nome`, `orig`, `revenda`, `img`, `url`) e `../descricoes.json`
(`url` -> descrição + características) e reescreve `index.html` + `produto/*.html`.

1. Edite `../produtos.json` (ou `../build.py` para textos/FAQ).
2. Rode: `python ../build.py`
3. Commit e push — o GitHub Pages atualiza sozinho.

> Os preços de revenda no JSON já vêm com o markup aplicado
> (1-9 → +2 | 10-99 → +20 | 100-999 → +200 | 1000-9999 → +300 | 10000+ → +500).

## Publicação (GitHub Pages)

1. Crie um repositório vazio no GitHub (ex.: `setup-informatica`), sem README.
2. Aqui no projeto:

```bash
git remote add origin https://github.com/SEU_USUARIO/setup-informatica.git
git branch -M main
git push -u origin main
```

3. No GitHub: **Settings → Pages → Source: Deploy from a branch → main → / (root)**.
4. A página fica em `https://SEU_USUARIO.github.io/setup-informatica/`.

## WhatsApp

Todos os botões de compra apontam para `wa.me/5561996052716` (número da loja,
chip novo 2026-09-03) com mensagem pré-preenchida com o nome do produto.
