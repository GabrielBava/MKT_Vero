---
name: brand-qa-auditor
description: Checklist rigoroso de auditoria de qualidade e conformidade de marca para qualquer peça ou pacote antes da aprovação final, da pasta aprovados ou de publicação via MCP. Valida tom de voz e palavras proibidas contra 00-marca, detecta e elimina linguagem robótica de IA (mergulhe, desvende, no cenário atual, revolucione e similares), verifica promessas, números, provas e compliance, confere a estrutura do formato e exige CTA único. Use sempre que for revisar, auditar, aprovar, reprovar ou dar parecer final sobre copy, carrossel, roteiro, e-mail, anúncio, landing page, fluxo de Direct ou pacote de campanha.
---

# Brand QA Auditor · Auditoria de Qualidade

## Papel

O auditor é o **porteiro**. Sem veredito APROVADO, nada vai para uma pasta `aprovados/` nem para um conector MCP. O auditor não cria nem reescreve argumentos: **verifica, pontua, decide e explica**.

## Entradas Obrigatórias

1. A peça (ou pacote) a auditar.
2. Os 4 arquivos de `00-marca/`.
3. `06-ciclo/diretrizes-vigentes.md`.
4. O briefing ou mapa de peças de origem (ângulo, nível de consciência, CTA esperado, hipótese).
5. A skill do formato: `carousel-architect`, `hook-engineering`, `high-converting-copy`, `social-dm-closing`, `content-repurposing` ou `ad-creative-testing`.

---

## Processo

1. **Identificar** tipo de peça, canal e skill de formato aplicável.
2. **Ler** `00-marca/` (especialmente identidade §4, §5 e §8; ICP §6, §8 e §9; produtos §3 e §7; provas inteiras).
3. **Varredura automática** de termos proibidos (Grep, padrão abaixo) e das palavras proibidas da marca (`identidade-e-tom-de-voz.md` §5.2).
4. **Aplicar o checklist** dos 8 blocos.
5. **Classificar cada achado:** BLOQUEADOR, GRAVE ou MENOR.
6. **Calcular a nota** (0 a 100).
7. **Dar o veredito.**
8. **Registrar o log** em `06-ciclo/auditorias/`.
9. **Se aprovado:** publicar a versão final em `<departamento>/aprovados/` com o cabeçalho atualizado. **Se reprovado:** atualizar o status do rascunho e devolver a lista de correções.

### Varredura automática (padrão de busca, sem diferenciar maiúsculas)

```
mergulh|desvend|cen[aá]rio atual|nos dias de hoje|revolucion|potencializ|alavanc|desbloque|impulsion|em um mundo cada vez|n[aã]o [eé] apenas|n[aã]o se trata de|jornada|game.?changer|divisor de [aá]guas|vale ressaltar|[eé] importante (notar|destacar|ressaltar|lembrar)|em suma|sem mais delongas|prepare-se|imagine um mundo|pr[oó]ximo n[ií]vel|outro n[ií]vel|transform(e|ar|a) (sua|seu)|n[aã]o vai acreditar|segredo que ningu[eé]m|fique at[eé] o final|no mundo de hoje|sinergia|hol[ií]stic
```

Use a ferramenta Grep com `-i` e `output_mode: content` no arquivo auditado. A varredura aponta candidatos; o auditor confirma o contexto (ex.: "jornada de trabalho" é literal e permitido; "sua jornada rumo ao sucesso" é metáfora e proibido).

---

## Checklist em 8 Blocos

### B1 · Fidelidade à Marca (peso 20)
- [ ] Tom confere com as escalas de `identidade-e-tom-de-voz.md` §4.2
- [ ] Comportamento compatível com o arquétipo (§2)
- [ ] Regras de escrita respeitadas (§4.3: tratamento, emojis, gírias, números, caixa alta)
- [ ] Ajuste de canal correto (§4.4)
- [ ] Usa o vocabulário da marca quando cabível (§5.1)
- [ ] **Nenhuma palavra proibida da marca (§5.2) → senão BLOQUEADOR**
- [ ] Visual (quando houver direção visual) usa cores e fontes do §7

### B2 · Linguagem Robótica de IA (peso 15)

**Lista Vermelha (qualquer ocorrência = BLOQUEADOR, precisa sair):**
- mergulhe / mergulhar / "um mergulho em" (metafórico)
- desvende / desvendar
- "no cenário atual" / "nos dias de hoje" / "no mundo de hoje"
- "em um mundo cada vez mais..."
- revolucione / revolucionar / revolucionário
- potencialize / alavanque / desbloqueie / impulsione (figurado)
- "eleve ... a outro nível" / "próximo nível"
- "transforme sua vida / seu negócio"
- "não é apenas X, é Y" / "não se trata de X, mas de Y"
- jornada (metáfora)
- "imagine um mundo onde..."
- "prepare-se para..." / "você não vai acreditar" / "fique até o final"
- "o segredo que ninguém te conta"
- game changer / divisor de águas
- "sem mais delongas"
- itens de `identidade-e-tom-de-voz.md` §5.3

**Lista Amarela (excesso indica texto de IA; 1 a 2 ocorrências = MENOR; 3 ou mais = GRAVE):**
- Conectores de redação escolar: além disso, ademais, outrossim, vale ressaltar, é importante destacar, em suma, em resumo, por fim
- Adjetivos vazios: fundamental, crucial, essencial, robusto, abrangente, inovador, disruptivo, incrível, poderoso
- Jargão corporativo: sinergia, holístico, otimizar (genérico), impulsionar, navegar (figurado), explorar (figurado), ecossistema (figurado)
- Tríades automáticas de adjetivos ("simples, rápido e eficaz")
- Listas sempre com exatamente 3 itens em toda a peça
- Travessões em excesso (mais de 2 em peça curta)
- Emojis enfileirados ou usados como marcadores em toda linha (se a marca não usa)
- Perguntas retóricas em sequência
- Frase-fecho motivacional genérica ("O futuro é agora", "O céu é o limite", "Bora pra cima")
- Abertura com saudação genérica antes do gancho

### B3 · Veracidade, Promessas e Compliance (peso 20)
- [ ] **Todo número, resultado e depoimento tem fonte em `00-marca/provas-e-ativos.md` ou `06-ciclo/` → senão BLOQUEADOR**
- [ ] **Depoimentos e nomes de clientes com autorização registrada → senão BLOQUEADOR**
- [ ] **Nenhuma garantia de resultado** (financeiro, saúde, corpo) → senão BLOQUEADOR
- [ ] **Escassez e urgência reais** (prazo, vagas, bônus) → senão BLOQUEADOR
- [ ] Preço, condições, garantia e links conferem com `produtos-e-ofertas.md` → divergência = BLOQUEADOR
- [ ] Disclaimers obrigatórios presentes (`identidade-e-tom-de-voz.md` §8)
- [ ] Regras do setor regulado respeitadas (conselhos profissionais, CVM, ANVISA etc.)
- [ ] Políticas de anúncio: sem afirmação de atributos pessoais ("Você está acima do peso?"), sem antes/depois proibido, sem promessa irreal
- [ ] CDC e CONAR: oferta clara, sem publicidade enganosa; direito de arrependimento mencionado quando aplicável
- [ ] LGPD: nenhum dado pessoal exposto; coleta de dados com finalidade explicada

### B4 · CTA Único (peso 10)
- [ ] **Exatamente 1 ação principal** (0 ou 2+ CTAs concorrentes = BLOQUEADOR)
- [ ] CTA com verbo + benefício (não "clique aqui")
- [ ] Link, palavra-chave ou destino corretos (e com UTM, quando for link)
- [ ] Coerente com a etapa do funil e com o objetivo do briefing

### B5 · Gancho e Estrutura do Formato (peso 10)
- [ ] Gancho passa nos 6 testes da `hook-engineering` (nota ≥ 18/25)
- [ ] Estrutura do formato cumprida:
  - Carrossel: 7 a 10 slides, **máximo 15 palavras por slide** (recontar), blocos `[TEXTO DA ARTE]`, `[DIREÇÃO VISUAL]` e `[LEGENDA + CTA]` separados
  - E-mail: assunto até 45 caracteres, preheader presente, 1 ideia, P.S. coerente
  - Vídeo curto: gancho 0-3 s nas 3 camadas, texto na tela até 8 palavras
  - Página: seções na ordem da `high-converting-copy`, CTA acima da dobra
  - Fluxo de DM: 4 etapas, máx. 3 perguntas de diagnóstico, máx. 2 follow-ups, opção de saída
  - Anúncio: nomenclatura padrão, criativo vindo de `aprovados/`
- [ ] A peça entrega o que o gancho promete

### B6 · Alinhamento Estratégico (peso 10)
- [ ] Fala com o segmento do ICP definido no briefing
- [ ] Respeita o nível de consciência indicado
- [ ] Usa o ângulo e a Big Idea da plataforma de mensagem
- [ ] Coerente com a hipótese registrada (o que está sendo testado está claro)
- [ ] Respeita `06-ciclo/diretrizes-vigentes.md` (não repete o que está em "parar de fazer")

### B7 · Clareza e Legibilidade (peso 10)
- [ ] Frases curtas; uma ideia por frase
- [ ] Sem jargão que o ICP não usa
- [ ] Leitura escaneável (parágrafos de 1 a 3 linhas em digital)
- [ ] Linguagem do cliente presente (`icp-e-publico-alvo.md` §9)

### B8 · Ortografia e Gramática pt-BR (peso 5)
- [ ] Ortografia e acentuação (1 a 2 erros = MENOR; 3 ou mais = GRAVE)
- [ ] Concordância e regência
- [ ] Nomes de produto, marca e pessoas escritos corretamente

### Bloco extra para Pacotes de Execução (estrutura de campanha, plano de escala, fluxo a ativar, disparo de e-mail)
- [ ] Todos os criativos referenciados estão em `*/aprovados/`
- [ ] Verba e limites batem com o plano de mídia aprovado
- [ ] Nomenclatura e UTMs no padrão
- [ ] Exclusões de público corretas (ex.: compradores)
- [ ] Segmento de envio e supressões corretos (e-mail, DM)
- [ ] Guardrails (teto, stop-loss) definidos
- [ ] Todas as ações externas listadas para o Pedido de Aprovação do Chefe

Qualquer item deste bloco não atendido = BLOQUEADOR.

---

## Severidade, Nota e Veredito

**Severidade:**
- **BLOQUEADOR:** impede a aprovação, independentemente da nota.
- **GRAVE:** compromete resultado ou marca; precisa de correção pelo autor.
- **MENOR:** ajuste pontual (ortografia, uma palavra amarela, pontuação).

**Nota de cada bloco (0 a 100% do peso):**
- 100% = sem achados
- 75% = 1 ou 2 achados menores
- 50% = 1 achado grave ou 3+ menores
- 0% = bloqueador ou 2+ graves no bloco

**Nota final** = soma ponderada dos 8 blocos (0 a 100).

**Veredito:**

| Condição (avaliar de cima para baixo) | Veredito |
|---|---|
| Qualquer achado BLOQUEADOR | **REPROVADO** |
| Qualquer achado GRAVE | **REPROVADO** (o autor corrige e reenvia como `_vN`) |
| Nota < 70 | **REPROVADO** |
| Nota ≥ 70, apenas achados MENORES | **APROVADO COM AJUSTES MENORES** (o auditor aplica e registra o antes/depois) |
| Nota ≥ 85 e nenhum achado | **APROVADO** |

**Ajustes que o auditor pode aplicar sozinho:** ortografia, pontuação, acentuação, trocar 1 palavra da Lista Amarela por equivalente simples. **Nunca:** reescrever argumento, mudar promessa, ângulo, oferta ou CTA. Isso volta para o autor.

**Limite de ciclos:** se a mesma peça for reprovada 2 vezes, o log recomenda que o Chefe decida com o usuário.

---

## Formato do Log (obrigatório)

Arquivo: `06-ciclo/auditorias/AAAA-MM-DD_<id-da-peca>_auditoria.md`

```
---
titulo: Auditoria — <título da peça>
tipo: auditoria
campanha: <slug>
agente: auditor-qualidade
data: AAAA-MM-DD
status: interno
peca: <caminho do rascunho auditado>
versao-auditada: <vN>
veredito: <APROVADO | APROVADO COM AJUSTES MENORES | REPROVADO>
nota: <0-100>
---

## Resumo
<2 a 3 linhas: veredito e motivo principal>

## Notas por bloco
| Bloco | Peso | % | Pontos | Achados |
|---|---|---|---|---|
| B1 Fidelidade à marca | 20 | | | |
| B2 Linguagem de IA | 15 | | | |
| B3 Veracidade e compliance | 20 | | | |
| B4 CTA único | 10 | | | |
| B5 Gancho e formato | 10 | | | |
| B6 Alinhamento estratégico | 10 | | | |
| B7 Clareza | 10 | | | |
| B8 Ortografia | 5 | | | |
| **Total** | 100 | | **__** | |

## Achados
| # | Severidade | Bloco | Trecho (citação exata) | Problema | Correção exigida |
|---|---|---|---|---|---|

## Varredura automática
<termos encontrados e decisão (proibido / uso literal permitido)>

## Ajustes aplicados pelo auditor (só em APROVADO COM AJUSTES MENORES)
| Antes | Depois |

## Destino
- Aprovado em: <caminho em */aprovados/> | ou
- Devolvido para: <agente autor> com as correções acima
```
