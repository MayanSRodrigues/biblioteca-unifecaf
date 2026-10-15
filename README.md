# Biblioteca Digital UniFECAF

Primeira interface web da biblioteca digital da UniFECAF, desenvolvida com **HTML e CSS puros** (sem frameworks, templates ou JavaScript) a partir de um protótipo de baixa fidelidade.

Projeto acadêmico da disciplina **Design Web**, do curso de Análise e Desenvolvimento de Sistemas.

**Site publicado:** https://mayansrodrigues.github.io/biblioteca-unifecaf/

## Sobre o projeto

A UniFECAF está criando uma biblioteca digital para facilitar o acesso dos estudantes a livros, materiais acadêmicos e conteúdos de apoio. Este repositório contém a primeira versão do site, com foco em uma experiência simples, **responsiva** e **acessível**, alinhada à identidade visual da instituição.

## Seções da página

O site mantém a organização do protótipo fornecido:

1. **Menu** fixo no topo, com navegação por âncoras (Biblioteca, Livros, Unidades, Contatos)
2. **Banner** principal
3. **Sobre a nossa biblioteca**: texto, imagem e texto lado a lado, mais uma galeria de 4 imagens
4. **Segundo banner**
5. **Nossos livros**: 6 cartões em grade, com imagem, descrição e botão "Saiba mais"
6. **As unidades**: 3 blocos de imagem com texto
7. **Contatos**: informações de atendimento e imagem
8. **Rodapé**

## Tecnologias

- HTML5 semântico (`header`, `nav`, `main`, `section`, `article`, `address`, `footer`)
- CSS3 (Grid, Flexbox, variáveis CSS, `clamp()`, media queries)
- Fonte [Poppins](https://fonts.google.com/specimen/Poppins) (Google Fonts)

## Estrutura de pastas

```
biblioteca-unifecaf/
├── index.html
├── css/
│   └── style.css
└── assets/
    └── imagens/
```

## Como executar localmente

Não há dependências nem etapa de build.

1. Clone o repositório:
   ```bash
   git clone https://github.com/MayanSRodrigues/biblioteca-unifecaf.git
   ```
2. Abra o arquivo `index.html` em qualquer navegador.

Se preferir, use a extensão **Live Server** do VS Code para atualizar a página automaticamente ao salvar.

## Identidade visual

As cores principais foram extraídas do material institucional da UniFECAF, e as demais são derivadas ou neutras. Todas ficam centralizadas em variáveis CSS (`:root`).

| Cor | Hex | Uso |
|---|---|---|
| Azul UniFECAF | `#0060A8` | Títulos, links e destaques |
| Verde UniFECAF | `#10B060` | Botões, linhas decorativas e detalhes |
| Azul-marinho | `#0B2545` | Menu, seção Unidades e rodapé |
| Azul claro | `#EAF2FA` | Fundo da seção Nossos livros |
| Cinza claro | `#F4F6F9` | Fundo da seção Contatos |

O contraste de cada combinação de texto foi verificado segundo a WCAG 2.1 (mínimo de 4,5:1). Por isso o verde não é usado como cor de texto sobre fundo branco, e os botões verdes têm texto escuro.

## Responsividade

O CSS parte do layout de computador e simplifica conforme a tela diminui:

| Largura até | O que muda |
|---|---|
| 900 px | "Sobre" em coluna única; livros em 2 colunas; contatos em coluna única |
| 700 px | Galeria em 2 colunas; unidades empilhadas |
| 600 px | Livros em 1 coluna; menu centralizado e compacto |
| 380 px | Menu ainda mais compacto, para caber em uma linha |

Além das media queries, a página usa medidas relativas, `clamp()` e `object-fit: cover` para evitar texto cortado, imagens distorcidas e rolagem horizontal.

## Acessibilidade

- Idioma declarado (`lang="pt-BR"`) e hierarquia de títulos sem saltos
- Texto alternativo em todas as imagens (vazio no banner decorativo)
- Foco visível no teclado e link "Pular para o conteúdo"
- Rótulos `aria-label` no menu e nos botões "Saiba mais"
- Respeito à preferência de movimento reduzido (`prefers-reduced-motion`)

## Limitações conhecidas

- Os botões "Saiba mais" apontam para a própria seção, pois ainda não existem páginas de detalhe.
- Os nomes dos livros e os dados de contato (e-mail, telefone e horário) são **ilustrativos**.
- As imagens não foram otimizadas para web.
- Não foram feitos testes com leitores de tela.

## Créditos

- Imagens: bancos de imagens gratuitos, como Unsplash e Pexels.
- Protótipo e identidade visual: UniFECAF.

## Autor

**Mayan** — [@MayanSRodrigues](https://github.com/MayanSRodrigues)
