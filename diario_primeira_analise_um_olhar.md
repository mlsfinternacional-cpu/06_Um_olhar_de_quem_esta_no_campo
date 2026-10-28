# Diário de bordo — Minha primeira análise de dados do início ao fim

**Projeto:** Um Olhar de Quem Está no Campo  
**Data:** 27 de outubro de 2026  
**Etapa:** Da base bruta à primeira leitura analítica

## 1. Ponto de partida: o arquivo CSV

A pesquisa foi realizada por meio de um formulário on-line. As respostas foram exportadas para um arquivo CSV (*Comma-Separated Values*), um formato que armazena dados tabulares em linhas e colunas.

- Cada linha representa um registro — neste projeto, uma resposta.
- Cada coluna representa uma variável da pesquisa.

O objetivo foi começar a trabalhar com essa base no Python, preparando os dados para investigá-los com mais autonomia.

## 2. Leitura da base com pandas

No VS Code, o trabalho foi desenvolvido no notebook Jupyter:

`notebooks/01_inspecao_inicial.ipynb`

Utilizamos a biblioteca pandas para carregar o arquivo:

```python
import pandas as pd

df_original = pd.read_csv(
    arquivo_original,
    dtype="string",
    keep_default_na=False
)
```

- `pd.read_csv()` lê o arquivo CSV.
- `arquivo_original` indica o caminho do arquivo.
- `dtype="string"` carrega os campos como texto.
- `keep_default_na=False` mantém campos vazios como strings vazias durante a leitura.

O resultado foi armazenado em `df_original`, um DataFrame do pandas — uma estrutura tabular de linhas e colunas mantida na memória do Python.

Carregar o CSV não altera, por si só, o arquivo original no computador.

## 3. Inspeção inicial

A primeira inspeção identificou:

- **54 registros**;
- **17 colunas**.

Antes de calcular indicadores ou criar visualizações, era necessário conhecer a estrutura da base, identificar as variáveis disponíveis e investigar campos vazios.

Essa etapa ajuda a evitar interpretações incorretas causadas por desconhecimento da estrutura dos dados.

## 4. Criação de uma cópia de trabalho

Para não trabalhar diretamente sobre o DataFrame original, criamos uma cópia:

```python
df_analise = df_original.copy()
```

- `df_original` mantém a referência aos dados carregados.
- `df_analise` é a cópia utilizada para preparar os dados.

Essa separação favorece a rastreabilidade: é possível voltar à referência original e verificar as transformações realizadas na cópia.

## 5. Padronização dos nomes das colunas

Alguns cabeçalhos continham espaços excedentes no início ou no final. Aplicamos:

```python
df_analise.columns = df_analise.columns.str.strip()
```

O método `.str.strip()` remove espaços excedentes das extremidades dos nomes das colunas. Depois, verificamos se a padronização havia produzido nomes duplicados; nenhum cabeçalho duplicado foi identificado.

Essa transformação padronizou os nomes, sem alterar o conteúdo das respostas.

## 6. Identificação dos campos vazios

Como a leitura foi feita com `keep_default_na=False`, os campos vazios foram inicialmente mantidos como strings vazias. Para que pudessem ser tratados como valores ausentes, aplicamos:

```python
df_analise = df_analise.replace(
    r"^\s*$",
    pd.NA,
    regex=True
)
```

- `replace()` substitui valores que correspondem ao padrão informado.
- `r"^\s*$"` identifica textos vazios ou compostos apenas por espaços.
- `regex=True` habilita o uso de expressão regular.
- `pd.NA` representa um valor ausente no pandas.

Depois, contamos os valores ausentes por coluna:

```python
df_analise.isna().sum()
```

Foram identificadas ausências nas seguintes variáveis:

| Variável | Ausências |
|---|---:|
| Frequência de uso de ferramentas de IA | 36 |
| Finalidades de uso de IA | 36 |
| Como a pessoa soube da pesquisa | 36 |
| Pergunta aberta sobre alertas e recomendações | 30 |
| Contato opcional | 24 |
| `Coluna 13` | 54 |

**Ausência não significa necessariamente falta de resposta.** As três perguntas sobre IA e divulgação da pesquisa foram adicionadas depois das primeiras 36 respostas. Por isso, as 36 células vazias nessas perguntas são compatíveis com participantes que não tiveram acesso a elas. Não devem ser interpretadas automaticamente como recusa ou omissão.

A pergunta aberta e o campo de contato precisam ser interpretados de acordo com suas condições no formulário. A `Coluna 13` estava inteiramente vazia.

## 7. Salvamento da base analítica inicial

Após a preparação, salvamos uma versão derivada:

`data/derivados/base_analitica_inicial.csv`

O salvamento foi feito com:

```python
df_analise.to_csv(
    arquivo_derivado,
    index=False,
    encoding="utf-8-sig"
)
```

- `to_csv()` grava o DataFrame em um arquivo CSV.
- `index=False` evita adicionar o índice do pandas como uma coluna extra.
- `encoding="utf-8-sig"` favorece a compatibilidade com ferramentas como o Excel, inclusive com caracteres acentuados.

Depois, comparamos a base original e a derivada. Ambas tinham 54 linhas e 17 colunas, e o conteúdo das respostas foi preservado, considerando a padronização dos cabeçalhos e a representação dos campos vazios.

## 8. Criação da base analítica V1

A validação confirmou que `Coluna 13` estava inteiramente vazia: 54 ausências em 54 registros. Como não continha informação observável, ela foi excluída da versão analítica de trabalho.

A nova versão foi salva em:

`data/derivados/base_analitica_v1.csv`

| Indicador | Antes | Depois |
|---|---:|---:|
| Linhas | 54 | 54 |
| Colunas | 17 | 16 |

Nenhum participante foi excluído. A base anterior foi preservada.

A diferença entre a base inicial e a V1 é a exclusão da coluna inteiramente vazia. Essa transformação deve permanecer registrada para que seja possível compreender a origem da versão analítica.

## 9. Primeiras análises descritivas

A análise descritiva resume e organiza os dados observados. Começamos pelo perfil dos participantes, usando recursos como:

```python
df_v1["Estado"].value_counts()
```

O método `.value_counts()` conta a frequência de cada categoria. A partir dessas contagens, construímos tabelas de frequências absolutas e percentuais.

Entre os resultados observados:

- **46 participantes de Santa Catarina** (85,19%);
- **40 participantes do gênero masculino** (74,07%);
- **22 participantes com graduação** (40,74%);
- **14 participantes na faixa de 35–44 anos** e outros **14 na faixa de 45–54 anos**.

Esses números descrevem os participantes da pesquisa. Como a amostra é não probabilística, não devem ser generalizados automaticamente para todos os profissionais de tecnologia.

## 10. Análise das influências na trajetória profissional

Em seguida, investigamos a pergunta:

> O que mais influenciou sua trajetória na área em que atua hoje?

Na primeira tentativa, contamos as respostas completas. Como cada célula podia conter várias alternativas, o Python contou combinações de opções como categorias únicas. Isso não permitia saber quantas pessoas haviam mencionado cada influência individualmente.

Para separar as alternativas, utilizamos:

```python
respostas.str.split(", ").explode()
```

- `.str.split(", ")` divide cada resposta usando vírgula e espaço como delimitador.
- `.explode()` transforma os elementos separados em linhas individuais.

Depois, usamos `.value_counts()` para contar cada alternativa.

### Resultados

| Influência mencionada | Participantes | Percentual |
|---|---:|---:|
| Autaprendizado e curiosidade pessoal | 38 | 70,37% |
| Formação acadêmica ou cursos | 34 | 62,96% |
| Transição de outra carreira | 22 | 40,74% |
| Busca por estabilidade ou oportunidade de mercado | 13 | 24,07% |
| Indicação ou influência de rede de contatos | 7 | 12,96% |
| Acaso ou oportunidade inesperada | 7 | 12,96% |
| Familiares da área | 1 | 1,85% |

*Nota: os nomes das categorias foram transcritos da saída do notebook. Antes de publicar, conferir a grafia com as alternativas originais do formulário.*

Os percentuais podem somar mais de 100%, porque uma mesma pessoa pode mencionar várias influências.

### Interpretação inicial

- Autaprendizado e curiosidade pessoal foram a influência mais frequentemente mencionada.
- Formação acadêmica ou cursos também apareceu com frequência elevada.
- A transição de outra carreira foi mencionada por aproximadamente quatro em cada dez participantes.

Esses resultados descrevem as influências mencionadas, mas não demonstram, isoladamente, relações causais nem a importância objetiva de cada fator na trajetória individual.

### Cuidado técnico pendente

A separação foi feita usando vírgula e espaço como delimitador. Antes de consolidar os resultados, é necessário conferir se alguma alternativa original contém vírgulas internas, pois isso poderia dividir uma opção indevidamente.

## 11. O que foi construído nesta sessão

1. Leitura do CSV no Python.
2. Inspeção da estrutura da base.
3. Criação de uma cópia de trabalho.
4. Padronização dos nomes das colunas.
5. Identificação e tratamento dos campos vazios.
6. Interpretação inicial das ausências estruturais.
7. Salvamento da base analítica inicial.
8. Verificação da integridade dos registros.
9. Criação da base analítica V1, com 16 colunas.
10. Tabelas descritivas do perfil dos participantes.
11. Primeira análise das influências na trajetória profissional.
12. Registro dos resultados e dos cuidados metodológicos.

## 12. Mapa do processo

**CSV original → Inspeção → Preparação → Validação → Base analítica → Análise descritiva → Interpretação → Investigação de relações → Comunicação dos resultados**

| Etapa | Pergunta central |
|---|---|
| CSV original | Quais dados foram coletados? |
| Inspeção | Como a base está estruturada? |
| Preparação | O que precisamos padronizar ou tratar? |
| Validação | As transformações preservaram os dados relevantes? |
| Base analítica | Qual versão será utilizada nas análises? |
| Análise descritiva | O que aparece nos dados? |
| Interpretação | O que os resultados significam, dentro dos limites da pesquisa? |
| Investigação de relações | Como diferentes variáveis podem se relacionar? |
| Comunicação | Como apresentar os achados com clareza e responsabilidade? |

## 13. Recursos de Python utilizados

- `Path`: localizar arquivos e organizar caminhos.
- `pandas`: manipular dados tabulares.
- `read_csv()`: ler o CSV.
- `copy()`: criar uma cópia de trabalho.
- `.columns.str.strip()`: padronizar cabeçalhos.
- `replace()` e `pd.NA`: representar valores ausentes.
- `isna().sum()`: contar ausências.
- `shape`: verificar dimensões.
- `to_csv()`: salvar uma versão derivada.
- `value_counts()`: contar categorias.
- `str.split()` e `explode()`: separar alternativas combinadas.

Não é necessário memorizar todos os comandos de uma vez. O importante é compreender a finalidade de cada operação e reconhecer como ela contribui para o processo analítico.

## 14. Próxima etapa

A próxima sessão começará pela variável:

> O que mais define seu cotidiano profissional hoje?

O objetivo será examinar a estrutura das respostas, confirmar como as alternativas estão registradas, contar suas frequências e interpretar os resultados. Depois, poderemos começar a conectar o caminho percorrido pelos participantes com a realidade profissional que relatam.

---

## Reflexão de encerramento

Esta foi minha primeira análise desenvolvida a partir de uma base de dados de uma pesquisa que eu mesma realizei.

Antes, na análise do projeto Mão na Massa, eu me apoiava principalmente nas informações apresentadas pelo formulário. Desta vez, estou aprendendo a carregar os dados no Python, inspecionar sua estrutura, preparar uma versão analítica, verificar as transformações e produzir minhas próprias tabelas de frequência.

O aprendizado não está apenas nos comandos. Está em compreender o caminho entre os dados coletados, as decisões de preparação, os resultados calculados e a interpretação que posso fazer deles.

A experiência reforça o motivo pelo qual entrei no curso de Análise de Dados: desenvolver autonomia para investigar dados, verificar evidências e construir interpretações fundamentadas.

**Status ao final da sessão:** base analítica V1 criada e primeira análise descritiva iniciada. A pesquisa ainda está em andamento analítico; os resultados registrados são preliminares e devem ser validados antes da comunicação final.
