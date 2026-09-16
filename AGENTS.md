# Diretrizes para Agentes de IA (`AGENTS.md`)

> **Guia de Execução e Protocolo de Trabalho**  
> *Este documento define o fluxo de trabalho, as normas obrigatórias e os padrões de qualidade para qualquer agente de IA que atuar nesta base de código. O repositório abriga o ecossistema integrado de RPG de Ficção Científica publicado via Quartz / Obsidian, composto pelo compêndio canônico de **Stars Without Number: Edição Revisada (Deluxe)** (*Inúmeras Estrelas*) e a ambientação expandida de **Coriolis** (*O Horizonte: O Terceiro Horizonte & A Grande Escuridão*).*

---

## 1. Estrutura de Diretórios e Documentação

### Pasta `documentos/` (Glossários Oficiais e Decisões de Tradução)
* **Objetivo:** Pasta oficial que centraliza os dicionários terminológicos, escolhas de tradução e convenções estilísticas do projeto.
* **Decisões sobre Tradução:** Consulte [documentos/decisoes-sobre-traducao.md](file:///home/caio/Documentos/github/coriolis/documentos/decisoes-sobre-traducao.md) para verificar as diretrizes de localização, convenções de regras e tom de publicação adotados.
* **Glossário Stars Without Number:** Consulte [documentos/Glossário-stars-without-number.md](file:///home/caio/Documentos/github/coriolis/documentos/Glossário-stars-without-number.md) para a correspondência canônica de mais de 500 termos mecânicos e de cenário de *Stars Without Number*.
* **Glossário O Horizonte (Coriolis / YZE):** Consulte [documentos/glossario-termos.md](file:///home/caio/Documentos/github/coriolis/documentos/glossario-termos.md) para a padronização oficial de regras da Year Zero Engine (v2) e elementos de ambientação do Terceiro Horizonte e da Grande Escuridão.

### Pasta `docs/` (Auditoria Técnica e Organização)
* **Painel de Auditoria de Completude:** Consulte o arquivo [docs/auditoria.md](file:///home/caio/Documentos/github/coriolis/docs/auditoria.md) para verificar a contagem de palavras, quantidade de arquivos e o status de revisão exaustiva do projeto (100% concluído para os 18 capítulos de SWN Deluxe).
* **Organização Modular de Capítulos:** Consulte [docs/organizacao-de-capitulos-e-arquivos.md](file:///home/caio/Documentos/github/coriolis/docs/organizacao-de-capitulos-e-arquivos.md) para diretrizes de divisão temática, arquivos Hub e nomenclatura de pastas e subpastas.

### Pasta `content/` (Conteúdo Oficial de Publicação - Quartz)
* **Objetivo:** Diretório base de onde o Quartz extrai o conteúdo da Wiki e compêndio digital.
* **Estrutura de Seções:**
  * `content/index.md`: Hub e índice principal de navegação da raiz da Wiki (deve conter no frontmatter YAML `title: Introdução` ou título equivalente da página inicial).
  * `content/1. Inúmeras Estrelas/`: Compêndio integral e exaustivo de *Stars Without Number: Edição Revisada (Deluxe)*, dividido em:
    * `1.1. Conteúdo do Jogador/` (Capítulos 2 a 6: Criação de Personagem, Psionismo, Sistemas, Equipamento e Veículos, Naves Espaciais).
    * `1.2. Conteúdo do Mestre/` (Capítulos 7 a 18: A História do Espaço, Criação de Setor, Criação de Aventuras, Xenobestiário, Facções, Recursos do Mestre, e Suplementos Deluxe 13 a 18).
  * `content/2. O Horizonte/`: Ambientação e expansão de *Coriolis* (O Terceiro Horizonte e A Grande Escuridão), dividida em pastas temáticas como `Espécies/`, `Locais Importantes/`, `Facções/` e outros tópicos de cenário.
* **Regras Estritas para `content/`:**
  * **Nomenclatura (Quartz):** NUNCA utilize hífens (`-`) para separar palavras no nome de pastas dentro de `content/`. Utilize a grafia oficial com acentos e espaços (ex: `content/1. Inúmeras Estrelas/1.1. Conteúdo do Jogador/2. Criação de Personagem/` ou `content/2. O Horizonte/Locais Importantes/`).
  * **Links Internos (Obsidian):** Utilize obrigatoriamente a sintaxe do Obsidian: `[[Caminho da Pasta/Nome do Arquivo|Texto Alternativo]]`.
  * **Proibido ASCII Art:** NUNCA crie tabelas usando caracteres decorativos de desenho de linhas (como `┌──┐`), pois elas corrompem a renderização do Quartz. Utilize exclusivamente tabelas em Markdown padrão GFM (`| Coluna |`).
  * **Proibido Uso de Emojis:** É terminantemente proibido o uso de emojis em qualquer título, marcador de lista, tabela ou corpo de texto em `content/`.
  * **Texto Puro de Publicação (Sem Metalinguagem de Chat):** Nenhum arquivo de `content/` deve conter saudações, introduções ou notas de IA (como *"Claro, aqui está..."*, *"Eu resumiria a civilização assim:"*). O conteúdo deve ser redigido diretamente como prosa editorial imersiva e formal de livro de RPG.

### Pasta `dev/` (Scripts, Automações, Campanhas e Fichas)
* **Objetivo:** Espaço de trabalho técnico, processamento de dados e suporte a jogo.
* **Execução de Scripts Python:** Sempre crie, edite e execute scripts de automação, auditoria ou extração de texto a partir da pasta `dev/` (evitando one-liners complexos no terminal).
* **Estrutura Interna de Suporte:**
  * `dev/3. Campanha/`: Diários de bordo, fichas de nave de campanha, histórico de missões e gerenciamento de NPCs.
  * `dev/5. Fichas/`: Modelos de fichas (Personagem, Nave, Mech, Veículo).
  * `dev/templates/`: Modelos e esqueletos rápidos para criação de planetas, NPCs e sessões.
  * Análises conceituais e mecânicas de integração (`dev/escopo-e-planejamento.md`, `dev/conflitos-e-solucoes-mecanicas.md`).

### Pasta `livros/` (Material Fonte e Referências Originais)
* **Objetivo:** Repositório dos PDFs originais de referência (`Stars Without Number: Revised Deluxe Edition`, manuais de Coriolis, etc.) para extração textual e conferência de regras.

---

## 2. Regras de Estilo, Terminologia e Qualidade

* **PROIBIDO USO DE EMOJIS:** É estritamente proibido o uso de emojis em títulos, marcadores de lista, tabelas ou no meio do texto em **qualquer arquivo** deste repositório.
* **ESTADO DE STARS WITHOUT NUMBER: 100% CONCLUÍDO E AUDITADO:**
  * Todos os 18 capítulos de *Stars Without Number: Edição Revisada (Deluxe)* foram integralmente traduzidos, modularizados e auditados em 108 arquivos modulares (~227.000 palavras em PT-BR), atingindo 99,5% de paridade com o texto original sem resumos.
  * **Diretriz de Não-Regressão:** Qualquer intervenção nos arquivos de `content/1. Inúmeras Estrelas/` é estritamente de manutenção, correção cirúrgica de links internos, erratas pontuais ou ajuste fino de tabelas. É expressamente proibido resumir, sintetizar, parafrasear ou podar conteúdos já traduzidos.
* **PADRÃO EXAUSTIVO PARA NOVOS CONTEÚDOS (O HORIZONTE / CORIOLIS):**
  * Toda produção de novos conteúdos narrativos ou regras para `content/2. O Horizonte/` deve manter o mesmo rigor e profundidade: descrições detalhadas, riqueza de cenário, parâmetros mecânicos completos e ausência total de sínteses simplistas.
* **CONSULTA OBRIGATÓRIA AOS GLOSSÁRIOS:**
  * Todos os termos técnicos, perícias, classes, atributos, naves, equipamentos e elementos de cenário devem seguir rigorosamente as decisões de [documentos/decisoes-sobre-traducao.md](file:///home/caio/Documentos/github/coriolis/documentos/decisoes-sobre-traducao.md), [documentos/Glossário-stars-without-number.md](file:///home/caio/Documentos/github/coriolis/documentos/Glossário-stars-without-number.md) e [documentos/glossario-termos.md](file:///home/caio/Documentos/github/coriolis/documentos/glossario-termos.md).
  * Ao introduzir conceitos mecânicos novos com termo de origem anglófona consagrado, insira o termo original em inglês entre parênteses na sua primeira ocorrência (ex.: *Dado de Fray (Fray Die)*, *PE (Pontos de Escuridão - Darkness Points)*).

---

## 3. Protocolo de Execução para Agentes de IA

1. **Leitura e Contextualização Prévia:** Antes de criar, editar ou revisar arquivos, verifique as diretrizes em `documentos/` e o estado atual em `docs/auditoria.md` e `docs/organizacao-de-capitulos-e-arquivos.md`.
2. **Modularização e Arquivos Hub:** Sempre que criar ou reestruturar um módulo extenso, crie uma pasta temática com nome descritivo (sem hífens), um arquivo Hub de introdução/sumário e subarquivos numerados e focados.
3. **Validação de Sintaxe e Links:**
   * Certifique-se de que todos os links internos utilizam a sintaxe `[[Pasta/Arquivo|Texto]]` com caminhos válidos.
   * Valide que todas as tabelas estão em formato GFM puro e que caracteres especiais (como `|` dentro de links ou textos de tabela) sejam devidamente escapados (`\|`).
   * Garanta que nenhum emoji ou arte ASCII foi introduzido.
4. **Trabalho Técnico Isolado em `dev/`:** Scripts de apoio, extrações de PDFs e códigos de checagem devem sempre ser salvos e executados na pasta `dev/`, mantendo a raiz do projeto e a pasta `content/` limpas de arquivos temporários.
5. **Controle de Versão (Git):**
   * Realize commits claros com mensagens no padrão Conventional Commits (`feat:`, `fix:`, `docs:`, `refactor:`) quando o fluxo de trabalho exigir commit.
   * **Atenção:** Se o usuário instruir explicitamente para **não commitar** ao finalizar a tarefa, **NÃO** realize `git commit` nem execute `git push`. Respeite a instrução do usuário.

---

> **AVISO CRÍTICO:** Qualquer agente que iniciar uma tarefa neste repositório **DEVE** ler este documento (`AGENTS.md`) e consultar os glossários em [documentos/](file:///home/caio/Documentos/github/coriolis/documentos/) e a auditoria em [docs/auditoria.md](file:///home/caio/Documentos/github/coriolis/docs/auditoria.md) antes de criar ou modificar qualquer arquivo.
