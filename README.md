# ☕ The Coffee — Landing Page

Uma landing page estática para cafeteria, desenvolvida com HTML5 e CSS3 puro. O projeto apresenta o cardápio, seção "Sobre nós", avaliações de clientes, localização e rodapé com redes sociais.

## Visão Geral

A **The Coffee** é uma página de apresentação de cafeteria com design escuro e elegante. Desenvolvida como projeto front-end, ela simula uma vitrine digital com navegação, menu de produtos, depoimentos de clientes e localização via Google Maps.

**Preview das seções:**

| Seção | Descrição |
|---|---|
| Home | Hero com imagem de fundo e chamada para ação |
| Sobre | Texto institucional com foto |
| Menu | Grade com 6 produtos e preços |
| Avaliações | Depoimentos de 3 clientes com estrelas |
| Endereço | Mapa incorporado do Google Maps |
| Footer | Links para redes sociais |

---

## Estrutura do Projeto

```
Coffee-Page/
|
├── index.html        # Estrutura principal da página
├── style.css         # Todos os estilos e responsividade
├── README.md         # Documentação do projeto
📂└── img/
    ├── logo.png           # Logo principal da cafeteria
    ├── logo(1).png        # Versão alternativa do logo
    ├── home-img.jpg       # Imagem de fundo do hero
    ├── about-img.jpg      # Foto da seção "Sobre nós"
    ├── menu-1.png         # Imagens dos itens do cardápio
    ├── menu-2.png
    ├── menu-3.png
    ├── menu-4.png
    ├── menu-5.png
    ├── menu-6.png
    ├── pic-1.png          # Fotos dos clientes (avaliações)
    ├── pic-2.png
    ├── pic-3.png
    └── quote-img.png      # Ícone de aspas decorativo
```

---

## Seções da Página

### 🔝 Header (Cabeçalho)
- Fixo no topo da tela (`position: fixed`)
- Contém: logo, menu de navegação com 6 links e ícones de busca e carrinho
- Links de âncora para todas as seções: `#home`, `#about`, `#menu`, `#review`, `#address`, `#contact`
- Ícones externos via [Icons8](https://icons8.com)

### 🏠 Home (Hero)
- Fundo com imagem de cobertura total (`background-size: cover`, altura `100vh`)
- Texto de destaque com chamada para ação
- Botão "Pegue o seu agora"

### ℹ️ Sobre Nós (`#about`)
- Layout em duas colunas: imagem à esquerda, texto à direita
- Fundo escuro (`--black: #13131a`)
- Botão "Saiba Mais"

### 🍵 Menu (`#menu`)
- Grade responsiva com `grid-template-columns: repeat(auto-fit, minmax(30rem, 1fr))`
- 6 itens com imagem, nome, preço promocional e botão de carrinho
- Efeito hover: fundo branco com texto escuro

### 💬 Avaliações (`#review`)
- Grade de 3 colunas (colapsa para 1 coluna em telas ≤ 768px)
- Cada card: ícone de aspas, texto do depoimento, foto circular do cliente, nome e estrelas
- Estrelas via Icons8 (4,5 estrelas para todos os clientes)

### 📍 Endereço (`#address`)
- `<iframe>` do Google Maps incorporado apontando para a unidade The Coffee

### 🦶 Footer (Rodapé)
- Ícones clicáveis de Instagram, Facebook e Twitter/X
- Efeito hover com fundo dourado nos ícones

---

## Tecnologias Utilizadas

| Tecnologia | Uso |
|---|---|
| HTML5 | Estrutura semântica da página |
| CSS3 | Estilização, layout e responsividade |
| Google Fonts | Fonte `Roboto` |
| Icons8 | Ícones SVG (busca, carrinho, estrelas, redes sociais) |
| Google Maps Embed API | Mapa na seção de endereço |

> O projeto **não utiliza JavaScript** — é 100% HTML e CSS.

---

## Paleta de Cores

As variáveis CSS estão definidas em `:root`:

```css
:root {
    --main-color: #d3ad7f;   /* Dourado/caramelo — cor de destaque */
    --black:      #13131a;   /* Preto azulado — fundos de cards */
    --bg:         #010103;   /* Preto quase puro — fundo geral */
    --border:     0.1rem solid rgba(255, 255, 255, 0.3); /* Borda sutil */
}
```

O tema é **dark** com detalhes em **dourado**, reforçando a identidade visual de uma cafeteria premium.

---

## Como Executar

Por ser um projeto estático, não há dependências ou build necessários.

**Opção 1 — Abrir diretamente no navegador:**

```bash
# Clone ou extraia os arquivos
# Abra o arquivo index.html no seu navegador
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

**Opção 2 — Servidor local (recomendado para evitar problemas com CORS):**

```bash
# Com Python 3
python -m http.server 3000

# Com Node.js (npx)
npx serve .

# Acesse em: http://localhost:3000
```

---

## Melhorias Futuras

- [ ] Adicionar JavaScript para navegação ativa no scroll
- [ ] Tornar o menu funcional em mobile
- [ ] Implementar responsividade completa para o header e hero
- [ ] Conectar o botão "Adicionar ao carrinho" a uma lógica de e-commerce
- [ ] Adicionar animações de entrada nas seções ao rolar a página
- [ ] Preencher a seção `#contact` (referenciada no nav, mas não implementada)
- [ ] Substituir nomes genéricos dos itens do menu por nomes reais dos produtos

---

## Autor

Desenvolvido por Paulo André Silva de Lima, como projeto de estudo de front-end.

> Feito com desempenho e dedicação.
