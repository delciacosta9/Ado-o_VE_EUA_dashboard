# Adocao_VE_EUA_dashboard
# Veículos de Combustível Alternativo — Painel de Adoção por Estado nos E.U.A.

Análise e painel interativo sobre o estado atual da adoção de veículos de combustível alternativo nos 50 estados dos EUA + D.C., desenvolvido para apoiar decisões de investimento em infraestrutura por parte de conselhos governamentais de transportes.

---

##  Visão Geral do Projeto

Este projeto foi desenvolvido como um relatório orientado a dados para ajudar decisores políticos a compreender as tendências de adoção de VE e a priorizar o investimento em infraestrutura de recarga. Cobre dados de registo de veículos por tipo de combustível em todos os estados dos EUA, com foco em veículos elétricos (VE), híbridos plug-in (PVEH), híbridos (VEH) e veículos a gasolina.

**Perguntas respondidas:**
- Qual a percentagem de VE, PVEH, VEH e gasolina em cada estado?
- Quais os estados que lideram ou ficam para trás na adoção de VE?
- Quais os combustíveis alternativos com presença relevante vs. nicho?
- Onde devem os decisores priorizar o investimento em infraestrutura de VE?

---

## Estrutura do Repositório

```
├── dataset
│   └── vehicle_data_clean.xlsx       # Dataset limpo (todos os estados e tipos de combustível)
├── dashboard/
│   └── ev_dashboard.twbx             # Workbook Tableau (packaged)
├── README.md
```

---

## Ferramentas Utilizadas

| Ferramenta | Utilização |
|------------|------------|
| **Excel** | Limpeza de dados, cálculo de KPIs, tabelas dinâmicas, colunas calculadas |
| **Tableau** | Campos calculados, painel interativo, visualizações por estado |

---

## Painel Interativo
[Ver painel complrto no Tableau Public](https://public.tableau.com/app/profile/delcia.costa/viz/Adocao_VE_EUA_Dashboard/Painel?publish=yes)


**O painel inclui:**
- KPI cards — taxa nacional de VE, estado líder, quota média de gasolina
- Top 5 estados por adoção de VE
- Comparação entre estados populosos (CA vs FL vs NY vs TX)
- Mix de combustível por estado — gráfico de barras empilhadas (VE / PVEH / VEH / Gasolina)
- Painel de combustíveis alternativos — presença vs. nicho
- Recomendação de investimento em infraestrutura

---

## Principais Conclusões

- **Califórnia** lidera com 3,4% de adoção de VE — quase 3× a média nacional (1,24%)
- **Gasolina** continua a dominar com 84,6% da frota nacional
- Apenas **5 estados** ultrapassaram o limiar de 2% de VE: CA, DC, HI, WA, NV
- **Hidrogénio** (0,000059%) e **Biodiesel** permanecem nichos — limitados a programas piloto e frotas comerciais
- **Texas** e **Nova Iorque**, apesar das grandes populações, ficam para trás com 0,9% e 1,2%

---

## Metodologia

### Limpeza de Dados — Excel
- Identificação e tratamento de valores em falta, zeros e outliers em todas as colunas de tipo de combustível
- Normalização dos nomes dos estados para compatibilidade com os papéis geográficos do Tableau
- Criação de colunas calculadas com a percentagem de cada tipo de combustível sobre o total de veículos por estado, usando fórmulas como:
  ```
  =EV / Total_Veículos * 100
  ```

### Análise de Quota de Mercado — Excel
- Tabelas dinâmicas (Pivot Tables) para agregar os registos por estado e tipo de combustível
- Ordenação e filtragem para identificar os Top 5 estados com maior taxa de adoção de VE
- Comparação direta entre estados populosos (CA, FL, NY, TX) numa tabela auxiliar referenciada pelo Tableau

### Campos Calculados — Tableau
Os campos calculados foram criados diretamente no Tableau para alimentar os KPI cards e os gráficos do painel.

### Visualizações — Tableau
- **Gráficos de barras horizontais** para ranking de estados (Top 5 e comparação de estados populosos)
- **Gráfico de barras empilhadas 100%** para mostrar o mix de combustível por estado
- **KPI cards** com campos calculados para resumo executivo no topo do painel
- **Filtro interativo por estado** para exploração dinâmica dos dados
- **Sheets auxiliares** por tipo de combustível (biodiesel, hidrogénio, PVEH, VEH) para análise de nicho

---

## Recomendação: Estados Prioritários para Investimento em Infraestrutura de VE

Três estados representam o maior retorno para investimento federal imediato:

**Califórnia** (3,4% de adoção) — maior frota de VE do país, infraestrutura sob pressão. Máximo impacto por dólar investido.

**Washington** (2,2%) — forte adoção urbana, mas zonas rurais sem cobertura. Corredores de carregamento rápido desbloqueiam o acesso a todo o estado.

**Flórida** (1,4%) — 2.º estado mais populoso, mercado subaproveitado. Maior potencial de crescimento a nível nacional.

Juntos cobrem três perfis distintos: saturação de mercado maduro, acessibilidade geográfica e desenvolvimento de mercado de alto crescimento — maximizando o retorno do portfólio federal de infraestrutura.


---

## Autora

LinkedIn: Delcia Costa · Delciacosta · github: delciacosta9

---

## 📄 Fonte dos Dados

Analyst builder
