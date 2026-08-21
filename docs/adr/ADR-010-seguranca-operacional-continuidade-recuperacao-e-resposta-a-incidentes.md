# ADR-010 — Segurança Operacional, Continuidade, Recuperação e Resposta a Incidentes

- **Status:** Aprovada e congelada
- **Data:** 20 de agosto de 2026
- **Projeto:** Agape Network
- **Repositório:** `bonushora/agape-network`
- **Classificação:** Decisão constitucional, operacional, institucional, arquitetural e de segurança
- **Escopo:** Prevenção, detecção, contenção, continuidade, recuperação, comunicação e aprendizagem
- **Precedência:** Subordinada à ADR-001 até ADR-009
- **Dependências:** ADR-001 a ADR-009

## 1. Contexto

A Agape Network poderá registrar ações de caridade verificável, dados protegidos, decisões institucionais, recursos materiais e relações de confiança entre participantes e instituições.

A indisponibilidade, a perda de integridade ou o uso abusivo dessa infraestrutura poderá causar danos:

- humanos;
- sociais;
- institucionais;
- econômicos;
- jurídicos;
- reputacionais;
- espirituais;
- operacionais.

Segurança não será tratada apenas como propriedade do código ou da blockchain.

Ela dependerá conjuntamente de pessoas, processos, dispositivos, chaves, redes, instituições, contratos, registros e capacidade de recuperação.

## 2. Decisão

A Agape Network adotará segurança operacional baseada em:

1. prevenção proporcional ao risco;
2. privilégio mínimo;
3. separação de poderes;
4. redução da superfície de ataque;
5. detecção verificável;
6. resposta coordenada;
7. continuidade degradada;
8. recuperação testada;
9. preservação de evidências;
10. aprendizagem sem ocultação.

Nenhum mecanismo técnico será considerado infalível.

## 3. Princípio fundamental

> Segurança existe para proteger pessoas e a missão; pessoas não existem para servir ao mecanismo de segurança.

Medidas defensivas deverão preservar dignidade, necessidade, privacidade, devido processo e assistência essencial.

## 4. Responsabilidade compartilhada

A segurança será responsabilidade compartilhada entre:

- governança;
- operadores;
- validadores;
- instituições;
- administradores;
- desenvolvedores;
- prestadores;
- auditores;
- participantes autorizados;
- responsáveis por proteção de dados.

Responsabilidade compartilhada não significará responsabilidade indefinida.

Papéis e deveres deverão ser explicitamente atribuídos.

## 5. Modelo de ameaças

Cada implantação deverá manter modelo de ameaças atualizado.

O modelo deverá considerar:

- atores externos;
- abuso interno;
- credenciais comprometidas;
- conluio;
- coerção;
- fraude;
- erro humano;
- falha de software;
- falha de infraestrutura;
- indisponibilidade de terceiros;
- desastre físico;
- manipulação de dados;
- desinformação;
- risco jurídico;
- risco à pessoa assistida.

## 6. Classificação de ativos

Os ativos deverão ser classificados conforme sua criticidade.

Poderão incluir:

- identidades;
- chaves;
- credenciais;
- dados pessoais;
- registros de ações;
- evidências;
- decisões de governança;
- recursos econômicos;
- configurações;
- código;
- infraestrutura;
- cópias de segurança;
- trilhas de auditoria;
- documentação operacional.

A classificação orientará acesso, proteção, retenção e recuperação.

## 7. Classificação de informações

Informações poderão ser classificadas como:

- públicas;
- internas;
- restritas;
- confidenciais;
- altamente sensíveis;
- legalmente protegidas.

A publicidade de um registro não autorizará a exposição de todos os dados associados.

## 8. Privilégio mínimo

Pessoas, serviços e componentes receberão apenas os privilégios necessários à função autorizada.

Privilégios deverão possuir, quando aplicável:

- finalidade;
- escopo;
- duração;
- responsável;
- justificativa;
- registro;
- revisão;
- revogação.

A conveniência operacional não justificará acesso irrestrito permanente.

## 9. Separação de poderes

Operações críticas não dependerão exclusivamente de uma pessoa, chave, nó ou instituição.

Deverão existir controles proporcionais, como:

- autorização múltipla;
- revisão independente;
- quórum;
- segregação de funções;
- dupla custódia;
- aprovação humana;
- auditoria posterior.

A separação de poderes seguirá as ADRs 002 e 003.

## 10. Identidade operacional

Toda ação administrativa relevante deverá estar vinculada a identidade autenticada e contexto autorizado.

Contas compartilhadas serão evitadas.

Quando tecnicamente inevitáveis, deverão possuir:

- custódia definida;
- uso registrado;
- rotação;
- limites;
- justificativa;
- plano de substituição.

## 11. Autenticação

A autenticação será proporcional ao risco.

Operações de alto impacto deverão exigir autenticação forte e, quando aplicável:

- múltiplos fatores;
- dispositivo confiável;
- confirmação fora de banda;
- nova autenticação;
- presença humana;
- limite temporal.

A perda de um fator não poderá implicar perda definitiva da identidade.

## 12. Autorização

Autenticação não implicará autorização universal.

A autorização considerará:

- identidade;
- instituição;
- função;
- finalidade;
- objeto;
- jurisdição;
- contexto;
- risco;
- tempo;
- política vigente.

A negação deverá ocorrer de forma segura quando requisitos essenciais não forem satisfeitos.

## 13. Chaves criptográficas

Chaves criptográficas serão tratadas como ativos críticos.

Seu ciclo de vida deverá abranger:

- geração;
- custódia;
- uso;
- cópia protegida;
- rotação;
- recuperação;
- suspensão;
- revogação;
- destruição verificável.

Nenhuma chave isolada deverá conceder poder constitucional ilimitado.

## 14. Perda ou comprometimento de chaves

A perda ou suspeita de comprometimento deverá permitir:

- comunicação segura;
- suspensão preventiva;
- análise;
- substituição;
- revogação;
- recuperação de identidade;
- preservação do histórico;
- contestação.

A recuperação não apagará registros legítimos anteriores.

## 15. Segredos operacionais

Senhas, tokens, certificados e credenciais técnicas não serão armazenados em:

- código-fonte público;
- documentação pública;
- mensagens desprotegidas;
- logs;
- imagens;
- exemplos reais;
- artefatos de build não protegidos.

Segredos deverão possuir mecanismo específico de custódia e rotação.

## 16. Segurança dos nós

Cada nó deverá possuir baseline operacional documentado.

O baseline poderá incluir:

- sistema suportado;
- atualizações;
- serviços necessários;
- portas autorizadas;
- firewall;
- sincronização temporal;
- proteção de credenciais;
- logs;
- monitoramento;
- cópias de segurança;
- recuperação.

Serviços desnecessários deverão permanecer desativados.

## 17. Endpoints e dispositivos

Dispositivos usados por operadores poderão constituir parte da superfície de confiança.

A política deverá considerar:

- criptografia local;
- bloqueio;
- atualizações;
- malware;
- perda física;
- acesso remoto;
- cópias locais;
- separação de perfis;
- descarte seguro.

Dispositivo pessoal não será presumido seguro apenas por pertencer a pessoa autorizada.

## 18. Segurança de rede

A comunicação entre componentes deverá aplicar proteção proporcional ao risco.

Deverão ser considerados:

- autenticação mútua;
- criptografia em trânsito;
- segmentação;
- filtragem;
- limitação de taxa;
- proteção contra replay;
- proteção contra interceptação;
- disponibilidade;
- observabilidade.

A exposição pública será minimizada.

## 19. Dependências e cadeia de suprimentos

Dependências de software, imagens, bibliotecas, serviços e artefatos deverão ser conhecidas e verificáveis.

A gestão deverá considerar:

- origem;
- versão;
- integridade;
- licença;
- vulnerabilidades;
- manutenção;
- substituição;
- comprometimento do fornecedor.

Atualização automática sem validação não será presumida segura.

## 20. Desenvolvimento seguro

Mudanças técnicas deverão obedecer a processo verificável com:

- escopo declarado;
- revisão;
- testes;
- análise de impacto;
- validação de segurança;
- rastreabilidade;
- reversão;
- aprovação proporcional.

Ambientes de desenvolvimento, teste e produção deverão permanecer logicamente separados.

## 21. Mudanças operacionais

Alterações de configuração, infraestrutura ou política deverão registrar:

- solicitante;
- finalidade;
- escopo;
- risco;
- aprovação;
- execução;
- resultado;
- reversão;
- evidências.

Mudanças emergenciais deverão ser revisadas após estabilização.

## 22. Gestão de vulnerabilidades

Vulnerabilidades deverão ser:

- recebidas;
- classificadas;
- confirmadas;
- priorizadas;
- corrigidas;
- mitigadas;
- verificadas;
- documentadas.

A prioridade considerará impacto humano, explorabilidade, exposição e criticidade do ativo.

## 23. Divulgação responsável

A rede deverá manter canal seguro para comunicação de vulnerabilidades.

Pesquisadores de boa-fé não deverão ser tratados automaticamente como atacantes.

A divulgação pública deverá equilibrar:

- proteção das pessoas;
- oportunidade de correção;
- transparência;
- interesse coletivo;
- obrigações legais.

## 24. Observabilidade

A rede deverá produzir sinais suficientes para identificar:

- falhas;
- abuso;
- degradação;
- mudanças não autorizadas;
- inconsistências;
- tentativas de acesso;
- perda de sincronização;
- comportamento anômalo.

Observabilidade não autorizará vigilância ilimitada.

## 25. Logs

Logs deverão ser:

- necessários;
- proporcionais;
- íntegros;
- temporalmente coerentes;
- protegidos;
- pesquisáveis;
- retidos por período justificado;
- acessíveis somente a funções autorizadas.

Dados sensíveis deverão ser minimizados ou protegidos.

## 26. Auditoria

Eventos relevantes deverão formar trilha de auditoria capaz de demonstrar:

- quem;
- fez o quê;
- sobre qual objeto;
- quando;
- por qual autoridade;
- com qual resultado;
- sob qual política.

A auditoria não será controlada exclusivamente pelo mesmo agente responsável pela operação auditada.

## 27. Detecção de incidentes

Sinais poderão originar-se de:

- monitoramento;
- usuário;
- instituição;
- auditoria;
- validação social;
- fornecedor;
- autoridade;
- pesquisador;
- inteligência artificial.

Alerta não será automaticamente tratado como prova conclusiva.

## 28. Definição de incidente

Incidente será evento confirmado ou razoavelmente suspeito que comprometa ou ameace:

- confidencialidade;
- integridade;
- disponibilidade;
- autenticidade;
- privacidade;
- segurança física;
- continuidade;
- governança;
- recursos;
- dignidade humana.

Falha técnica sem impacto ainda poderá exigir tratamento preventivo.

## 29. Classificação de severidade

Incidentes serão classificados por critérios documentados.

A avaliação considerará:

- pessoas afetadas;
- urgência;
- extensão;
- reversibilidade;
- dados envolvidos;
- recursos envolvidos;
- propagação;
- impacto institucional;
- impacto jurídico;
- risco à vida.

Severidade não dependerá apenas do valor econômico envolvido.

## 30. Comando de incidente

Cada incidente relevante deverá possuir coordenação explicitamente designada.

A coordenação deverá organizar:

- segurança humana;
- contenção;
- investigação;
- continuidade;
- comunicação;
- recuperação;
- decisões;
- registro;
- encerramento.

O comando temporário não concederá autoridade permanente.

## 31. Contenção

A contenção poderá incluir:

- suspensão de credenciais;
- isolamento de nó;
- bloqueio de operação;
- limitação de integração;
- pausa de automação;
- alteração temporária de rota;
- preservação de evidência;
- operação degradada.

A contenção deverá ser proporcional e revisável.

## 32. Interruptor de emergência

Poderão existir mecanismos de interrupção de funções específicas.

Esses mecanismos deverão:

- possuir escopo limitado;
- exigir autoridade definida;
- gerar registro;
- evitar controle unilateral permanente;
- preservar evidências;
- permitir revisão;
- possuir critérios de retorno.

Um interruptor de emergência não apagará o histórico.

## 33. Continuidade operacional

A rede deverá identificar funções mínimas que precisam continuar durante falhas.

A continuidade poderá usar:

- operação degradada;
- processos manuais;
- canais alternativos;
- registros temporários;
- filas;
- redundância;
- priorização;
- suspensão seletiva.

Continuidade não significará manter todas as funcionalidades disponíveis.

## 34. Assistência durante indisponibilidade

A indisponibilidade da rede não justificará abandono de pessoa em necessidade.

Instituições deverão possuir procedimentos alternativos para assistência essencial.

Registros produzidos fora do sistema poderão ser reconciliados posteriormente mediante validação.

## 35. Objetivos de recuperação

Cada serviço crítico deverá definir, quando aplicável:

- tempo máximo tolerável de interrupção;
- perda máxima tolerável de dados;
- ordem de recuperação;
- dependências;
- responsáveis;
- critérios de validação.

Valores numéricos dependerão da implantação e de ADR técnica.

## 36. Cópias de segurança

Cópias de segurança deverão considerar:

- frequência;
- escopo;
- criptografia;
- segregação;
- imutabilidade;
- retenção;
- restauração;
- custódia;
- descarte;
- jurisdição.

Possuir backup sem testar restauração não constituirá recuperação validada.

## 37. Redundância

Redundância será aplicada segundo criticidade e risco.

Ela poderá abranger:

- nós;
- comunicação;
- energia;
- armazenamento;
- operadores;
- instituições;
- fornecedores;
- localizações.

Redundância aparente baseada na mesma dependência não será considerada independência real.

## 38. Recuperação

A recuperação deverá seguir procedimento documentado e verificável.

Ela deverá confirmar:

- integridade;
- autenticidade;
- estado autorizado;
- versão;
- políticas;
- credenciais;
- conectividade;
- trilhas de auditoria;
- capacidade funcional.

A pressa para retornar não justificará reintroduzir comprometimento conhecido.

## 39. Reconciliação de estado

Após operação degradada ou isolamento, estados divergentes deverão ser reconciliados por regras explícitas.

A reconciliação deverá:

- preservar origem;
- identificar conflito;
- impedir duplicidade;
- registrar decisão;
- permitir contestação;
- proteger dados pessoais;
- manter histórico.

Nenhuma versão será escolhida silenciosamente apenas por ser tecnicamente mais recente.

## 40. Integridade dos registros

Registros críticos deverão possuir mecanismos capazes de detectar alteração indevida.

A proteção poderá utilizar:

- hashes;
- assinaturas;
- encadeamento;
- redundância;
- testemunho independente;
- controle de versão;
- auditoria.

Integridade criptográfica não prova, isoladamente, verdade material.

## 41. Preservação de evidências

Incidentes deverão preservar evidências de forma proporcional.

A preservação deverá registrar:

- origem;
- coletor;
- data;
- método;
- integridade;
- custódia;
- acesso;
- derivação;
- transferência;
- descarte.

A coleta não autorizará exposição desnecessária de pessoas vulneráveis.

## 42. Investigação

Investigações deverão manter independência proporcional à gravidade.

Elas distinguirão:

- fato observado;
- hipótese;
- indicador;
- inferência;
- conclusão;
- responsabilidade.

Suspeita técnica não equivalerá automaticamente a culpa humana.

## 43. Devido processo

Pessoa ou instituição potencialmente responsabilizada deverá possuir, quando cabível:

- ciência;
- acesso proporcional aos fundamentos;
- oportunidade de manifestação;
- contestação;
- revisão;
- correção;
- recurso.

Medidas preventivas urgentes poderão anteceder a manifestação, mas permanecerão revisáveis.

## 44. Comunicação de incidentes

A comunicação deverá ser:

- verdadeira;
- tempestiva;
- proporcional;
- coordenada;
- compreensível;
- compatível com a legislação;
- protetiva das pessoas.

A rede não ocultará incidentes relevantes apenas para preservar reputação institucional.

## 45. Notificação às pessoas afetadas

Pessoas afetadas deverão ser notificadas quando necessário para sua proteção ou por obrigação legal.

A notificação deverá informar, conforme aplicável:

- natureza do incidente;
- possíveis consequências;
- medidas adotadas;
- ações recomendadas;
- canal de suporte;
- direitos;
- atualizações posteriores.

A comunicação não deverá transferir culpa indevida à vítima.

## 46. Autoridades e obrigações legais

Incidentes poderão exigir comunicação a:

- autoridades de proteção de dados;
- autoridades policiais;
- reguladores;
- auditorias;
- parceiros;
- seguradoras;
- órgãos de governança.

A decisão observará jurisdição, materialidade, competência e proteção das pessoas.

## 47. Terceiros e fornecedores

Contratos com terceiros deverão prever, conforme o risco:

- requisitos de segurança;
- notificação;
- auditoria;
- continuidade;
- localização de dados;
- subcontratação;
- encerramento;
- devolução ou eliminação;
- responsabilidade.

A terceirização não elimina a responsabilidade institucional.

## 48. Segurança física

Ambientes físicos críticos deverão considerar:

- acesso;
- energia;
- incêndio;
- água;
- temperatura;
- furto;
- vandalismo;
- desastres naturais;
- descarte;
- continuidade.

A localização de infraestrutura sensível não será divulgada sem necessidade legítima.

## 49. Proteção das pessoas

Uma resposta a incidente não poderá expor pessoas assistidas a:

- retaliação;
- estigma;
- coerção;
- perseguição;
- humilhação;
- violência;
- divulgação indevida;
- perda arbitrária de assistência.

A segurança humana prevalecerá sobre a conveniência investigativa.

## 50. Inteligência artificial

Inteligência artificial poderá auxiliar:

- correlação de eventos;
- identificação de anomalias;
- classificação preliminar;
- análise de vulnerabilidades;
- priorização;
- simulação;
- produção de relatórios.

Não poderá decidir isoladamente:

- culpa;
- expulsão definitiva;
- exposição pública;
- sanção de alto impacto;
- interrupção total da rede;
- acesso irrestrito a dados sensíveis.

## 51. Automação defensiva

Automação poderá executar respostas previamente autorizadas e de baixo risco.

Ações de alto impacto deverão considerar:

- confirmação humana;
- limites;
- reversibilidade;
- evidência;
- escopo;
- expiração;
- auditoria.

Automação sem supervisão não receberá autoridade constitucional aberta.

## 52. Testes e exercícios

Planos de continuidade e resposta deverão ser testados periodicamente.

Os exercícios poderão incluir:

- restauração;
- perda de chave;
- indisponibilidade;
- comprometimento de nó;
- vazamento;
- corrupção de estado;
- falha de fornecedor;
- comunicação;
- operação manual.

Testes não deverão colocar pessoas ou dados reais em risco desnecessário.

## 53. Pós-incidente

Após incidente relevante deverá existir análise que identifique:

- sequência;
- causas;
- fatores contribuintes;
- impacto;
- controles eficazes;
- controles ausentes;
- decisões;
- recuperação;
- recomendações;
- responsáveis;
- prazos.

A finalidade será corrigir o sistema sem eliminar responsabilização legítima.

## 54. Cultura justa

Erro humano, negligência e fraude não serão tratados como equivalentes.

A resposta deverá distinguir:

- engano;
- limitação de formação;
- falha de processo;
- comportamento imprudente;
- abuso consciente;
- ação maliciosa;
- coerção.

A cultura de segurança não dependerá do ocultamento de falhas.

## 55. Métricas

Métricas poderão acompanhar:

- disponibilidade;
- detecção;
- contenção;
- recuperação;
- recorrência;
- correções;
- testes;
- vulnerabilidades;
- acessos;
- impacto.

Métricas não substituirão análise qualitativa nem serão usadas para humilhar operadores.

## 56. Proibições constitucionais

A rede não poderá:

- possuir chave mestra constitucional irrestrita;
- ocultar incidente relevante;
- apagar evidência para proteger reputação;
- abandonar assistência essencial por indisponibilidade;
- presumir culpa por alerta automatizado;
- expor vítimas como método de investigação;
- manter privilégio administrativo sem revisão;
- armazenar segredo em código público;
- tratar backup não testado como recuperação;
- usar segurança para eliminar devido processo;
- permitir que riqueza compre exceções de segurança;
- conceder autoridade permanente por emergência.

## 57. Consequências

Esta decisão:

- estabelece segurança como responsabilidade compartilhada;
- exige privilégio mínimo;
- protege chaves e credenciais;
- define continuidade degradada;
- preserva assistência essencial;
- exige recuperação testada;
- protege evidências;
- exige comunicação proporcional;
- preserva devido processo;
- limita inteligência artificial;
- impede poder emergencial permanente.

## 58. Riscos reconhecidos

Permanecem riscos de:

- erro humano;
- comprometimento interno;
- ataques externos;
- conluio;
- dependência de terceiros;
- falha simultânea;
- corrupção de backups;
- perda de chaves;
- indisponibilidade prolongada;
- resposta excessiva;
- comunicação inadequada;
- falsa sensação de segurança.

Esses riscos exigirão evolução contínua, testes e revisão humana.

## 59. Próxima decisão

A próxima ADR fundamental deverá definir:

> ADR-011 — Interoperabilidade, integrações externas, portabilidade e independência entre projetos.

Ela deverá estabelecer contratos explícitos para a Agape Network consumir e oferecer serviços sem tornar-se dependente, proprietária ou centro arquitetural de outros projetos.

## 60. Estado da decisão

Esta ADR foi expressamente aprovada e congelada por decisão humana em 20 de agosto de 2026.

A segurança operacional, a continuidade, a recuperação e a resposta a incidentes deverão permanecer subordinadas a esta decisão durante todo o ciclo de vida da Agape Network.

Nenhum controle técnico, mecanismo de interrupção, política de retenção, procedimento de recuperação ou automação defensiva está autorizado exclusivamente por esta ADR. Cada implementação continuará sujeita à análise de risco, à Inspeção Declarativa, à ADR técnica correspondente, a testes verificáveis e à autorização humana.
