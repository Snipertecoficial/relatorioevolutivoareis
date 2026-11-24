# Relatório Executivo de Evolução Tecnológica — A.Reis Advogados
**Parceria Estratégica:** A.Reis Advogados & Snipertec Tecnologia e Automação LTDA  
**Período Consolidado:** 01 de Setembro de 2026 (Início do Contrato Evolutivo) a 24 de Novembro de 2026  

---

## 1. Marco Inicial: O Contrato de Desenvolvimento Evolutivo

Em setembro de 2026, com a base fundacional do sistema jurídico (`sistema.areisadvogados.com.br`) já implantada e operando no escritório, a **A.Reis Advogados** e a **Snipertec Tecnologia e Automação** deram início ao **Ciclo de Suporte e Desenvolvimento Evolutivo** — desenhado para expandir a plataforma sob medida, conectá-la diretamente aos tribunais e criar automações exclusivas para a rotina da Diretoria, da Controladoria e de toda a equipe jurídica.

| Dado Oficial do Contrato | Registro no Documento Assinado (Autentique) |
| :--- | :--- |
| **Instrumento** | Contrato de Prestação de Serviços – Suporte e Desenvolvimento Evolutivo |
| **Data do Contrato** | **01 de setembro de 2026** |
| **Assinatura Snipertec (Douglas Nogueira)** | **01/09/2026 às 16h19** (Assinatura eletrônica Autentique) |
| **Assinatura A.Reis Advogados (Dra. Angélica Reis)** | **04/09/2026 às 10h03** (Assinatura eletrônica Autentique) |
| **Vigência do Ciclo** | 06 meses (Setembro/2026 a Março/2027) |
| **Escopo Contratual (Cláusula 1ª)** | **1. Evolução Sob Demanda:** criação de novos recursos e conexões com novas APIs conforme a necessidade operacional do escritório.<br>**2. Manutenção e Backups:** evolução preventiva, estabilidade contínua e rotinas de backup a cada atualização.<br>**3. Suporte Especializado:** atendimento técnico dedicado à equipe. |

---

## 2. Indicadores Executivos dos Primeiros 85 Dias

Em apenas **85 dias de ciclo evolutivo**, a Snipertec conduziu uma expansão acelerada da plataforma, elevando o sistema da sua **Base Fundacional (Fase 1)** para uma **Plataforma de Inteligência Jurídica Integrada (Fase 2)**:

* **239 Pacotes Publicados (PRs) e 1.308 Commits (`PR #4` ao `PR #253`):** 239 Pull Requests efetivamente mergeados e publicados em produção no período — média de quase **3 entregas por dia corrido**.
* **140 Processos Sincronizados no Piloto Judit:** conexão direta com os tribunais (101 processos do TJSP, 38 do TRT-2 e 1 do TRF-3). Só nesses 140 processos consultados, o robô preencheu sozinho todo o histórico de **14.800 movimentações do tribunal** (média de ~105 linhas de histórico por processo) e localizou **10.511 documentos/anexos**.
* **631 Processos da Carteira Estruturados e Padronizados:** 100% da base não-excluída organizada na nova taxonomia de 12 Áreas do Direito — composta por **519 processos judiciais (CNJ)**, **109 processos administrativos tributários** (Receita Federal) importados em outubro e 3 processos administrativos diversos (incluindo a consolidação de 279 processos Cíveis).
* **16.090 Testes Automatizados de Qualidade (+8.120 criados no ciclo evolutivo):** bateria de testes automáticos de engenharia (9.669 na API, 2.765 no banco PostgreSQL real, 3.468 nas telas e 188 no Portal) executada antes de cada publicação.
* **178 Rotas Atualizadas para Segurança Ativa (cobrindo 100% das 594 rotas da API):** conferência instantânea de usuário ativo no banco de dados e sigilo processual a cada clique.
* **100% das Atualizações com Backup Prévio no Servidor:** cópia completa de segurança do banco de dados PostgreSQL realizada antes de cada atualização, com zero perda de informações.

---

## 3. Evolução por Área Estratégica (Linguagem Simples, Clara e Executiva)

Abaixo apresentamos tudo o que foi construído nas **8 áreas do escritório**, comparando a **Fase Fundacional (Base Inicial)** com o **Novo Padrão Entregue no Evolutivo**.

---

### ÁREA 1 — Alta Disponibilidade, Performance & Acesso Inteligente
*(Ciclo Setembro/2026 — PRs #4 a #16 e #248)*

* **📐 Fase Fundacional (Base Inicial):** Configuração inicial dimensionada para a partida da operação e regra de segurança de login baseada no endereço de internet (IP) geral do escritório.
* **🚀 Novo Padrão Entregue no Evolutivo:**
  1. **Arquitetura para Múltiplos Acessos Simultâneos (PRs #4, #15, #16):** Com toda a equipe utilizando notificações em tempo real (sininho), documentos no GED e agenda simultaneamente, implementamos a reciclagem inteligente e automática de conexões (WebSocket, memória Redis e MinIO). Resultado: servidor leve, rápido e com estabilidade contínua o dia inteiro.
  2. **Proteção de Login por Conta Individual (PRs #5, #8, #13):** Evoluímos a segurança do login para atuar por conta individual e não pelo IP da rede. Assim, caso uma colaboradora erre sua senha repetidas vezes, apenas o acesso dela aguarda por segurança, sem jamais interromper o Wi-Fi das demais pessoas do escritório.

---

### ÁREA 2 — Agenda Executiva, Governança de Prazos & Automação Extrajudicial
*(Ciclos Setembro a Novembro/2026 — 35+ entregas publicadas)*

A Agenda recebeu automações desenhadas diretamente a partir da rotina da Dra. Angélica, da Adriana e das advogadas:

1. **Calendário Inteligente em Dias Úteis e Feriados (PR #30):** O motor de geração de acompanhamentos diários de prazos agora calcula automaticamente apenas **dias úteis**, pulando sábados, domingos e feriados nacionais.
2. **Baixa Inteligente em Lote em 1 Clique (PRs #66, #67, #68):** Quando um prazo possui diversos acompanhamentos diários e a advogada conclui a demanda antecipadamente, o sistema pergunta se ela deseja **dar baixa em todas as repetições futuras de uma só vez** (preservando automaticamente qualquer item que tenha anotação específica e permitindo reabrir em lote caso necessário).
3. **Aba "Histórico" para Rastreabilidade Completa da Gestão (PRs #37, #38, #39):** Toda tarefa passou a contar com uma linha do tempo de auditoria imutável que registra automaticamente quem criou, quem alterou uma data, status, título ou responsável, com data e horário exatos.
4. **Governança sobre o Título da Tarefa (PRs #40 e #41):** Após o cadastro de um compromisso ou prazo, o título original fica protegido por cadeado, podendo ser alterado exclusivamente pela Controladoria (Adriana) e pela Diretoria/Administração.
5. **Novo Campo "Providência" com Destaque Visual (PRs #43, #44, #45):** Espaço dedicado para registrar a providência adotada na tarefa, que passa a aparecer em destaque nos cartões da agenda e nos alertas de prazos urgentes.
6. **Fluxo Formal de "Pedir Nova Data" com Aprovação (PRs #181, #182, #188, #210):** Solicitação estruturada de reagendamento com justificativa obrigatória, trava de segurança que impede datas posteriores ao Prazo Fatal, aviso imediato no sininho da gestão e opções de *Aprovar*, *Aprovar com outra data* ou *Recusar com justificativa*.
7. **Seleção Exclusiva de Profissionais da Equipe como Responsáveis (PRs #168, #176, #177, #189, #190):** Separação rigorosa entre o campo *Cliente* e o campo *Responsáveis pela execução* (restrito exclusivamente aos membros da equipe do escritório), acompanhada da higienização automática de 221 registros históricos.
8. **Múltiplos Alertas Prévios e Vínculo Rápido com Processos (PRs #21, #22, #24, #31, #230):** Persistência completa dos alertas de prazo (72h, 24h, 6h e 1h antes) no fuso horário de Brasília, sugestão automática dos processos do cliente selecionado ao criar uma tarefa e abertura imediata do prazo ao clicar nos indicadores urgentes do Painel.
9. **Workflow Automático de Notificação Extrajudicial em 6 Etapas (PRs #70, #73, #74):** Ao concluir uma etapa do fluxo extrajudicial, o sistema já sugere e pré-preenche a etapa seguinte na sequência: *1. Notificação extrajudicial → 2. Tratativa → 3. Envio de notificação → 4. Retorno → 5. Reenvio → 6. Ação judicial*.
10. **Nova "Agenda do Escritório" com Carga por Pessoa e Kanban de Alta Velocidade (PRs #169, #191, #192, #240):** Painel gerencial que exibe a distribuição de tarefas abertas, concluídas e vencidas por colaboradora, além de quadro Kanban paginado com movimentação automática para a coluna *Feito*.

---

### ÁREA 3 — Integração Empresarial com a Judit: Conexão Direta com os Tribunais
*(Ciclo Novembro/2026 — PRs #75 a #132 e #241 — mais de 55 entregas)*

* **📐 Fase Fundacional (Base Inicial):** Consulta inicial conectada à API pública governamental (DataJud/CNJ), cuja cobertura pública apresenta limitações de atualização nos tribunais estaduais e trabalhistas.
* **🚀 Novo Padrão Entregue no Evolutivo:** Implementamos a integração empresarial completa com a **Judit**, conectando o Areis diretamente aos tribunais de todo o Brasil:
  1. **Botão "Atualizar via Judit" em 1 Clique (PRs #79, #83, #88 a #92):** Sincroniza instantaneamente a capa oficial do tribunal (classe, assunto, vara, juiz, valor da causa e partes) e todo o histórico de andamentos, sem duplicar registros e com trava inteligente de 24h para evitar consumo repetido acidental.
  2. **Robô de Monitoramento Diário de Processos (PRs #94, #95, #98, #100, #101, #127, #241):** Chave individual na ficha e ativação em lote na listagem para que o robô acompanhe diariamente novas movimentações nos tribunais e alimente o sistema automaticamente.
  3. **Monitoramento Automático do Diário da Justiça (DJEN) por OAB (PRs #99, #103, #105, #106):** Captura diária de intimações eletrônicas no DJEN para as OABs cadastradas (com a OAB/SP 417687 ativa no piloto). **Arquitetura segura:** construída em módulo 100% independente, preservando intacta a integração existente com a **AASP**.
  4. **Download Direto de Autos e Documentos do Tribunal para o GED (PRs #110, #117, #120 a #124):** O botão *"Baixar autos (Judit)"* importa os PDFs e anexos oficiais do processo no tribunal diretamente para a aba GED do Areis, com visualizador de PDF integrado no navegador.
  5. **Enriquecimento Automático de Cadastro ("Completar com Judit") (PRs #128, #129, #132):** A partir do CPF ou CNPJ na ficha do cliente, o sistema preenche automaticamente endereço, telefones, e-mails e dados cadastrais oficiais em segundos.
  6. **Painel Executivo de Governança e Custos em `Admin › Judit` (PRs #93, #96, #97, #111 a #114, #130):** Transparência total sobre cada consulta realizada, profissional solicitante, monitoramentos ativos e resumo financeiro estimado em reais (R$).

---

### ÁREA 4 — Inteligência Areis, Jurimetria, Due Diligence (CPF/CNPJ) & Central de Relatórios
*(Ciclo Novembro/2026 — PRs #108 a #212)*

1. **Piloto Real Executado em 140 Processos da Carteira (PR #155):** Sincronizamos **140 processos reais do escritório** (101 do TJSP, 38 do TRT-2 e 1 do TRF-3), incorporando **14.800 andamentos oficiais** e mapeando **10.511 documentos** nos tribunais.
2. **Nova Central de Relatórios "Que relatório você quer?" em 3 Cliques (PRs #140, #142, #145, #148, #163 a #167, #174, #175, #179, #180, #186, #187):**
   * Substituímos o formulário técnico de múltiplos parâmetros por um assistente visual intuitivo com **8 cartões prontos**: *Processos de um cliente, Processos de um advogado, Processos de uma área, Prazos que estão chegando, Processos parados, Novidades nos processos, Relatório completo de um processo (Dossiê) e Lista de todos os processos*.
   * O usuário responde 2 ou 3 perguntas simples, confere a prévia ao vivo na tela e exporta em **PDF** ou **Excel**, com histórico organizado em português claro (*"Relatórios gerados"*) e permissão configurável para assistentes e estagiárias.
3. **Dossiê Executivo do Processo em PDF — Versão Cliente × Versão Interna (PRs #141 e #143):**
   * Gera um documento executivo em PDF com a marca da A.Reis Advogados em duas opções: **Para o cliente** (traduz termos técnicos para linguagem acessível e protege automaticamente qualquer observação interna ou dado financeiro) e **Interno** (ficha técnica completa para a equipe).
4. **Cartão "Raio-X do Processo" na Ficha (PR #149):** Resumo visual imediato ao abrir qualquer processo, exibindo fase atual, linha do tempo por instância, decisões identificadas e comparativo de duração com a média da vara.
5. **Jurimetria Visual e Busca de Jurisprudência Interna + AASP (PRs #108, #109, #115, #116, #135, #139, #144, #146, #147, #150, #151, #154, #156, #173, #178):** Estatísticas visuais de tempo e desfechos por tribunal/vara e buscador instantâneo de palavras-chave em todas as decisões do escritório e publicações da AASP.
6. **Módulo "Consulta por CPF/CNPJ" para Due Diligence e Contratações/RH (PRs #125, #126, #131, #202, #203, #208, #209, #211, #212):**
   * Nova tela em **Inteligência › Consulta por CPF/CNPJ** equipada com **busca por partes inferidas e consulta direta aos tribunais** (capaz de localizar inclusive processos trabalhistas nos TRTs que omitem o CPF na capa pública). Apresenta resumo classificado por área (Trabalhista, Cível, Penal, Consumidor) e exporta dossiê em PDF sem misturar a pesquisa com a base de clientes do escritório.

---

### ÁREA 5 — Gestão de Processos em 3 Passos, Expansão Tributária & Padronização da Carteira
*(Ciclos Outubro e Novembro/2026 — PRs #20 a #62 e #157 a #206)*

1. **Novo Fluxo de Cadastro de Processos em 3 Etapas Guiadas (PRs #157, #161, #162, #197 a #206):**
   * **Passo 1:** Definição da **Natureza** — **Judicial (CNJ)** (com validação instantânea do dígito verificador e busca automática na Judit) ou **Administrativo** (Receita Federal, CARF, PGFN, SEFAZ, Prefeitura, INSS, com numeração flexível).
   * **Passo 2:** Classificação nas **12 Áreas do Direito** padronizadas, Classe oficial, Cliente e **múltiplos advogados co-responsáveis** (com compartilhamento automático de acesso em processos sigilosos).
   * **Passo 3:** Dados complementares e persistência completa de Comarca/Foro.
2. **Importação Estruturada da Carteira Tributária (PRs #25, #26, #32):** Desenvolvimento de importador dedicado para a planilha da área Tributária, incorporando **109 processos administrativos da Receita Federal** e organizando **39 empresas clientes (CNPJs)**.
3. **Padronização de 631 Processos Históricos e Consolidação da Área Cível (PRs #86, #87 e #204):** Unificação de **279 processos na área Cível** e migração inteligente de **631 processos anteriores** para a nova estrutura de Natureza, Área e Classe, adicionando o filtro rápido **"Conferir"** na listagem.
4. **Ficha do Processo Organizada entre "Dados do Escritório" e "Dados do Tribunal" (PR #201):** Separação visual clara entre as anotações estratégicas da equipe e os dados oficiais sincronizados via Judit.
5. **Prevenção Inteligente de Duplicidades e Exportação Integral da Carteira (PRs #20, #23, #28, #50 a #58, #62, #251):** Verificação automática de CPF/CNPJ e número de processo (comparando apenas dígitos e alertando inclusive quando o registro está na Lixeira), contagem em tempo real direto no banco de dados e exportação Excel/PDF de 100% da carteira filtrada.

---

### ÁREA 6 — Central Admin › Equipe, Mobilidade Celular/Tablet & Ajuda Contextual "?"
*(Ciclos Outubro e Novembro/2026 — PRs #17 a #72, #170 a #207, #244 a #253)*

1. **Nova Central `Admin › Equipe` com Gaveta Lateral e 5 Perfis Prontos (PRs #17, #18, #60, #61, #172, #185, #193):**
   * Interface moderna com busca instantânea e gaveta lateral contendo chaves simples de ligar/desligar (*"Vê a agenda de todos"*, *"Gera relatórios da agenda"*, *"Gera relatórios de processos"*, *"Gerencia a equipe"*, *"Usa a Judit"*).
   * Inclui **5 botões de Perfil Rápido** que configuram todas as permissões em 1 clique e garante autonomia segura para a Adriana gerenciar a equipe e as 7 assistentes.
2. **Convite Digital com Link Copiável para WhatsApp (PRs #47, #63, #64, #65):** Geração imediata de link seguro de ativação com o botão **"Link de acesso"**, permitindo copiar e enviar o convite diretamente no WhatsApp da nova colaboradora, além de exibir na tela o status em tempo real do envio por e-mail.
3. **Fluxo de Desligamento Seguro com Redistribuição de Tarefas (PRs #69, #71, #72):** Ao desativar ou remover o acesso de uma profissional que deixou o escritório, o sistema identifica automaticamente quantas tarefas abertas ela possui e permite transferi-las em lote para outra colaboradora na mesma tela, mantendo ainda o filtro histórico **"Ex-colaboradoras"** na Agenda.
4. **Balões de Ajuda Contextual ("?") em Todas as Telas Estratégicas (PRs #118, #119, #244 a #247, #250, #252, #253):** Ícones **"?"** posicionados ao lado das ações de Financeiro, Faturas, Timesheet, Admin, Equipe, Portal, Lixeira, Processos, Publicações e Agenda, explicando de forma direta: **O que faz**, **Como usar** e **O que acontece depois**.
5. **Mobilidade Completa em Celular, Tablet e Computador (PRs #158, #170, #171, #183, #184, #194 a #196, #207):** Adaptação responsiva de janelas, tabelas, abas e seletores de busca para uso confortável no celular (375px), tablet (768px) e monitor desktop (1440px).

---

### ÁREA 7 — Portal do Cliente Executivo, Nova Aba Financeiro & Governança Contábil
*(Ciclos Setembro a 23/11/2026 — PRs #7 a #29 e #214 a #251)*

1. **Nova Aba "Financeiro" no Portal do Cliente — Visão Dra. Angélica (PRs #235 e #236 — Publicada em 23/11/2026):**
   Ao acessar a aba **Financeiro** no Portal, o cliente do escritório visualiza um painel executivo claro e elegante com 3 blocos:
   * **Cartão 1 — "Cliente desde":** destaca o mês e o ano de início do relacionamento com o escritório (alimentado pelo novo campo na ficha do cliente ou automaticamente pelo contrato mais antigo).
   * **Cartão 2 — "Mensalidades" do Ano:** apresenta o resumo anual de adimplência (ex.: **"11 de 12 pagas"** em 2026), com seletor de ano e alimentação automática a partir dos lançamentos da categoria **"Mensalidade"** no Financeiro.
   * **Bloco 3 — Tabela "Processos em andamento":** lista os processos ativos do cliente exibindo **Partes** (Autor × Réu), **Número do processo**, **Tipo/Classe**, **Valor da causa** (com interruptor em *Admin › Portal* para exibir ou ocultar) e a coluna **"Situação"** (que apresenta o resumo escrito pela equipe no novo campo *"Situação para o cliente"* ou, automaticamente, a próxima audiência/último andamento).
2. **Privacidade e Precisão no Portal e no Financeiro Interno (PRs #7, #10, #14, #29, #215, #222, #223, #225, #232, #233, #243):**
   * Blindagem total para que o cliente visualize apenas informações destinadas a ele (nunca tarefas internas, observações internas ou faturas em rascunho);
   * Reconhecimento automático de faturas quitadas como **"Pago"** no Portal;
   * Sincronização contábil que evita duplicidade no DRE ao importar lançamentos para faturas, exige estorno formal antes do cancelamento de lançamentos já pagos, protege contratos encerrados e reabre horas editadas no Timesheet para nova aprovação.

---

## 4. Frentes em Andamento neste Momento (Acompanhamento Assistido)

1. **Ativação Assistida da Nova Aba Financeiro do Portal com Clientes Reais:** Com a funcionalidade 100% no ar desde 23/11 e o guia operacional entregue à Controladoria, estamos apoiando o preenchimento inicial (manual ou via planilha em lote) de *"Cliente desde"*, *"Mensalidades"* e *"Situação para o cliente"* para a estreia com o cliente selecionado pela Dra. Angélica.
2. **Consolidação do Piloto Judit & Planejamento de Expansão:** Acompanhamento diário das capturas automáticas nos 140 processos enriquecidos e na OAB/SP 417687 no Diário da Justiça (DJEN), preparando a decisão de expansão gradual para os demais processos ativos da carteira.
3. **Homologação Prática do Workflow Extrajudicial:** Validação do fluxo de 6 etapas em produção junto à Adriana para, na sequência, liberar o construtor visual de novos fluxos personalizados.
4. **Expansão da Ajuda Contextual ("?") para Módulos Complementares (Etapas P2 e P3):** Continuidade da adição dos balões explicativos para as abas de GED, Contratos, Serviços e CRM.
5. **Catalogação Arquitetural Viva da Engenharia Snipertec:** Mais de 84% do código-fonte mapeado em 5 manuais técnicos auditados para acelerar continuamente as próximas entregas evolutivas.

---

## 5. Próximas Etapas do Roteiro Evolutivo

> **Nota de Atualização Operacional (24/11/2026):** As seguintes frentes operacionais e de higienização já foram **100% concluídas** e incorporadas às entregas realizadas:
> * ✅ **Atualização da credencial do e-mail institucional (`tecnologia@areisadvogados.com.br`) e autenticação DMARC na KingHost**;
> * ✅ **Ativação dos perfis e permissões das 7 assistentes** (*Aline, Barbara, Isis, Larissa, Letícia Caroline, Mariana e Sophia*) na nova central `Admin › Equipe`;
> * ✅ **Redistribuição das tarefas históricas** (tarefas sem titular e filtro *"Ex-colaboradoras"*) e **validação do filtro "Conferir"** nos 631 processos padronizados;
> * ✅ **Unificação e higienização de cadastros históricos duplicados** anteriores à trava automática de CPF/CNPJ.

### A. Cronograma Técnico Programado (Snipertec)
1. **Espelhamento Automático Externo de Backups em Nuvem (Google Drive 3 TB):** Ativação da rotina diária de madrugada para enviar cópia criptografada do banco de dados PostgreSQL e dos documentos do GED (MinIO) para armazenamento externo fora do servidor VPS, garantindo dupla redundância geográfica.
2. **Refinamento Financeiro (Atalho de Quitação, Estorno e Painéis em SQL):** Integração do botão rápido *"Marcar como pago"* ao motor de atualização imediata de saldo bancário, adição do botão *"Estornar pagamento"* em 1 clique e processamento dos gráficos de DRE/Fluxo diretamente em SQL.
3. **Seletor de Visibilidade em Andamentos Manuais para o Portal:** Inclusão da opção *"Visível ao cliente"* ao cadastrar um andamento manual na ficha do processo (mantendo andamentos da Judit visíveis por padrão e anotações manuais da equipe privadas até liberação).
4. **Inteligência de Notificações na Edição de Compromissos:** Preservação do histórico de lembretes já enviados quando uma tarefa tiver apenas seu texto editado na Agenda.

### B. Próximos Passos Conjuntos com a Diretoria (A.Reis + Snipertec)
1. **Seleção do Cliente Piloto para Estreia da Nova Aba Financeiro do Portal:** Definir junto à Dra. Angélica o primeiro cliente real para validarmos a visualização executiva de *"Cliente desde"*, *"Mensalidades Pagas"* e *"Processos em Andamento"*.
2. **Expansão Gradual do Monitoramento Judit para o Restante da Carteira:** Com os 140 processos do piloto enriquecidos e o monitoramento diário da OAB no DJEN validado, alinhar a ativação gradual da sincronização Judit para os demais processos ativos do escritório.
3. **Homologação do Fluxo Extrajudicial & Liberação do Construtor de Fluxos:** Acompanhar o uso prático do workflow automático de 6 etapas pela Controladoria para, em seguida, habilitar a tela que permite ao escritório criar novos roteiros passo a passo personalizados.
4. **Agendamento do Treinamento Prático da Equipe:** Com todas as configurações das 7 assistentes, e-mail institucional, padronização dos 631 processos e novas telas já concluídas, realizar o treinamento guiado com as colaboradoras sobre os novos recursos publicados.
