# O Chapéu de Merlim — Leitor Imersivo

Site de leitura imersiva (rolagem contínua) para *O Chapéu de Merlim — Livro Um das Crônicas de Lovecraft*.

Tudo vive em um único arquivo: **`index.html`**. É só abrir no navegador ou hospedar em qualquer lugar (GitHub Pages, Netlify, etc.). Não precisa de login nem servidor.

## O que já está pronto (Capítulo 1)

- **Rolagem contínua** — o leitor avança como num pergaminho, sem trocar de página.
- **Fundos que mudam por cena** — atmosferas em dark fantasy que trocam suavemente conforme a cena.
- **Música por capítulo (YouTube)** — botão de ambientação no canto; toca só o áudio, dá para pausar e trocar.
- **Desbloqueio ao fim do capítulo** — botão de concluir abre um painel com duas abas:
  - **Documentos** — notas de referência, isoladas por categoria: *Personagens · Locais · Itens & Artefatos · Mistérios*.
  - **Mapa Mental** — mapa visual dos mistérios em aberto; toque num ponto para ler a anotação.
- Sem login: o desbloqueio vale para a sessão de leitura atual.

## Como editar (sem mexer no resto)

Abra `index.html` e procure o bloco **`CONFIG DO AUTOR`**, no início do `<script>`:

- **Música**: cole o link do YouTube em `CHAPTER_MUSIC`.
- **Imagens de fundo (arte pintada)**: em `SCENE_IMAGES`, cole a URL da sua arte ao lado do id da cena
  (`arrival`, `tavern`, `brawl`, `bard`, `after-song`, `morning`, `battle`, `aftermath`).
  Enquanto estiver vazio, usa a atmosfera em CSS.

Logo abaixo, os blocos `SCENES`, `DOCS` e `MM_NODES` guardam, respectivamente, o texto do capítulo,
as notas de documentação (cada uma com `category:`) e os nós do mapa mental. Basta seguir o mesmo formato para
adicionar conteúdo.

## Próximos passos possíveis

- Adicionar o Capítulo 2 (o texto já existe, termina em "continua...").
- Trocar as atmosferas em CSS pelas artes pintadas definitivas.
- Numa versão futura: contas de usuário para salvar o progresso entre dispositivos.
