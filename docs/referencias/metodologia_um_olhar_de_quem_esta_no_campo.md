# Metodologia — "Um Olhar de Quem Está no Campo"

## 1. Objetivo

Reunir experiências e percepções de profissionais que atuam em diferentes frentes da área de tecnologia, com foco em trajetória de carreira, realidade profissional cotidiana e recomendações para quem está começando na área.

O questionário foi construído no âmbito da formação em Análise de Dados, Visualização de Dados e Business Intelligence do Programa SCTEC (iniciativa do Governo de Santa Catarina em parceria com o SENAI/SC), com uso restrito a fins de aprendizagem e pesquisa dentro do processo de Mentoria de Carreira.

## 2. Realização

- **Pesquisa e condução** — Maria Laura Corrêa da Silva
- **Mentoria** — Helena Vaz Trindade

## 3. Desenho metodológico

- **Tipo:** pesquisa quantitativa e qualitativa combinada (survey autoaplicado)
- **Instrumento:** questionário estruturado online, com perguntas de múltipla escolha, caixas de seleção, escala linear e campos abertos (parágrafo e resposta curta)
- **Distribuição:** compartilhamento direto via LinkedIn (rede de contatos da pesquisadora e da mentora), indicação em cadeia ("conhece alguém que possa contribuir? envie o link"), e divulgação pontual no chat da transmissão ao vivo do Startup Summit 2026
- **Amostragem:** não probabilística, por conveniência e indicação (snowball)

## 4. Período de coleta

**Início: 14 de agosto de 2026**
**Encerramento previsto: 18 de setembro de 2026 (em possível extensão)**

A equipe Meet SGB solicitou a extensão do prazo de coleta. A nova data de encerramento ainda será confirmada; este documento será atualizado assim que definida.

## 5. Amostra

- **N = 36 respondentes** até o marco `BASELINE_36_RESPOSTAS` (em crescimento contínuo até o encerramento da coleta)
- A partir da resposta 37, o instrumento passou a coletar três novas variáveis (ver Seção 6.1 e Seção 7.1). A amostra segue única e contínua — o marco de 36 não é um corte de coleta, mas um marco de **evolução do instrumento** (schema evolution), registrado para permitir leitura correta dos dados ausentes nas novas variáveis.

## 6. Estrutura do questionário

### Bloco 1 — Perfil Profissional
- Estado (todas as 27 UFs + opção "Outro / Fora do Brasil")
- Gênero (Feminino, Masculino, Outra identidade de gênero, Prefiro não informar, Outro)
- Escolaridade (Ensino médio a Doutorado, + Outro)
- Faixa etária (Até 24 até 55 ou mais, + Prefiro não informar)
- Área de atuação (múltipla escolha — Análise de Dados/Analytics, BI, Engenharia de Dados, Ciência de Dados, IA/Machine Learning, Desenvolvimento de Software, Cloud, DevOps/SRE, Cibersegurança, Produto, UX/UI, Automação/RPA, Arquitetura de Soluções, Governança de Dados, Gestão de Projetos em Tecnologia, + Outro)
- Tempo de atuação na área (Menos de 1 ano a Mais de 15 anos)

### Bloco 2 — Jornada
- O que mais influenciou sua trajetória na área em que atua hoje? (seleção de até 3 — formação acadêmica, autoaprendizado, transição de carreira, indicação/rede, busca por estabilidade, acaso, + Outro)
- **REALIDADE** — O que mais define seu cotidiano profissional hoje? (seleção de até 4 — resolução de problemas, conhecimento técnico, aprendizado contínuo, comunicação e colaboração, criatividade, adaptação a mudanças, prazos e pressão por entregas, gestão de prioridades, autonomia, + Outro)
- Escala linear (1–5): Quanto sua realidade profissional corresponde ao que você imaginava quando começou? ("Nada corresponde" a "Corresponde totalmente")

### Bloco 2.1 — Uso de IA no trabalho *(variáveis adicionadas — ver Seção 6.1)*
- Com que frequência você utiliza ferramentas de IA generativa no seu trabalho?
- Para quais dessas finalidades você já utilizou IA no seu trabalho? (múltipla escolha, por função)

### Bloco 3 — Olhando para Frente
- O que você considera mais importante para quem está começando na sua área? (seleção de até 3 — conhecimento técnico, aprendizado contínuo, habilidades comportamentais, experiência prática, rede de contatos, tendências de mercado, conhecer diferentes áreas da tecnologia, + Outro)
- Campo aberto (parágrafo, opcional): "Há algum alerta, tendência, recomendação ou outro ponto sobre sua experiência que você gostaria de registrar?"
- Como você ficou sabendo desta pesquisa? *(variável adicionada — ver Seção 6.1)*
- Contato — opcional (resposta curta): e-mail ou LinkedIn, para quem deseja receber os resultados ou manter contato

### 6.1 Evolução do instrumento (schema evolution)

Após o marco de 36 respostas, três novas variáveis foram incorporadas ao questionário:

1. **Frequência de uso de IA** — escala de frequência ancorada (não utilizo / algumas vezes por mês / algumas vezes por semana / diariamente ou quase todos os dias / integrado ao fluxo de trabalho), substituindo advérbios subjetivos ("raramente", "às vezes") por unidades de tempo concretas, reduzindo variação de ancoragem entre respondentes.
2. **Finalidade de uso de IA** — múltipla escolha organizada por *função de trabalho* (geração/revisão de código, análise e interpretação de dados, redação e revisão de textos, automação de tarefas, pesquisa e síntese, planejamento e apoio à decisão, criação de conteúdo visual/design, construção de soluções com IA, nunca utilizei). O critério de função — em vez de tarefa técnica específica — foi escolhido para contemplar a amplitude de áreas já mapeada no Bloco 1 (Produto, UX/UI, Governança, Gestão de Projetos, etc.), e não apenas perfis de programação.
3. **Canal de descoberta da pesquisa** (LinkedIn, Instagram, WhatsApp, Curso/evento/instituição, Outro) — categorizado por um único eixo (canal), evitando sobreposição categórica com dimensões de mecanismo social (ex.: "grupo/comunidade" e "indicação pessoal" podem ocorrer dentro de qualquer um dos canais listados, e por isso não constam como opções à parte).

**Justificativa da inclusão:** a decisão de acrescentar as variáveis de uso de IA partiu da leitura cruzada com a ementa pedagógica de uma pós-graduação em Data Science + IA, cuja estrutura curricular (prompt engineering avançado, RAG, fine-tuning de LLMs, guardrails em produção, MLOps) evidencia que a integração de IA ao fluxo de trabalho passou a ser um eixo relevante de formação e, por extensão, um traço relevante do perfil profissional que esta pesquisa busca descrever.

## 7. Tratamento e qualidade dos dados

- Respostas do campo aberto de alerta/recomendação e do campo de contato opcional são tratadas separadamente na tabulação, pois há sobreposição observada: pelo menos um caso de contato (e-mail) preenchido no campo de texto livre destinado a alerta/recomendação, em vez do campo de contato logo abaixo. Nesses casos, a resposta é reclassificada manualmente: removida da análise de conteúdo qualitativo e realocada para a base de contatos de outreach.
- Respostas "Outro" nos campos de seleção múltipla são revisadas manualmente para identificar se representam uma nova categoria recorrente (candidata a virar opção fixa em rodadas futuras) ou um caso isolado.
- Nenhuma resposta é descartada da amostra total (N) por conta desse tipo de inconsistência — apenas realocada para o campo correto na tabulação.
- **Verificação de possível duplicidade de respondentes:** dado que o questionário não coleta identificador único (Seção 8), a checagem de duplicidade é feita por similaridade, não por confirmação direta. Respostas com timestamp muito próximo, combinação idêntica de campos fechados (Estado, Área de Atuação, Faixa Etária, Tempo de Atuação) e/ou texto do campo aberto quase idêntico são sinalizadas manualmente para revisão. Nenhuma resposta sinalizada é removida automaticamente da amostra — a similaridade é um indício, não uma prova, dado que duas pessoas reais podem legitimamente coincidir em respostas de campos fechados. Casos sinalizados são documentados à parte e considerados na leitura qualitativa dos resultados.
- **Nota sobre aglomerados de timestamp:** nos dias do Startup Summit 2026, o link da pesquisa foi divulgado diretamente no chat da transmissão ao vivo. Isso gera aglomerados legítimos de respostas com poucos segundos de diferença entre si (múltiplas pessoas respondendo simultaneamente ao mesmo estímulo). Esses aglomerados, por si só, não devem ser tratados como indício de duplicidade — o critério de sinalização (item acima) só se aplica quando o timestamp próximo vem acompanhado de coincidência nos demais campos.

### 7.1 Dados ausentes por evolução do instrumento

Respondentes 1 a 36 (marco `BASELINE_36_RESPOSTAS`) não possuem valor registrado nas três variáveis descritas na Seção 6.1, porque essas perguntas não existiam no instrumento no momento em que responderam — e não porque tenham deixado de respondê-las.

Essa ausência é tratada como **estrutural**, não como nonresponse:
- Não entra no cálculo de taxa de não-resposta das novas variáveis.
- Não é imputada nem tratada como "Prefiro não informar".
- Qualquer análise das variáveis de uso de IA e de canal de descoberta deve reportar sua base amostral efetiva (N a partir da resposta 37), não o N total da pesquisa, evitando subestimar as proporções por diluição com respondentes que nunca viram a pergunta.

## 8. Ética e LGPD

- Participação voluntária, sem obrigatoriedade de identificação.
- **Minimização de dados por padrão:** o questionário não solicita nome nem CPF em nenhum momento. Não há campo de identificação obrigatória em nenhuma etapa da pesquisa.
- Coleta de contato (e-mail/LinkedIn) é explicitamente opcional, separada das demais respostas e de iniciativa exclusiva do respondente — quem não deseja se identificar permanece completamente anônimo.
- Essa escolha de desenho tem também um efeito metodológico: por não haver rastreabilidade da resposta até a pessoa, reduz-se o incentivo à desejabilidade social, favorecendo respostas mais honestas nos campos de percepção e experiência subjetiva (Bloco 2 — Jornada).
- Dados tratados exclusivamente para fins de aprendizagem e pesquisa no âmbito da Mentoria de Carreira (SCTEC/SENAI-SC), em conformidade com a Lei Geral de Proteção de Dados (LGPD).
- Contatos que deixaram informações recebem retorno direto (agradecimento) por parte da pesquisadora.

## 9. Limitações

- Amostragem não probabilística (conveniência/indicação): os resultados não são representativos do universo de profissionais de tecnologia no Brasil, refletindo majoritariamente a rede de contatos da pesquisadora e da mentora no LinkedIn.
- Possível viés de desejabilidade social em respostas de caráter mais simbólico ou reflexivo.
- Distribuição concentrada em Santa Catarina, dado o ponto de partida da divulgação (a confirmar quantitativamente na análise de "Estado").
- Como contrapartida ao desenho anônimo (ver Seção 8): não é possível verificar duplicidade de respondentes nem realizar acompanhamento longitudinal de quem não deixou contato voluntariamente.
- As variáveis de uso de IA e canal de descoberta (Seção 6.1) têm base amostral menor e temporalmente posterior ao restante do instrumento (ver Seção 7.1), o que impede comparações diretas de proporção com as demais variáveis do questionário sem ajuste de base.

## 10. Próximos passos

- Confirmar nova data de encerramento da coleta (extensão solicitada pela equipe Meet SGB).
- Consolidação da análise integrada por bloco (Perfil, Jornada, Realidade, Uso de IA, Olhando para Frente).
- **Cruzamentos analíticos:** ainda não estabelecidos. A definir conforme os padrões que emergirem na base consolidada — candidatos possíveis incluem tempo de atuação x percepção de correspondência com a expectativa inicial (escala linear), área de atuação x principais influências na trajetória, faixa etária x visão sobre o que é mais importante para quem está começando, e (a partir da base pós-resposta 37) área de atuação x finalidade de uso de IA. A confirmar.
- Devolutiva aos respondentes que deixaram contato.
