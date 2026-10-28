# Diário de Análise

## Projeto: Um Olhar de Quem Está no Campo

### 1. Identificação

* **Pesquisadora:** Maria Laura Corrêa da Silva
* **Contexto:** SCTEC/SENAI-SC — formação em Análise de Dados, Visualização de Dados e Business Intelligence.
* **Objetivo:** registrar o percurso analítico, as decisões metodológicas, as verificações realizadas e as justificativas que sustentam o trabalho.

### 2. Registro de início

**Data:** 27/10/2026

**Etapa:** preparação do ambiente de análise.

**Objetivo da etapa:** organizar os arquivos do projeto e estabelecer as condições para inspecionar a base de respostas antes de iniciar a análise descritiva.

**Organização definida:**

* `data/fonte_original/`: preservação do arquivo original da pesquisa.
* `data/derivados/`: armazenamento de arquivos produzidos durante o processamento.
* `data/fontes_publicas/`: armazenamento de bases externas selecionadas para contextualização.
* `docs/analise/`: documentação das análises e decisões.
* `notebooks/`: código e resultados das inspeções e análises em Python.

### 3. Ponto de atenção inicial

O arquivo disponível está identificado como `BASELINE_36_RESPOSTAS`, enquanto as diretrizes atualizadas do projeto mencionam uma base consolidada de 54 respostas.

Essa diferença precisa ser esclarecida antes de definir qual arquivo será utilizado como base de referência da análise.

**Decisão:** não substituir, alterar ou tratar o arquivo original como se fosse a versão consolidada sem verificar sua origem e seu conteúdo.

### 4. Próximas atividades

1. Confirmar a versão da base de respostas disponível.
2. Inspecionar a estrutura do CSV.
3. Verificar quantidade de linhas e colunas, tipos de dados e valores ausentes.
4. Construir o dicionário de dados com base nas colunas e no instrumento de pesquisa.
5. Registrar inconsistências e decisões de tratamento.
6. Iniciar a análise descritiva.
7. Identificar perguntas que justifiquem a busca por dados públicos.

### 5. Critérios de rastreabilidade

* Preservar os dados originais.
* Registrar as transformações realizadas e suas justificativas.
* Distinguir resultados observados de interpretações.
* Documentar as fontes externas utilizadas.
* Não excluir registros ou alterar valores sem justificativa documentada.

---

*Este diário será atualizado à medida que as atividades forem executadas. Os procedimentos previstos não serão registrados como concluídos antes de sua realização.*

# Registro de análise 01 — Perfil dos participantes

**Data:** 27/10/2026
**Projeto:** Um Olhar de Quem Está no Campo
**Base:** `base_analitica_v1.csv`
**Número de participantes:** 54

## 1. Objetivo

Descrever o perfil dos participantes a partir das variáveis estado, gênero, escolaridade e faixa etária, contextualizando as análises subsequentes.

## 2. Principais achados

### Distribuição geográfica

Santa Catarina concentra 46 dos 54 participantes (85,19%). Os outros oito participantes estão distribuídos por sete unidades federativas.

A concentração geográfica deverá ser considerada na interpretação dos resultados e em eventuais comparações com fontes externas.

### Gênero

A amostra reúne 40 homens (74,07%), 13 mulheres (24,07%) e uma pessoa que preferiu não informar (1,85%).

A distribuição descreve os participantes da pesquisa e não deve ser generalizada para o conjunto dos profissionais de tecnologia.

### Escolaridade

Graduação e pós-graduação somam 39 participantes (72,22%). Também há participantes com formação técnica, ensino médio, mestrado e doutorado.

A interpretação definitiva das categorias depende da conferência da redação original da pergunta.

### Faixa etária

As faixas de 35–44 e 45–54 anos reúnem 28 participantes (51,85%). Há também participantes com até 24 anos, entre 25 e 34 anos e com 55 anos ou mais.

A composição etária permite investigar possíveis diferenças de experiência profissional entre grupos, sem presumir antecipadamente que elas existam.

## 3. Síntese interpretativa

O perfil da amostra é marcado pela concentração em Santa Catarina, pela predominância masculina e pela presença expressiva de participantes entre 35 e 54 anos.

Essas características contextualizam as percepções registradas no questionário. Não constituem, isoladamente, evidência sobre a composição do mercado de tecnologia.

## 4. Questões para investigação posterior

* Como a trajetória profissional se distribui entre as diferentes faixas etárias?
* Há diferenças nas influências de entrada na área entre participantes de diferentes gêneros?
* A realidade profissional percebida varia conforme a escolaridade?
* Quais características da amostra precisam ser consideradas ao comparar os achados com dados externos?

## 5. Limitações

A pesquisa utiliza amostragem não probabilística. Os resultados descrevem os respondentes e não representam estimativas estatísticas do conjunto dos profissionais de tecnologia.

As questões registradas nesta seção são hipóteses para análises posteriores, não conclusões já demonstradas.

# Registro de análise 02 — Influências na trajetória profissional

**Data:** 27/10/2026
**Projeto:** Um Olhar de Quem Está no Campo
**Base:** `base_analitica_v1.csv`
**Participantes:** 54

## Objetivo

Identificar quais influências foram mencionadas pelos participantes ao descreverem sua trajetória na área em que atuam.

## Resultados descritivos

* Autaprendizado e curiosidade pessoal: 38 participantes (70,37%).
* Formação acadêmica ou cursos: 34 (62,96%).
* Transição de outra carreira: 22 (40,74%).
* Busca por estabilidade ou oportunidade de mercado: 13 (24,07%).
* Indicação ou influência de rede de contatos: 7 (12,96%).
* Acaso ou oportunidade inesperada: 7 (12,96%).
* Familiares da área: 1 (1,85%).

## Interpretação inicial

O autaprendizado e a curiosidade pessoal constituem a influência mais frequentemente mencionada na amostra. A formação acadêmica ou por cursos também aparece com frequência elevada.

A transição de outra carreira foi mencionada por aproximadamente quatro em cada dez participantes, indicando que trajetórias de mudança profissional fazem parte das experiências relatadas.

Os resultados também mostram que diferentes influências podem coexistir na trajetória de uma mesma pessoa.

## Limites da interpretação

As frequências representam menções às alternativas, não medidas da importância causal de cada fator.

Como a pergunta permite múltiplas escolhas, os percentuais não devem ser somados para representar uma distribuição exclusiva.

A amostra é não probabilística e não permite generalizar os resultados para todos os profissionais de tecnologia.

## Próximas questões de investigação

* Como as influências na trajetória se relacionam com a faixa etária?
* A transição de carreira aparece com frequência diferente entre os grupos etários?
* Como os participantes descrevem seu cotidiano profissional?
* Quais relações entre trajetória e realidade profissional podem ser investigadas com as demais variáveis?

## Nota técnica

A separação das alternativas foi realizada utilizando vírgula e espaço como delimitador. A estrutura das opções originais deverá ser conferida antes da consolidação definitiva dos resultados.
