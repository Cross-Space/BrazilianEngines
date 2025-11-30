```markdown
# Research Report — BrazilianEngines (preliminar)

Data: 30 Nov 2025

Objetivo
- Compilar fontes públicas e extrair parâmetros de motores (Isp, empuxo, tempo de queima, massa quando disponível) para propor ajustes nos `ModuleEngineConfigs` e `@CONFIG` do mod `BrazilianEngines`.

Fontes locais (cópias salvas durante a pesquisa)
- `/tmp/s20_pt.html` — Wikipédia/pt (Sonda II / S20)
- `/tmp/s40_pt.html` — páginas relacionadas a S‑40
- `/tmp/s43_pt.html` — página S‑43
- `/tmp/s44_pt.html` — página S‑44
- `/tmp/s50_pt.html` — página S‑50
- `/tmp/vls1.html` e `/tmp/vls1_pt.html` — páginas do VLS (contexto e boosters)

Resumo preliminar por família

- S20 (sólido, pequeno)
  - Fonte: `/tmp/s20_pt.html` (Wikipédia pt — tabela de parâmetros contém "Tempo de queima").
  - Valores a extrair/confirmar: Isp (s), empuxo (kN), burn time (s). Ainda pendente extração numérica final.

- S30 / S33 (sólidos médios)
  - Fontes locais salvas; extração pendente. Proposta: alinhar Isp entre 250–285 s dependendo do setor do motor (valores típicos para SRM de VLS).

- S40 / S43 / S43B / S44 (sólidos maiores)
  - Observações preliminares:
    - S‑43 (boosters): empuxo total citado ~303 kN; Isp aproximado citado ~225 s (fonte: `/tmp/s43_pt.html`).
    - S‑40: Isp preliminar em referência encontrada ~275 s (`/tmp/s40_pt.html`).
    - S‑44: Isp preliminar ~282 s (`/tmp/s44_pt.html`).
  - Ação: confirmar cada valor nas páginas originais (AEB/Avibras/relatórios técnicos) e em publicações técnicas.

- S50 (maior SRM)
  - Página salva `/tmp/s50_pt.html`; extração de números pendente.

- L15 / L15E (líquidos pequenos)
  - Decisão de projeto: `L15` e `L15E` devem ser LOX + Etanol (confirmado por preferência do projeto). (Edição do autor, assim como o L75H, o L15E deve ser uma variante estendida do L15, porem, movida a bomba elétrica)
  - Ações: buscar Isp em bibl. técnica de motores LOX/EtOH; estimar Isp em ~280–320 s (dependendo da câmara e mistura) e propor um `ModuleEngineConfigs` conservador inicialmente.

- L75 / L75-H (médios)
  - `L75`: LOX + RP‑1 (consistente com motores de 2a geração do VLS); `L75-H`: variante hydrolox (experimental).
  - Ações: coletar Isp e empuxo real de publicações IAE/AEB/Avibras; valores típicos: RP‑1/LOX lox‑rp1 ≈ 280–330 s (vac/sea dependente); hydrolox mais alto (≈ 350–450 s vac dependendo do ciclo).

Observações e recomendações
- Os arquivos HTML originais foram salvos em `/tmp/` e devem ser usados como referência para citações no relatório final.
- Próxima etapa (recomendada): realizar extração numérica explícita das páginas salvas, organizar em uma tabela CSV com colunas: motor, propulsor, Isp_vac, Isp_sl, thrust_vac(kN), thrust_sl(kN), burn_time(s), massa(kg), fonte(URL).
- Após sua aprovação do relatório final, aplico as mudanças nos `@CONFIG`/`ModuleEngineConfigs` e atualizo `entryCost`/`techRequired` conforme justificativa histórica/RO balance.

Notas sobre o trabalho atual
- Gereis um arquivo unificado `GameData/BrazilianEngines/WaterfallUnified.cfg` e movi os `*_Waterfall.cfg` originais para `GameData/BrazilianEngines/legacy/Waterfall/`.
- Todos os backups anteriores dos `_TREE-*.cfg` já estão em `GameData/BrazilianEngines/legacy/`.

Próximos passos sugeridos (após sua confirmação)
1. Eu finalizo a extração numérica e preencho a tabela CSV.
2. Você revisa e aprova as propostas.
3. Eu aplico as mudanças e executo verificações sintáticas.

-- Fim do relatório (preliminar)

```
