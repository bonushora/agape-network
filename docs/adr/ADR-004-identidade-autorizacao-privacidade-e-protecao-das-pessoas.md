# ADR-004 — Identidade, Autorização, Privacidade e Proteção das Pessoas

- **Status:** Aprovada e congelada
- **Data:** 20 de agosto de 2026
- **Projeto:** Agape Network
- **Repositório:** `bonushora/agape-network`
- **Classificação:** Decisão constitucional, institucional e de segurança
- **Escopo:** Identidade, credenciais, autorização, consentimento, privacidade e proteção humana
- **Precedência:** Subordinada à ADR-001, ADR-002 e ADR-003
- **Dependências:** ADR-001, ADR-002 e ADR-003

## 1. Contexto

A Agape Network tratará informações de instituições, operadores, voluntários, doadores, auditores, pessoas assistidas, crianças e pessoas em situação de vulnerabilidade.

Uma blockchain possui características de persistência, replicação e dificuldade de remoção. Essas características podem proteger a integridade dos registros, mas também podem ampliar danos quando dados pessoais são gravados indevidamente.

A identidade necessária para responsabilizar validadores não deve produzir exposição das pessoas assistidas.

A transparência institucional não deve eliminar privacidade humana.

Esta ADR define princípios obrigatórios antes da classificação definitiva de dados on-chain e off-chain, que será objeto da ADR-005.

## 2. Decisão

A Agape Network adotará identidade verificável, autorização explícita, privilégio mínimo, proteção por finalidade e privacidade desde a concepção.

A rede distinguirá:

- identidade institucional;
- identidade do representante;
- identidade técnica;
- identidade operacional;
- identidade do usuário;
- identidade protegida ou pseudonimizada da pessoa assistida.

A força da identificação será proporcional ao papel, ao risco e à responsabilidade.

## 3. Princípio fundamental

> A rede deverá identificar suficientemente quem exerce autoridade, protegendo ao máximo quem procura ou recebe ajuda.

Responsabilidade institucional e proteção humana serão objetivos simultâneos.

## 4. Categorias de sujeitos

A arquitetura deverá reconhecer, no mínimo:

1. instituições participantes;
2. representantes legais;
3. responsáveis técnicos;
4. operadores de nós;
5. membros dos órgãos de governança;
6. auditores;
7. voluntários;
8. doadores;
9. prestadores de serviços;
10. pessoas assistidas;
11. responsáveis legais por crianças ou incapazes;
12. sistemas e agentes automatizados.

Cada categoria possuirá requisitos próprios de identidade e autorização.

## 5. Identidade institucional

Instituições que exerçam autoridade deverão possuir identidade verificável.

O registro institucional deverá permitir verificar:

- existência;
- nome oficial;
- jurisdição aplicável;
- responsáveis autorizados;
- chaves públicas;
- papéis;
- situação;
- período de validade;
- conflitos declarados;
- domínio de controle;
- histórico de alterações.

Nós validadores não poderão operar sob anonimato institucional.

## 6. Identidade dos representantes

Toda ação institucional relevante deverá ser atribuível a representante autorizado ou processo institucional verificável.

A credencial deverá vincular:

- pessoa responsável;
- instituição;
- papel;
- escopo;
- validade;
- autoridade concedente;
- restrições;
- chave ou mecanismo de autenticação.

A representação cessará quando expirar, for revogada ou perder fundamento.

## 7. Identidade técnica

Nós, serviços, aplicações e agentes automatizados possuirão identidades técnicas distintas das identidades humanas.

Uma identidade técnica:

- não será tratada como pessoa;
- não possuirá autoridade implícita;
- terá capacidades limitadas;
- deverá ser vinculada a responsável institucional;
- terá credenciais rotacionáveis;
- produzirá trilha auditável;
- não poderá ampliar seus próprios privilégios.

## 8. Identidade das pessoas assistidas

A pessoa assistida não será obrigada a tornar pública sua identidade, religião, vulnerabilidade ou história pessoal para receber ajuda.

Quando identificação for necessária:

- serão coletados apenas os dados mínimos;
- a finalidade será explícita;
- o acesso será restrito;
- a informação ficará preferencialmente fora da blockchain;
- identificadores públicos serão evitados;
- referências pseudonimizadas serão utilizadas quando adequadas;
- riscos de reidentificação serão avaliados.

Ausência de documentação não implicará automaticamente recusa de assistência emergencial.

## 9. Religião e liberdade de consciência

Religião, crença, ausência de crença, conversão e práticas espirituais serão tratadas como informações especialmente protegidas.

A rede não deverá coletá-las por padrão.

Quando excepcionalmente necessárias para finalidade legítima e autorizada:

- a necessidade deverá ser demonstrada;
- a coleta será mínima;
- o uso não poderá produzir discriminação;
- o dado não será utilizado para medir mérito;
- o atendimento não será condicionado à resposta;
- o dado não será gravado diretamente na blockchain;
- o acesso será rigorosamente limitado.

## 10. Crianças e pessoas vulneráveis

A proteção de crianças, adolescentes, incapazes e pessoas vulneráveis terá prioridade reforçada.

A arquitetura deverá contemplar:

- representação legítima quando necessária;
- verificação proporcional do responsável;
- proteção contra exploração;
- prevenção de exposição;
- restrição de acesso;
- minimização extrema;
- revisão humana de operações sensíveis;
- canais de denúncia;
- rastreabilidade dos acessos;
- resposta rápida a incidentes.

O interesse institucional nunca prevalecerá automaticamente sobre a segurança da pessoa vulnerável.

## 11. Identificadores

Identificadores deverão ser:

- específicos à finalidade quando possível;
- não significativos externamente;
- resistentes a enumeração;
- não derivados diretamente de documentos pessoais;
- separáveis entre contextos;
- revogáveis ou substituíveis quando aplicável.

CPF, passaporte, endereço, telefone, e-mail, diagnóstico ou número de benefício não deverão funcionar como identificador público on-chain.

## 12. Pseudonimização e anonimização

Pseudonimização reduzirá exposição, mas não será tratada automaticamente como anonimização.

Hashes de dados pessoais também poderão permitir correlação ou reidentificação.

Antes de registrar hash, compromisso ou prova relacionada a uma pessoa, será necessário avaliar:

- previsibilidade do dado original;
- possibilidade de ataque por dicionário;
- correlação entre contextos;
- existência de salt ou segredo adequado;
- necessidade real do registro;
- permanência do risco;
- possibilidade de revogação lógica.

Alegação de anonimização deverá ser tecnicamente demonstrável.

## 13. Autenticação

A autenticação será proporcional ao risco.

Operações críticas deverão exigir mecanismos reforçados, podendo incluir:

- múltiplos fatores;
- chaves criptográficas;
- dispositivos autorizados;
- confirmação independente;
- autenticação resistente a phishing;
- aprovação humana adicional;
- separação de funções.

Senha isolada não deverá ser suficiente para operações constitucionais ou de custódia crítica.

## 14. Modelo de autorização

A autorização combinará:

- papéis;
- atributos;
- contexto;
- finalidade;
- risco;
- situação da credencial;
- situação institucional;
- política vigente.

O modelo deverá suportar RBAC e ABAC sem conceder autoridade apenas pelo nome de um cargo.

Toda autorização crítica deverá ser explicitamente derivada de política válida.

## 15. Privilégio mínimo

Cada identidade receberá somente as capacidades necessárias:

- para finalidade definida;
- durante período limitado;
- no contexto autorizado;
- sobre recursos específicos;
- sob condições verificáveis.

Permissões genéricas, globais ou permanentes deverão ser evitadas.

A conveniência operacional não justificará privilégio excessivo.

## 16. Negação por padrão

Na ausência de autorização válida, a operação será negada.

Também serão negadas operações quando houver:

- identidade inválida;
- credencial expirada;
- revogação;
- política ausente;
- finalidade incompatível;
- conflito impeditivo;
- risco não tratado;
- consentimento exigido e ausente;
- contexto inconsistente;
- falha de verificação.

A rede operará em modo fail-closed.

## 17. Capacidades críticas

Serão consideradas críticas, entre outras:

- admitir ou excluir validadores;
- alterar políticas;
- acessar dados sensíveis;
- administrar identidades;
- emitir credenciais privilegiadas;
- rotacionar chaves;
- executar recuperação;
- alterar consenso;
- ativar código crítico;
- suspender serviços;
- realizar exportações amplas;
- quebrar pseudonimização;
- atuar em nome de pessoa vulnerável.

Essas capacidades exigirão controles adicionais e auditoria.

## 18. Separação de funções

Nenhuma pessoa ou identidade técnica deverá, isoladamente:

- criar sua própria credencial privilegiada;
- aprovar sua própria elevação;
- emitir e auditar a mesma autorização;
- quebrar pseudonimização e apagar evidências;
- recuperar e utilizar imediatamente uma chave crítica sem controle;
- conceder acesso irrestrito a dados sensíveis;
- substituir representantes sem registro.

Exceções emergenciais deverão ser temporárias, justificadas e revisadas.

## 19. Credenciais

Credenciais deverão possuir:

- emissor;
- sujeito;
- tipo;
- escopo;
- finalidade;
- emissão;
- validade;
- restrições;
- identificador;
- mecanismo de verificação;
- situação de revogação.

Credenciais não serão prova de fé, caráter moral ou santidade.

## 20. Expiração, revogação e suspensão

Toda credencial privilegiada deverá ser:

- limitada no tempo;
- revogável;
- verificável antes do uso;
- reavaliada em operações críticas;
- vinculada a eventos de desligamento e mudança de função.

Revogação deverá produzir efeito operacional previsível.

Histórico legítimo permanecerá preservado sem permitir uso futuro da credencial revogada.

## 21. Consentimento

Quando o consentimento for necessário, ele deverá ser:

- informado;
- específico;
- compreensível;
- demonstrável;
- livre de coerção indevida;
- revogável para usos futuros quando aplicável;
- separado de adesão religiosa;
- adequado à capacidade da pessoa.

A recusa de consentimento não poderá ser convertida em punição espiritual ou humilhação.

Consentimento não será usado como justificativa universal para qualquer tratamento.

## 22. Outras bases legítimas

A arquitetura deverá reconhecer que proteção vital, obrigação jurídica, execução de política social ou outras bases legítimas poderão existir conforme a jurisdição.

Nenhuma base será presumida silenciosamente.

Cada tratamento deverá possuir:

- finalidade;
- fundamento;
- responsável;
- limites;
- retenção;
- controles;
- registro.

A definição jurídica detalhada será realizada posteriormente por jurisdição.

## 23. Minimização de dados

A rede coletará apenas o necessário.

Antes de incluir um campo, deverá ser perguntado:

1. qual finalidade exige esse dado;
2. quem necessita acessá-lo;
3. por quanto tempo;
4. se existe alternativa menos invasiva;
5. se pode permanecer fora da blockchain;
6. qual dano sua exposição causaria;
7. como será corrigido, revogado ou desvinculado.

Dados “possivelmente úteis no futuro” não justificam coleta indiscriminada.

## 24. Limitação de finalidade

Dados coletados para assistência não poderão ser reutilizados automaticamente para:

- propaganda;
- proselitismo;
- perfil religioso;
- avaliação moral;
- venda;
- crédito;
- emprego;
- vigilância política;
- discriminação;
- treinamento de sistemas de IA;
- publicação de histórias pessoais.

Novo uso exigirá fundamento específico e controles próprios.

## 25. Dados on-chain

Por princípio, não serão gravados diretamente on-chain:

- nomes de pessoas assistidas;
- documentos;
- endereços;
- contatos;
- diagnósticos;
- prontuários;
- histórias familiares;
- imagens pessoais;
- religião;
- localização precisa;
- dados de crianças;
- credenciais secretas;
- chaves privadas;
- relatos de vulnerabilidade.

A ADR-005 definirá a classificação completa e as exceções estritamente justificadas.

## 26. Dados off-chain

Dados pessoais e sensíveis permanecerão preferencialmente off-chain em sistemas com:

- criptografia;
- controle de acesso;
- segregação;
- retenção definida;
- registro de acesso;
- cópias de segurança protegidas;
- correção;
- exclusão quando juridicamente e tecnicamente aplicável;
- resposta a incidentes.

A blockchain poderá conter provas ou referências sem se tornar repositório de exposição humana.

## 27. Correção e atualização

A imutabilidade técnica não eliminará o direito de corrigir informações.

A arquitetura deverá permitir:

- correção no sistema off-chain;
- novo registro que substitua logicamente informação anterior;
- indicação de revogação;
- preservação do histórico autorizado;
- prevenção do uso continuado de dado incorreto;
- explicação da relação entre versões.

Registro antigo não poderá continuar sendo apresentado como estado atual quando tiver sido legitimamente corrigido.

## 28. Exclusão e desvinculação

Quando houver obrigação ou direito aplicável de exclusão, a arquitetura deverá permitir:

- exclusão off-chain;
- destruição de chaves quando apropriado;
- remoção de índices;
- desvinculação de referências;
- revogação de acesso;
- registro mínimo de cumprimento.

Nenhuma promessa de apagamento completo da blockchain será feita quando tecnicamente impossível.

Essa limitação deverá ser comunicada antes da coleta.

## 29. Acesso aos dados

Todo acesso a dados protegidos deverá considerar:

- identidade;
- autorização;
- finalidade;
- necessidade;
- contexto;
- risco;
- período;
- registro de auditoria.

Consultas amplas, exportações e quebra de pseudonimização serão operações críticas.

A curiosidade institucional não constitui finalidade legítima.

## 30. Auditoria de acesso

A rede deverá registrar, conforme o risco:

- quem acessou;
- qual recurso;
- quando;
- sob qual papel;
- com qual finalidade declarada;
- qual política autorizou;
- qual resultado ocorreu;
- se houve exportação ou alteração.

A trilha de auditoria não deverá replicar o próprio conteúdo sensível.

## 31. Delegação

Delegações deverão ser:

- explícitas;
- limitadas;
- temporárias;
- rastreáveis;
- revogáveis;
- incapazes de exceder a autoridade do delegante.

Subdelegação somente será permitida quando expressamente autorizada.

A delegação não eliminará responsabilidade.

## 32. Recuperação de identidade

Recuperação de acesso deverá evitar tanto perda definitiva quanto tomada indevida.

Processos de recuperação crítica exigirão:

- prova proporcional;
- múltiplas verificações;
- espera ou revisão quando apropriada;
- notificação;
- registro;
- invalidação segura da credencial anterior;
- proteção contra engenharia social.

Detalhes criptográficos serão definidos na ADR-008.

## 33. Incidentes de privacidade

Incidentes deverão acionar:

- contenção;
- preservação de evidências;
- avaliação do impacto;
- bloqueio de credenciais comprometidas;
- comunicação aos responsáveis;
- medidas de proteção às pessoas;
- notificações juridicamente exigidas;
- correção;
- auditoria posterior.

A reputação da instituição não prevalecerá sobre a proteção das pessoas afetadas.

## 34. Sistemas de inteligência artificial

Sistemas de IA não receberão acesso irrestrito a dados pessoais.

Seu uso exigirá:

- finalidade explícita;
- minimização;
- autorização;
- isolamento;
- avaliação de risco;
- registro;
- supervisão humana;
- proibição de inferir mérito espiritual;
- prevenção de discriminação;
- controle sobre retenção e treinamento.

Dados de assistência não serão utilizados automaticamente para treinamento de modelos.

## 35. Interoperabilidade de identidade

A rede poderá aceitar identidades e credenciais externas quando:

- o emissor for confiável para a finalidade;
- o nível de garantia for suficiente;
- a validade puder ser verificada;
- a revogação puder ser consultada;
- os atributos forem mínimos;
- houver compatibilidade jurídica e constitucional.

Nenhum provedor externo será autoridade universal obrigatória por presunção.

## 36. Jurisdições

A Agape Network poderá operar em diferentes jurisdições.

A arquitetura deverá permitir:

- políticas por território;
- armazenamento compatível;
- restrições de transferência;
- retenções distintas;
- autoridades responsáveis identificáveis;
- adaptação regulatória;
- preservação dos princípios constitucionais.

Conformidade local não poderá ser usada como pretexto para exploração da fé ou exposição desnecessária.

## 37. Responsabilidade

Deverão ser identificáveis:

- controlador ou responsável institucional pelo tratamento;
- operadores autorizados;
- responsáveis por segurança;
- emissores de credenciais;
- autoridades de política;
- auditores;
- responsáveis por incidentes.

A descentralização não eliminará responsabilidade.

## 38. Direitos das pessoas

A arquitetura deverá permitir, conforme aplicável:

- informação;
- acesso;
- correção;
- oposição;
- restrição;
- revogação de consentimento;
- portabilidade quando cabível;
- revisão humana;
- reclamação;
- conhecimento das limitações da blockchain.

O exercício de direitos não poderá produzir retaliação religiosa ou perda arbitrária de assistência.

## 39. Proibições constitucionais

Fica proibido:

- criar ranking de fé;
- registrar pecados;
- calcular santidade;
- inferir mérito espiritual;
- expor vulnerabilidade para atrair doações;
- condicionar ajuda à publicidade da pessoa;
- vender dados de assistidos;
- usar religião para discriminar;
- utilizar credencial como certificado moral;
- permitir vigilância irrestrita;
- conceder acesso secreto sem fundamento;
- usar blockchain para impedir direitos legítimos.

## 40. Consequências

Esta decisão:

- fortalece responsabilização institucional;
- protege pessoas assistidas;
- impõe identidade forte aos detentores de autoridade;
- exige autorização granular;
- estabelece negação por padrão;
- limita dados on-chain;
- aumenta complexidade de identidade e segurança;
- exige sistemas off-chain protegidos;
- impede transparência baseada em exposição humana;
- prepara a classificação detalhada da ADR-005.

## 41. Riscos reconhecidos

Permanecem riscos de:

- reidentificação;
- correlação entre registros;
- roubo de credenciais;
- abuso interno;
- falsa representação;
- exclusão de pessoas sem documentos;
- excesso de coleta;
- vazamentos off-chain;
- dependência de provedores de identidade;
- conflitos entre jurisdições;
- uso indevido de IA;
- tratamento irreversível on-chain.

Esses riscos deverão ser tratados continuamente.

## 42. Decisões adiadas

Esta ADR não define:

- fornecedor de identidade;
- padrão de credenciais;
- algoritmo criptográfico;
- carteira;
- formato de identificador;
- banco de dados off-chain;
- política completa de retenção;
- tecnologia de autenticação;
- implementação de RBAC ou ABAC;
- localização física dos dados;
- procedimentos jurídicos por país;
- classificação final de cada campo.

## 43. Próximas decisões necessárias

A próxima decisão será:

> ADR-005 — Classificação, Localização e Ciclo de Vida dos Dados On-chain e Off-chain.

Depois dela serão tratadas consenso, gênese, chaves, auditoria, operações, interoperabilidade e sustentabilidade.

## 44. Compatibilidade

Esta ADR deverá ser interpretada sob a autoridade da ADR-001, ADR-002 e ADR-003.

Em caso de conflito, prevalecerão os princípios que:

- protejam a dignidade humana;
- limitem autoridade;
- preservem responsabilidade;
- minimizem exposição;
- impeçam exploração da fé.

## 45. Estado da decisão

Esta ADR foi expressamente aprovada e congelada por decisão humana em 20 de agosto de 2026.

A identidade, a autorização, a privacidade e a proteção das pessoas na Agape Network deverão permanecer subordinadas a esta decisão durante todo o ciclo de vida do projeto.

Nenhuma implementação técnica está autorizada exclusivamente por esta ADR. Cada fase continuará sujeita à Inspeção Declarativa, decisão arquitetural correspondente e autorização humana.
