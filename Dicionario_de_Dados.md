# Dicionário de Dados - Análise de Evasão em Sistemas de Informação

---

**Nome do arquivo:** `dados_alunos.csv`
**Tabela:** Histórico Acadêmico, Vínculo e Evasão dos Alunos
**Descrição:** Dados cadastrais, demográficos, socioeconômicos e de ingresso/evasão dos discentes, integrados ao registro completo de sua trajetória acadêmica em disciplinas (notas, faltas, situação e carga horária).
**Descrição das colunas:**
  
| Coluna | Tipo do Dado | Característica | Significado / Descrição |
| :--- | :--- | :--- | :--- |
| **Seq** | Numérico (Inteiro) | Identificador Sequencial | Número sequencial incremental que serve como identificador único da linha/registro no arquivo. |
| **ID** | Texto (String) | Identificador Único | Código hash (MD5) que identifica anonimamente cada aluno, preservando sua privacidade nos sistemas institucionais. |
| **COD_CURSO** | Numérico (Inteiro) | Identificador Categórico | Código numérico oficial padrão que representa o curso de graduação do aluno (ex: 30 para Sistemas de Informação). |
| **NOME_CURSO** | Texto (String) | Categórica Nominal | Nome completo do curso superior ao qual o aluno está vinculado (ex: Bacharelado em Sistemas de Informação) |
| **NIVEL_CURSO** | Texto (String) | Categórica Nominal | Nível acadêmico da formação ofertada pela instituição (ex: Graduação). |
| **TIPO_CURSO** | Texto (String) | Categórica Nominal | Classificação administrativa do tipo de estrutura acadêmica (ex: Curso). |
| **MODALIDADE_CURSO** | Texto (String) | Categórica Nominal | Indica a modalidade de ensino do curso (ex: Bacharelado, Licenciatura) |
| **TURNO_CURSO** | Texto (String) | Categórica Nominal | Turno de oferta regular das aulas do curso (ex: Integral, Noturno, Matutino). |
| **ESTADO_CIVIL** | Texto (String) | Categórica Nominal | Estado civil do estudante registrado no cadastro acadêmico (ex: Solteiro(a), Casado(a)). |
| **GENERO** | Texto (String) | Categórica Nominal | Identificação de gênero ou sexo biológico do aluno (pode estar em branco ou omitido em alguns registros). |
| **DT_NASCIMENTO** | Data (Date) | Temporal | Data de nascimento do aluno no formato AAAA-MM-DD, útil para análises de faixa etária no ingresso e evasão. |
| **ANO_INGRESSO** | Numérico (Inteiro) | Temporal | Ano civil em que o aluno iniciou oficialmente o seu vínculo com o curso de graduação (ex: 2019). |
| **FORMA_INGRESSO** | Texto (String) | Categórica Nominal | Método ou processo seletivo oficial utilizado pelo discente para ingressar no curso (ex: Processo Seletivo - SiSU, Transferência Externa, Portador de Diploma Superior). |
| **ANO_EVASAO** | Numérico (Inteiro) | Temporal | Ano civil em que foi oficializado o encerramento ou interrupção do vínculo do discente. Fica em branco se não houver evasão. |
| **FORMA_EVASAO** | Texto (String) | Categórica Nominal | Descreve o motivo do encerramento do vínculo (ex: Jubilamento, Desistência, Transferido) ou se o aluno permanece ativo (Sem Evasão). |
| **NATURALIDADE** | Texto (String) | Categórica Nominal | Cidade e Estado de nascimento do aluno (ex: Porto Walter-AC, Rio Branco-AC, Assis Chateaubriand-PR). |
| **RACA_CENSO** | Texto (String) | Categórica Nominal | Autodeclaração de raça ou cor do discente seguindo as categorias padrão do Censo da Educação Superior (ex: 1.Branca, 2.Preta, 4.Parda, Não Declarada). |
| **ETNIA** | Texto (String) | Categórica Nominal | Especificação de etnia, utilizado primariamente para autodeclaração de povos indígenas. |
| **DEFICIENCIAS** | Texto (String) | Categórica Nominal | Indica a presença de alguma deficiência informada pelo aluno ou "Sem Deficiência". |
| **BOLSAS** | Texto (String) | Categórica Nominal | Registro histórico concatenado por ponto e vírgula de todos os auxílios financeiros e bolas acadêmicas que o aluno recebeu. |
| **BAIRRO** | Texto (String) | Categórica Nominal | Bairro residencial declarado no cadastro de endereço do discente (ex: Base, Vitória, Portal da Amazônia). |
| **MUNICIPIO** | Texto (String) | Categórica Nominal | Município onde se localiza a residência atual do aluno (ex: Rio Branco, Itajubá). |
| **ESTADO** | Texto (String) | Categórica Nominal | Unidade Federativa (UF) da residência atual do aluno (ex: Acre, Minas Gerais). |
| **INFO_COTAS** | Texto (String) | Categórica Nominal | Categoria de concorrência ou política de ações afirmativas pela qual o estudante ingressou (ex: Ampla Concorrência, L2 - Candidatos de Escola Pública com Baixa Renda PPI). |
| **COD_DISCIPLINA** | Texto (String) | Identificador Categórico | Código alfanumérico padrão de identificação da disciplina (ex: CCET010 para Lógica para Computação, CELA465 para Leitura e Produção de Textos Técnicos). |
| **NOME_DISCIPLINA** | Texto (String) | Categórica Nominal | Nome oficial completo da disciplina cursada pelo aluno (ex: Lógica para Computação). |
| **ANO_DISCIPLINA** | Numérico (Inteiro) | Temporal | Ano letivo no qual a matrícula na respectiva disciplina foi efetuada e cursada (ex: 2019, 2021). |
| **PERIODO_DISCIPLINA** | Texto (String) | Temporal | Período ou semestre letivo específico em que a disciplina foi cursada (ex: 1° Semestre, 2° Semestre, PLE/ERE). |
| **SITUACAO_DISCIPLINA** | Texto (String) | Categórica Nominal | Situação e resultado final do aluno após o encerramento do período na disciplina (ex: Aprovado, Reprovado, Reprovado por Freqüência, Trancamento Parcial, Matrícula). |
| **CH_TOTAL** | Numérico (Decimal) | Quantitativa Contínua | Carga horária total da disciplina expressa em horas (ex: 60.00, 30.00, 90.00). |
| **CREDITOS** | Numérico (Inteiro) | Quantitativa | Quantidade de créditos acadêmicos que a disciplina integraliza no histórico (ex: 3, 4). |
| **MEDIA_FINAL** | Numérico (Decimal) | Quantitativa Contínua | Nota média final obtida pelo aluno após o encerramento da disciplina (ex: 8.00, 0.00, 2.58). |
| **NUM_FALTAS** | Numérico (Inteiro) | Quantitativa Discreta | Quantidade total de faltas computadas para o aluno na disciplina ao longo do semestre. |
| **PERIODO_IDEAL** | Numérico (Inteiro) | Categórica Ordinal | Semestre aconselhado na estrutura curricular do Projeto Pedagógico (PPC) para cursar a referida disciplina (ex: 1, 2). |
| **COD_CURSO_OFERTA_DISC** | Numérico (Inteiro) | Identificador Categórico | Código oficial do curso de graduação que foi responsável por ofertar administrativamente a turma da disciplina (ex: 30, 71L). |

---

**Nome do arquivo:** `dados_alunos_disciplinas.csv`
**Tabela:** Histórico de Disciplinas e Desempenho Acadêmico
**Descrição:** Detalhamento da vida acadêmica do aluno semestre a semestre, registrando as disciplinas cursadas, notas obtidas e carga horária integralizada.
**Descrição das colunas:**

| Coluna | Tipo do Dado | Característica | Significado / Descrição |
| :--- | :--- | :--- | :--- |
| **ID_ALUNO** | Texto (String) | Identificador Único | Código hash que identifica anonimamente cada aluno, preservando sua privacidade. |
| **ESTADO_CIVIL** | Texto (String) | Categórica Nominal | Estado civil do estudante registrado no cadastro acadêmico (ex: Solteiro(a)). |
| **IDADE** | Texto (String) | Categórica Ordinal | Faixa etária do aluno registrada no sistema (ex: Menos de 19 anos). |
| **ANO_INGRESSO** | Numérico (Inteiro) | Temporal | Ano civil em que o aluno iniciou oficialmente o seu vínculo com a instituição (ex: 2008). |
| **FORMA_INGRESSO** | Texto (String) | Categórica Nominal | Método ou processo seletivo utilizado pelo discente para ingressar no curso (ex: Vestibular). |
| **ANO_EVASAO** | Numérico (Inteiro) | Temporal | Ano civil em que foi oficializado o encerramento do vínculo do discente. |
| **FORMA_EVASAO** | Texto (String) | Categórica Nominal | Motivo do encerramento ou interrupção do vínculo do aluno com a instituição (ex: Desistência). |
| **NATURALIDADE** | Texto (String) | Categórica Nominal | Cidade e Estado de nascimento do aluno (ex: Rio Branco-AC). |
| **ETNIA** | Texto (String) | Categórica Nominal | Autodeclaração de raça/cor ou etnia do discente (ex: Não Declarada). |
| **DEFICIENCIAS** | Texto (String) | Categórica Nominal | Indicação da presença de alguma deficiência informada pelo aluno ou "Sem Deficiência". |
| **COTAS** | Texto (String) | Categórica Nominal | Categoria de concorrência ou política de ações afirmativas de ingresso (ex: Ampla Concorrência). |
| **NOME_DISCIPLINA** | Texto (String) | Categórica Nominal | Nome oficial completo da disciplina cursada pelo aluno (ex: Administração, Lógica para Computação). |
| **ANO_DISCIPLINA** | Numérico (Inteiro) | Temporal | Ano letivo no qual a disciplina foi cursada (ex: 2008). |
| **PERIODO_DISCIPLINA** | Texto (String) | Temporal | Período ou semestre letivo específico em que a matrícula na disciplina ocorreu (ex: 1° Semestre, DPLE). |
| **SITUACAO_DISCIPLINA** | Texto (String) | Categórica Nominal | Situação e resultado final do aluno na respectiva disciplina (ex: Aprovado, Reprovado). |
| **CH_TOTAL** | Numérico (Inteiro) | Quantitativa Discreta | Carga horária total da disciplina expressa em horas (ex: 60, 30, 90). |
| **CREDITO_DISCIPLINA** | Texto (String) | Categórica Nominal | Distribuição dos créditos acadêmicos da disciplina em formato estruturado (ex: 4-0-0, 2-1-0). |
| **MEDIA_FINAL** | Texto (String) | Categórica Ordinal | Faixa de nota média final obtida pelo aluno na disciplina (ex: 8-10, 5-8, 0-5). |
| **FALTAS** | Texto (String) | Categórica Ordinal | Faixa percentual que representa a proporção de faltas do aluno na disciplina (ex: 0-5%, 20-25%). |
| **BOLSA** | Texto (String) | Categórica Nominal | Indicação sobre o recebimento de auxílios financeiros ou bolsas acadêmicas pelo aluno (ex: Não Possuia). |

---

**Nome do arquivo:** `dados_alunos_unicos.csv` e `dados_alunos_unicos2.csv`
**Tabela:** Alunos Únicos — Perfil Demográfico por Aluno
**Descrição:** Consolidação dos dados demográficos e de vínculo institucional com um registro único por aluno, sem repetição por disciplina. O arquivo `dados_alunos_unicos2.csv` possui uma abrangência temporal maior (2004–2024) e nomenclatura mais descritiva nas categorias de idade.
**Descrição das colunas (comuns a ambos os arquivos):**

| Coluna | Tipo do Dado | Característica | Significado / Descrição |
| :--- | :--- | :--- | :--- |
| **ID_ALUNO** | Texto (String) | Identificador Único | Hash MD5 de 32 caracteres que identifica o aluno de forma anônima nos sistemas da instituição. |
| **IDADE** | Texto (String) | Categórica Ordinal | Faixa etária do aluno no momento do ingresso, agrupada em intervalos (ex: Menos de 19 anos, 19-25 anos, 26-35 anos, Acima de 35 anos). |
| **ANO_INGRESSO** | Texto (String) | Temporal | Ano de ingresso do aluno no curso de graduação. |
| **FORMA_INGRESSO** | Texto (String) | Categórica Nominal | Modalidade ou processo seletivo pelo qual o aluno obteve vaga na instituição (ex: Processo Seletivo - SiSU, Vestibular, Enem). |
| **ANO_EVASAO** | Texto (String) | Temporal | Ano em que o vínculo do aluno foi encerrado. Valor vazio indica aluno ainda ativo ou sem evasão registrada. |
| **FORMA_EVASAO** | Texto (String) | Categórica Nominal | Motivo ou forma de encerramento do vínculo institucional (ex: Formado, Desistência, Jubilamento, Cancelamento) ou "Sem Evasão" para alunos ativos. |
| **NATURALIDADE** | Texto (String) | Categórica Nominal | Cidade e estado de nascimento do aluno, no formato Cidade-UF (ex: Rio Branco-AC, Porto Velho-RO). |
| **ETNIA** | Texto (String) | Categórica Nominal | Cor/raça autodeclarada pelo aluno conforme padrões do IBGE (ex: Branca, Parda, Preta, Amarela, Indígena, Não Declarada). |
| **DEFICIENCIAS** | Texto (String) | Categórica Nominal | Tipo de deficiência ou necessidade especial declarada pelo aluno (ex: Sem Deficiência, Deficiência Sensorial Visual, Física). |
| **COTAS** | Texto (String) | Categórica Nominal | Modalidade de cota ou ação afirmativa utilizada pelo aluno no processo seletivo de ingresso (ex: Ampla Concorrência, Candidatos de Escola Pública com Baixa Renda). |
| **BOLSA** | Texto (String) | Categórica Binária | Indica se o aluno era beneficiário de algum programa de auxílio financeiro ou bolsa acadêmica (Possuia / Não Possuia). |

---

**Nome do arquivo:** `dados_disciplinas_periodo_1.csv` a `dados_disciplinas_periodo_8.csv`
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
