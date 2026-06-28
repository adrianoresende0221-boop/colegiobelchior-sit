# Identidade visual

> Como a marca aparece em tudo que o MazyOS gera.
> As skills de conteúdo, carrossel e post leem esse arquivo antes de criar qualquer visual.
> Edite quando a marca evoluir.

---

## Cores

> Confirmado pelo usuário (2026-06-27): a marca usa **vermelho, azul e amarelo** — confirmado também pela fachada real (foto enviada no chat: parede amarela, base/portão azul, faixa vermelha de sinalização) e pelo logo oficial (texto azul-marinho + detalhe vermelho). Hex abaixo são estimativas visuais a partir dessas fotos — ajustar se a escola tiver manual de marca com hex exatos.

- **Fundo principal:** branco — `#FFFFFF`

- **Azul (marca / Fundamental I):** `#1B4F8C` — cor do texto do logo e da base/portão da fachada

- **Vermelho (destaque / Fundamental II):** `#D32F2F` — faixa de sinalização e detalhe do logo

- **Amarelo (Educação Infantil):** `#F2B705` — parede da fachada, tom mais lúdico pra fase infantil

- **Texto principal:** grafite escuro, não preto puro — `#2B2622`

- **Fundo alternativo / cards:** cinza muito claro — `#F7F7F5`

- **Cor proibida:** *(nada definido ainda)*

---

## Tipografia

- **Títulos e destaques:** fonte humanista arredondada (sugestão: Poppins ou Quicksand) — transmite acolhimento, combina com "Caminho Suave"

- **Corpo, subtítulos e botões:** fonte neutra legível (sugestão: Inter ou Nunito Sans)

- **Peso do título:** semibold/bold

---

## Estilo geral

Acolhedor, colorido e family-friendly (como o feed do Instagram: gradientes quentes, ilustrações lúdicas pras postagens infantis), mas com uma camada institucional mais sóbria nas páginas pra pais (estrutura, segurança, matrícula) — sem virar "site de balada infantil".

---

## Elementos-chave

- Bordas: suaves, sem cantos vivos
- Border-radius dos cards: 16-20px
- Botões: arredondados, com o vermelho-vinho de destaque, texto branco
- Sombras: leves, difusas (nada de sombra dura tipo Material Design antigo)

---

## O que NUNCA fazer

- Não usar emoji em excesso fora das redes sociais
- Não usar jargão pedagógico vazio nas peças visuais
- Não poluir o layout — escola pra crianças pequenas pede leveza visual, não excesso de cor em tudo

---

## Logo

- **Arquivo:** logo oficial recebida e em uso real no site, em `colegiobelchior/assets/LOGO.png` (arquivo original) e `colegiobelchior/assets/logo-cabecalho.png` (recorte sem a margem em branco, usado no `<header>` das 5 páginas). O ícone circular (anel vermelho + silhueta pai/filho) também foi recortado pra gerar o favicon (`favicon-32.png`, `apple-touch-icon.png`).
- **Versão pra fundo escuro:** *(se tiver — ex: identidade/logo-branco.png)* — ainda não recebida; necessária se quiser a logo sobre o hero (hoje o hero usa foto de fundo, não a logo)
- **Onde usar:** header do site (já aplicado), favicon (já aplicado), slide final do carrossel (CTA), header de propostas
- **Tamanho sugerido:** 44px de altura no header desktop, 34px no mobile (já implementado em `css/style.css`)

---

## Horário de funcionamento

Dias de semana, 7h às 18h. Fechado sábado e domingo. *(Confirmado pelo usuário em 2026-06-27.)*

---

## Observações adicionais

Paleta atualizada em 2026-06-27 com as cores reais confirmadas pelo usuário (vermelho/azul/amarelo) e fotos reais da fachada. Próximo ajuste fino: hex exatos se houver manual de marca.

## Padrões visuais do site (implementados em 2026-06-28)

- **Hero com foto de fundo:** cada página (Início, Sobre, Infantil, Fund. I, Fund. II) tem uma foto em tela cheia atrás do título, com degradê escuro (mais forte à esquerda, onde fica o texto, e na base, onde ficam os botões) pra garantir leitura branca sobre qualquer foto. A foto se move em parallax sutil acompanhando o scroll (CSS + JS leve, sem libs externas), funciona em PC e mobile. O texto do hero também reage ao scroll (translateY + fade), em sincronia com a foto, criando sensação de profundidade.
- **Títulos do hero curtos e diretos:** desde 2026-06-28, os H1/subtítulos do hero das 5 páginas são frases curtas (ex: "Maternal ao 9º ano, em Uberlândia."), não parágrafos — prioriza leitura rápida e visual limpo sobre a foto.
- **Object-position da foto da fachada (Início e Sobre):** em telas largas (acima de 860px), a foto da fachada usa `object-position: 33% 32%` (em vez de `center`) pra não cortar a placa "Colégio Belchior Costa" — o crop padrão centralizado tirava o texto da placa em viewports muito largos (ex: 1920px). No mobile o enquadramento padrão (`center 28%`) já funciona bem e foi mantido.
- **Blobs decorativos:** formas orgânicas borradas (`blur(60px)`), nas 3 cores da marca (azul/amarelo/vermelho), opacidade baixa (~16%), flutuando bem lentamente (24s por ciclo) atrás de uma seção por página (ex: "Missão, visão e valores" na Sobre, "Por que famílias escolhem" na Home). Dá uma sensação de movimento/modernidade sem pesar visualmente — pensado pra não cair no erro de ficar "futurista demais" pra uma escola.
- **Fotos de turma (Infantil, Fund. I, Fund. II):** ainda são imagens geradas por IA (estilo fotográfico realista, mesma sala/decoração entre as 3, cores combinando com cada segmento), usadas como placeholder até a escola enviar fotos reais das turmas. O `alt` dessas imagens não afirma que são fotos reais da escola, de propósito.
