# Casa 3D Links

Página de links da bio da **Casa 3D — Espaço Maker** (Governador Valadares, MG).

- No ar: https://links.casa3d.online (também em https://casa3d-links.vercel.app)
- Hospedagem: Vercel, time **SRC NETWORK**, projeto `casa3d-links`. Cada commit na `main` publica sozinho.
- DNS: Hostinger, registro `CNAME links` apontando para a Vercel.

## Mascote

O mascote oficial da Casa 3D é o **BERIGUDIGO**, um ornitorrinco laranja. Use sempre esse nome em conteúdo, site, vídeos, jogos e briefs. Não use "Patocrinco" nem "Ornito".

É o Berigudigo que aparece no vídeo de largura total antes do mapa (`berigudigo.mp4`) e no ícone do botão Visitas Mediadas.

## Arquivos

| Arquivo | O que é |
|---|---|
| `index.html` | A página inteira: HTML, CSS e JS num arquivo só, sem build. |
| `berigudigo.mp4` | Vídeo do Berigudigo (0,55 MB, sem faixa de áudio), em loop, na largura toda. |
| `icons/*.webp` | Ícones 3D dos botões, 132 px (3× o tamanho exibido de 44 px), 8–13 KB cada. |

Ícones por botão: Inscrição Feira Maker → `feira-maker.webp`, Filamentos & Resinas → `filamentos.webp`, Encomendas 3D → `encomendas.webp`, Impressoras 3D → `impressoras.webp`, Treinamentos & Suporte → `treinamentos.webp`, Visitas Mediadas → `berigudigo.webp`, Outros → `outros.webp`. O Black Friday usa um ícone desenhado em código (etiqueta).

## Identidade visual

Segue a ID oficial em https://casa3d.online/identidade-visual.

- **Cores:** Preto Casa `#111211`, Branco `#F9F9F6`, Laranja Casa `#FF6B19`, Azul `#147DF5`, Verde `#B8F457`.
- **Tons de fundo:** Laranja fundo `#CF4A08` e Azul fundo `#0F6FE0`, usados só como fundo de botão com texto branco, para passar no contraste WCAG AA.
- **Tipografia:** Chakra Petch é a voz da marca (nome, rótulos, assinatura). Inter é para leitura e ação (botões, textos, contatos).
- **Fundo:** Preto Casa sólido; a página tem um visual único escuro (não muda com o tema do sistema).

## Botões e para onde vão

O roteamento fica no `<script>` do fim do `index.html`, nas constantes `ATENDIMENTO` e `SETORES`. Essa é a única fonte da verdade: para mudar quem atende o quê, edite só ali.

| Botão | Destino |
|---|---|
| Black Friday (destaque, borda laranja) | WhatsApp (33) 3082-3168, com a mensagem "Vim das redes sociais e quero comprar na Casa 3D" |
| Inscrição Feira Maker (destaque, borda verde) | https://casa3d.online/eventos/feira-maker-natal-solidario-2026#inscricao |
| Filamentos & Resinas, Impressoras 3D, Outros | WhatsApp (33) 8465-3046 |
| Encomendas 3D | WhatsApp oficial (33) 3082-3168, com pedido de orçamento |
| Treinamentos & Suporte | WhatsApp (33) 8412-1784 |
| Visitas Mediadas (contorno, institucional) | https://casa3d.online/visitas-mediadas |
| Rodapé | WhatsApp (33) 3082-3168, contatocasa3d@casa3d.online e Política de uso de dados (casa3d.online/privacidade) |
| Links do topo | Site, Loja Maker, Blog, Podcast |
| Seção Como chegar | Mapa do Google (Rua Dom Pedro II, 348) e botão Abrir no Google Maps |

A mensagem de cada setor começa com "Olá Casa3D! Vim do Instagram e…". Para medir outras origens, use o parâmetro `?origem=`:

- `links.casa3d.online/?origem=anuncio` → "Vim do anúncio"
- Outras opções: `google`, `site`, `tiktok`
- Sem parâmetro → Instagram

Os botões de destaque (`.btn.evento`) são para campanhas temporárias, como Black Friday e a inscrição da Feira Maker. Quando a campanha acabar, troque o rótulo e o link ou remova o bloco.

## Análises (Vercel Web Analytics, plano grátis)

O mesmo GA4 do site principal (`G-DE5D5Y1RW3`) e a Vercel Web Analytics medem o subdomínio somente após o visitante aceitar estatísticas no aviso de privacidade. A escolha é local ao subdomínio e pode ser alterada no rodapé. O Search Console da propriedade de domínio `casa3d.online` também abrange `links.casa3d.online`; o sitemap próprio é `/sitemap.xml`.

Para ver as análises:

1. Abra vercel.com, entre no projeto **casa3d-links** e clique em **Analytics**.
2. No topo estão os visitantes e as visualizações.
3. **Pages** mostra os cliques. Cada clique é registrado como uma página virtual `/clique/<botão>`, por exemplo `/clique/black-friday` ou `/clique/encomendas-3d`.
4. **Referrers** e **UTM Parameters** mostram de onde as pessoas vieram.

Use estes endereços **nos canais de divulgação** para atribuir a entrada corretamente no GA4:

| Canal | URL pronta |
|---|---|
| Bio do Instagram | `https://links.casa3d.online/?utm_source=instagram&utm_medium=social&utm_campaign=bio` |
| Stories da Feira | `https://links.casa3d.online/?utm_source=instagram&utm_medium=social&utm_campaign=feira-maker&utm_content=stories` |
| WhatsApp | `https://links.casa3d.online/?utm_source=whatsapp&utm_medium=social&utm_campaign=feira-maker` |
| QR na loja | `https://links.casa3d.online/?utm_source=loja&utm_medium=qrcode&utm_campaign=links` |

`utm_source` identifica o canal, `utm_medium` o formato, `utm_campaign` a campanha e `utm_content` diferencia peças. Os links **dentro** do site de links para `casa3d.online` não recebem nova UTM: os dois usam a mesma propriedade GA4 e uma campanha interna poderia alterar a atribuição da origem. O botão escolhido é medido pelo evento `select_content` após consentimento. Links para WhatsApp abrem o aplicativo; o evento mede o clique, não confirma mensagem enviada.

Limites do plano grátis: 30 dias de histórico e 50 mil eventos por mês. Os cliques também entram na soma de "Page Views". Para saber as visitas reais, olhe só a página `/`.

No GA4, o Instagram aparece em select_content com item_id=instagram para o botao atual e link_domain=instagram.com para todos os links destinados ao Instagram.

## Acessibilidade e desempenho

- Áreas de toque de pelo menos 44 px e foco visível no teclado.
- O vídeo fica parado para quem ativou "reduzir movimento" no sistema.
- Vídeo de 0,55 MB sem faixa de áudio; ícones em WebP de poucos KB; o mapa só carrega quando chega perto da tela (`loading="lazy"`).
