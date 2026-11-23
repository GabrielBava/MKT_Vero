---
titulo: Teardown — @tramontanaconsorcios (INTERROMPIDO: concorrente não confirmado)
tipo: teardown
campanha: teste-tramontana
agente: analista-concorrentes
data: 2026-11-23
versao: v1
status: interno
canal: n/a
etapa-funil: n/a
hipotese: n/a
fontes: [00-marca/ (4 arquivos, template vazio), 06-ciclo/diretrizes-vigentes.md, URLs do Log]
auditoria: n/a
---

## Resumo executivo
- A existência e a identidade de @tramontanaconsorcios NÃO foram confirmadas. Por instrução do briefing (handle não confirmado → registrar e parar), o teardown de 8 camadas não foi feito.
- O Instagram não pôde ser lido: o host www.instagram.com não resolve neste ambiente (fora dos domínios de rede permitidos).
- 3 buscas web não retornaram site oficial, perfil, Reclame Aqui, nem registro no Banco Central para "Tramontana Consórcios". O único nome parecido ("Trasmontano") é de saúde e bem-estar, sem relação com consórcio [INFERÊNCIA: homônimo, não é o alvo].
- Nenhuma brecha, matriz ou recomendação foi produzida: sem evidência, qualquer uma seria invenção.
- Para destravar: liberar instagram.com na rede da sessão, ou o usuário fornecer prints, URL do site, razão social ou CNPJ.

## Escopo
| Pergunta de negócio | Concorrentes (tipo) | Canais | Período |
|---|---|---|---|
| Avaliar o concorrente indicado pelo usuário (teste de fluxo, Workflow I) | @tramontanaconsorcios (tipo: `[PENDENTE: classificar após confirmar]`) | Instagram, site, bibliotecas de anúncios, reputação | Ativos em 2026-11-23 |

## Log de evidências
| ID | Concorrente | Tipo de ativo | URL | Data | Observação |
|---|---|---|---|---|---|
| E01 | Tramontana | Perfil Instagram | https://www.instagram.com/tramontanaconsorcios/ | 2026-11-23 | acesso bloqueado (host não resolve; precisa estar nos domínios permitidos) |
| E02 | Tramontana | Busca web "tramontanaconsorcios consórcios Tramontana" | (WebSearch) | 2026-11-23 | Sem resultado relevante. Retornou apenas "Trasmontano" (saúde), PDFs de administradoras e normas do BCB |
| E03 | Tramontana | Busca web "Tramontana Consórcios administradora consórcio Banco Central" | (WebSearch) | 2026-11-23 | Sem menção. Só normas gerais do BCB (Res. BCB 233/2022, IN BCB 398/2023) |
| E04 | Tramontana | Busca web "Tramontana Consórcios Reclame Aqui / instagram / site oficial" | (WebSearch) | 2026-11-23 | Sem página da empresa; só outras administradoras (Reserva, Tradição, Âncora etc.) |
| E05 | Tramontana | Meta Ad Library | https://www.facebook.com/ads/library/ | 2026-11-23 | não tentado: sem página confirmada para buscar |
| E06 | Tramontana | Google Ads Transparency Center | https://adstransparency.google.com/ | 2026-11-23 | não tentado: mesmo motivo |

## Teardown por concorrente
Não realizado. Nenhum ativo do concorrente foi lido; as 8 camadas e os sinais de performance ficam `[PENDENTE: acesso aos ativos]`.

## Matriz comparativa
Não realizada. Coluna "Nossa marca": `[PENDENTE: onboarding]`.

## Brechas de mercado
Encontradas: 0. Motivo: nenhuma evidência primária do concorrente foi coletada.

## Recomendações
Adaptar / Evitar / Atacar: nenhuma. Não há base factual.

## Hipóteses propostas
- Se confirmarmos o handle e lermos 5 a 10 posts e os anúncios ativos, então o teardown completo será viável, porque o bloqueio atual é de acesso e não de ausência de conteúdo `[INFERÊNCIA]`.
- Observação de setor (não é achado do concorrente): consórcio é regulado pelo Banco Central; no Reclame Aqui há reclamações de outras administradoras sobre "promessa de contemplação" e propaganda enganosa (resultados de busca E04). Promessas de contemplação são ponto sensível de compliance a verificar quando houver material do concorrente.

## Limitações
- Rede: www.instagram.com fora dos domínios permitidos; Meta Ad Library, Google Transparency, Reclame Aqui e BCB não foram lidos diretamente (só resultados de busca).
- Pode haver variação de grafia (ex.: Trasmontano, Tramontana, outro nome da razão social); o handle não foi validado.
- `00-marca/` é template vazio: sem posicionamento, ICP ou ofertas para comparar.
- Total de consultas: 4 (1 WebFetch bloqueado, 3 WebSearch).
