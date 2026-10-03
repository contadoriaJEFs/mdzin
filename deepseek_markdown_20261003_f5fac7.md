# ✏️ Editor e Leitor Markdown

Um editor e leitor de Markdown **100% client-side**, feito em um único arquivo HTML. Não precisa de instalação, servidor, back-end ou dependências externas — basta abrir no navegador.

> **Importante:** quando você carrega arquivos `.md` nesta ferramenta, **eles não são enviados para nenhum servidor**. Todo o processamento acontece localmente, dentro do seu navegador. Veja a seção [Privacidade e funcionamento offline](#-privacidade-e-funcionamento-offline) para entender por quê.

---

## 📋 Índice

- [Demonstração](#-demonstração)
- [Funcionalidades](#-funcionalidades)
- [Como usar](#-como-usar)
- [Carregando vários arquivos](#-carregando-vários-arquivos)
- [Modo Leitura](#-modo-leitura)
- [Leitura por voz](#-leitura-por-voz)
- [Atalhos e sintaxe Markdown suportada](#-sintaxe-markdown-suportada)
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

- **Editor ao vivo** com prévia renderizada em tempo real
- **Carregamento de múltiplos arquivos** `.md`, `.markdown` e `.txt` de uma só vez
- **Barra lateral de navegação** entre os documentos carregados
- **Modo Leitura** que oculta o editor e mantém a navegação lateral
- **Leitura por voz** (Text-to-Speech) com controle de velocidade e escolha de voz
- **Exportar** o documento ativo como `.md`
- **Imprimir / salvar como PDF** (imprime apenas a prévia)
- **Sincronização automática** — edições são mantidas ao trocar de documento
- **Drag & drop** — arraste um ou vários arquivos direto para a área tracejada
- **Sem dependências** — HTML + CSS + JS puros, em um único arquivo

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
- Use **🗑️ Limpar lista** para recomeçar do zero.

---

## 📖 Modo Leitura

Clique em **📖 Modo Leitura** no topo. O layout muda para:
