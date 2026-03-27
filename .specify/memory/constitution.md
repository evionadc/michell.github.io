<!--
Sync Impact Report:
- Version change: 1.0.0 -> 1.1.0
- Modified principles:
  - Simplicidade -> Storytelling Enxuto
  - Acessibilidade -> Acessibilidade Como Base
  - Conteudo em Primeiro Lugar -> Conteudo Guiado por Narrativa
- Added principles:
  - Identidade Visual Reutilizavel
  - Publicacao Estatica e Manutencao Leve
- Added sections:
  - Experience Standards
  - Content Workflow
- Removed sections: None
- Templates requiring updates:
  - ✅ reviewed only: .specify/templates/plan-template.md
  - ✅ reviewed only: .specify/templates/spec-template.md
  - ✅ reviewed only: .specify/templates/tasks-template.md
  - ✅ updated: README.md
- Follow-up TODOs: None
-->

# Michell Talks Constitution

## Core Principles

### Storytelling Enxuto
Cada pagina e cada slide MUST existir para reforcar uma mensagem principal.
Texto longo, blocos densos e ornamentacao sem funcao MUST ser evitados.
Rationale: apresentacoes eficazes dependem de compreensao rapida e progressao
clara da narrativa.

### Conteudo Guiado por Narrativa
Cada palestra MUST nascer com uma estrutura identificavel: abertura, tensao ou
contexto, desenvolvimento e fechamento. Placeholders de conteudo MUST deixar
claro onde entram titulo, tese, exemplos, evidencias e chamada final.
Rationale: o repositorio precisa ficar pronto para receber conteudo iterativo sem
perder consistencia entre palestras.

### Identidade Visual Reutilizavel
Home, decks e componentes compartilhados MUST usar tokens visuais coerentes de
tipografia, espacamento, contraste e destaque. Variacoes por palestra MAY
acontecer, desde que preservem a mesma familia visual e o mesmo padrao de
navegacao.
Rationale: o site deve transmitir marca pessoal consistente sem sacrificar a
individualidade de cada tema.

### Acessibilidade Como Base
Todo layout MUST manter contraste legivel, navegacao por teclado, estrutura
semantica e comportamento responsivo em desktop e mobile. Slides MUST evitar
depender somente de cor para comunicar hierarquia ou estado.
Rationale: palestras precisam funcionar tanto ao vivo quanto no acesso posterior
via GitHub Pages, em diferentes telas e contextos.

### Publicacao Estatica e Manutencao Leve
O projeto MUST permanecer compativel com hospedagem estatica no GitHub Pages,
com assets locais, caminhos relativos e minimo de dependencias operacionais.
Qualquer adicao tecnica SHOULD justificar claramente o ganho sobre a simplicidade
de manutencao.
Rationale: a velocidade de publicacao e a baixa friccao operacional sao parte do
produto.

## Experience Standards

O site MUST apresentar claramente quem e Michell, quais palestras estao
disponiveis e como iniciar cada apresentacao. A home SHOULD funcionar como um
catalogo editorial, nao apenas como uma lista de links. Os decks MUST compartilhar
elementos recorrentes de abertura, divisao de secoes e encerramento para reduzir
o custo de criar novas apresentacoes.

## Content Workflow

Novas palestras SHOULD ser criadas a partir de uma estrutura reutilizavel.
Conteudos em rascunho MUST ser marcados de forma explicita para distinguir
template de material final. Mudancas de narrativa, layout ou identidade visual
MUST considerar impacto simultaneo na home e nos decks existentes.

## Tecnologias Utilizadas

O projeto usa HTML, CSS e JavaScript estaticos com Reveal.js para os decks.
Hospedagem e distribuicao acontecem via GitHub Pages, sem etapa obrigatoria de
build.

## Processo de Desenvolvimento

Mudancas MUST priorizar edicao direta dos arquivos estaticos do repositorio.
Antes de publicar, toda entrega SHOULD verificar:

- consistencia visual entre home e decks
- legibilidade em viewport desktop e mobile
- navegacao e links principais funcionando
- placeholders claramente identificados quando o conteudo final ainda nao existir

## Governance

Esta constituicao prevalece sobre preferencias locais de implementacao. Toda
alteracao MUST registrar impacto na experiencia, manutencao estatica e fluxo de
conteudo. Versionamento segue semver:

- MAJOR: remocao ou redefinicao incompatível de principios
- MINOR: novo principio, nova secao normativa ou expansao material de regras
- PATCH: esclarecimentos, redacao e ajustes nao normativos

Revisoes de conformidade MUST acontecer sempre que layout compartilhado,
estrutura de decks ou fluxo editorial forem alterados.

**Version**: 1.1.0 | **Ratified**: 2026-03-27 | **Last Amended**: 2026-03-27
