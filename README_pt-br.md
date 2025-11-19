Projeto de Análise Exploratória de Dados

Vendas de Jogos – Loja Online ICE

Este projeto examina dados históricos de vendas de videogames com o objetivo de entender quais fatores influenciam o sucesso comercial de um jogo. A análise simula o cenário de dezembro de 2016, quando a loja online fictícia ICE está planejando campanhas de marketing e decisões estratégicas para 2017.

A base de dados inclui informações de vendas por região, avaliações de usuários e críticos, plataformas, gêneros e a classificação etária ESRB.

⸻

Objetivos do Projeto
	•	Investigar padrões de vendas ao longo dos anos e por plataforma.
	•	Identificar os fatores que mais influenciam o sucesso de um jogo.
	•	Criar perfis de consumidores por região (América do Norte, Europa e Japão).
	•	Testar hipóteses estatísticas sobre diferenças de avaliações entre plataformas e gêneros.
	•	Produzir insights acionáveis para campanhas de marketing em 2017.

⸻

1. Entendimento do Dataset

Nesta etapa o foco é explorar:
	•	Estrutura das colunas
	•	Tipos de dados
	•	Volume de jogos por ano
	•	Disponibilidade de informações essenciais (vendas, gênero, plataforma, rating, avaliações)

⸻

2. Preparação dos Dados

As ações principais incluem:

Limpeza e padronização
	•	Ajustar nomes das colunas
	•	Criar, manter ou remover colunas conforme necessário
	•	Converter tipos (datas, numéricos, strings)
	•	Documentar cada alteração e explicar o porquê

Tratamento de valores ausentes
	•	Verificar a natureza dos nulos
	•	Determinar quando preencher, remover ou manter valores
	•	Registrar a estratégia adotada para cada coluna

Feature engineering
	•	Criar coluna de vendas globais somando todas as regiões

⸻

3. Análise Exploratória

3.1 Lançamentos ao longo dos anos
	•	Quantidade de jogos lançados por ano
	•	Identificação de períodos com dados confiáveis (para projetar 2017)

3.2 Evolução das plataformas
	•	Comparar vendas totais por plataforma
	•	Observar ciclos de surgimento e queda de plataformas
	•	Selecionar plataformas mais relevantes para o período recente

3.3 Foco temporal
	•	Determinar um intervalo de anos adequado para modelar 2017
	•	Excluir anos pouco relevantes conforme análise anterior

3.4 Vendas por plataforma
	•	Identificar plataformas líderes
	•	Verificar crescimento/declínio
	•	Criar boxplots de vendas globais por plataforma
	•	Comparar médias e dispersões

3.5 Impacto das avaliações
	•	Escolher uma plataforma popular (ex.: PS4, Xbox One ou 3DS)
	•	Criar um scatterplot relacionando avaliação x vendas
	•	Calcular correlação e interpretar
	•	Comparar desempenho dos mesmos jogos em outras plataformas

3.6 Gêneros de jogos
	•	Avaliar distribuição geral
	•	Identificar os gêneros mais lucrativos
	•	Diferenciar entre gêneros de alto e baixo desempenho

⸻

4. Perfil de Usuário por Região (AN, UE, JP)

Para cada região:

Plataformas principais
	•	Selecionar top 5
	•	Analisar diferenças de participação de mercado

Gêneros principais
	•	Selecionar top 5
	•	Explicar variações entre regiões

Influência da classificação ESRB
	•	Verificar se o rating impacta vendas de forma diferente em cada mercado

⸻

5. Teste de Hipóteses

Hipóteses avaliadas
	1.	As avaliações médias de usuários para Xbox One e PC são iguais.
	2.	As avaliações médias de usuários para os gêneros Action e Sports são diferentes.

Documentação do processo
	•	Definir hipóteses nulas e alternativas
	•	Selecionar nível de significância (alfa) e justificar
	•	Escolher o teste estatístico adequado
	•	Interpretar os resultados em termos práticos

⸻

6. Conclusão Geral

A conclusão deve sintetizar:
	•	Principais fatores que determinam o sucesso de um jogo
	•	Plataformas mais promissoras para 2017
	•	Gêneros com maior potencial
	•	Comportamentos distintos por região
	•	Resultados dos testes estatísticos
	•	Recomendações para campanhas de marketing da loja ICE