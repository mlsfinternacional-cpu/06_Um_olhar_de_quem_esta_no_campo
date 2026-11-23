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

---

# Registro de análise 03 — Cotidiano profissional, expectativas e recomendações

**Data:** 29/10/2026  
**Projeto:** Um Olhar de Quem Está no Campo  
**Base analítica:** `base_analitica_v1.csv`  
**Participantes:** 54

## 1. Cotidiano profissional

A pergunta sobre o que define o cotidiano profissional permitiu múltiplas escolhas. As frequências observadas foram:

| Aspecto mencionado | Participantes | Percentual da amostra |
|---|---:|---:|
| Resolução de problemas | 39 | 72,22% |
| Aprendizado contínuo | 37 | 68,52% |
| Conhecimento técnico | 26 | 48,15% |
| Comunicação e colaboração | 24 | 44,44% |
| Adaptação a mudanças | 19 | 35,19% |
| Gestão de prioridades | 18 | 33,33% |
| Criatividade | 10 | 18,52% |
| Autonomia | 10 | 18,52% |
| Prazos e pressão por entregas | 9 | 16,67% |

**Interpretação inicial:** resolução de problemas e aprendizado contínuo foram as alternativas mais mencionadas. Como a pergunta permite múltiplas escolhas, os percentuais não são parcelas exclusivas de um total e não devem ser somados.

## 2. Relação entre influências na trajetória e cotidiano profissional

Foi construída uma matriz de coocorrência entre as influências mencionadas na trajetória e os aspectos associados ao cotidiano profissional, seguida de visualização em mapa de calor.

Entre as coocorrências observadas estão:

- Autoaprendizado e curiosidade pessoal + resolução de problemas: 29 participantes.
- Formação acadêmica ou cursos + resolução de problemas: 26 participantes.

Esses números indicam que as duas alternativas foram assinaladas pelas mesmas pessoas. Não demonstram causalidade nem, por si só, uma associação estatística. A leitura deve considerar também a frequência de cada alternativa na amostra.

## 3. Correspondência entre realidade profissional e expectativa inicial

A pergunta foi respondida pelos 54 participantes, em escala numérica de 1 a 5. Como os rótulos dos extremos da escala não foram confirmados neste registro, os valores são apresentados numericamente, sem atribuir-lhes descrições verbais.

| Valor registrado | Participantes | Percentual |
|---|---:|---:|
| 1 | 1 | 1,85% |
| 2 | 3 | 5,56% |
| 3 | 22 | 40,74% |
| 4 | 17 | 31,48% |
| 5 | 11 | 20,37% |

Os valores 4 e 5 somam 28 participantes (51,85%); os valores 1 e 2 somam 4 participantes (7,41%). A interpretação substantiva depende da confirmação do significado dos pontos da escala no questionário original.

## 4. Correspondência entre realidade e expectativa por tempo de atuação

Foi cruzada a avaliação numérica com o tempo de atuação. Foram incluídos os 54 participantes, sem exclusões por ausência nessas variáveis.

A distribuição percentual dentro de cada grupo apresentou diferenças entre as faixas de tempo de atuação. Por exemplo, a categoria 3 correspondeu a 62,50% do grupo com menos de um ano e a 66,67% do grupo com 8–15 anos. No grupo de 1–3 anos, a categoria 4 correspondeu a 46,67%.

**Limite de interpretação:** trata-se de uma comparação exploratória. Os tamanhos dos grupos e a natureza não probabilística da amostra impedem concluir que o tempo de atuação explique as avaliações observadas.

## 5. Recomendações para quem está começando

A pergunta permitia até três escolhas. As frequências das alternativas predefinidas foram:

| Recomendação | Participantes | Percentual |
|---|---:|---:|
| Aprender continuamente | 38 | 70,37% |
| Buscar experiência prática | 30 | 55,56% |
| Desenvolver conhecimento técnico | 27 | 50,00% |
| Desenvolver habilidades comportamentais | 25 | 46,30% |
| Construir uma rede de contatos | 18 | 33,33% |
| Acompanhar tendências do mercado | 16 | 29,63% |
| Conhecer diferentes áreas da tecnologia | 11 | 20,37% |

Também foram identificadas duas contribuições adicionais registradas junto às respostas:

- “visão para a resolução de problemas”;
- “Visão de produto e conceitos sólidos de arquitetura”.

As contribuições foram preservadas como texto, sem incorporá-las automaticamente às alternativas predefinidas. Como a exportação reúne escolhas e texto na mesma coluna, a leitura deve respeitar essa limitação do formato exportado.

**Interpretação inicial:** aprender continuamente foi a alternativa mais assinalada, seguida de experiência prática e conhecimento técnico. Como era possível selecionar até três opções, os percentuais não são exclusivos.

## 6. Preparação e classificação exploratória das respostas abertas

A pergunta “Há algum alerta, tendência, recomendação ou outro ponto sobre sua experiência que você gostaria de registrar?” contém 24 respostas preenchidas e 30 registros vazios na base de 54 participantes.

Foram criados os arquivos:

- `docs/analise/respostas_abertas_para_analise.md`: cópia organizada para leitura das respostas;
- `docs/analise/classificacao_qualitativa.csv`: planilha de trabalho para classificação temática.

As respostas originais foram preservadas. A classificação temática é uma interpretação analítica exploratória, não uma estrutura prevista no questionário.

### Temas principais

Das 24 respostas preenchidas, 23 continham contribuição textual passível de classificação temática. Um registro continha apenas um endereço de e-mail e foi marcado como “Registro sem conteúdo temático”. A resposta sobre aplicar ferramentas à resolução de problemas, inicialmente pendente, foi classificada como “Resolução de problemas”.

| Tema principal | Respostas | Percentual das 23 respostas temáticas |
|---|---:|---:|
| Aprendizagem contínua | 8 | 34,8% |
| IA e produtividade | 3 | 13,0% |
| Fundamentos e preparação técnica | 2 | 8,7% |
| Prática e experiência | 2 | 8,7% |
| Comunicação profissional | 2 | 8,7% |
| Oportunidades profissionais | 1 | 4,3% |
| Transformação tecnológica | 1 | 4,3% |
| Resolução de problemas | 1 | 4,3% |
| Atualização tecnológica | 1 | 4,3% |
| Propósito e impacto coletivo | 1 | 4,3% |
| Colaboração e networking | 1 | 4,3% |

**Leitura preliminar:** aprendizagem contínua é o tema principal mais frequente. Também aparecem relatos sobre uso de IA e produtividade, fundamentos técnicos, prática, comunicação, oportunidades, transformação tecnológica e impacto coletivo.

### Temas secundários

A primeira contagem revelou variações de escrita, como “Fundamentos” e “fundamentos”. Foi aplicada uma normalização de espaços e maiúsculas/minúsculas, sem unir conceitos semanticamente diferentes.

Após essa normalização, os rótulos secundários mais frequentes foram:

- fundamentos: 5 ocorrências;
- aprendizagem contínua: 2;
- inteligência artificial: 2;
- troca de experiências: 2;
- pensamento crítico: 2;
- colaboração: 2;
- rede profissional: 2.

Os demais rótulos apareceram uma vez cada. A contagem refere-se aos rótulos registrados na classificação atual. Ela não equivale à frequência definitiva de todos os assuntos presentes nas respostas, pois ainda não foi feita uma consolidação semântica sistemática.

## 7. Decisões metodológicas registradas nesta etapa

1. Preservar os dados originais e manter os arquivos de análise como derivados.
2. Distinguir frequência de respostas, frequência de menções e coocorrência.
3. Não interpretar coocorrências como causalidade.
4. Não atribuir significado verbal à escala de 1 a 5 sem conferir os rótulos originais.
5. Preservar as contribuições adicionais da pergunta sobre recomendações sem forçá-las para categorias predefinidas.
6. Tratar a classificação das respostas abertas como exploratória e manter os textos originais acessíveis.
7. Normalizar variações de escrita dos temas secundários, sem agrupar automaticamente conceitos apenas parecidos.
8. Considerar que a amostra é não probabilística; os resultados descrevem os respondentes e não permitem generalização para todos os profissionais de tecnologia.

## 8. Situação do trabalho ao final desta sessão

**Concluído nesta etapa:**

- análise descritiva do perfil dos participantes;
- frequência das influências na trajetória profissional;
- frequência dos aspectos do cotidiano profissional;
- matriz de coocorrência entre trajetória e cotidiano, com visualização;
- distribuição da escala de correspondência entre realidade e expectativa;
- cruzamento exploratório dessa escala com tempo de atuação;
- frequência das recomendações para iniciantes e registro das duas contribuições adicionais;
- preparação das 24 respostas abertas, classificação temática inicial e contagem dos temas principais e secundários normalizados.

**Ainda pendente:**

- analisar as duas perguntas sobre uso de IA, cuja base efetiva é de 18 respostas, pois foram acrescentadas após as primeiras 36 respostas;
- revisar quais cruzamentos quantitativos adicionais respondem a perguntas relevantes para a pesquisa;
- decidir se a classificação qualitativa precisa de uma segunda rodada de revisão semântica e documentar seus critérios, caso realizada;
- integrar resultados, gráficos, interpretações e limitações no relatório final em HTML.

A análise de “como a pessoa ficou sabendo da pesquisa” não foi priorizada nesta etapa, por não ter sido identificada como necessária para responder às questões centrais do estudo.

---

*Registro atualizado em 29/10/2026 com base nos procedimentos e resultados visíveis no notebook de inspeção inicial. As etapas pendentes estão identificadas como pendentes e não são apresentadas como concluídas.*


---

# Registro de análise 04 — Pausa para auditoria da classificação qualitativa

**Data:** 30/10/2026  
**Projeto:** Um Olhar de Quem Está no Campo  
**Arquivos envolvidos:** `notebooks/01_inspecao_inicial.ipynb`, `notebooks/02_consolidacao_analitica.ipynb` e `docs/analise/classificacao_qualitativa.csv`

## 1. Contexto da decisão

Durante a revisão da etapa de respostas abertas, surgiu a necessidade de verificar se cada tema atribuído está coerente com a resposta original e se o CSV exportado corresponde à versão mais recente da classificação.

A pesquisadora decidiu interromper temporariamente o trabalho após essa revisão, para retomar com calma e evitar que possíveis inconsistências sejam levadas ao relatório final. A pausa é uma decisão de controle de qualidade; não significa que todo o trabalho anterior esteja errado.

## 2. Pontos identificados para verificação

A revisão preliminar apontou itens que precisam ser conferidos diretamente nos registros e no código antes de qualquer alteração definitiva:

- verificar a correspondência entre resposta original, tema principal, temas secundários e observação analítica;
- reexaminar classificações apontadas como possivelmente incompatíveis com o conteúdo das respostas;
- conferir a ordem das células que atribuem temas e exportam `classificacao_qualitativa.csv`, para garantir que o arquivo salvo reflita a última versão da classificação;
- confirmar a cobertura dos 24 registros preenchidos, distinguindo as 23 respostas com conteúdo temático do registro que contém apenas um endereço de e-mail;
- proteger dados pessoais desnecessários, especialmente o endereço de e-mail, caso o arquivo de classificação seja compartilhado ou incorporado a materiais de entrega;
- recalcular as frequências dos temas somente depois de concluída a revisão.

Esses itens são pendências de auditoria. As frequências e interpretações da classificação atual não devem ser tratadas como definitivas até a conferência.

## 3. Procedimento acordado para a retomada

A retomada deverá seguir esta ordem, sem refazer automaticamente as análises quantitativas já realizadas:

1. Conferir as 24 respostas preenchidas e seus identificadores.
2. Comparar cada resposta original com a classificação atribuída.
3. Registrar e justificar eventuais mudanças, preservando o texto original.
4. Verificar se todos os registros foram tratados segundo critérios consistentes.
5. Recalcular as contagens dos temas principais e secundários após a revisão.
6. Exportar novamente `docs/analise/classificacao_qualitativa.csv` somente depois de concluídas as atribuições.
7. Atualizar a síntese do Eixo 4 no Notebook 02 com os resultados revisados.
8. Manter explícitos os limites interpretativos e a distinção entre evidência textual e interpretação analítica.

## 4. O que permanece válido e o que está pendente

As análises descritivas quantitativas já registradas — perfil dos participantes, influências na trajetória, cotidiano profissional, coocorrências, escala de correspondência entre expectativa e realidade, cruzamentos exploratórios e recomendações para iniciantes — não são invalidadas automaticamente pela necessidade de auditar a classificação qualitativa.

A auditoria atual está concentrada na coerência e na rastreabilidade das respostas abertas e nos arquivos derivados dessa classificação. Qualquer conclusão sobre o alcance das correções deverá ser feita depois da verificação dos registros.

## 5. Estado do trabalho ao encerrar a sessão

**Concluído nesta sessão:**

- identificação da necessidade de uma auditoria de rastreabilidade da classificação qualitativa;
- definição da sequência de verificação antes de atualizar as frequências e a síntese analítica;
- decisão de pausar o trabalho antes de avançar para a triangulação com fontes externas.

**Pendente para a próxima sessão:**

- realizar a conferência sistemática das 24 respostas preenchidas;
- documentar eventuais alterações de classificação;
- confirmar a versão final do CSV exportado;
- atualizar a síntese qualitativa somente após a auditoria.

**Nota de processo:** seguir etapas documentadas e identificar a necessidade de revisão fazem parte de um processo analítico responsável. A identificação de pontos a conferir não significa que todas as etapas anteriores tenham sido executadas incorretamente. O objetivo da pausa é preservar a qualidade, a transparência e a rastreabilidade do trabalho.

---

*Registro atualizado em 30/10/2026. A auditoria qualitativa está planejada, mas ainda não foi concluída.*
