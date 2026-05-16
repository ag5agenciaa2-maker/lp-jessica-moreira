# SITE DNA — JÉSSICA MOREIRA ADVOCACIA

**Nicho:** Advocacia Previdenciária — Aposentadorias, benefícios do INSS e planejamento previdenciário. Atendimento local em Campo Grande (Zona Oeste - RJ) e online para todo o Brasil.
**Posicionamento:** Autoridade técnica acessível — transmite confiança institucional (OAB, Comissão Previdenciária) sem afastar o cidadão comum. A sensação de impacto é de segurança jurídica humanizada: "Alguém competente do meu lado".
**Data de criação:** 2025

---

## IDENTIDADE VISUAL

### Paleta de Cores

| Variável CSS | Hex | Função Específica no Layout |
|---|---|---|
| `--color-primary` | `#4A5D23` | Verde musgo escuro — cor dominante: botões CTA, tags, bordas de destaque, fundo `.como-funciona` e `.cta-final` |
| `--color-primary-dark` | `#3D4D1C` | Hover state de todos os botões primários (escurecimento -15%) |
| `--color-primary-light` | `#5A7029` | Variação de apoio — não usada extensivamente, reserva de hover alternativo |
| `--color-gold` | `#B8860B` | Dourado escuro — ícone shield/OAB, estrelas de rating, ícones de contato no footer, `.passo-numero` background |
| `--color-gold-light` | `#D4A84B` | Hover do link da agência no footer bottom |
| `--color-white` | `#FFFFFF` | Backgrounds de cards, header, seção FAQ e Empatia |
| `--color-black` | `#1A1A1A` | Reserva, não aplicada diretamente |
| `--color-gray-100` | `#F8F9F7` | Background de seções alternadas (Serviços, Sobre) — tom levemente esverdeado |
| `--color-gray-200` | `#E8EBE5` | Bordas do header e separadores de FAQ |
| `--color-gray-300` | `#D1D6CC` | Não aplicada — reserva de sistema |
| `--color-gray-500` | `#6B7280` | Textos secundários: subtítulos de badge, ícone FAQ, `stars-text` |
| `--color-gray-700` | `#374151` | Cor padrão do `body` — texto de parágrafos e nav-links |
| `--color-gray-900` | `#111827` | Headings H1/H2/H3, textos de peso máximo |
| `#25D366` | `#25D366` | Exclusivo do botão WhatsApp flutuante |

### Tipografia

| Elemento | Família | Peso | Tamanho Exato | Observações |
|---|---|---|---|---|
| `h1` | Playfair Display | 600 | `clamp(2rem, 5vw, 3rem)` → min 32px / max 48px | Serif editorial para autoridade |
| `h2` | Playfair Display | 600 | `clamp(1.75rem, 4vw, 2.5rem)` → min 28px / max 40px | Títulos de seção; variação `.light` muda para `#FFFFFF` |
| `h3` | Playfair Display | 600 | `clamp(1.125rem, 2.5vw, 1.375rem)` → min 18px / max 22px | Títulos de cards |
| `h4` (footer) | Playfair Display | 600 | `0.875rem` / 14px | `text-transform: uppercase; letter-spacing: 0.05em` |
| `.hero-subtitle` | Inter | 400 | `1.0625rem` / 17px | `line-height: 1.7` |
| `.hero-bullets li` | Inter | 400 | `0.9375rem` / 15px | Com ícone SVG inline à esquerda (check circle verde) |
| `.hero-tag / .section-tag` | Inter | 600 | `0.75rem` / 12px (hero) · `0.6875rem` / 11px (seções) | `text-transform: uppercase; letter-spacing: 0.05–0.08em` |
| `body / p` | Inter | 400 | `1rem` / 16px base | `line-height: 1.6`; parágrafos de card: `0.875rem` |
| `.btn-primary / .btn-cta` | Inter | 600 | `0.9375rem` / 15px (primary) · `1rem` / 16px (cta) | |
| `.nav-link` | Inter | 500 | `0.875rem` / 14px | Underline animado no hover |
| `.autoridade-quote p` | Playfair Display | 400 | `0.9375rem` / 15px | `font-style: italic` |
| `.sobre-text blockquote p` | Playfair Display | 400 | herda `0.9375rem` | `font-style: italic` |
| `.cta-title` | Playfair Display | 600 | `clamp(1.5rem, 4vw, 2rem)` | Variação menor do H2 |
| `.footer-bottom` | Inter | 400 | `0.75rem` / 12px | `color: rgba(255,255,255,0.5)` |
| `.info-item strong` | Playfair Display | 600 | `1.125rem` / 18px | Cor `--color-primary` |
| `.info-item span` | Inter | 400 | `0.625rem` / 10px | `text-transform: uppercase; letter-spacing: 0.08em` |

### Estilo Geral

Design jurídico editorial de alta legibilidade, construído sobre um sistema bipartite tipográfico rigoroso: Playfair Display como voz de autoridade (headings e citações em itálico) contrastada com Inter como motor funcional de clareza (body, nav, botões). A paleta inverte o clichê azul-marinho do direito em favor de um verde musgo institucional (`#4A5D23`) — evocando equilíbrio, responsabilidade ambiental e credibilidade terrena — pontuada por dourado sóbrio (`#B8860B`) reservado exclusivamente a elementos de validação (OAB shield, estrelas, ícones de contato). O ritmo visual alterna fundos `#F8F9F7` e `#FFFFFF` em seções consecutivas para criar separação sem bordas explícitas, enquanto a seção "Como Funciona" e o CTA final quebram esse padrão com background sólido `#4A5D23`, criando ilhas imersivas de conversão. As sombras seguem hierarquia estrita (`shadow-sm → shadow-md → shadow-lg → shadow-xl`) e nenhum elemento usa `border-radius` acima de `24px`, mantendo sofisticação sem infantilização.

---

## LAYOUT — SEÇÃO POR SEÇÃO

### SEÇÃO 1 — Header (Fixo)

**Estrutura:** `position: fixed; top: 0; z-index: 1000`. Flexbox `justify-content: space-between; align-items: center`. Altura fixa de `70px`. Container `max-width: 1200px; padding: 0 1.25rem` (mobile) / `0 2rem` (tablet+).

**Fundo:** `background: rgba(255, 255, 255, 0.98)` + `backdrop-filter: blur(10px)`. `border-bottom: 1px solid #E8EBE5`. Ao scroll > 10px, JS injeta `box-shadow: 0 2px 10px rgba(0,0,0,0.1)`.

**Elementos Restritos:** Logo (img `height: 45px`) à esquerda → Nav central (desktop, `display: none` abaixo de 1024px) → Botão "Atendimento" (verde, `display: none` < 1024px) → Hambúrguer (visível apenas mobile).

**Animação:** Header "smart-hide" via JS: `transform: translateY(-100%)` quando `currentScroll > lastScroll && currentScroll > 100`; retorna `translateY(0)` ao rolar para cima. `transition: all 0.3s ease`.

**Micro-interações:** `.nav-link::after` — pseudo-elemento `height: 2px; background: #4A5D23; width: 0` → `width: 100%` em `0.3s ease` no hover. `.btn-header:hover` → `background: #3D4D1C` (sem translateY). Hambúrguer: spans 1 e 3 giram `±45deg` com `translate(5px, ±5px)`; span 2 `opacity: 0`.

**Diferenciador Visual:** Backdrop blur glacial com opacidade 98% garante leitura perfeita sem opacidade total, criando sensação de material "fosco premium".

---

### SEÇÃO 2 — Hero

**Estrutura:** Mobile: `flex-direction: column` — imagem acima (order 1), texto abaixo (order 2). Tablet+: `flex-direction: row; align-items: center; gap: 3rem`, cada coluna com `flex: 1`. `padding: 100px 0 60px` (mobile) / `120px 0 80px` (tablet) / `140px 0 100px` (desktop).

**Fundo:** `background: linear-gradient(135deg, #F8F9F7 0%, #FFFFFF 100%)` + pseudo-elemento `.hero-decoration` posicionado `absolute top:0 right:0 width:50% height:100%` com `linear-gradient(135deg, rgba(74,93,35,0.05) 0%, transparent 100%)` — sutil "halo verde" no lado direito.

**Elementos Restritos:** `.hero-tag` (pill verde claro, uppercase, 12px) → `H1` → `.hero-subtitle` → `.hero-bullets` (3 ítens com ícone check-circle SVG `20×20px` cor `#4A5D23`) → `.hero-buttons` (row gap 0.875rem: `.btn-primary` verde + `.btn-secondary` outline). Imagem com `filter: drop-shadow(0 20px 40px rgba(0,0,0,0.1))` + `.hero-badge` absoluto `bottom: 20px; right: 0 (mobile) / -20px (desktop)`, white card com shield icon dourado + texto "OAB/RJ Ativa / Compromisso Ético".

**Animação:** Nenhuma CSS entrance — scroll reveal JS aplica `opacity: 0 → 1; translateY(20px) → 0` em `0.5s ease` apenas nos cards de serviços/passos/FAQ, não no hero.

**Micro-interações:** `.btn-primary:hover` → `translateY(-2px); box-shadow: --shadow-lg` em `0.3s ease`. `.btn-secondary:hover` → `background: #4A5D23; color: #fff` (fill reverso). Botões WhatsApp com click feedback: `scale(0.98)` por `150ms`.

**Diferenciador Visual:** `.hero-badge` flutuante sobre a foto — micro-card independente com credencial OAB posicionado como "etiqueta" na imagem, criando camada de confiança visual sem precisar de seção separada de credenciais.

---

### SEÇÃO 3 — Empatia

**Estrutura:** `padding: 60px 0`. Coluna única centralizada `max-width: 800px; margin: 0 auto; text-align: center`.

**Fundo:** `background: #FFFFFF`.

**Elementos Restritos:** `H2` centralizado → parágrafo introdutório (`font-size: 1.0625rem; line-height: 1.8`) → `.empatia-highlight` — bloco de destaque com `background: rgba(74,93,35,0.05); border-left: 3px solid #4A5D23; border-radius: 10px; padding: 1.25rem`.

**Animação:** Scroll reveal JS (opacity + translateY).

**Micro-interações:** Nenhuma — seção estática informativa.

**Diferenciador Visual:** `.empatia-highlight` com `border-left` em cor primária substitui o clichê de "caixa de callout" genérica — funciona como "fala direta" da advogada ao cliente, sem iconografia excessiva.

---

### SEÇÃO 4 — Serviços

**Estrutura:** `padding: 60px 0`. Grid responsivo: 1 col (mobile) → `repeat(2, 1fr)` (tablet) → `repeat(3, 1fr)` (desktop). `.servico-cta-card` usa `grid-column: span 2` no tablet e `span 1` no desktop (entra normalmente na grade 3×2).

**Fundo:** `background: #F8F9F7`.

**Elementos Restritos:** `.section-header` centralizado (`max-width: 700px`) com tag "Excelência Jurídica" + H2 + descrição → Grid de 5 `.servico-card` + 1 `.servico-cta-card`. Cada card: ícone SVG em container `56×56px` com `background: rgba(74,93,35,0.1); border-radius: 10px` → H3 → parágrafo descritivo.

**Animação:** Scroll reveal JS: `opacity: 0; transform: translateY(20px)` → `opacity: 1; transform: translateY(0)` em `0.5s ease`. Threshold: `windowHeight - 100px`.

**Micro-interações:** `.servico-card:hover` → `transform: translateY(-4px); box-shadow: 0 10px 15px -3px rgba(0,0,0,0.1), 0 4px 6px -2px rgba(0,0,0,0.05)` em `0.3s ease`. `.servico-cta-card` sem hover transformado — fundo sólido verde com `.btn-outline:hover` → `background: #fff; color: #4A5D23`.

**Diferenciador Visual:** O 6º card (`.servico-cta-card`) quebra o padrão visual sendo o único card de fundo sólido verde na grade branca — funciona como CTA embutido no próprio grid de serviços, eliminando a necessidade de botão externo.

---

### SEÇÃO 5 — Como Funciona

**Estrutura:** `padding: 60px 0`. Grid: 1 col (mobile) → `repeat(2, 1fr)` (tablet) → `repeat(4, 1fr)` (desktop). `gap: 1.5rem`.

**Fundo:** `background: #4A5D23` — seção sólida de imersão verde.

**Elementos Restritos:** `.section-header` com H2 branco (`.section-title.light`) → 4 `.passo-card`. Cada card: `.passo-numero` (círculo dourado `32×32px`, posição `absolute top: -12px left: 1.25rem`) + ícone SVG em container `48×48px` com `background: rgba(255,255,255,0.15)` + H3 branco + parágrafo `rgba(255,255,255,0.8)`.

**Animação:** Scroll reveal JS nos `.passo-card`.

**Micro-interações:** Nenhum hover nos `.passo-card` — intencionalmente passivos. `backdrop-filter: blur(10px)` nos cards para efeito glass-morphism sobre o verde.

**Diferenciador Visual:** Numeração posicionada como "badge flutuante" (`position: absolute; top: -12px`) — o número dosa entre "fora" e "dentro" do card, criando profundidade sem uso de z-index complexo. Contraste máximo branco-sobre-verde sem perda de legibilidade.

---

### SEÇÃO 6 — Autoridade (Institucional)

**Estrutura:** `padding: 60px 0`. Mobile: coluna única (imagem acima order 1, texto abaixo order 2). Tablet+: `flex-direction: row; align-items: center; gap: 3rem; flex: 1` cada lado.

**Fundo:** `background: #FFFFFF`.

**Elementos Restritos:** Lado texto: tag "Reconhecimento Institucional" → H2 → parágrafo → 2 `.badge-item` (flex row com ícone shield + texto strong/span em `background: #F8F9F7; border-radius: 10px; padding: 1rem`) → linha de estrelas `★★★★★` cor `#B8860B`. Lado imagem: `<img>` com `border-radius: 16px; box-shadow: --shadow-lg` + `.autoridade-quote` absoluto `bottom: -20px; left/right: 1rem` — card verde com quote em itálico Playfair + fonte uppercase `0.625rem`.

**Animação:** Nenhuma de entrada diferenciada.

**Micro-interações:** Nenhum hover nos badges.

**Diferenciador Visual:** `.autoridade-quote` sobrepõe a foto com `position: absolute; bottom: -20px` — o texto "sai" da imagem, criando ancoragem visual única entre foto e copy institucional sem necessidade de div separada.

---

### SEÇÃO 7 — Sobre (Quem Somos)

**Estrutura:** `padding: 80px 0 60px`. Mobile: coluna única. Tablet+: `flex-direction: row; align-items: center; gap: 3rem; flex: 1` cada lado.

**Fundo:** `background: #F8F9F7`.

**Elementos Restritos:** Lado esquerdo: foto centralizada `max-height: 400px; border-radius: 16px; box-shadow: --shadow-lg`. Lado direito: tag "A Advogada" → H2 → 2 parágrafos → `<blockquote>` com `border-left: 3px solid #B8860B` (dourado) + texto Playfair itálico → `.sobre-info` (2 colunas flex com dados: "Campo Grande / Base de Atendimento" e "OAB Ativa / Registro OAB/RJ").

**Animação:** Nenhuma específica.

**Micro-interações:** Nenhum hover. Blockquote é elemento passivo de credibilidade.

**Diferenciador Visual:** O `blockquote` usa borda esquerda dourada (`#B8860B`) em contraste com a borda esquerda verde das demais seções — o dourado marca exclusivamente as "vozes pessoais/citações" da advogada, criando um sistema semântico de cor.

---

### SEÇÃO 8 — FAQ (Dúvidas Frequentes)

**Estrutura:** `padding: 60px 0`. Lista centralizada `max-width: 800px; margin: 0 auto`. Accordion via JS (toggle de classe `.active`).

**Fundo:** `background: #FFFFFF`.

**Elementos Restritos:** `.section-header` com H2 + descrição → Lista de `.faq-item`. Cada item: `.faq-question` (flex `justify-content: space-between; padding: 1.25rem 0; border-bottom: 1px solid #E8EBE5`) com span de pergunta + SVG chevron. `.faq-answer` com `max-height: 0; overflow: hidden`.

**Animação:** Accordion: `max-height: 0 → 300px` + `padding-bottom: 0 → 1.25rem` em `0.3s ease`. Ícone chevron: `transform: rotate(180deg); color: #4A5D23` quando `.active`.

**Micro-interações:** `.faq-question:hover` → `color: #4A5D23` em `0.3s ease`. Apenas um item pode estar aberto simultaneamente (JS fecha os demais ao abrir novo).

**Diferenciador Visual:** Sem cards/backgrounds separados por item — o FAQ usa apenas `border-bottom` como separador, mantendo leveza total. A animação de `max-height` cria transição suave sem JavaScript de altura dinâmica.

---

### SEÇÃO 9 — CTA Final

**Estrutura:** `padding: 60px 0`. Coluna única centralizada `max-width: 700px; margin: 0 auto; text-align: center`.

**Fundo:** `background: #4A5D23` — espelha o verde da seção "Como Funciona", criando bookend visual de conversão.

**Elementos Restritos:** H2 branco (`clamp(1.5rem, 4vw, 2rem)`) → parágrafo `rgba(255,255,255,0.85)` → `.btn-cta` verde escuro + WhatsApp icon → nota `rgba(255,255,255,0.6)` 12px.

**Animação:** Nenhuma específica.

**Micro-interações:** `.btn-cta:hover` → `background: #3D4D1C; transform: translateY(-2px); box-shadow: --shadow-xl` em `0.3s ease`. Click feedback via JS: `scale(0.98)` por `150ms`.

**Diferenciador Visual:** `.btn-cta` verde escuro sobre fundo verde médio — contraste sutil mas funcional, com sombra `--shadow-lg` elevando o botão visualmente da superfície. A nota de rodapé em `rgba(255,255,255,0.6)` entrega transparência sem comprometer o ritmo visual.

---

### SEÇÃO 10 — Footer

**Estrutura:** `padding: 60px 0 0`. Grid: 1 col (mobile) → `repeat(2, 1fr)` (tablet) → `2fr 1fr 1.5fr 1.5fr` (desktop). `background: #111827`.

**Fundo:** `#111827` (gray-900). Separador superior: `border-bottom: 1px solid rgba(255,255,255,0.1)`.

**Elementos Restritos:** Col 1 (brand): logo `height: 50px` + parágrafo `rgba(255,255,255,0.7)` + ícones sociais (Instagram + WhatsApp) em círculos `40×40px` `rgba(255,255,255,0.1)`. Col 2 (navegação): H4 uppercase + lista de links. Col 3 (contato): H4 + lista com ícones SVG dourados `18×18px` cor `#B8860B`. Col 4 (localização): H4 + parágrafo + `.footer-hours` (box `background: rgba(255,255,255,0.05)` com label dourado uppercase). Footer-bottom: flex row no desktop, coluna no mobile, com copyright e crédito agência (link dourado).

**Animação:** Nenhuma.

**Micro-interações:** Social icons hover → `background: #4A5D23`. Nav links hover → `color: #FFFFFF`. Agência link hover → `color: #D4A84B`.

**Diferenciador Visual:** `.footer-hours` com `background: rgba(255,255,255,0.05)` cria um "caixote" quase invisível — mais sutil que um card tradicional, mas ainda delimita a informação de horário sem pesar o footer escuro.

---

### COMPONENTE FLUTUANTE — WhatsApp Float Button

**Estrutura:** `position: fixed; bottom: 20px; right: 20px; width: 60px; height: 60px; border-radius: 50%; z-index: 999`.

**Fundo:** `background: #25D366; box-shadow: 0 4px 12px rgba(37,211,102,0.4)`.

**Animação:** `@keyframes pulse` — alterna `box-shadow` de `rgba(37,211,102,0.4)` para `rgba(37,211,102,0.6)` em `2s infinite` (suave respiração).

**Micro-interações:** `:hover` → `transform: scale(1.1); box-shadow: 0 6px 20px rgba(37,211,102,0.5)`.

---

## COMPONENTES REUTILIZÁVEIS

### Botões

```css
/* BTN PRIMARY — CTA principal do hero e header */
.btn-primary {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 1rem 1.5rem;             /* 16px 24px */
  background: #4A5D23;
  color: #FFFFFF;
  font-size: 0.9375rem;             /* 15px */
  font-weight: 600;
  border-radius: 10px;              /* --radius-md */
  box-shadow: 0 4px 6px -1px rgba(0,0,0,0.1), 0 2px 4px -1px rgba(0,0,0,0.06);
  transition: all 0.3s ease;
}
.btn-primary:hover {
  background: #3D4D1C;
  transform: translateY(-2px);
  box-shadow: 0 10px 15px -3px rgba(0,0,0,0.1), 0 4px 6px -2px rgba(0,0,0,0.05);
}

/* BTN SECONDARY — outline, hero secundário */
.btn-secondary {
  padding: 1rem 1.5rem;
  background: transparent;
  color: #4A5D23;
  border: 2px solid #4A5D23;
  border-radius: 10px;
  font-size: 0.9375rem;
  font-weight: 600;
  transition: all 0.3s ease;
}
.btn-secondary:hover {
  background: #4A5D23;
  color: #FFFFFF;
}

/* BTN OUTLINE — cards de CTA (fundo escuro) */
.btn-outline {
  padding: 0.875rem 1.5rem;         /* 14px 24px */
  background: transparent;
  color: #FFFFFF;
  border: 2px solid #FFFFFF;
  border-radius: 10px;
  font-size: 0.875rem;
  font-weight: 600;
  transition: all 0.3s ease;
}
.btn-outline:hover {
  background: #FFFFFF;
  color: #4A5D23;
}

/* BTN CTA — CTA final, maior */
.btn-cta {
  padding: 1.125rem 2rem;           /* 18px 32px */
  background: #4A5D23;
  color: #FFFFFF;
  font-size: 1rem;
  font-weight: 600;
  border-radius: 10px;
  box-shadow: 0 10px 15px -3px rgba(0,0,0,0.1), 0 4px 6px -2px rgba(0,0,0,0.05);
  transition: all 0.3s ease;
}
.btn-cta:hover {
  background: #3D4D1C;
  transform: translateY(-2px);
  box-shadow: 0 20px 25px -5px rgba(0,0,0,0.1), 0 10px 10px -5px rgba(0,0,0,0.04);
}
```

### Cards de Serviço

```css
.servico-card {
  background: #FFFFFF;
  padding: 1.75rem;                 /* 28px */
  border-radius: 16px;             /* --radius-lg */
  box-shadow: 0 1px 2px rgba(0,0,0,0.05);  /* --shadow-sm */
  transition: all 0.3s ease;
}
.servico-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 10px 15px -3px rgba(0,0,0,0.1), 0 4px 6px -2px rgba(0,0,0,0.05);
}

/* Ícone container */
.servico-icon {
  width: 56px;
  height: 56px;
  background: rgba(74, 93, 35, 0.1);
  border-radius: 10px;
  /* SVG interno: 28×28px, color: #4A5D23 */
}
```

### Cards de Passo (Como Funciona)

```css
.passo-card {
  background: rgba(255, 255, 255, 0.1);
  padding: 1.75rem;
  border-radius: 16px;
  border: 1px solid rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
  position: relative;   /* para passo-numero absoluto */
}

.passo-numero {
  position: absolute;
  top: -12px;
  left: 1.25rem;
  width: 32px;
  height: 32px;
  background: #B8860B;  /* --color-gold */
  color: #FFFFFF;
  font-size: 0.875rem;
  font-weight: 700;
  border-radius: 50%;
}
```

### Accordion FAQ

```css
.faq-answer {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.3s ease, padding 0.3s ease;
}
.faq-item.active .faq-answer {
  max-height: 300px;
  padding-bottom: 1.25rem;
}
.faq-icon {
  transition: all 0.3s ease;
}
.faq-item.active .faq-icon {
  transform: rotate(180deg);
  color: #4A5D23;
}
```

### Tags / Pills de Seção

```css
.section-tag {
  display: inline-block;
  padding: 0.375rem 0.875rem;       /* 6px 14px */
  background: rgba(74, 93, 35, 0.1);
  color: #4A5D23;
  font-size: 0.6875rem;             /* 11px */
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  border-radius: 6px;               /* --radius-sm */
}
```

### Sistema de Sombras (hierarquia)

```css
--shadow-sm:  0 1px 2px rgba(0,0,0,0.05);
--shadow-md:  0 4px 6px -1px rgba(0,0,0,0.1), 0 2px 4px -1px rgba(0,0,0,0.06);
--shadow-lg:  0 10px 15px -3px rgba(0,0,0,0.1), 0 4px 6px -2px rgba(0,0,0,0.05);
--shadow-xl:  0 20px 25px -5px rgba(0,0,0,0.1), 0 10px 10px -5px rgba(0,0,0,0.04);
```

### Border-Radius System

```css
--radius-sm: 6px;    /* tags/pills */
--radius-md: 10px;   /* botões, badges, inputs */
--radius-lg: 16px;   /* cards de serviço, imagens */
--radius-xl: 24px;   /* reserva — não usado */
```

---

## ANTI-PADRÕES REGISTRADOS

❌ **Paleta azul-marinho genérica de "escritório de advocacia"** — O projeto deliberadamente abandona o binômio azul-dourado saturado ubíquo em sites jurídicos. O verde musgo `#4A5D23` posiciona a marca em um nicho cromático inexplorado no segmento, gerando diferenciação imediata na memória visual do usuário.

❌ **Hero com fundo fotográfico escuro + overlay + texto branco centrado** — O hero usa fundo gradiente claro `#F8F9F7 → #FFFFFF` com texto escuro, quebrando o padrão "foto de balança/martelo + texto branco sobreposto" que domina landing pages jurídicas. A imagem da advogada ocupa coluna separada, sem servir de plano de fundo.

❌ **Listagem genérica de "anos de experiência / clientes atendidos / casos ganhos" em formato contador animado** — Nenhum bloco de estatísticas fabricadas. A prova de autoridade é construtiva: nome da comissão OAB específica (29ª Subseção), registro ativo, foto em evento institucional real com legenda — tangível e verificável.

❌ **Seção de depoimentos com fotos de stock e estrelas decorativas sem credibilidade** — O projeto não usa seção de testimonials. A prova social é substituída pela credencial institucional (Comissão de Direito Previdenciário da OAB) e pelo posicionamento consultivo do copy, evitando depoimentos que o usuário não pode verificar.

❌ **Formulário de captação com campos nome/email/telefone/mensagem como CTA principal** — Todo o fluxo de conversão é direcionado ao WhatsApp com mensagem pré-preenchida (`?text=Olá, vim pelo site...`), eliminando fricção de formulário e reduzindo a barreira de entrada. O único CTA é contato imediato.

❌ **Seção "Por que nos escolher?" com ícones de check genéricos (rapidez, qualidade, confiança)** — A seção "Como Funciona" substitui o padrão de promessas vazias por um fluxo operacional concreto de 4 passos (Contato → Análise → Estratégia → Acompanhamento), transformando a promessa em processo.

❌ **Footer minimalista com apenas copyright e redes sociais** — O footer é informacionalmente denso com grid 4 colunas: brand, navegação, contato com endereço físico/telefone formatado com ícones dourados, e bloco de horários com visual diferenciado (`rgba(255,255,255,0.05)`) — reforça credibilidade local e profissional até o último elemento da página.
