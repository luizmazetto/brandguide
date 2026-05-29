# Viva Design System — Tokens

Documento mestre dos tokens de design da Viva. Codifica as decisões atômicas do brand guide em variáveis reutilizáveis. Tudo que for construído daqui em diante — site, app, decks, welcome books, peças sociais — deve referenciar esses tokens.

**Princípio orientador:** O design system traduz "operação premium em escala" para o nível tático. Cada token tem razão estratégica, não estética arbitrária.

---

## 1. Cores

### 1.1 Paleta base

| Token | Hex | Uso |
|---|---|---|
| `color.navy` | `#0B1B2E` | Cor estrutural primária. Tipografia em fundos claros, fundos institucionais, profundidade |
| `color.creme` | `#F5F1E8` | Fundo primário. Substitui o branco em quase todos os contextos de marca |
| `color.terracota` | `#C45A3D` | Acento de cor. Usado com extrema parcimônia |
| `color.ocre` | `#D4A574` | Acento secundário. Detalhes editoriais, ilustrações |
| `color.branco` | `#FFFFFF` | Apenas para contextos digitais funcionais (OTAs, sistemas) |

### 1.2 Escala de opacidade do navy

Para hierarquia tipográfica sobre fundo claro. Nunca usar cinzas neutros — sempre navy com opacidade.

| Token | Valor | Uso |
|---|---|---|
| `color.navy.100` | `rgba(11,27,46,1.0)` | Títulos principais, ênfase máxima |
| `color.navy.80` | `rgba(11,27,46,0.8)` | Subtítulos, corpo principal |
| `color.navy.60` | `rgba(11,27,46,0.6)` | Corpo secundário |
| `color.navy.40` | `rgba(11,27,46,0.4)` | Texto auxiliar, captions |
| `color.navy.20` | `rgba(11,27,46,0.2)` | Bordas, dividers |
| `color.navy.10` | `rgba(11,27,46,0.1)` | Fundos sutis, hover states |
| `color.navy.06` | `rgba(11,27,46,0.06)` | Bordas extremamente sutis |

### 1.3 Escala de opacidade do creme (sobre navy)

Para hierarquia tipográfica sobre fundo navy.

| Token | Valor | Uso |
|---|---|---|
| `color.creme.100` | `rgba(245,241,232,1.0)` | Títulos sobre navy |
| `color.creme.70` | `rgba(245,241,232,0.7)` | Corpo sobre navy |
| `color.creme.50` | `rgba(245,241,232,0.5)` | Texto secundário sobre navy |
| `color.creme.30` | `rgba(245,241,232,0.3)` | Labels, metadata sobre navy |
| `color.creme.12` | `rgba(245,241,232,0.12)` | Bordas e dividers sobre navy |

### 1.4 Cores semânticas (apenas para produto digital)

Para feedbacks de sistema. Não usar em peças de marca.

| Token | Hex | Uso |
|---|---|---|
| `color.success` | `#3D6B4E` | Confirmações, sucesso |
| `color.warning` | `#C49E3D` | Alertas, atenção |
| `color.error` | `#A4453A` | Erros, ações destrutivas |
| `color.info` | `#3D5F8C` | Informações neutras |

### 1.5 Regras de uso de cor

**Navy é estrutural.** Aparece como tipografia, fundos institucionais, ícones funcionais. É a cor que sustenta a identidade.

**Creme é o fundo padrão.** Substitui o branco em peças de marca. Branco puro só em contextos digitais funcionais onde a saturação cromática do creme atrapalha (formulários, dashboards internos).

**Terracota é acento, nunca protagonista.** Usar para:
- Eyebrows/labels de seção (small caps, 9-10px)
- Pingo do "i" em variações específicas do logo (quando aprovado)
- Detalhes editoriais em ilustrações
- Nunca para botões primários, nunca para grandes áreas de cor

**Ocre é o quarto plano.** Detalhes em ilustrações, gravuras, contextos editoriais. Aparece menos que terracota.

**Proporção recomendada em qualquer composição:** ~70% creme + ~25% navy + ~5% acentos (terracota + ocre).

---

## 2. Tipografia

### 2.1 Famílias

| Token | Família | Uso |
|---|---|---|
| `font.display` | `'Fraunces', serif` | Títulos, frases-âncora, citações editoriais |
| `font.accent` | `'Architects Daughter', cursive` | Camada manuscrita, anotações editoriais, never body |
| `font.body` | `'Jost', sans-serif` | Corpo de texto, UI, labels, dados |

### 2.2 Escala de tamanhos

Sistema modular. Cada nível tem propósito específico — não inventar tamanhos fora da escala.

| Token | Tamanho | Line-height | Uso |
|---|---|---|---|
| `font.size.xs` | `10px` | `1.4` | Labels uppercase, eyebrows, metadata |
| `font.size.sm` | `12px` | `1.5` | Captions, footnotes, micro-texto |
| `font.size.base` | `14px` | `1.6` | Corpo padrão em UI |
| `font.size.md` | `16px` | `1.7` | Corpo principal em prosa |
| `font.size.lg` | `18px` | `1.6` | Corpo enfatizado, intro paragraphs |
| `font.size.xl` | `22px` | `1.5` | Subtítulos |
| `font.size.2xl` | `28px` | `1.4` | Títulos de seção |
| `font.size.3xl` | `36px` | `1.3` | Títulos principais |
| `font.size.4xl` | `48px` | `1.2` | Hero, frase-âncora |
| `font.size.5xl` | `64px` | `1.1` | Apenas hero principal |

### 2.3 Pesos

| Token | Valor | Uso |
|---|---|---|
| `font.weight.light` | `300` | Jost apenas, em corpo amplo |
| `font.weight.regular` | `400` | Padrão para Fraunces e Jost |
| `font.weight.medium` | `500` | Fraunces em títulos de destaque |
| `font.weight.semibold` | `600` | Jost em labels, eyebrows |

**Regra:** Nunca usar bold (700+). Hierarquia se faz por tamanho, peso médio (500) e tracking, nunca por bold.

### 2.4 Letter-spacing (tracking)

| Token | Valor | Uso |
|---|---|---|
| `tracking.tight` | `-0.02em` | Apenas em títulos muito grandes (4xl+) em Fraunces |
| `tracking.normal` | `0` | Corpo de texto |
| `tracking.wide` | `0.05em` | Botões, labels |
| `tracking.wider` | `0.15em` | Eyebrows, small caps |
| `tracking.widest` | `0.25em` | Eyebrows de seção principal |

### 2.5 Hierarquia tipográfica (regra de uso)

**Display (Fraunces):** títulos de seção, frases-âncora, citações editoriais. Sempre em peso 400 ou 500. Nunca em caixa alta.

**Body (Jost):** todo o resto. Corpo, UI, labels, dados, navegação. Versátil.

**Accent (Architects Daughter):** uso extremamente seletivo. Apenas para anotações editoriais que reforçam a camada humana — uma frase manuscrita ao lado de uma estatística, uma nota de rodapé sobre uma foto. Nunca como corpo, nunca em UI. Se em dúvida, não usa.

---

## 3. Espaçamento

Sistema de 4px. Toda decisão de espaço deve ser múltiplo de 4. Cria ritmo visual consistente.

| Token | Valor | Uso |
|---|---|---|
| `space.1` | `4px` | Micro ajustes, dentro de pills/tags |
| `space.2` | `8px` | Entre elementos relacionados (label + valor) |
| `space.3` | `12px` | Padding interno de pequenos componentes |
| `space.4` | `16px` | Padding padrão de cards, entre parágrafos |
| `space.6` | `24px` | Padding de cards maiores, entre subseções |
| `space.8` | `32px` | Entre seções relacionadas |
| `space.12` | `48px` | Entre blocos de conteúdo |
| `space.16` | `64px` | Separação de seções principais |
| `space.24` | `96px` | Espaço vertical entre seções de página |
| `space.32` | `128px` | Espaço de respiração em hero sections |

**Princípio:** Quando em dúvida entre dois valores, escolher o maior. Espaço em branco é luxo estratégico da Viva.

---

## 4. Border radius

| Token | Valor | Uso |
|---|---|---|
| `radius.none` | `0` | Tabelas, dividers |
| `radius.sm` | `2px` | Inputs, pills muito pequenos |
| `radius.base` | `4px` | Cards padrão, botões |
| `radius.md` | `6px` | Cards de destaque, modais |
| `radius.lg` | `12px` | Imagens, cards grandes |
| `radius.full` | `9999px` | Avatares, badges circulares |

**Regra:** Nunca usar radius >12px em cards retangulares — fica boutique demais. A Viva é sóbria, não fofa.

---

## 5. Shadows (elevação)

Usar com extrema parcimônia. Sombras adicionam ruído visual. A Viva prefere bordas sutis a sombras dramáticas.

| Token | Valor | Uso |
|---|---|---|
| `shadow.none` | `none` | Padrão |
| `shadow.sm` | `0 1px 2px rgba(11,27,46,0.04)` | Cards em listagem |
| `shadow.base` | `0 2px 8px rgba(11,27,46,0.06)` | Cards interativos em hover |
| `shadow.md` | `0 8px 24px rgba(11,27,46,0.08)` | Modais, dropdowns |
| `shadow.lg` | `0 16px 48px rgba(11,27,46,0.12)` | Overlays principais |

**Regra:** Prefira `border: 1px solid var(--color-navy-06)` a shadows quando possível. Sombras só quando há elevação real (modal, dropdown, drag).

---

## 6. Breakpoints

Mobile-first. Build para mobile, escala para desktop.

| Token | Valor | Dispositivo |
|---|---|---|
| `breakpoint.sm` | `640px` | Mobile landscape, tablet portrait |
| `breakpoint.md` | `768px` | Tablet |
| `breakpoint.lg` | `1024px` | Desktop pequeno |
| `breakpoint.xl` | `1280px` | Desktop padrão |
| `breakpoint.2xl` | `1536px` | Desktop amplo |

---

## 7. Iconografia

**Estilo:** Line art hand-drawn, contínuo, traço único quando possível.

**Parâmetros para geração via Midjourney:**
- Stroke weight: `--s 40`
- Style: `loose confident ink strokes`, `open lines with breathing room`
- Cor: sempre navy `#0B1B2E` sobre fundo transparente
- Tamanho de referência: 64x64px (escalável a 16-256px)

**Não usar:**
- Ícones de bibliotecas genéricas (Material, FontAwesome) sem adaptação
- Ícones com fill colorido
- Ícones em estilo flat geométrico

**Quando precisar de ícone:**
1. Verificar se existe na biblioteca Viva (toalhas, amenities, gym, wi-fi, Nespresso)
2. Se não existe, gerar via Midjourney com os parâmetros acima
3. Vetorizar (Illustrator) e adicionar à biblioteca

---

## 8. Imagens e fotografia

**Princípio:** "Presença invisível. Humana quando faz diferença." Os ambientes falam pelo cuidado da operação, não pela performance de pessoas vivendo neles.

**Diretrizes:**
- Vida sem gente: ambientes acabados de arrumar, sem figurantes
- Luz natural sempre que possível
- Composições limpas, mobiliário em uso real (cama feita, mesa posta)
- Detalhes operacionais visíveis: toalha dobrada, água na mesa de cabeceira, controle alinhado
- Pessoas apenas quando o cuidado humano é o ponto (anfitriã, técnico, equipe)

**Tratamento:**
- Sem filtros saturados
- Cores reais dos ambientes
- Em watercolor/sketch: preservar as cores originais do prédio, nunca impor a paleta Viva sobre arquitetura existente

**Proporções padrão:**
- Hero: 16:9
- Card: 3:2 ou 4:3
- Square (Instagram): 1:1
- Vertical (Stories, Reels): 9:16

---

## 9. Densidade de layout

Espaço em branco é o luxo que a Viva tem e que a concorrência não usa.

**Regras:**
- Margens laterais mínimas em desktop: 64px (mobile: 24px)
- Largura máxima de coluna de texto: 680px (legibilidade)
- Padding interno mínimo de cards: 24px (mobile) / 32px (desktop)
- Espaço vertical entre seções: nunca menos que 64px

**Princípio:** Se a peça parece "muito vazia", está no ponto certo. Adicionar mais conteúdo é tentação, raramente é necessidade.

---

## 10. Como usar este documento

**No Claude:** Anexe este arquivo ao iniciar uma conversa, ou inclua no system prompt de um Projeto. O Claude consulta antes de produzir qualquer peça com identidade Viva.

**No código:** Use o `viva_design_tokens.css` como source of truth. Importe no projeto e use as variáveis CSS.

**No Figma:** Os tokens devem ser sincronizados como Variables. Cada designer deve estar usando a biblioteca Viva, nunca cores/tamanhos custom.

**Em qualquer aplicação:** Se você está prestes a inventar um valor que não está aqui (uma cor nova, um tamanho de fonte fora da escala, um espaçamento custom), pare. Provavelmente existe um token que serve. Se realmente não existe, é uma exceção que deve ser discutida — não decisão individual.
