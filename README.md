# SETUP INFORMÁTICA — Landing Page

Loja de hardware: PCs gamer, computadores, placas de vídeo, placas-mãe,
processadores, memórias e SSDs. Página minimalista — zero JavaScript, zero
CDN, zero fontes externas. Só HTML + CSS + imagens locais.

## Estrutura

```
site/
├── index.html   ← página gerada (não editar à mão)
├── style.css    ← CSS próprio, paleta da loja (#293f4e, #1598c9, #13b918, #ffb648)
├── assets/      ← logo e fotos dos produtos (redimensionadas: máx. 600px / q.80)
├── produto/     ← uma página de descrição por produto, gerada
└── README.md
```

## Como atualizar (preços, produtos, textos)

A página é **gerada** pelo script `../build.py`, que lê os JSON do catálogo
(hardware e componentes e PCs Gamer, ambos com prazo de transportadora) e o arquivo
de descrições (`url` → descrição + características), e reescreve `index.html`,
`produto/*.html`, `sitemap.xml` e `robots.txt`.

1. Edite os JSON (ou `../build.py` para textos/FAQ).
2. Rode: `python ../build.py`
3. Commit e push — o GitHub Pages atualiza sozinho.

> Os preços de revenda saem de `../politica_precos.py`, por faixa de custo.
> O número publicado de cada produto fica no campo `n`: é ele que mantém a
> mesma URL quando itens entram ou saem do catálogo.

## WhatsApp

Todos os botões de compra apontam para `wa.me/556196052716` com mensagem
pré-preenchida com o nome do produto.
