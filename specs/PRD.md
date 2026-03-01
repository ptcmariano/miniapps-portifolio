project using: astro
npm create astro@latest

# PRD — Mini Apps (Landing Page Estática)

## 1. Resumo
O **Mini Apps** é uma página web estática que funciona como um catálogo/portfólio para divulgar micro-aplicativos. O conceito central foca em simplicidade, velocidade e privacidade, oferecendo ferramentas que não exigem cadastro e mantêm os dados do usuário salvos localmente.

*   **Nome do Produto:** Mini Apps
*   **Domínio/Branding:** `MiniApps.br`
*   **Publicação:** GitHub Pages
*   **Estratégia de URLs:** Subrotas (ex: `/semana-treino/`, `/proximo-onibus/`)
*   **Stack Técnica:** HTML5, CSS3 e JavaScript Vanilla (sem frameworks; dependências mínimas).

## 2. Objetivos
*   Divulgar os apps de forma visualmente atraente e intuitiva.
*   Direcionar tráfego para os aplicativos hospedados no GitHub Pages.
*   **Reforçar os pilares:** Sem cadastro, dados locais (`localStorage`), rápido e leve.
*   Estabelecer canal de contato via WhatsApp e mensuração via Analytics.

## 3. Não-objetivos (Fora de escopo)
*   Transformar a própria landing page em um PWA.
*   Incluir botões de "Instalar como app" (reservado para os mini apps individuais).
*   Prometer funcionamento 100% offline na landing (requer Service Workers).
*   Definir métricas rígidas de performance (manter apenas como princípio de design).

## 4. Público-alvo
*   Usuários mobile que buscam ferramentas diretas e sem fricção (sem login).
*   **Comunidades específicas:**
    *   **Fitness:** Usuários do *Semana-Treino*.
    *   **Mobilidade:** Usuários do *Próximo Ônibus*.
    *   **Geeks/Jogadores:** Jogadores de Pokémon TCG (*PokéVidas*).

## 5. Proposta de Valor
> "Mini Apps: simples, instantâneos, sem cadastro e feitos com carinho. Seus dados ficam no seu dispositivo (localStorage) — e você só abre e usa."

## 6. Requisitos de Conteúdo (Copywriting)

**6.1 Hero (Primeira Dobra)**
*   **Título (H1):** "Mini Apps que resolvem problemas reais."
*   **Subtítulo:** "Sem cadastro. Sem enrolação. Rápidos no celular."
*   **Badges:** `LocalStorage` • `Mobile-first` • `Leve`

**6.2 Seção "Apps Desenvolvidos"**
Exibição em cards (1 coluna mobile / 3 colunas desktop) com cores de acento específicas:

*   **Semana-Treino** (Acento: `#22c55e`)
    *   *Descrição:* "Treino semanal sem complicação."
    *   *Destaques:* Lista • Limpar Semana • Configurações.
    *   *Tags:* `localStorage`, `Sem cadastro`, `Rápido`.
*   **Próximo Ônibus** (Acento: `#3b82f6`)
    *   *Descrição:* "Quanto tempo falta pro meu ônibus?"
    *   *Destaques:* Ida e volta favoritadas • Horários do dia.
    *   *Tags:* `localStorage`, `Sem cadastro`, `Interface limpa`.
*   **PokéVidas** (Acento: `#a855f7`)
    *   *Descrição:* "Prêmios e dano no Pokémon TCG, sem papel."
    *   *Destaques:* Histórico local • Exportar em texto.
    *   *Tags:* `localStorage`, `Sem cadastro`, `Feito pra torneios`.

**6.3 Seção "Por que Mini Apps?"**
*   **Sem cadastro:** Abre e usa.
*   **Dados locais:** Salvo no seu dispositivo com `localStorage`.
*   **Leves e rápidos:** Foco no essencial.
*   **Propósito:** Feitos com carinho (e um pouco de ódio de esperar ônibus).

**6.4 Seção "Em breve"**
*   Cards de placeholder: "Em desenvolvimento" e "Sugira um mini app" (CTA WhatsApp).

**6.5 Footer**
*   Créditos: "Feito em Salto de Pirapora, SP."
*   Links: GitHub e Redes Sociais.
*   **CTA Final:** "Quer um app personalizado? Me chama no WhatsApp."

## 7. Requisitos Funcionais

**7.1 Estrutura de Navegação**
Single page com rolagem suave nas seções: Header > Hero > Apps > Sobre > Em Breve > Footer.

**7.2 Header Fixo**
*   Logo à esquerda; Links de navegação à direita.
*   Menu hambúrguer para dispositivos móveis.

**7.3 Interação de Cards**
*   O clique no card deve abrir um **Modal de Detalhes**.
*   Botões internos: "Detalhes" e "Abrir app →" (abre em nova aba).

**7.4 Modal "Mini-Landing"**
*   Nome do app + Cor de acento.
*   Parágrafo descritivo e lista de features (3 a 6 itens).
*   **CTAs:** "Abrir app em tela cheia", "Ver código no GitHub" e "Compartilhar" (Web Share API).
*   *Opcional:* Iframe com demo (carregamento via lazy-load).

## 8. Requisitos Não-Funcionais

*   **Performance:** Carregamento instantâneo, imagens em SVG/WebP e lazy-load de componentes pesados.
*   **Responsividade:** Grid adaptável (1 a 3 colunas).
*   **Acessibilidade:** Dark theme com alto contraste, navegação por teclado, `aria-labels` e fechamento de modais via tecla `Esc`.
*   **SEO:** Meta tags otimizadas para termos como "sem cadastro" e "localStorage".

## 9. Design System

*   **Paleta de Cores:**
    *   Fundo: `#0a0a0a` (Dark)
    *   Texto: `#f4f4f5`
    *   Acentos: Verde (`#22c55e`), Azul (`#3b82f6`), Roxo (`#a855f7`).
*   **Tipografia:** Inter ou Satoshi.
*   **Interações:** Hover nos cards com `scale(1.02)` e brilho sutil (*glow*) na cor temática do app.

## 10. Analytics e Privacidade

*   **Transparência:** Texto no footer explicando o uso de analytics agregado e reforçando que dados sensíveis não são coletados.
*   **Eventos Rastreados:** Visualização da home, cliques em abrir app, detalhes, GitHub, WhatsApp e compartilhamentos.
*   **Página de Privacidade:** `/privacidade.html` com termos simplificados.

---

#### 11. Critérios de Aceitação (DoD)
1.  [ ] Landing publicada e acessível no GitHub Pages.
2.  [ ] Layout mobile-first validado.
3.  [ ] 3 cards de apps funcionais com modais e links corretos.
4.  [ ] Analytics configurado com eventos básicos.
5.  [ ] Link de WhatsApp e página de privacidade operacionais.

---

#### 12. Backlog (Futuro)
*   Padronização de URLs para `/apps/{slug}/`.
*   Inclusão de screenshots reais dos aplicativos.
*   Páginas dedicadas por app para melhor indexação SEO.
*   Implementação de PWA nos mini apps individuais.