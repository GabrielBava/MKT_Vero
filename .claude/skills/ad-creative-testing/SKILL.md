---
name: ad-creative-testing
description: Matriz de criação e teste de criativos de anúncios (3 ângulos x 3 ganchos x 2 formatos = 18 variações) para Meta Ads, TikTok Ads e YouTube ou Google Ads, com nomenclatura padrão, estrutura de teste, fórmulas e métricas de corte (CTR, Hook Rate, Hold Rate, CPM, CPC, CPA, ROAS, frequência), árvore de diagnóstico, detecção de fadiga de criativo e regras de escala vertical e horizontal. Use sempre que for planejar testes de criativos, analisar desempenho de anúncios, decidir pausar, iterar ou escalar, distribuir verba ou diagnosticar queda de resultado em mídia paga.
---

# Ad Creative Testing · Matriz de Teste e Escala

## Princípios

1. **O criativo é o fator que mais pesa** no desempenho de contas com segmentação ampla: ele escolhe o público.
2. **Teste uma variável por vez** (ângulo, depois gancho, depois formato) sempre que a verba não permitir a matriz completa.
3. **Decida por regra, não por sensação.** Regras de corte e escala são definidas antes de o teste começar.
4. **Dê tempo e verba suficientes** para cada criativo antes de julgar.
5. **Toda alteração de verba é uma proposta.** Executar exige `[APROVAR]` do usuário (CLAUDE.md §4.3).

---

## Métricas e Fórmulas

| Métrica | Fórmula | O que diz |
|---|---|---|
| **CPM** | gasto ÷ impressões × 1.000 | Custo de atenção; leilão e qualidade |
| **CTR (link)** | cliques no link ÷ impressões | Força do criativo + CTA |
| **CPC (link)** | gasto ÷ cliques no link | Eficiência do clique |
| **Hook Rate** | reproduções de 3 s ÷ impressões | O gancho parou o polegar? |
| **Hold Rate** | ThruPlays (15 s ou vídeo completo, se menor) ÷ reproduções de 3 s | O corpo do vídeo segurou? |
| **CVR (página)** | conversões ÷ cliques no link (ou visualizações da página) | Página e oferta |
| **CPA** | gasto ÷ conversões | Custo por resultado |
| **ROAS** | receita atribuída ÷ gasto | Retorno direto |
| **Frequência** | impressões ÷ alcance | Saturação do público |
| **MER** (blended) | receita total ÷ gasto total em mídia | Saúde geral, independente de atribuição |

### Economia da unidade (calcular antes de qualquer teste)
- **CPA máximo** = ticket médio × margem de contribuição (antes da mídia).
- **ROAS de equilíbrio** = 1 ÷ margem de contribuição.
- **CPA alvo** = definido em `00-marca/produtos-e-ofertas.md` §8.3 ou pelo `diretor-trafego`. Se houver upsell/recorrência, o `estrategista-esteira` pode autorizar CPA de front-end maior (LTV).

### Referências iniciais de benchmark
Valores de partida para contas sem histórico, a serem **substituídos pela média da própria conta** após 30 dias de dados. Variam muito por nicho, país, posicionamento e objetivo.

| Métrica | Fraco | Ok | Forte |
|---|---|---|---|
| Hook Rate | < 20% | 20% a 30% | > 30% |
| Hold Rate | < 20% | 20% a 35% | > 35% |
| CTR (link), feed, prospecção | < 0,8% | 0,8% a 1,5% | > 1,5% |
| Frequência em 7 dias (prospecção) | — | até 2,5 | — (acima de 3, atenção à fadiga) |

---

## A Matriz 3 × 3 × 2

| Dimensão | Variações | Fonte |
|---|---|---|
| **Ângulos (A1, A2, A3)** | ex.: Dor, Mecanismo/Contraintuitivo, Prova/Caso | `01-referencias/mensagens/` (3 ângulos priorizados) |
| **Ganchos (G1, G2, G3)** por ângulo | motores diferentes da `hook-engineering` | Copywriter / editor de vídeo |
| **Formatos (F1, F2)** | F1 = vídeo 9:16 (UGC, talking head, demonstração) · F2 = estático 4:5 ou carrossel | Criador de criativos / editor de vídeo |

3 × 3 × 2 = **18 criativos**. O corpo do anúncio (desenvolvimento + CTA) é o mesmo dentro de cada ângulo; o que muda é o gancho e o formato.

```
| ID          | Ângulo | Gancho (texto)            | Formato | Arquivo aprovado        | Status   |
|-------------|--------|---------------------------|---------|-------------------------|----------|
| A1-G1-F1    | Dor    | "..."                     | Vídeo   | 03-video/aprovados/...  | em teste |
| A1-G1-F2    | Dor    | "..."                     | Estático| 02-criacao/aprovados/...| em teste |
...
```

### Verba baixa? Teste sequencial
1. **Fase 1 · Ângulos:** A1, A2, A3 × melhor gancho × F1 = 3 criativos.
2. **Fase 2 · Ganchos:** ângulo vencedor × G1, G2, G3 = 3 criativos.
3. **Fase 3 · Formatos:** gancho vencedor × F1, F2 = 2 criativos.

### Verba mínima por criativo
Antes de julgar um criativo por CPA, deixe gastar **pelo menos 1× o CPA alvo** (ideal 2× a 3×), exceto quando uma regra de corte por métrica de topo disparar antes.

---

## Nomenclatura Padrão

- **Campanha:** `[AAAAMM]_[OBJETIVO]_[FUNIL]_[PRODUTO]_[TIPO]` → ex.: `202611_VENDAS_FRIO_METODO3C_TESTE`
- **Conjunto:** `[PUBLICO]_[POSICIONAMENTO]_[OTIMIZACAO]` → ex.: `BROAD-BR-25-55_AUTO_COMPRA`
- **Anúncio:** `[DDMM]_[ANGULO]-[GANCHO]-[FORMATO]_[VERSAO]` → ex.: `2311_A2-G1-F1_v1`

Sem espaços e sem acentos. A mesma nomenclatura vai nas UTMs (`utm_content=A2-G1-F1_v1`).

## Estrutura de Teste (Meta Ads, referência)

- Campanha de teste **separada** da campanha de escala.
- Um conjunto por ângulo (3 a 6 anúncios por conjunto) **ou** CBO com limite mínimo de gasto por conjunto, conforme o plano do `diretor-trafego`.
- Público amplo (broad) com exclusão de compradores, salvo indicação do plano.
- Otimização para o evento de conversão final (ou o mais próximo com volume suficiente).
- **Não edite durante o teste**: edições relevantes reiniciam a fase de aprendizado. A Meta indica cerca de 50 eventos de otimização em 7 dias por conjunto para sair do aprendizado.
- Duração mínima: 72 h, salvo disparo de regra de corte.

---

## Árvore de Diagnóstico (funil do criativo)

```
Impressão → Hook (3 s) → Hold (15 s) → Clique → Conversão
```

| Sintoma | Diagnóstico | Ação |
|---|---|---|
| Hook Rate baixo | Gancho não para o polegar | Manter corpo, **trocar gancho** (novo motor) |
| Hook alto + Hold baixo | Gancho bom, corpo fraco ou desalinhado com o gancho | **Reeditar o corpo**; checar se o gancho promete o que o corpo entrega |
| Hold alto + CTR baixo | Conteúdo bom, CTA ou oferta fracos | **Reforçar CTA**, deixar o próximo passo mais claro |
| CTR alto + CVR baixo | Problema na página, oferta ou *message match* | Acionar `analista-conversao` |
| CPM muito acima da média | Público pequeno, criativo de baixa qualidade percebida, concorrência sazonal | Ampliar público, renovar criativo, checar sazonalidade |
| Tudo bom + CPA alto | Ticket/margem insuficientes ou atribuição | Acionar `estrategista-esteira` (LTV, bumps) e checar rastreamento |

## Regras de Corte (definir no plano; padrão abaixo)

| Regra | Condição | Ação |
|---|---|---|
| C1 | Gasto ≥ 1× CPA alvo, 0 conversões **e** CTR abaixo da faixa "fraco" | Pausar |
| C2 | Hook Rate < 20% após ≥ 1.000 impressões | Pausar e iterar gancho |
| C3 | Gasto ≥ 2× CPA alvo **e** CPA > 1,5× alvo | Pausar |
| C4 | CPA ≤ alvo com ≥ 3 conversões | **Candidato a vencedor** → manter e avaliar escala |
| C5 | CPA entre 1× e 1,5× o alvo | Manter até 3× CPA alvo de gasto; depois decidir |

## Fadiga de Criativo

Sinais (comparar com os 7 dias anteriores):
- Frequência subindo **e** CTR caindo 20% ou mais.
- CPM subindo com CTR caindo.
- CPA 30% acima do alvo por 3 dias seguidos, com gasto estável.

Ações, em ordem:
1. Novos ganchos para o mesmo corpo (iteração barata).
2. Novo formato do mesmo ângulo.
3. Novo ângulo.
4. Rodízio: pausar e reativar depois de algumas semanas, se a análise indicar.

---

## Regras de Escala

**Elegibilidade:** CPA ≤ alvo por pelo menos 3 dias seguidos, volume mínimo de conversões definido no plano, frequência saudável, fora da fase de aprendizado.

### Vertical (mais verba no mesmo conjunto/campanha)
- Aumentar **15% a 25%** a cada 48 a 72 h enquanto o CPA se mantiver ≤ alvo.
- Se o CPA subir mais de 20% após um aumento, voltar ao patamar anterior e segurar 72 h.
- Evitar saltos grandes de uma vez (podem reiniciar o aprendizado).

### Horizontal (mais lugares para o que funciona)
- Duplicar o vencedor em novos públicos, posicionamentos ou regiões.
- Criar iterações do criativo vencedor (novo gancho, novo apresentador, novo formato).
- Levar vencedores para a campanha de escala (CBO ou campanhas automatizadas como Advantage+).

### Proteções (guardrails)
- Teto diário de gasto por campanha definido no plano de mídia.
- Stop-loss: pausar se o CPA passar de 2× o alvo em 24 h com gasto relevante.
- Nunca escalar com menos conversões do que o mínimo definido no plano.
- **Todas as mudanças de verba são propostas e exigem `[APROVAR]`.**

---

## Formatos de Saída

### (a) Plano de Teste
```
## PLANO DE TESTE DE CRIATIVOS — <campanha>
Economia da unidade: ticket R$__ | margem __% | CPA máximo R$__ | CPA alvo R$__ | ROAS de equilíbrio __
Verba de teste: R$__/dia por __ dias (total R$__)
Estratégia: matriz completa 3×3×2 | sequencial (fase __)
Estrutura: <campanha / conjuntos / anúncios com nomenclatura>
Matriz: <tabela de IDs>
Regras de corte: <C1 a C5 com valores>
Regras de escala: <valores>
Hipóteses: <H-### por ângulo>
Leitura prevista: AAAA-MM-DD
```

### (b) Relatório de Decisão
```
## DECISÃO DE CRIATIVOS — <campanha> — período AAAA-MM-DD a AAAA-MM-DD
| ID | Gasto | Impressões | CPM | Hook | Hold | CTR | CPC | Conv. | CPA | ROAS | Freq. | Regra disparada | Veredito |
Vereditos: PAUSAR | MANTER | ITERAR (o quê) | ESCALAR (como)
Aprendizados por ângulo / gancho / formato: ...
Pedidos de aprovação necessários: <lista de mudanças de verba/status>
```
