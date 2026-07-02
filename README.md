# O Chapéu de Merlim — Leitor Imersivo

Site de leitura imersiva (rolagem contínua) para *O Chapéu de Merlim — Livro Um das Crônicas de Lovecraft*.

Tudo vive em um único arquivo: **`index.html`**. É só abrir no navegador ou hospedar em qualquer lugar (GitHub Pages, Netlify, etc.). Não precisa de login nem servidor. Feito para virar um app mobile depois.

## Funcionalidades

- **Rolagem contínua** — o leitor avança como num pergaminho, sem trocar de página, pelos capítulos em sequência.
- **Fundos que mudam por cena** — atmosferas em dark fantasy que trocam suavemente conforme a cena (uma por cena).
- **Música por capítulo (YouTube)** — botão ♪ no canto; toca só o áudio, dá para pausar e trocar. Ao entrar em outro capítulo, a trilha acompanha automaticamente (se estiver tocando).
- **Aba "Arquivo" sempre disponível** — botão 📜 no canto para abrir os documentos e o mapa mental a qualquer momento durante a leitura.
- **Trava progressiva** — todo o conteúdo existe no arquivo, mas cada capítulo só desbloqueia seus documentos e mistérios quando o leitor marca aquele capítulo como concluído. Quem parou no Cap. 3 não vê nada do Cap. 9.
- **Documentos por categoria** — Personagens · Locais · Itens & Artefatos · Mistérios, com filtros.
- **Mapa mental interativo com perguntas respondíveis** — cada mistério é um ponto no mapa. Ao tocar, o leitor marca o que descobriu:
  - **💡 Tenho uma ideia** → o app indica um capítulo/trecho para reler (campo `rehint`).
  - **✓ Já sei a resposta** → parabeniza o leitor.
  - **🌫 Não faço ideia** → também indica trechos para reler.
  Perguntas respondidas ganham um anel colorido no mapa.
- Sem login: o progresso e as respostas valem para a sessão de leitura atual.

## Como editar (bloco `CONFIG DO AUTOR`, no topo do `<script>`)

- **Música de cada capítulo**: preencha o campo `music` do capítulo em `BOOK` (link do YouTube).
- **Imagens de fundo (arte pintada)**: em `SCENE_IMAGES`, cole a URL da sua arte ao lado do id da cena
  (ex.: `"c1-chegada"`, `"c2-ruas"`...). Enquanto vazio, usa a atmosfera em CSS.
- **Dicas de releitura das perguntas**: campo `rehint` em cada nó do mapa mental — troque o texto
  placeholder pelo capítulo/trecho real que o leitor deve reler.

O array `BOOK` guarda os capítulos; cada capítulo tem `scenes` (texto), `docs` (notas, cada uma com
`category:`) e `mindmap` (nós e ligações). Basta seguir o mesmo formato para adicionar os próximos capítulos.

## Conteúdo atual

- **Capítulo 1 — O Chapéu de Merlim** (completo)
- **Capítulo 2 — As Ruas de Lovecraft** (até onde o texto vai, termina em "continua...")

## Próximos passos

- Adicionar os próximos capítulos conforme o livro avança.
- Trocar as atmosferas em CSS pelas artes pintadas definitivas e definir as músicas.
- Preencher os campos `rehint` com os trechos de releitura de cada pergunta.
- Empacotar como app mobile (ex.: um wrapper como Capacitor/PWA) quando o conteúdo estiver fechado.
- Versão futura: contas de usuário para salvar progresso entre dispositivos.
