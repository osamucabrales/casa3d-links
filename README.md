# Casa 3D Links

Página de links da bio da **Casa 3D — Espaço Maker** (Governador Valadares, MG).

- No ar: https://links.casa3d.online (também em https://casa3d-links.vercel.app)
- Hospedagem: Vercel, time **SRC NETWORK**, projeto `casa3d-links`. Cada commit na `main` publica sozinho.
- DNS: Hostinger, registro `CNAME links` apontando para a Vercel.

## Mascote

O mascote oficial da Casa 3D é o **BERIGUDIGO**, um ornitorrinco laranja. Use sempre esse nome em conteúdo, site, vídeos, jogos e briefs. Não use "Patocrinco" nem "Ornito".

É o Berigudigo que aparece no vídeo do pé da página (`gemini_generated_video_70d15027.mp4`).

## Arquivos

| Arquivo | O que é |
|---|---|
| `index.html` | A página inteira: HTML, CSS e JS num arquivo só, sem build. |
| `gemini_generated_video_70d15027.mp4` | Vídeo do Berigudigo, sem som, em loop, acima do rodapé. |

## Identidade visual

Segue a ID oficial em https://casa3d.online/identidade-visual.

- **Cores:** Preto Casa `#111211`, Branco `#F9F9F6`, Laranja Casa `#FF6B19`, Azul `#147DF5`, Verde `#B8F457`.
- **Tons de fundo:** Laranja fundo `#CF4A08` e Azul fundo `#0F6FE0`, usados só como fundo de botão com texto branco, para passar no contraste WCAG AA.
- **Tipografia:** Chakra Petch é a voz da marca (nome, rótulos, assinatura). Inter é para leitura e ação (botões, textos, contatos).
- **Temas:** a página tem tema claro e escuro, que segue o sistema do visitante.

## Botões e para onde vão

O roteamento fica no `<script>` do fim do `index.html`, nas constantes `ATENDIMENTO` e `SETORES`. Essa é a única fonte da verdade: para mudar quem atende o quê, edite só ali.

| Botão | Destino |
|---|---|
| Black Friday (destaque, preto e laranja) | WhatsApp (33) 3082-3168, com a mensagem "Vim das redes sociais e quero comprar na Casa 3D" |
| Filamentos & Resinas, Impressoras 3D, Outros | WhatsApp (33) 8465-3046 |
| Encomendas 3D, Treinamentos & Suporte | WhatsApp (33) 8412-1784 |
| Visitas Mediadas (contorno, institucional) | https://casa3d.online/visitas-mediadas |
| Rodapé | WhatsApp (33) 3082-3168 e contatocasa3d@casa3d.online |

A mensagem de cada setor começa com "Olá Casa3D! Vim do Instagram e…". Para medir outras origens, use o parâmetro `?origem=`:

- `links.casa3d.online/?origem=anuncio` → "Vim do anúncio"
- Outras opções: `google`, `site`, `tiktok`
- Sem parâmetro → Instagram

O botão de destaque (`.btn.evento`) é para campanhas temporárias, como Halloween ou Black Friday. Quando a campanha acabar, troque o rótulo e o link ou remova o bloco.

## Análises (Vercel Web Analytics, plano grátis)

Para ver as análises:

1. Abra vercel.com, entre no projeto **casa3d-links** e clique em **Analytics**.
2. No topo estão os visitantes e as visualizações.
3. **Pages** mostra os cliques. Cada clique é registrado como uma página virtual `/clique/<botão>`, por exemplo `/clique/black-friday` ou `/clique/encomendas-3d`.
4. **Referrers** e **UTM Parameters** mostram de onde as pessoas vieram.

Limites do plano grátis: 30 dias de histórico e 50 mil eventos por mês. Os cliques também entram na soma de "Page Views". Para saber as visitas reais, olhe só a página `/`.

## Acessibilidade e desempenho

- Áreas de toque de pelo menos 44 px e foco visível no teclado.
- O vídeo fica parado para quem ativou "reduzir movimento" no sistema.
- O vídeo atual tem 4,2 MB e ainda traz uma faixa de áudio, que nunca toca. Uma versão de 0,55 MB, sem áudio, está pronta para substituir.
