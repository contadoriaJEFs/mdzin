# ✏️ Editor e Leitor Markdown

Um editor e leitor de Markdown **100% client-side**, feito em um único arquivo HTML. Não precisa de instalação, servidor, back-end ou dependências externas — basta abrir no navegador.

> **Importante:** quando você carrega arquivos `.md` nesta ferramenta, **eles não são enviados para nenhum servidor**. Todo o processamento acontece localmente, dentro do seu navegador. Veja a seção [Privacidade e funcionamento offline](#-privacidade-e-funcionamento-offline) para entender por quê.

---

## 📋 Índice

- [Demonstração](#-demonstração)
- [Funcionalidades](#-funcionalidades)
- [Como usar](#-como-usar)
- [Atalhos de teclado](#-atalhos-de-teclado)
- [Carregando vários arquivos](#-carregando-vários-arquivos)
- [Barra lateral de documentos](#-barra-lateral-de-documentos)
- [Modo Leitura](#-modo-leitura)
- [Leitura por voz](#-leitura-por-voz)
- [Salvamento automático](#-salvamento-automático)
- [Sintaxe Markdown suportada](#-sintaxe-markdown-suportada)
- [Privacidade e funcionamento offline](#-privacidade-e-funcionamento-offline)
- [Publicando no GitHub Pages](#-publicando-no-github-pages)
- [Compatibilidade com navegadores](#-compatibilidade-com-navegadores)
- [Estrutura do projeto](#-estrutura-do-projeto)
- [Limitações conhecidas](#-limitações-conhecidas)
- [Ideias futuras](#-ideias-futuras)
- [Licença](#-licença)

---

## 🎬 Demonstração

Abra o arquivo `index.html` diretamente no navegador (duplo clique) ou publique no GitHub Pages — funciona do mesmo jeito.

---

## ✨ Funcionalidades

### Editor
- **Edição ao vivo** com prévia renderizada em tempo real
- **Atalhos de teclado** para negrito, itálico, link e salvar
- **Contador de palavras, caracteres e tempo estimado de leitura** no rodapé
- **Indicador de salvamento** (● não salvo / ✔ salvo) ao lado do nome do arquivo
- **Salvamento automático** dos documentos no `localStorage` do navegador

### Documentos
- **Carregamento de múltiplos arquivos** `.md`, `.markdown` e `.txt` de uma só vez
- **Barra lateral de navegação** com busca e lista de documentos
- **Renomear com duplo-clique** no nome do arquivo
- **Remover individualmente** com o botão ✕ em cada item
- **Exportar tudo concatenado** em um único `.md`
- **Baixar o documento ativo** como `.md`

### Leitura
- **Modo Leitura** que oculta o editor e mantém a navegação lateral
- **Leitura por voz** (Text-to-Speech) com controle de velocidade e escolha de voz
- **Copiar prévia renderizada** para a área de transferência
- **Imprimir / salvar como PDF** (imprime apenas a prévia, sem interface)

### Técnico
- **Sem dependências** — HTML + CSS + JS puros, em um único arquivo
- **Sem servidor** — funciona offline depois do primeiro carregamento
- **Sem envio de dados** — tudo acontece no seu navegador

---

## 🚀 Como usar

### Opção 1 — Localmente

1. Salve o arquivo como `index.html`.
2. Dê duplo clique nele.
3. Pronto. Tudo funciona offline.

### Opção 2 — GitHub Pages

1. Faça upload do `index.html` para um repositório.
2. Vá em **Settings → Pages → Branch: main / root**.
3. Acesse `https://<seu-usuário>.github.io/<repositório>/`.

---

## ⌨️ Atalhos de teclado

Com o cursor no editor:

| Atalho | Ação |
|---|---|
| `Ctrl+B` (ou `Cmd+B`) | Envolve a seleção com `**` (negrito). Se já estiver em negrito, remove. |
| `Ctrl+I` (ou `Cmd+I`) | Envolve a seleção com `*` (itálico). Se já estiver em itálico, remove. |
| `Ctrl+K` (ou `Cmd+K`) | Abre prompt para inserir um link `[texto](url)`. Usa a seleção como texto. |
| `Ctrl+S` (ou `Cmd+S`) | Baixa o documento ativo como `.md`. |
| `Esc` | Interrompe a leitura por voz em andamento. |

**Dicas:**
- Sem seleção, `Ctrl+B` insere `****` e coloca o cursor no meio.
- Com uma palavra selecionada, `Ctrl+B` aplica e desaplica (toggle).
- O `Ctrl+S` do navegador é interceptado — não abre o diálogo "Salvar página".

---

## 📂 Carregando vários arquivos

Duas formas:

| Método | Como fazer |
|---|---|
| **Seletor de arquivos** | Clique na caixa azul. Na janela do sistema, segure `Ctrl` (Windows/Linux) ou `Cmd` (macOS) para selecionar vários `.md` ao mesmo tempo. |
| **Arrastar e soltar** | Selecione vários `.md` no Explorer/Finder e solte todos juntos sobre a caixa tracejada. |

**Comportamento:**
- Os arquivos são **adicionados** à lista (não substituem os existentes).
- O primeiro arquivo carregado remove automaticamente o exemplo de boas-vindas.
- A ordem respeita o que o sistema operacional entrega no `FileList`.
- Use **🗑️ Limpar** para recomeçar do zero.

---

## 📚 Barra lateral de documentos

A barra lateral esquerda concentra o gerenciamento dos arquivos:

### Busca
Digite no campo **"🔍 Buscar por nome..."** para filtrar a lista em tempo real. O contador vira `X / Y` (visíveis / total) quando há filtro ativo.

### Navegação
Clique em qualquer item para carregá-lo no editor e na prévia. O item ativo fica destacado em azul.

### Renomear
**Duplo-clique** no nome do arquivo → vira campo editável → `Enter` salva, `Esc` cancela. A extensão fica pré-selecionada para facilitar.

### Remover um item
Clique no **✕** ao lado do nome → confirmação → remove da lista. Se era o documento ativo, o anterior é selecionado.

### Ações do rodapé

| Botão | Ação |
|---|---|
| **📦 Exportar** | Baixa **todos** os documentos em um único `.md`, separados por `---` e com o nome de cada um como título. |
| **🗑️ Limpar** | Remove todos os documentos da lista (pede confirmação). |

---

## 📖 Modo Leitura

Clique em **📖 Modo Leitura** no topo. O layout muda para:
