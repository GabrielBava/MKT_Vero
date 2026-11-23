---
name: competitor-teardown
description: Autópsia de concorrentes. Analisa páginas de vendas, anúncios ativos (Meta Ad Library, TikTok Creative Center, Google Ads Transparency Center, LinkedIn Ad Library), perfis e posts usando busca web, leitura de páginas e conectores MCP de scraping, e extrai gancho, promessa e Big Idea, estrutura da oferta, mecanismo único, provas, objeções quebradas, funil, sinais de performance e brechas de mercado. Use sempre que precisar analisar, comparar ou estudar concorrentes, benchmarks, referências de mercado, anúncios de terceiros ou encontrar oportunidades de posicionamento.
---

# Competitor Teardown · Autópsia de Concorrentes

## Princípio

Concorrente não é para ser copiado: é para ser **lido**. O teardown responde a três perguntas:
1. **O que está funcionando para eles** (e por quê)?
2. **O que está saturado** (todo mundo fala igual)?
3. **Onde está a brecha** que a nossa marca pode ocupar com credibilidade?

## Ética e Limites (inegociáveis)

- Use apenas informação **pública**. Não faça login em contas de terceiros, não contorne paywall, não se passe por cliente.
- **Não copie** textos, roteiros ou criativos literalmente. Extraia o princípio e adapte à voz da marca.
- Registre **fonte e data** de cada evidência.
- Separe sempre `[FATO]` (observado) de `[INFERÊNCIA]` (sua interpretação).
- Não use marca, nome ou imagem do concorrente em peças da nossa marca.

## Ferramentas

| Fonte | Como acessar | O que extrair |
|---|---|---|
| Busca web | WebSearch | Páginas de vendas, entrevistas, reviews, menções, preços |
| Leitura de páginas | WebFetch (ou MCP de scraping, se configurado: Firecrawl, Apify, Bright Data etc.) | Copy completa, estrutura, oferta, FAQ |
| Meta Ad Library | `https://www.facebook.com/ads/library/` (busca pelo nome da página) | Anúncios ativos, data de início, variações, plataformas |
| TikTok Creative Center | `https://ads.tiktok.com/business/creativecenter/` | Anúncios em alta por nicho, ganchos |
| Google Ads Transparency Center | `https://adstransparency.google.com/` | Anúncios de Search, YouTube e Display |
| LinkedIn Ad Library | `https://www.linkedin.com/ad-library/` | Anúncios B2B |
| Perfis sociais | WebFetch do perfil público / prints fornecidos pelo usuário | Formatos, frequência, posts com mais engajamento |
| Reclamações e reviews | Reclame Aqui, Google Reviews, comentários públicos | Insatisfações, promessas quebradas |

Se uma página exigir login ou bloquear a leitura automática, registre `acesso bloqueado` e peça ao Chefe prints ou exports do usuário. Nunca invente o conteúdo que não conseguiu ver.

---

## Passo 1 · Escopo

| Campo | Definição |
|---|---|
| Pergunta de negócio | ex.: "Por que o concorrente X está crescendo em anúncios?" |
| Concorrentes (até 5 por rodada) | classificar: **direto** (mesma solução, mesmo público), **indireto** (outra solução, mesmo problema), **aspiracional** (referência de execução, outro nicho) |
| Canais a analisar | páginas, anúncios, Instagram, YouTube, TikTok, e-mail (se houver acesso a newsletter pública) |
| Período | ex.: anúncios ativos nos últimos 90 dias |

## Passo 2 · Coleta (Log de Evidências)

| ID | Concorrente | Tipo de ativo | URL | Data da coleta | Observação |
|---|---|---|---|---|---|
| E01 | ... | Página de vendas | ... | AAAA-MM-DD | ... |
| E02 | ... | Anúncio (Meta) | ... | AAAA-MM-DD | Ativo desde AAAA-MM-DD |

## Passo 3 · Dissecação em 8 Camadas (por ativo relevante)

| # | Camada | Perguntas |
|---|---|---|
| 1 | **Gancho** | Qual é a abertura (texto e visual)? Que motor usa (quebra de padrão, curiosidade, contraintuitivo, especificidade — ver `hook-engineering`)? |
| 2 | **Promessa / Big Idea** | Qual o resultado prometido? Em quanto tempo? Sem qual sacrifício? Qual a ideia central que embala tudo? |
| 3 | **Mecanismo único** | Tem nome? Como explicam por que funciona? É crível? |
| 4 | **Estrutura da oferta** | Produto, formato, preço, parcelamento, bônus, garantia, escassez/urgência, ancoragem de valor |
| 5 | **Provas** | Que tipos (números, depoimentos, cases, autoridade, demonstração)? Quantas? Qualidade e especificidade? |
| 6 | **Objeções quebradas** | Quais objeções aparecem respondidas (FAQ, copy, garantia)? Quais ficam sem resposta? |
| 7 | **Consciência e sofisticação** | Para qual nível de consciência a peça fala? Em que estágio de sofisticação o concorrente opera? |
| 8 | **Funil e CTA** | Para onde o anúncio leva (captura, VSL, checkout, Direct, WhatsApp, webinar)? Quantas etapas até a compra? |

## Passo 4 · Sinais de Performance (indícios, não certezas)

| Sinal | Leitura provável |
|---|---|
| Anúncio ativo há mais de 30 dias | Provável vencedor (ninguém paga por muito tempo o que não converte) |
| Várias variações do mesmo conceito | Conceito validado, em fase de escala |
| Mesmo ângulo reaparecendo em formatos diferentes | Ângulo central da estratégia |
| Comentários de compradores reais (não bots) | Prova de tração |
| Frequência de lançamentos / promoções | Dependência de picos de venda |
| Mudança recente de preço ou oferta | Teste ou problema de conversão |

Marque todos como `[INFERÊNCIA]`.

## Passo 5 · Matriz Comparativa

| Camada | Concorrente A | Concorrente B | Concorrente C | Nossa marca (hoje) |
|---|---|---|---|---|
| Gancho dominante | | | | |
| Promessa | | | | |
| Mecanismo | | | | |
| Preço / oferta | | | | |
| Garantia | | | | |
| Provas | | | | |
| Funil | | | | |
| Tom de voz | | | | |

## Passo 6 · Brechas de Mercado

Procure 7 tipos de brecha:

| Tipo de brecha | Pergunta |
|---|---|
| Promessa não feita | Que resultado o ICP deseja e ninguém promete (com credibilidade)? |
| Público ignorado | Que segmento ninguém está falando diretamente? |
| Objeção não respondida | Qual objeção do ICP (`icp-e-publico-alvo.md` §8) ninguém quebra? |
| Mecanismo não explicado | Todos prometem o mesmo sem explicar como? |
| Formato / canal subexplorado | Que formato ou canal ninguém usa bem? |
| Tom saturado | Todos falam igual? Há espaço para uma voz diferente (a nossa)? |
| Insatisfação dos clientes deles | O que os clientes dos concorrentes reclamam (reviews, Reclame Aqui, comentários)? |

## Passo 7 · Recomendações

Três listas, cada item com hipótese pronta para o registro:

- **Adaptar** (princípio que funciona, traduzido para a nossa marca): `Se usarmos <princípio> com <nossa prova>, esperamos <métrica>, porque <evidência do teardown>.`
- **Evitar** (o que está saturado ou arrisca a marca).
- **Atacar** (brecha + ângulo sugerido + teste proposto).

---

## Formato de Saída (obrigatório)

```
## TEARDOWN — <mercado / concorrentes> — AAAA-MM-DD

### Resumo executivo (5 bullets)
- ...

### Escopo
<tabela do Passo 1>

### Log de evidências
<tabela do Passo 2>

### Teardown por concorrente
#### <Concorrente A> (direto | indireto | aspiracional)
| Camada | Achado | Evidência (ID) | [FATO]/[INFERÊNCIA] |
|---|---|---|---|
| 1. Gancho | ... | E02 | [FATO] |
...
Sinais de performance: ...

#### <Concorrente B> ...

### Matriz comparativa
<tabela do Passo 5>

### Brechas de mercado
<tabela: brecha | evidência | tamanho da oportunidade (alta/média/baixa) | ângulo sugerido>

### Recomendações
**Adaptar:** ...
**Evitar:** ...
**Atacar:** ...

### Hipóteses propostas
- Se ..., então ..., porque ...

### Limitações
- Acessos bloqueados, dados não verificáveis, período curto etc.
```

---

## Checklist Final

- [ ] Toda evidência tem URL e data
- [ ] Fatos e inferências separados
- [ ] As 8 camadas analisadas para cada concorrente relevante
- [ ] Matriz comparativa inclui a nossa marca
- [ ] Pelo menos 3 brechas identificadas, com evidência
- [ ] Recomendações viram hipóteses testáveis
- [ ] Nenhum texto de concorrente copiado para uso em peças
