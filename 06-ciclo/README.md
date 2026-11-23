# 06 · O Ciclo: Planos, Dados, Aprendizado e Qualidade

Memória do **Departamento 6 (O Ciclo)**. É aqui que a agência aprende: plano → execução → medição → retrospectiva → novas diretrizes.

| Caminho | Conteúdo | Quem escreve |
|---|---|---|
| `planos/` | Planos de missão (objetivo, métrica, hipóteses, fases, agentes, entregáveis, registro de execuções) | Chefe de Marketing |
| `dados-brutos/` | Exports e coletas via MCP (Ads, Instagram, YouTube, GA4, e-mail, checkout, CRM) | Chefe de Marketing (ou usuário) |
| `relatorios/` | Relatórios executivos semanais e mensais | analista-dados |
| `conversao/` | Diagnósticos de CRO (páginas, checkout, funis de Direct e e-mail) | analista-conversao |
| `retrospectivas/` | Retrospectivas semanais: hipóteses × resultados, aprendizados | analista-retrospectiva |
| `auditorias/` | Logs de auditoria de qualidade de todas as peças | auditor-qualidade |
| `diretrizes-vigentes.md` | Arquivo vivo com os aprendizados ativos para Referências e Criação | **apenas** analista-retrospectiva |
| `registro-hipoteses.md` | Registro de todas as hipóteses testadas | Chefe (cria) / analista-retrospectiva (atualiza status) |

**Dados pessoais:** exports com dados de clientes (nome, e-mail, telefone) devem ser anonimizados ou agregados antes de entrar em `dados-brutos/`. Nunca copie dados pessoais para relatórios ou peças.

**Nomenclatura:** `AAAA-MM-DD_<tema>_<tipo>.md` (dados brutos: `AAAA-MM-DD_<fonte>_<periodo>.<csv|json|md>`)
