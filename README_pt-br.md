 Projeto de Análise Exploratória de Dados  
 Vendas de Jogos – Loja Online ICE

Este projeto analisa dados históricos de vendas de videogames com o objetivo de entender quais fatores influenciam o sucesso comercial de um jogo. O cenário simulado é dezembro de 2016, quando a loja online fictícia ICE planeja suas estratégias de marketing para o ano seguinte.

A base de dados contém informações de vendas por região, avaliações de usuários e críticos, plataformas, gêneros e classificações ESRB.

---

 Objetivos do Projeto

- Investigar padrões de vendas ao longo dos anos e por plataforma.  
- Identificar fatores que influenciam o desempenho comercial de um jogo.  
- Criar perfis de consumidores por região (América do Norte, Europa e Japão).  
- Testar hipóteses estatísticas relacionadas às avaliações dos usuários.  
- Gerar insights para orientar decisões estratégicas em 2017.

---

 1. Dicionário de Dados

A seguir, uma descrição clara das colunas do dataset, incluindo unidades e interpretações importantes.

 **Colunas principais**

| Coluna | Descrição | Unidade / Observações |
|-------|-----------|------------------------|
| `name` | Nome do jogo | Texto |
| `platform` | Plataforma em que o jogo foi lançado | Ex.: PS4, X360, DS |
| `year_of_release` | Ano de lançamento | Inteiro; valores ausentes foram removidos antes da conversão |
| `genre` | Gênero do jogo | Ex.: Action, Sports |
| `na_sales` | Vendas na América do Norte | **Milhões de dólares** |
| `eu_sales` | Vendas na Europa | **Milhões de dólares** |
| `jp_sales` | Vendas no Japão | **Milhões de dólares** |
| `row_sales` | Vendas no restante do mundo ("Rest of World") | **Milhões de dólares** |
| `critic_score` | Avaliação média da crítica | Escala 0–100 |
| `user_score` | Avaliação média dos usuários | Escala 0–10; valores "tbd" foram convertidos para `NaN` e depois substituídos por `-1` como placeholder |
| `rating` | Classificação etária ESRB | E, T, M, etc. |

 **Coluna derivada**
| Coluna | Descrição |
|-------|-----------|
| `global_sales` | Soma de todas as vendas regionais; unidade: **milhões de dólares** |

---

 2. Preparação dos Dados

 **Limpeza e padronização**
- Ajuste dos nomes das colunas para formato consistente (snake_case).  
- Conversão de `year_of_rzelease` para inteiro após remoção dos valores nulos.  
- Transformação de `user_score` para tipo numérico:  
  - valores `"tbd"` foram tratados como dados ausentes,  
  - convertidos para `NaN`,  
  - posteriormente substituídos por `-1` para permitir conversão numérica.  

 **Tratamento de valores ausentes**
- `year_of_release`: removidos apenas os registros com valores ausentes.  
- `user_score`: mantidos registros e utilizado placeholder numérico.  
- `critic_score` e `rating`: mantidos como `NaN` devido à natureza informativa desses campos.

 **Feature engineering**
- Criação de `global_sales` a partir da soma das colunas regionais.

---

 3. Análise Exploratória

 3.1 Lançamentos ao longo dos anos
- Volume de jogos por ano.  
- Identificação de períodos estáveis para modelagem.  

 3.2 Evolução das plataformas
- Comparação de vendas totais por plataforma.  
- Análise do ciclo de vida das plataformas.  

 3.3 Foco temporal
- Seleção de uma janela temporal relevante para projeções de 2017.  

 3.4 Vendas por plataforma
- Boxplots de `global_sales` por plataforma.  
- Comparação de médias e dispersão.  

 3.5 Impacto das avaliações
- Relação entre `critic_score`, `user_score` e vendas.  
- Análise de correlação.  
- Comparações entre plataformas.  

 3.6 Gêneros
- Identificação dos gêneros mais lucrativos.  
- Distribuição por desempenho.

---

 4. Perfil de Usuário por Região (NA, EU, JP)

Para cada região:

 Plataformas principais  
- Identificação das Top 5 e suas diferenças de mercado.

 Gêneros predominantes  
- Preferências regionais e variações culturais.

 Influência da classificação ESRB  
- Diferenças no impacto do rating sobre vendas dependendo da região.

---

 5. Teste de Hipóteses

 Hipóteses estudadas
1. As avaliações médias dos usuários para Xbox One e PC são iguais.  
2. As avaliações médias dos usuários para Action e Sports são diferentes.

 Documentação
- Definição formal de H₀ e H₁.  
- Escolha do teste estatístico apropriado.  
- Interpretação dos resultados em termos práticos.

---

 6. Conclusão Geral

A conclusão apresenta:

- Principais fatores que influenciam vendas.  
- Plataformas mais promissoras para 2017.  
- Gêneros com maior potencial.  
- Diferenças regionais relevantes.  
- Resultados e implicações dos testes de hipótese.  
- Recomendações estratégicas para a loja ICE.