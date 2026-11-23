---
titulo: Teste da agência — teardown do concorrente @tramontanaconsorcios
tipo: plano
campanha: teste-tramontana
agente: chefe-de-marketing
data: 2026-11-23
status: interno
---

## Objetivo e métrica
- Objetivo de negócio: validar o fluxo da agência (Workflow I) com um teardown real e gerar inteligência sobre um concorrente do mercado de consórcios.
- Métrica principal e meta: teardown salvo em `01-referencias/concorrentes/` no formato da skill `competitor-teardown`, com ≥ 3 brechas evidenciadas e log de evidências com URL e data.
- Prazo: mesma sessão (teste breve).

## Contexto e suposições
- Pedido do usuário: "fazer um teste breve, para validar, onde quero que avalie o concorrente @tramontanaconsorcios".
- `00-marca/` ainda é template (onboarding não feito). A coluna "nossa marca" da matriz fica `[PENDENTE]`.
- Suposição: o handle é do Instagram e o mercado é consórcio no Brasil.

## Hipóteses
- Nenhuma registrada (teste de fluxo). Hipóteses propostas no handoff serão avaliadas após o onboarding.

## Fases, agentes e entregáveis
| Fase | Agente | Entregável (caminho) | Depende de | Status |
|---|---|---|---|---|
| 1 | analista-concorrentes | `01-referencias/concorrentes/2026-11-23_tramontana-consorcios_teardown.md` | — | interrompido: concorrente não confirmado |

## Resultado do teste (2026-11-23)
- Fluxo validado: briefing → sub-agente → arquivo com cabeçalho padrão → handoff → checagem do Chefe.
- Inteligência: nenhuma. O Instagram está bloqueado pela rede do ambiente (proxy 403, confirmado pelo Chefe). As buscas web (do analista e do Chefe) não encontraram site, perfil ou registro de "Tramontana Consórcios".
- Ambiguidade: em espanhol rioplatense, "consorcios" significa administração de condomínios. O handle pode ser de uma administradora de condomínios da Argentina ou do Uruguai, e não de consórcio brasileiro [INFERÊNCIA].
- Para destravar: URL do site, cidade/país, CNPJ ou prints do perfil e dos anúncios.

## Pedidos de aprovação e execuções
| Data/hora | Ação | Aprovado pelo usuário? | Resultado da ferramenta |
|---|---|---|---|
| — | Nenhuma ação externa prevista (só leitura pública) | n/a | — |

## Próximos passos
- Após o onboarding: `estrategista-mensagens` usar as brechas para Big Idea e ângulos.
