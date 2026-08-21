# ADR-011 — Interoperabilidade, Integrações Externas, Portabilidade e Independência entre Projetos

- **Status:** Aprovada e congelada
- **Data:** 21 de agosto de 2026
- **Projeto:** Agape Network
- **Repositório:** `bonushora/agape-network`
- **Classificação:** Decisão constitucional, arquitetural, institucional, operacional e de integração
- **Escopo:** Contratos, APIs, eventos, portabilidade, federação, integrações e independência
- **Precedência:** Subordinada à ADR-001 até ADR-010
- **Dependências:** ADR-001 a ADR-010

## 1. Contexto

A Agape Network poderá cooperar com instituições, comunidades, sistemas públicos, organizações privadas e outros projetos tecnológicos.

Essa cooperação poderá exigir troca de:

- identidades protegidas;
- autorizações;
- necessidades;
- ações;
- compromissos;
- evidências;
- validações;
- recursos;
- eventos;
- relatórios;
- decisões;
- dados agregados.

A interoperabilidade não poderá transformar cooperação em dependência estrutural, concentração de poder ou perda de autonomia.

## 2. Problema

Integrações improvisadas podem produzir:

- acoplamento oculto;
- dependência de fornecedor;
- perda de dados;
- duplicidade;
- inconsistência;
- vazamento;
- autoridade implícita;
- confusão de identidade;
- propagação de fraude;
- indisponibilidade em cascata;
- aprisionamento tecnológico.

A existência de uma API não torna uma integração segura ou constitucionalmente autorizada.

## 3. Decisão

A Agape Network será arquiteturalmente independente e interoperável por contratos explícitos.

Ela poderá atuar simultaneamente como:

1. consumidora de serviços;
2. provedora de serviços;
3. participante de uma federação;
4. fonte autorizada de eventos;
5. destinatária autorizada de eventos.

Nenhum desses papéis transformará a Agape Network em proprietária ou subordinada automática de outro projeto.

## 4. Princípio fundamental

> Interoperar significa cooperar por contrato; não significa perder identidade, autoridade ou independência.

Toda integração deverá preservar os limites constitucionais da Agape Network.

## 5. Ausência de centro obrigatório

Nenhum projeto será presumido como centro, proprietário ou autoridade universal do ecossistema.

A Agape Network, o BH-SMC, o Surgical Kernel e outros sistemas deverão permanecer componentes independentes.

A cooperação ocorrerá por interfaces, políticas e autorizações explícitas.

## 6. Independência de implantação

A Agape Network deverá poder ser:

- instalada;
- configurada;
- operada;
- atualizada;
- interrompida;
- recuperada;
- auditada;
- substituída;

sem exigir a presença operacional permanente de outro projeto específico, salvo dependência expressamente contratada para determinada implantação.

## 7. Independência de evolução

A evolução de outro projeto não alterará automaticamente a Agape Network.

Mudanças externas deverão passar por:

- análise de compatibilidade;
- avaliação de risco;
- testes;
- versionamento;
- aprovação;
- implantação controlada;
- possibilidade de reversão.

## 8. Independência jurídica

Integração técnica não produzirá automaticamente:

- sociedade;
- representação;
- mandato;
- solidariedade;
- propriedade conjunta;
- transferência de responsabilidade;
- subordinação institucional.

As relações jurídicas dependerão de instrumentos próprios.

## 9. Independência econômica

Integração não autorizará automaticamente:

- conversão de unidades;
- compartilhamento de saldos;
- compensação financeira;
- emissão conjunta;
- garantia;
- investimento;
- participação societária;
- mercado comum.

As limitações da ADR-009 permanecerão aplicáveis.

## 10. Contrato explícito

Toda integração relevante deverá possuir contrato técnico explícito.

O contrato deverá definir, conforme aplicável:

- partes;
- finalidade;
- versão;
- operações;
- dados;
- autoridade;
- autenticação;
- autorização;
- erros;
- limites;
- auditoria;
- segurança;
- encerramento.

## 11. Autoridade do contrato

O contrato técnico definirá o comportamento permitido da integração, mas não poderá superar:

- as ADRs;
- a legislação;
- os direitos humanos;
- a governança;
- o consentimento;
- as políticas institucionais aplicáveis.

Contrato tecnicamente válido poderá ainda ser institucionalmente proibido.

## 12. Interfaces

Interfaces poderão incluir:

- APIs;
- eventos;
- arquivos;
- filas;
- webhooks;
- protocolos federativos;
- importações;
- exportações;
- conectores;
- procedimentos manuais controlados.

A tecnologia concreta dependerá de decisão técnica posterior.

## 13. APIs

APIs deverão possuir:

- finalidade definida;
- escopo mínimo;
- autenticação;
- autorização;
- versionamento;
- validação;
- limites;
- tratamento de erros;
- observabilidade;
- documentação.

Endpoint exposto não significará acesso público irrestrito.

## 14. Eventos

Eventos de integração deverão registrar:

- tipo;
- origem;
- produtor;
- momento;
- identificador;
- versão;
- finalidade;
- escopo;
- correlação;
- integridade.

Um evento representará uma declaração de fato ou estado, não uma ordem universal.

## 15. Comandos externos

Comandos recebidos de sistemas externos deverão ser tratados como solicitações sujeitas à autoridade local.

Nenhum sistema externo poderá comandar automaticamente operação crítica apenas por possuir conectividade.

## 16. Identidade da origem

Toda mensagem relevante deverá permitir identificar sua origem lógica.

A origem deverá ser distinguida de:

- intermediário;
- transportador;
- operador;
- validador;
- destinatário;
- pessoa representada.

O transporte de uma declaração não transfere sua autoria.

## 17. Identidade federada

A rede poderá aceitar identidade federada mediante confiança explícita.

A federação deverá definir:

- emissor;
- atributos aceitos;
- validade;
- nível de garantia;
- revogação;
- finalidade;
- vínculo local;
- auditoria.

Identidade federada não concederá autorização universal.

## 18. Identificadores

Identificadores deverão possuir namespace ou contexto suficiente para evitar colisões.

A implementação deverá distinguir:

- pessoa;
- instituição;
- tenant;
- projeto;
- ação;
- registro;
- evento;
- credencial;
- unidade;
- versão.

Semelhança textual não estabelecerá identidade.

## 19. Multi-institucionalidade

Cada instituição participante manterá identidade, responsabilidade e autoridade próprias.

A integração deverá preservar:

- origem institucional;
- contexto;
- políticas;
- jurisdição;
- responsáveis;
- limites;
- rastreabilidade.

## 20. Multi-tenancy

Quando houver múltiplos tenants, deverão existir controles para:

- isolamento;
- identidade;
- autorização;
- configuração;
- dados;
- chaves;
- auditoria;
- limites;
- exportação;
- encerramento.

Nenhum tenant poderá acessar outro por mera coexistência na infraestrutura.

## 21. Consumidor e provedor

A Agape Network poderá consumir e fornecer capacidades de modo simultâneo.

Cada capacidade deverá declarar:

- quem fornece;
- quem consome;
- quem autoriza;
- quem responde;
- quais dados circulam;
- quais garantias existem.

O papel de provedor não concede autoridade sobre o consumidor.

## 22. Catálogo de capacidades

Capacidades interoperáveis deverão possuir catálogo verificável.

O catálogo poderá registrar:

- nome;
- finalidade;
- proprietário operacional;
- versão;
- disponibilidade;
- requisitos;
- riscos;
- dados;
- suporte;
- descontinuação.

Descoberta de capacidade não equivale à autorização de uso.

## 23. Descoberta de serviços

Mecanismos de descoberta deverão ser protegidos contra:

- falsificação;
- redirecionamento;
- serviço impostor;
- versão incompatível;
- captura;
- indisponibilidade;
- enumeração indevida.

A descoberta será separada da decisão de confiança.

## 24. Versionamento

Contratos interoperáveis deverão possuir versão identificável.

Mudanças incompatíveis deverão gerar nova versão ou processo explícito de migração.

A interpretação silenciosa de contrato incompatível será proibida.

## 25. Compatibilidade

Compatibilidade deverá ser avaliada em dimensões:

- sintática;
- semântica;
- operacional;
- jurídica;
- institucional;
- de segurança;
- de privacidade;
- de governança.

Formato igual não garante significado igual.

## 26. Semântica

Campos, eventos e operações deverão possuir significado documentado.

A documentação deverá distinguir:

- fato;
- alegação;
- validação;
- autorização;
- recomendação;
- decisão;
- correção;
- revogação.

A interoperabilidade não poderá apagar essas distinções.

## 27. Schemas

Dados estruturados deverão usar schemas versionados quando aplicável.

Schemas deverão definir:

- campos;
- tipos;
- obrigatoriedade;
- cardinalidade;
- formatos;
- enumerações;
- extensões;
- restrições;
- regras de evolução.

Validação estrutural não provará veracidade material.

## 28. Extensibilidade

Contratos poderão admitir extensões sem comprometer o núcleo comum.

Extensões deverão:

- possuir namespace;
- ser opcionais quando apropriado;
- não alterar silenciosamente campos existentes;
- preservar compatibilidade;
- ser documentadas;
- ser ignoradas com segurança quando desconhecidas.

## 29. Idempotência

Operações repetíveis deverão possuir mecanismos de idempotência quando duplicidade puder causar dano.

A idempotência deverá considerar:

- chave;
- escopo;
- validade;
- identidade;
- payload;
- resultado;
- concorrência;
- persistência.

Repetição divergente não será tratada como repetição equivalente.

## 30. Correlação e causalidade

Operações distribuídas deverão permitir correlação entre:

- solicitação;
- autorização;
- execução;
- evento;
- resposta;
- correção;
- falha.

Correlação técnica não será presumida como prova absoluta de causalidade humana.

## 31. Ordenação

Quando a ordem for relevante, o contrato deverá definir a garantia disponível.

A implementação não presumirá ordem global perfeita em ambiente distribuído.

Conflitos de ordem deverão ser detectáveis e reconciliáveis.

## 32. Tempo

Registros interoperáveis deverão distinguir, quando aplicável:

- momento declarado;
- momento observado;
- momento recebido;
- momento processado;
- momento confirmado.

Relógios divergentes não poderão ser ocultados como certeza temporal.

## 33. Entrega

A integração deverá declarar sua garantia de entrega, como:

- melhor esforço;
- ao menos uma vez;
- no máximo uma vez;
- entrega confirmada;
- processamento idempotente.

Nenhuma garantia será anunciada sem mecanismo verificável correspondente.

## 34. Erros

Erros deverão ser explícitos, classificados e seguros.

Respostas não deverão revelar:

- segredos;
- dados pessoais desnecessários;
- topologia sensível;
- credenciais;
- detalhes exploráveis.

Falha externa não poderá ser convertida silenciosamente em sucesso local.

## 35. Timeouts e repetição

Timeouts e políticas de repetição deverão possuir limites.

Repetições deverão evitar:

- duplicidade;
- tempestade de requisições;
- sobrecarga;
- propagação de falha;
- amplificação;
- bloqueio indefinido.

## 36. Circuit breaker e isolamento

Integrações poderão ser temporariamente isoladas quando apresentarem falha ou risco.

O isolamento deverá:

- possuir motivo;
- gerar registro;
- ter escopo definido;
- preservar funções essenciais;
- permitir revisão;
- possuir critérios de retorno.

## 37. Operação degradada

A indisponibilidade de integração externa não deverá necessariamente interromper toda a Agape Network.

Funções essenciais deverão possuir, quando possível:

- fallback;
- fila;
- cache autorizado;
- procedimento manual;
- reconciliação posterior;
- comunicação de degradação.

## 38. Segurança da integração

Cada integração deverá aplicar os princípios da ADR-010.

Deverão ser considerados:

- autenticação;
- autorização;
- criptografia;
- integridade;
- replay;
- falsificação;
- abuso;
- limitação;
- monitoramento;
- resposta a incidentes.

## 39. Privacidade

Compartilhamento de dados deverá obedecer às ADRs 004 e 005.

A integração deverá observar:

- finalidade;
- necessidade;
- minimização;
- consentimento quando aplicável;
- base legítima;
- retenção;
- acesso;
- correção;
- revogação;
- eliminação quando cabível.

Interoperabilidade não será justificativa genérica para coleta ilimitada.

## 40. Dados de pessoas assistidas

Dados de pessoas assistidas receberão proteção reforçada.

Sua integração não poderá ser condicionada a:

- exposição pública;
- propaganda;
- conversão religiosa;
- cessão comercial;
- criação de mercado;
- perda de assistência essencial.

## 41. Portabilidade

A Agape Network deverá permitir portabilidade legítima de dados e registros.

A portabilidade deverá preservar:

- significado;
- origem;
- integridade;
- contexto;
- versão;
- autorização;
- relações;
- correções;
- revogações.

## 42. Exportação

Exportações deverão usar formato documentado e verificável.

O processo deverá indicar:

- solicitante;
- autoridade;
- escopo;
- data;
- formato;
- integridade;
- limitações;
- resultado.

Exportação não autorizará o destinatário a usar os dados para qualquer finalidade.

## 43. Importação

Importações deverão ser validadas antes de afetar o estado canônico.

A validação deverá considerar:

- origem;
- integridade;
- schema;
- versão;
- duplicidade;
- autorização;
- finalidade;
- riscos;
- conflitos.

Dados importados não receberão confiança superior à sua evidência.

## 44. Migração

Migração entre versões ou plataformas deverá possuir:

- plano;
- inventário;
- mapeamento;
- validação;
- backup;
- reversão;
- reconciliação;
- critérios de aceite;
- registro.

Nenhuma migração apagará silenciosamente informação constitucionalmente relevante.

## 45. Reversibilidade

Integrações deverão ser reversíveis quando técnica e juridicamente possível.

A reversibilidade deverá considerar:

- desativação;
- exportação;
- revogação;
- substituição;
- preservação do histórico;
- eliminação legítima;
- continuidade.

## 46. Prevenção de lock-in

Nenhum fornecedor deverá deter, por desenho oculto, capacidade exclusiva de:

- interpretar dados;
- recuperar o sistema;
- operar identidades;
- acessar evidências;
- exportar registros;
- validar integridade;
- substituir componentes.

Dependências inevitáveis deverão ser documentadas e aceitas conscientemente.

## 47. Código e tecnologia

Esta ADR não determina:

- linguagem;
- framework;
- banco de dados;
- blockchain;
- protocolo de transporte;
- nuvem;
- fornecedor;
- formato único;
- middleware;
- barramento de eventos.

Essas escolhas dependerão de inspeção e ADR técnica.

## 48. Integrações com sistemas públicos

Integrações governamentais deverão respeitar:

- competência;
- finalidade pública;
- legislação;
- acessibilidade;
- transparência;
- privacidade;
- segurança;
- devido processo;
- continuidade.

A integração não transformará a Agape Network em órgão estatal.

## 49. Integrações privadas

Integrações com empresas deverão impedir:

- venda indevida de dados;
- publicidade coercitiva;
- discriminação econômica;
- aprisionamento;
- prioridade comprada;
- captura da governança;
- exploração de vulnerabilidade.

Interesse comercial permanecerá subordinado às ADRs.

## 50. Relação com o BH-SMC

A Agape Network poderá interoperar com o BH-SMC por contratos explícitos.

Essa possibilidade não estabelece:

- identidade entre os projetos;
- dependência obrigatória;
- banco de dados comum;
- propriedade comum;
- autoridade automática;
- conversão econômica;
- integração já implementada.

Cada projeto permanecerá independente, multi-institucional e capaz de atuar como consumidor ou provedor.

## 51. Relação com o Surgical Kernel

A Agape Network poderá utilizar o Surgical Kernel para governança de operações, políticas, auditoria ou execução controlada.

Essa possibilidade não estabelece:

- incorporação do Kernel à Agape Network;
- domínio do Kernel sobre a governança humana;
- acesso irrestrito;
- implantação já autorizada;
- dependência exclusiva;
- transferência de responsabilidade.

Toda integração dependerá de contrato, política e ADR técnica.

## 52. Relação com o Surgical DevOps

O Surgical DevOps poderá auxiliar a evolução segura dos artefatos técnicos da Agape Network.

Ele não será componente obrigatório do runtime da rede.

Sua atuação deverá permanecer subordinada a:

- inspeção declarativa;
- escopo autorizado;
- modo PATCH;
- preservação do estado;
- validação;
- auditoria;
- autoridade humana.

## 53. Inteligência artificial

Inteligência artificial poderá auxiliar:

- mapeamento de schemas;
- detecção de incompatibilidades;
- classificação;
- documentação;
- testes;
- reconciliação assistida;
- detecção de anomalias.

Não poderá decidir isoladamente:

- confiança institucional;
- compartilhamento de dados sensíveis;
- equivalência jurídica;
- fusão de identidades;
- migração irreversível;
- autoridade entre projetos.

## 54. Auditoria interoperável

Cada integração relevante deverá produzir evidências suficientes para reconstruir:

- contrato vigente;
- origem;
- autorização;
- solicitação;
- processamento;
- resposta;
- falha;
- repetição;
- correção;
- encerramento.

Auditoria compartilhada não eliminará a trilha local de cada participante.

## 55. Encerramento de integração

O encerramento deverá prever:

- comunicação;
- data;
- bloqueio de novas operações;
- tratamento das pendências;
- exportação;
- revogação de credenciais;
- retenção legítima;
- eliminação aplicável;
- continuidade;
- auditoria final.

Encerrar a integração não apagará fatos históricos legítimos.

## 56. Proibições constitucionais

A Agape Network não poderá:

- tornar outro projeto seu centro obrigatório;
- declarar-se proprietária de todo o ecossistema;
- conceder autoridade por mera conectividade;
- aceitar comandos externos sem autorização local;
- fundir identidades silenciosamente;
- compartilhar dados sem finalidade legítima;
- usar formato proprietário para impedir saída;
- converter unidades econômicas automaticamente;
- tratar compatibilidade sintática como equivalência semântica;
- ocultar dependência crítica;
- permitir acesso entre tenants por coexistência;
- apagar origem ou histórico em migração;
- permitir que integração supere as ADRs.

## 57. Consequências

Esta decisão:

- preserva independência entre projetos;
- permite cooperação contratual;
- estabelece papéis de consumidor e provedor;
- protege ambientes multi-institucionais;
- exige versionamento;
- protege semântica;
- exige idempotência quando necessária;
- assegura portabilidade;
- reduz lock-in;
- limita comandos externos;
- mantém integrações subordinadas à autoridade humana.

## 58. Riscos reconhecidos

Permanecem riscos de:

- acoplamento gradual;
- incompatibilidade semântica;
- dependência de fornecedor;
- perda de contexto;
- duplicidade;
- atraso;
- indisponibilidade em cascata;
- falha de identidade;
- compartilhamento excessivo;
- migração defeituosa;
- contrato desatualizado;
- confiança indevida;
- fragmentação do ecossistema.

Esses riscos exigirão contratos testáveis, auditoria e evolução controlada.

## 59. Próxima decisão

A próxima ADR fundamental deverá definir:

> ADR-012 — Ciclo de vida, implantação progressiva, pilotos, métricas e critérios de maturidade.

Ela deverá estabelecer como a Agape Network passará da fundamentação constitucional para protótipos, pilotos limitados, homologação e eventual produção sem antecipar capacidades não validadas.

## 60. Estado da decisão

Esta ADR foi expressamente aprovada e congelada por decisão humana em 21 de agosto de 2026.

A interoperabilidade, as integrações externas, a portabilidade e a independência entre projetos deverão permanecer subordinadas a esta decisão durante todo o ciclo de vida da Agape Network.

Nenhuma API, integração, federação, migração, importação, exportação ou interoperabilidade com outro projeto está autorizada exclusivamente por esta ADR. Cada implementação continuará sujeita à Inspeção Declarativa, ao contrato explícito, à análise jurídica e de segurança, à ADR técnica correspondente, a testes verificáveis e à autorização humana.
