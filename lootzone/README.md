# LootZone — Site gamer (CSS + HTML)

Recriação em **HTML + CSS** do design da loja LootZone (tema dark gamer, verde neon,
sistema de raridades Comum/Raro/Épico/Lendário). Tudo vive num único arquivo
autocontido: **`index.html`** — só CSS puro, sem framework, responsivo.

## O que tem
- Top bar (frete grátis / envio rápido / atendimento / rastrear / conta)
- Header com logo, busca e ações (favoritos / carrinho com badge)
- Menu de navegação fixo (sticky)
- Hero "EQUIPAMENTOS DIGNOS DE UMA LENDA"
- Faixa de confiança (produtos originais, pagamento seguro, envio, suporte)
- Abas de raridade (Comum · Raro · Épico · Lendário)
- **Destaques da Loja** — 6 cards de produto (rating, preço, botão)
- **Gadgets Modernos** — 4 gadgets + card "Missão"
- **Ofertas da Taverna** — contador + Loot da Semana + ofertas com % OFF
- Faixa de benefícios + Footer completo (colunas, pagamentos, redes sociais)

## Como subir no Wix

O Wix não deixa colar um site inteiro "por cima" do editor, mas você tem 2 caminhos:

### 1) Rápido — widget "Incorporar HTML" (Embed)
1. No editor do Wix: **Adicionar (+) → Incorporar código → Incorporar HTML / iFrame**.
2. Clique em **"Inserir código"** e cole **todo o conteúdo de `index.html`**.
3. Estique o widget para ocupar a largura/altura da página.
> Obs.: o Embed roda dentro de um iframe, então funciona melhor ocupando uma
> seção grande ou a página inteira. As imagens dos produtos aqui são placeholders
> (emoji + gradiente) — troque pelos seus produtos reais editando o HTML.

### 2) Fiel ao design — reconstruir com Wix nativo
Use este arquivo como **referência visual**. As variáveis de cor estão no topo do
`<style>` (`:root`), então dá pra copiar a paleta direto para o tema do Wix:
- Fundo: `#05080c` · Painéis: `#0d131b`
- Verde marca: `#3fe07a` · Ouro: `#e7b64c`
- Raridades: Comum `#9aa6b4` · Raro `#3d8bff` · Épico `#b268ff` · Lendário `#e7b64c`
- Fontes: **Rajdhani** (títulos) + **Inter** (texto)

## Personalizar
- **Cores:** edite o bloco `:root` no topo do `<style>`.
- **Produtos:** cada `<article class="card">` é um produto — troque nome, preço,
  raridade (`epico`/`raro`/`comum`/`lendario`) e o emoji do `.thumb`.
- **Imagens reais:** substitua `<span class="emo">🖱️</span>` por
  `<img src="URL-da-imagem">` dentro de `.thumb`.
