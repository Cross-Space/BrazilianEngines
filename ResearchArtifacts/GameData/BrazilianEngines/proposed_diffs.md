```markdown
# Proposed diffs (preliminar)

Status: não aplicados — aguardando sua revisão e aprovação.

Resumo geral das mudanças propostas (aplicar apenas após revisão):

- Propulsor / Descrições
  - Garantir que `L15` e `L15E` estejam documentados como `LOX + Etanol` e que `L15E` seja markeada como variante com bomba elétrica.
  - Garantir que `L75` esteja como `LOX + RP-1` e `L75-H` como `Hydrolox` (experimental).

- Valores de desempenho
  - Preencher `Isp` (SL/Vac), `thrust` (SL/Vac), `burn_time` e `mass` nos `@CONFIG` e `ModuleEngineConfigs` conforme tabela `research_table_prelim.csv`.
  - Onde houver incerteza, manter valores conservadores e documentar a fonte.

- Entry cost / Tech nodes
  - Ajustar `entryCost` e `techRequired` apenas quando houver justificação histórica/técnica clara (documentar em comentário no patch).

- ModuleEngineIgnitionReliability
  - Inserir `ModuleEngineIgnitionReliability` em PARTs de motores com parâmetros iniciais padronizados (ex.: `minIgnitions = 1`, `baseIgnitionReliability = 0.995`) — valores a definir após tabela final.

Arquivo CSV preliminar com dados extraídos: `GameData/BrazilianEngines/research_table_prelim.csv`.

Próxima ação sugerida (após aprovação):
1. Eu gero um patch (`proposed_changes.patch`) contendo edições `@CONFIG` e `@PART` com os novos `Isp`/`thrustCurve`/`entryCost`/`ModuleEngineIgnitionReliability` para cada motor listados no CSV.
2. Você revisa o patch e pede alterações ou aprova.
3. Eu aplico o patch e executo verificações sintáticas.

Observação: Todos os arquivos originais são preservados em `GameData/BrazilianEngines/legacy/` para rollback.

```