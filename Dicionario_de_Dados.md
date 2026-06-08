# Dicionário de Dados - Análise de Evasão em Sistemas de Informação

**Nome do arquivo:** `dados_alunos.csv`
**Tabela:** Histórico de Vínculo e Evasão dos Alunos
**Descrição:** [Preencha aqui com a descrição, ex: Dados demográficos básicos e o registro da trajetória de permanência (entrada e saída) dos alunos no curso.]
**Descrição das colunas:**

| Coluna | Tipo do Dado | Característica | Significado / Descrição |
| :--- | :--- | :--- | :--- |
| **ID_PESSOA** | Numérico (Inteiro) | Identificador Único | Código numérico que representa unicamente o aluno como pessoa física dentro dos sistemas da instituição. |
| **NOME_PESSOA** | Texto (String) | Categórica Nominal | Nome completo do aluno registrado oficialmente na universidade. |
| **SEXO** | Texto (Char) | Categórica Nominal | Indica o gênero biológico do discente, preenchido com as letras 'M' (Masculino) ou 'F' (Feminino). |
| **DT_NASCIMENTO** | Data (Date) | Temporal | Data de nascimento do aluno, útil para calcular a idade de ingresso ou evasão. |
| **FORMA_INGRESSO** | Texto (String) | Categórica Nominal | Método ou processo seletivo pelo qual o aluno entrou no curso (ex: SiSU, Vestibular, ENEM). |
| **FORMA_EVASAO** | Texto (String) | Categórica Nominal | Descreve o status final do vínculo do aluno, informando o motivo da saída (ex: Jubilamento, Desistência, Formado) ou se ainda está cursando (Sem Evasão). |
| **COD_CURSO** | Numérico (Inteiro) | Identificador Categórico | Código numérico padrão que representa o curso de graduação (ex: 30 para Sistemas de Informação). |
| **NOME_UNIDADE** | Texto (String) | Categórica Nominal | Nome por extenso do curso ou departamento ao qual o aluno está vinculado. |
| **MATR_ALUNO** | Texto (String) | Identificador Único | Número da matrícula acadêmica que identifica o vínculo do aluno com a instituição de ensino. |
| **NUM_VERSAO** | Texto (String) | Categórica Temporal | Representa o ano e semestre de aprovação do Projeto Pedagógico do Curso (PPC) ao qual o aluno está submetido (ex: grade 1996/1 ou 2008/1). |
| **PERIODO_INGRESSO** | Texto (String) | Temporal | Indica o ano e o semestre letivo exatos em que o aluno iniciou seus estudos na graduação. |
| **DT_EVASAO** | Data (Date) | Temporal | Data exata (dia, mês e ano) em que o encerramento do vínculo do aluno foi oficializado no sistema. |
| **PERIODO_EVASAO** | Texto (String) | Temporal | Indica o ano e o semestre letivo em que ocorreu a evasão, formatura ou encerramento da matrícula. |

---

**Nome do arquivo:** `dados_alunos_disciplinas.csv`
**Tabela:** Histórico de Disciplinas e Desempenho Acadêmico
**Descrição:** [Preencha aqui com a descrição, ex: Detalhamento da vida acadêmica do aluno semestre a semestre, registrando as disciplinas cursadas, notas obtidas e carga horária integralizada.]
**Descrição das colunas:**

| Coluna | Tipo do Dado | Característica | Significado / Descrição |
| :--- | :--- | :--- | :--- |
| **ID_PESSOA** | Numérico (Inteiro) | Identificador Relacional | Código único da pessoa física, que atua como chave de ligação com a Tabela 1. |
| **NOME_PESSOA** | Texto (String) | Categórica Nominal | Nome completo do aluno associado àquele registro de nota. |
| **ID_ALUNO** | Numérico (Inteiro) | Identificador Único | Código numérico interno de identificação do discente no módulo acadêmico. |
| **MATR_ALUNO** | Texto (String) | Identificador Único | Número de matrícula institucional do aluno vinculado ao curso. |
| **NUM_VERSAO** | Texto (String) | Categórica Temporal | Identifica a versão da grade curricular exigida para aquele discente específico. |
| **NOME_CURSO** | Texto (String) | Categórica Nominal | Nome por extenso do curso de graduação frequentado (Bacharelado em Sistemas de Informação). |
| **COD_CURSO** | Numérico (Inteiro) | Identificador Categórico | Código de referência do curso dentro da instituição. |
| **ID_VERSAO_CURSO** | Numérico (Inteiro) | Identificador Interno | Código numérico do sistema associado à versão do currículo. |
| **ANO** | Numérico (Inteiro) | Temporal | Ano letivo correspondente à oferta da disciplina cursada. |
| **COD_ATIV_CURRIC** | Texto (String) | Identificador Alfanumérico | Código de referência oficial da disciplina na grade (ex: CCJSA136). |
| **NOME_ATIV_CURRIC** | Texto (String) | Categórica Nominal | Nome por extenso da disciplina ou atividade curricular cursada. |
| **CREDITOS** | Numérico (Inteiro) | Quantitativa Discreta | Quantidade de créditos acadêmicos que a disciplina fornece ao ser concluída com êxito. |
| **MEDIA_FINAL** | Numérico (Decimal/Float) | Quantitativa Contínua | Nota final alcançada pelo aluno na disciplina, variando numa escala definida. |
| **DESCR_SITUACAO** | Texto (String) | Categórica Nominal | Indica o resultado do desempenho do aluno naquela atividade específica (ex: Aprovado, Reprovado). |
| **PERIODO** | Texto (String) | Temporal | Especifica em qual semestre ou ciclo do ano letivo a disciplina foi cursada. |
| **ID_CURSO_ALUNO** | Numérico (Inteiro) | Identificador do Vínculo | Código de banco de dados que amarra o aluno ao seu registro específico no curso. |
| **SITUACAO_ITEM** | Numérico (Inteiro) | Categórica Numérica | Código numérico interno de sistema que representa a situação da disciplina no histórico. |
| **CH_TEORICA** | Numérico (Inteiro) | Quantitativa Discreta | Representa a quantidade total de horas teóricas exigidas e cumpridas na disciplina. |
| **CH_PRATICA** | Numérico (Inteiro) | Quantitativa Discreta | Representa a quantidade total de horas práticas em laboratório ou projeto exigidas na disciplina. |
| **TOTAL_CARGA_HORARIA**| Numérico (Inteiro) | Quantitativa (Fórmula) | Soma das horas teóricas e práticas, representando o esforço total em horas exigido. |
| **FORMA_INGRESSO** | Texto (String) | Categórica Nominal | Replica a informação do método pelo qual o aluno ingressou na universidade. |
| **ANO_INGRESSO** | Numérico (Inteiro) | Temporal | O ano civil de entrada do aluno na graduação. |
| **FORMA_EVASÃO** | Texto (String) | Categórica Nominal | Replica o status atual do vínculo ou motivo de saída. |
| **ANO_EVASÃO** | Numérico (Inteiro/Nulo)| Temporal | Ano em que ocorreu a perda do vínculo, ficando nulo ou em branco para alunos ainda ativos. |
| **SEXO** | Texto (Char) | Categórica Nominal | Replica a informação do gênero do aluno no registro. |

---

**Nome do arquivo:** `dados_alunos_unicos1e2.csv`
**Tabela:** [Preencha com o nome/apelido da tabela]
**Descrição:** [Preencha aqui com uma breve descrição do que trata o arquivo, ex: consolidação de alunos únicos dos primeiros períodos.]
**Descrição das colunas:**

| Coluna | Tipo do Dado | Característica | Significado / Descrição |
| :--- | :--- | :--- | :--- |
| **[Nome_da_Coluna_1]** | [Tipo] | [Característica] | [Descrição/Significado da coluna 1] |
| **[Nome_da_Coluna_2]** | [Tipo] | [Característica] | [Descrição/Significado da coluna 2] |
| **[Nome_da_Coluna_3]** | [Tipo] | [Característica] | [Descrição/Significado da coluna 3] |

---

**Nome do arquivo:** `dados_disciplinas_periodo_1-8.csv`
**Tabela:** Perfil Socioeconômico e Desempenho Agrupado
**Descrição:** Compila o perfil sociodemográfico dos alunos e apresenta seu desempenho nas disciplinas de forma agrupada por faixas (bins), unificando os dados do 1º ao 8º período.
**Descrição das colunas:**

| Coluna | Tipo do Dado | Característica | Significado / Descrição |
| :--- | :--- | :--- | :--- |
| **ESTADO_CIVIL** | Texto (String) | Categórica Nominal | Indica o estado civil do aluno no momento do registro ou ingresso (ex: Solteiro(a)). |
| **IDADE** | Texto (String) | Categórica Ordinal | Faixa etária do discente agrupada em intervalos (ex: Menos de 19 anos, 19-25 anos). |
| **FORMA_INGRESSO** | Texto (String) | Categórica Nominal | Método pelo qual o aluno obteve sua vaga na instituição (ex: Vestibular). |
| **FORMA_EVASAO** | Texto (String) | Categórica Nominal | Status final do vínculo do aluno com a universidade (ex: Desistência, Formado, Jubilamento). |
| **ETNIA** | Texto (String) | Categórica Nominal | Autodeclaração de raça ou cor do aluno, conforme padrões do IBGE (ex: Branca, Não Declarada). |
| **DEFICIENCIAS** | Texto (String) | Categórica Nominal | Informa se o aluno declarou possuir algum tipo de deficiência ou necessidade especial. |
| **COTAS** | Texto (String) | Categórica Nominal | Categoria de concorrência ou tipo de ação afirmativa utilizada pelo aluno no ingresso (ex: Ampla Concorrência). |
| **NOME_DISCIPLINA** | Texto (String) | Categórica Nominal | Nome por extenso da atividade curricular cursada pelo discente (ex: Álgebra Linear, Inglês Técnico). |
| **SITUACAO_DISCIPLINA** | Texto (String) | Categórica Nominal | Resultado acadêmico final obtido na disciplina (ex: Aprovado, Reprovado, Trancamento Parcial). |
| **MEDIA_FINAL** | Texto (String) | Categórica Ordinal | Faixa de nota final obtida pelo aluno, discretizada em intervalos de valores (ex: 8-10, 5-8, 0-5). |
| **FALTAS** | Texto (String) | Categórica Ordinal | Percentual de ausências do aluno na disciplina, agrupado em faixas percentuais (ex: 0-5%, Acima de 25%). |
| **BOLSA** | Texto (String) | Categórica Binária | Indica se o aluno era beneficiário de algum programa de auxílio financeiro ou bolsa acadêmica (Possuía / Não Possuía). |

