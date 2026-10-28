# Dicionário de Dados
## Projeto: Um Olhar de Quem Está no Campo

## 1. Identificação da base

- **Projeto:** Um Olhar de Quem Está no Campo
- **Etapa:** Inspeção estrutural e documentação das variáveis
- **Arquivo identificado no inventário:** `Pesquisa — Um Olhar de Quem Está no Campo - BASELINE_36_RESPOSTAS.csv`
- **Registros encontrados na inspeção:** 54
- **Colunas encontradas:** 17
- **Data da documentação:** 27/10/2026
- **Status:** versão inicial do dicionário; significados e algumas condições de preenchimento ainda dependem de conferência com o formulário original.

> **Nota de rastreabilidade:** o nome do arquivo contém `BASELINE_36_RESPOSTAS`, enquanto a inspeção do notebook identificou 54 registros. A pesquisa passou a incluir três perguntas adicionais após a 36ª resposta. Registrar essa particularidade ajuda a explicar a estrutura da base; não significa que os registros devam ser removidos ou que a base esteja errada.

## 2. Objetivo

Documentar os nomes originais das colunas, o significado de cada variável, o tipo observado, os valores encontrados e as particularidades de preenchimento. Este documento orienta a análise e registra as pendências metodológicas sem alterar a base original.

## 3. Dicionário de variáveis

**Como interpretar a coluna “Valores sem conteúdo”:** a contagem considera células nulas ou vazias/apenas com espaços, conforme a inspeção feita no notebook. Ela não equivale automaticamente a “não resposta”: é necessário considerar quando a pergunta passou a existir e se o preenchimento era opcional.

| Nº | Nome original da coluna | Tipo observado | Valores sem conteúdo | % sem conteúdo | Valores distintos observados | Significado / uso da variável | Observações metodológicas |
|---:|---|---|---:|---:|---:|---|---|
| 1 | `Carimbo de data/hora` | Texto (`str`) | 0 | 0,00% | 54 | Data e hora de envio da resposta. | Útil para ordenar registros e documentar o período de coleta. Não usar o horário, isoladamente, como evidência de duplicidade. |
| 2 | `Estado` | Texto (`str`) | 0 | 0,00% | 8 | Estado informado pela pessoa respondente. | Variável de localização declarada. Confirmar categorias exatas no formulário e padronizar somente se houver justificativa documentada. |
| 3 | `Gênero` | Texto (`str`) | 0 | 0,00% | 3 | Categoria de gênero selecionada pela pessoa respondente. | Preservar as categorias originais; não inferir identidade além do que foi declarado. |
| 4 | `Escolaridade` | Texto (`str`) | 0 | 0,00% | 6 | Escolaridade informada. | Confirmar opções e ordem das categorias no instrumento original. |
| 5 | `Faixa Etária` | Texto (`str`) | 0 | 0,00% | 6 | Faixa etária selecionada. | Tratar como variável categórica ordinal apenas se a ordem das faixas for confirmada no questionário. |
| 6 | ` Área de Atuação` | Texto (`str`) | 0 | 0,00% | 34 | Área profissional de atuação informada. | O nome original contém espaço inicial; preservá-lo nesta documentação de origem. Há 34 valores distintos, o que pode refletir áreas variadas e/ou respostas de texto livre. |
| 7 | ` Tempo de atuação na Área` | Texto (`str`) | 0 | 0,00% | 5 | Tempo de atuação na área informado. | O nome original contém espaço inicial. Confirmar categorias e sua ordem no formulário. |
| 8 | `O que mais influenciou sua trajetória na área em que atua hoje? \n` | Texto (`str`) | 0 | 0,00% | 19 | Fator(es) que influenciaram a trajetória profissional. | Confirmar se a pergunta permitia uma única resposta ou múltiplas seleções. Os valores distintos, por si sós, não permitem determinar isso. |
| 9 | `O que mais define seu cotidiano profissional hoje? ` | Texto (`str`) | 0 | 0,00% | 39 | Aspectos que definem o cotidiano profissional. | Confirmar se aceita múltiplas seleções e como as respostas são armazenadas na exportação. |
| 10 | `Quanto sua realidade profissional corresponde ao que você imaginava quando começou? ` | Texto (`str`) | 0 | 0,00% | 5 | Percepção de correspondência entre a realidade profissional atual e as expectativas iniciais. | A inspeção encontrou cinco valores distintos. Não interpretar como satisfação no trabalho: a pergunta trata de correspondência entre expectativa e realidade. Confirmar a escala e os rótulos originais. |
| 11 | `O que você considera mais importante para quem está começando na sua área? ` | Texto (`str`) | 0 | 0,00% | 35 | Recomendações ou aspectos considerados importantes para iniciantes. | Confirmar se a pergunta permitia múltiplas seleções e/ou resposta aberta. |
| 12 | `Há algum alerta, tendência, recomendação ou outro ponto sobre sua experiência que você gostaria de registrar?  ` | Texto (`str`) | 30 | 55,56% | 25 | Campo para comentário ou recomendação adicional sobre a experiência profissional. | Campo de texto aberto. Confirmar no formulário se era opcional e se a exportação deixa respostas não preenchidas como células vazias. Não classificar automaticamente as ausências como erro. |
| 13 | `CONTATO — OPCIONAL  \nQuer receber os resultados da pesquisa ou manter contato? Se desejar, deixe seu e-mail ou LinkedIn ` | Texto (`str`) | 24 | 44,44% | 31 | Contato voluntário para receber resultados ou manter contato. | Campo identificado como opcional. Tratar os dados de contato com cuidado e não os incluir em produtos públicos sem base adequada e avaliação de privacidade. |
| 14 | `Com que frequência você utiliza ferramentas de IA generativa (ex: ChatGPT, Copilot, Claude) no seu trabalho com dados?  ` | Texto (`str`) | 36 | 66,67% | 4 | Frequência de uso de ferramentas de IA generativa no trabalho com dados. | Pergunta incluída após a 36ª resposta. Base efetiva esperada: 18 participantes. As 36 células vazias anteriores são ausência estrutural, não não resposta. |
| 15 | `Para quais dessas finalidades você já utilizou IA no seu trabalho? (marque todas que se aplicam)` | Texto (`str`) | 36 | 66,67% | 16 | Finalidades para as quais a pessoa utilizou IA no trabalho. | Pergunta incluída após a 36ª resposta. Base efetiva esperada: 18 participantes. A indicação “marque todas” aponta para múltipla seleção; verificar como as seleções foram serializadas no CSV antes de contar frequências. |
| 16 | `Como você ficou sabendo desta pesquisa?  ` | Texto (`str`) | 36 | 66,67% | 2 | Canal pelo qual a pessoa soube da pesquisa. | Pergunta incluída após a 36ª resposta. Base efetiva esperada: 18 participantes. As 36 células vazias anteriores são ausência estrutural, não não resposta. |
| 17 | `Coluna 13` | Texto (`str`) | 54 | 100,00% | 1 | Ainda não determinado. | Coluna sem conteúdo em todos os registros. Investigar a origem no arquivo exportado e no formulário. Não remover da base original; eventual exclusão de uma cópia analítica deve ser registrada e justificada. |

## 4. Resumo das ausências identificadas

| Campo | Registros sem conteúdo | Percentual | Leitura inicial |
|---|---:|---:|---|
| Pergunta aberta sobre alertas, tendências e recomendações | 30 de 54 | 55,56% | Verificar se era opcional e confirmar o comportamento do campo no formulário. |
| Contato opcional | 24 de 54 | 44,44% | A ausência é compatível com o caráter opcional do campo. |
| Frequência de uso de IA | 36 de 54 | 66,67% | Ausência estrutural nas respostas anteriores à inclusão da pergunta; base efetiva esperada de 18. |
| Finalidades de uso de IA | 36 de 54 | 66,67% | Ausência estrutural nas respostas anteriores à inclusão da pergunta; base efetiva esperada de 18. |
| Canal de descoberta da pesquisa | 36 de 54 | 66,67% | Ausência estrutural nas respostas anteriores à inclusão da pergunta; base efetiva esperada de 18. |
| `Coluna 13` | 54 de 54 | 100,00% | Campo completamente vazio; origem a investigar. |

**Importante:** a tabela de inspeção inicial que reportou “valores ausentes = 0” usou a definição de nulos do pandas. Células com strings vazias ou espaços podem não ser contabilizadas como nulas por esse método. Para a análise de completude, usar a verificação que considera nulos e conteúdo vazio, mantendo documentada a regra aplicada.

## 5. Decisões e cuidados metodológicos

1. A base original deve permanecer preservada e sem alterações nesta etapa.
2. Nenhum registro foi removido.
3. Nenhuma coluna foi removida ou renomeada na base original.
4. Nenhum valor ausente foi preenchido ou imputado.
5. Os nomes originais das colunas são mantidos para garantir correspondência com o arquivo de origem.
6. As perguntas sobre frequência de uso de IA, finalidades de uso de IA e canal de descoberta foram adicionadas após a resposta 36; a base efetiva esperada dessas variáveis é de 18 participantes.
7. Ausência estrutural não deve ser tratada como não resposta.
8. A ausência no campo de contato não é, por si só, inconsistência, porque o campo é opcional.
9. O campo aberto sobre alertas precisa ser conferido no instrumento para determinar sua obrigatoriedade.
10. A coluna `Coluna 13` deve ser investigada antes de qualquer decisão de exclusão em uma base derivada.
11. O tipo `str` indica como o pandas leu os valores; não determina, por si só, o tipo conceitual da variável.
12. Não iniciar cruzamentos ou gráficos antes de validar os significados, as categorias e as regras de contagem das variáveis.

## 6. Pendências para validação

- [ ] Confirmar a origem e a versão exata do CSV usado na inspeção, registrando a diferença entre o nome `BASELINE_36_RESPOSTAS` e os 54 registros identificados.
- [ ] Conferir cada pergunta e suas opções no formulário original.
- [ ] Confirmar quais perguntas permitiam múltiplas seleções.
- [ ] Confirmar se a pergunta aberta sobre alertas era obrigatória ou opcional.
- [ ] Investigar a origem da coluna `Coluna 13`.
- [ ] Conferir a representação das respostas de múltipla seleção no CSV.
- [ ] Validar a quantidade efetiva de respostas de cada variável usando a regra de ausência documentada.
- [ ] Completar categorias e valores permitidos com base no formulário, sem inferi-los apenas pelos valores distintos.

## 7. Critério de conclusão

O dicionário será considerado validado quando os significados, as opções de resposta, os tipos conceituais, as regras de preenchimento e as particularidades de ausência de todas as variáveis tiverem sido conferidos com o instrumento original e documentados.

Até lá, este arquivo deve ser tratado como **dicionário inicial em validação**, e não como versão metodológica definitiva.

## 8. Critério de rastreabilidade das decisões futuras

Toda decisão de tratamento deve registrar:

- **Campo afetado:** nome original da coluna.
- **Evidência:** resultado observado na base ou no instrumento.
- **Decisão:** ação adotada ou decisão de não alterar.
- **Justificativa:** razão metodológica.
- **Efeito esperado:** consequência para a análise.
- **Data e localização do registro:** quando e onde a decisão foi documentada.

A documentação não autoriza, por si só, a publicação da base bruta. Antes de compartilhar dados, avaliar consentimento, privacidade e risco de identificação, especialmente em campos de contato e respostas textuais.
