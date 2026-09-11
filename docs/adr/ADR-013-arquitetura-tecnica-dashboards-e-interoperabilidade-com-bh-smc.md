# ADR-013 — Arquitetura Técnica, Dashboards e Interoperabilidade Contratual com o BH-SMC

- **Status:** Aprovada e congelada
- **Data:** 11 de setembro de 2026
- **Projeto:** Agape Network
- **Classificação:** Decisão técnica, arquitetural, de experiência humana, observabilidade e integração
- **Escopo:** Arquitetura do protótipo, dashboards, simulação de governança, observabilidade dos validadores e interoperabilidade contratual com o BH-SMC
- **Precedência:** Subordinada às ADR-001 até ADR-012
- **Dependências de implementação:** Pacote canônico do BH-SMC para qualquer interoperabilidade; contratos técnicos; análise jurídica e de segurança; gates e validação humana aplicáveis

## 1. Contexto

As ADR-001 até ADR-012 estabeleceram o fundamento ético, institucional, federativo, econômico, de segurança, interoperabilidade e ciclo de vida da Agape Network.

A próxima fronteira é transformar esses limites em uma arquitetura técnica verificável, sem confundir protótipo com produção e sem conceder autoridade por meio da interface.

## 2. Problema

Uma implementação prematura poderia:

- escolher tecnologia sem evidência suficiente;
- tornar um dashboard uma fonte oculta de autoridade;
- confundir simulação de voto com votação real;
- expor dados de instituições ou pessoas;
- tratar endpoints existentes do BH-SMC como contrato canônico;
- converter compatibilidade de formato em equivalência de significado;
- antecipar emissão, integração ou produção.

## 3. Decisão

Esta ADR propõe definir o envelope técnico do primeiro protótipo da Agape Network, incluindo:

1. módulos arquiteturais e fronteiras de confiança;
2. dashboards amigáveis para usuários e instituições candidatas;
3. sandbox de simulação de votação sem efeito na rede;
4. dashboard de observabilidade e operação para candidatos a validador;
5. adaptador contratual para futura interoperabilidade com o BH-SMC;
6. critérios de validação antes de qualquer piloto.

Esta ADR não autoriza produção, gênese federativa, emissão, homologação institucional ou integração operacional.

## 4. Princípio fundamental

> A arquitetura deve tornar limites, evidências e incertezas visíveis; nunca transformar conveniência técnica em autoridade.

## 5. Natureza da decisão

O documento foi criado a partir de uma proposta e agora é registrado como decisão aprovada e congelada por manifestação humana expressa. A aprovação congela apenas o escopo desta ADR; não libera os gates de implementação nem os bloqueios de interoperabilidade.

Nenhuma afirmação desta ADR equivale a capacidade implementada ou homologada.

## 6. Objetivos

São objetivos desta decisão:

- permitir um protótipo isolado e auditável;
- separar experiência humana, operação e autoridade;
- oferecer visualizações adequadas a cada papel;
- testar contratos e fluxos com dados sintéticos;
- preservar independência entre Agape Network e BH-SMC;
- preparar evidência para decisões técnicas posteriores.

## 7. Não objetivos

Esta ADR não decide:

- provedor de nuvem;
- compra de hardware;
- framework definitivo;
- gênese da rede;
- conjunto de validadores de produção;
- emissão ou circulação de qualquer unidade social;
- integração com dados reais;
- homologação definitiva de instituição;
- produção pública ou irreversível.

## 8. Envelope arquitetural

O protótipo deverá ser modular, permissionado, reversível e executável em ambiente isolado.

As fronteiras entre identidade, governança, registros, APIs, dashboards, observabilidade e adaptadores externos deverão ser explícitas.

## 9. Neutralidade tecnológica

Cosmos SDK, Substrate ou outra alternativa poderão ser avaliados, mas nenhum é selecionado por esta decisão.

A seleção deverá obedecer aos requisitos das ADR-001 até ADR-012 e a evidência obtida no protótipo.

## 10. Critérios de seleção

Alternativas técnicas deverão ser comparadas por:

- determinismo e reprodutibilidade;
- consenso permissionado e governança de validadores;
- isolamento de tenants;
- autorização verificável;
- observabilidade sem exposição indevida;
- recuperação e reversibilidade;
- portabilidade de dados;
- manutenção sem lock-in;
- execução local sem dependência obrigatória de cobrança;
- capacidade de teste com dados sintéticos.

## 11. Registro da seleção

Enquanto não houver comparação documentada, a seleção tecnológica permanecerá `DEFERRED`.

Uma demonstração de framework não será tratada como decisão arquitetural.

## 12. Ambiente do protótipo

O primeiro ambiente deverá ser `localhost` ou ambiente de teste explicitamente identificado.

Ele deverá possuir identidade, credenciais, dados, chaves, logs e autoridade separados de qualquer ambiente externo.

## 13. Ciclo de vida

O protótipo seguirá a sequência:

1. descoberta;
2. desenho;
3. implementação mínima;
4. teste com dados sintéticos;
5. demonstração controlada;
6. revisão humana;
7. eventual piloto mediante nova decisão.

Nenhuma etapa avança automaticamente para produção.

## 14. Módulos mínimos

O desenho deverá prever, sem obrigar implementação imediata:

- núcleo de registros e estados;
- identidade e autorização;
- governança e votação;
- catálogo de ações e eventos;
- adaptadores de integração;
- APIs versionadas;
- dashboards por papel;
- observabilidade;
- auditoria e recuperação.

## 15. Estados explícitos

Capacidades e operações deverão usar estados observáveis, como:

- `PASSOU`;
- `FALHOU`;
- `BLOCKED`;
- `NÃO_EXECUTADO`;
- `DEFERRED`;
- `NOT_APPLICABLE`.

Ausência de evidência não poderá ser apresentada como sucesso.

## 16. Dados do protótipo

O protótipo utilizará dados sintéticos ou dados anonimizados sem possibilidade razoável de reidentificação.

Dados reais somente poderão ser considerados em fase posterior quando todos os requisitos da ADR-012 e das ADR-004/005 estiverem satisfeitos, com autorização específica. Nenhum dado real é autorizado por esta ADR.

## 17. Identidade e autorização

Cada usuário, instituição, operador e validador deverá possuir identidade e capacidade compatíveis com seu papel.

Autenticação não implicará autorização universal.

## 18. Isolamento institucional

Nenhum tenant poderá acessar outro por mera coexistência na infraestrutura.

Dashboards deverão filtrar dados por escopo, finalidade e autorização verificável.

## 19. Portal do usuário candidato

O portal destinado a usuários e instituições candidatas deverá apresentar, em linguagem clara:

- propósito da rede;
- regras de adesão voluntária;
- direitos e responsabilidades;
- estado da candidatura;
- dados compartilhados e finalidade;
- eventos e ofertas não essenciais, quando autorizados;
- canal de contestação e saída.

O portal não poderá prometer autoridade, rendimento ou acesso garantido.

## 20. Adesão institucional

O fluxo deverá separar:

- manifestação de interesse;
- análise documental;
- período de observação;
- validação técnica;
- decisão de homologação;
- manutenção e revisão.

Indicação por uma instituição candidata não equivalerá a homologação pela rede.

## 21. Sandbox de votação

O dashboard de governança deverá oferecer uma sandbox de votação com:

- identidades sintéticas;
- chaves de teste;
- propostas fictícias;
- simulação de quórum;
- registro de votos de ensaio;
- resultado claramente marcado como simulado.

Nenhum voto da sandbox poderá alterar estado canônico, saldo, autoridade, composição de validadores ou contrato externo.

A simulação deverá representar, sem produzir autoridade real, o quórum superior a dois terços exigido pela ADR-006 e o quórum mínimo de dois terços para admissões e exclusões previsto nas ADR-002/003, excluindo participantes impedidos por conflito de interesses.

## 22. Separação entre simulação e decisão

A interface deverá mostrar, de forma persistente:

- `SIMULAÇÃO` ou `PRODUÇÃO`;
- ambiente;
- origem dos dados;
- autoridade aplicável;
- efeito esperado;
- efeito realmente produzido.

Não será permitido reutilizar uma chave ou endpoint de produção na sandbox.

## 23. Dashboard de validação institucional

O dashboard da instituição candidata deverá exibir:

- requisitos de ingresso;
- documentos pendentes;
- evidências aceitas e rejeitadas;
- conflitos declarados;
- período de observação;
- decisão humana pendente;
- regras de manutenção;
- condições de suspensão e saída.

O dashboard não atribuirá mérito espiritual, superioridade religiosa ou valor humano.

## 24. Dashboard de usuário e comunidade

O dashboard comunitário poderá exibir:

- ações disponíveis;
- eventos não essenciais homologados;
- regras de participação;
- registros próprios;
- benefícios autorizados;
- histórico de decisões relevantes;
- avisos de degradação ou suspensão.

Não exibirá saldos ou rankings como medida de dignidade, fé ou autoridade espiritual.

## 25. Dashboard do validador candidato

O dashboard de observabilidade e operação deverá exibir, conforme o escopo autorizado:

- identidade do nó e do domínio;
- estado de sincronização;
- saúde dos processos;
- versão e compatibilidade;
- latência e disponibilidade;
- incidentes e ações pendentes;
- backups e recuperação;
- estado de chaves sem revelar segredos;
- evidências exigidas para manutenção.

## 26. Observabilidade operacional

Métricas, logs, traces e alertas deverão possuir origem, timestamp, ambiente e retenção definidos.

Agregação não poderá ocultar falha material ou divergência entre nós.

## 27. Métricas

O protótipo poderá medir:

- disponibilidade;
- latência;
- atraso de sincronização;
- taxa de erro;
- tempo de recuperação;
- cobertura de auditoria;
- acessibilidade;
- compreensão do estado pelo usuário.

Nenhuma métrica operacional será convertida automaticamente em reputação humana ou autoridade institucional.

## 28. Segurança dos dashboards

Dashboards deverão aplicar:

- privilégio mínimo;
- separação de leitura e mutação;
- proteção contra replay;
- limitação de requisições;
- redaction de segredos;
- proteção contra enumeração;
- registro de acesso;
- expiração de sessão;
- isolamento entre ambientes.

## 29. APIs do protótipo

APIs deverão ser versionadas, documentadas e testáveis.

Cada operação deverá declarar método, finalidade, autorização, schema, resposta, erro, idempotência e efeito esperado.

Uma rota descoberta em outro sistema não será adotada como contrato sem validação.

## 30. Classificação do material BH-SMC

O material disponível do BH-SMC contém referências operacionais de backend, implantação, endpoints, dashboards e textos públicos sobre o protocolo BônusHora.

Essas referências são úteis para descoberta e mapeamento, mas não foram verificadas como ADRs canônicas, contrato constitucional ou pacote semântico assinado e versionado.

Sua autoridade nesta ADR é, portanto, `referência não normativa`.

## 31. Dependência canônica do BH-SMC

A interoperabilidade permanecerá `BLOCKED` até que seja fornecido ou identificado um pacote canônico do BH-SMC contendo, no mínimo:

- identidade do projeto e versão;
- glossário e semântica oficial;
- propósito e limites de uso;
- definição de PoSQ e PoVC, se mantidos;
- regras de registro, emissão, uso e revogação;
- distinção entre registros fungíveis, não fungíveis ou outras representações, se aplicável;
- governança e autoridade;
- schemas e versões de API;
- tratamento de privacidade e segurança;
- evidências de testes e aprovação.

## 32. Independência entre projetos

Agape Network e BH-SMC permanecerão independentes.

Interoperabilidade não criará automaticamente:

- banco de dados comum;
- propriedade comum;
- autoridade compartilhada;
- conversão entre unidades;
- mandato institucional;
- dependência obrigatória;
- homologação recíproca.

## 33. Adaptador contratual

Qualquer futura conexão deverá ocorrer por adaptador isolado, com:

- contrato explícito;
- identidade da origem;
- versão do schema;
- finalidade;
- escopo mínimo;
- autorização local;
- correlação;
- idempotência;
- garantia de entrega;
- tratamento de falha;
- revogação e encerramento.

## 34. Equivalência semântica

Formato igual não garante significado igual.

O adaptador deverá distinguir:

- campo compatível;
- campo parcialmente compatível;
- campo sem equivalente;
- campo cuja interpretação está `BLOCKED`.

Nenhum mapeamento automático poderá decidir equivalência jurídica, econômica, religiosa ou institucional.

## 35. Fluxo de confiança

Dados recebidos do BH-SMC deverão ser tratados como evidência externa com confiança limitada ao contrato e à prova disponível.

Validação estrutural não provará veracidade material.

O estado canônico da Agape Network não será alterado por importação não autorizada.

## 36. Tempo, correlação e entrega

Mensagens interoperáveis deverão distinguir, quando aplicável:

- momento declarado;
- momento observado;
- momento recebido;
- momento processado;
- momento confirmado.

Também deverão possuir identificador de correlação, política de repetição, garantia de entrega e mecanismo de reconciliação.

## 37. Erros e operação degradada

Falha externa não poderá ser convertida silenciosamente em sucesso local.

O protótipo deverá prever, conforme aplicável:

- timeout limitado;
- retry limitado;
- circuit breaker;
- fila;
- cache autorizado;
- fallback manual;
- reconciliação posterior;
- comunicação de degradação.

## 38. Encerramento da integração

O contrato futuro deverá prever bloqueio de novas operações, tratamento de pendências, exportação, revogação de credenciais, retenção legítima, eliminação aplicável, continuidade e auditoria final.

Encerramento não apagará fatos históricos legítimos.

## 39. Eventos e instituições credenciadas

O protótipo poderá modelar acesso a eventos culturais, religiosos, educacionais ou de entretenimento como reciprocidade comunitária não essencial, quando autorizado.

Isso não será compra, venda, preço, pagamento, revenda, conversão financeira ou garantia de ingresso.

Instituição candidata poderá indicar um evento, mas sua apresentação como oferta da rede exigirá propósito explícito, critérios observáveis, homologação independente e respeito à liberdade de consciência.

## 40. Vocabulário e finalidade social

O projeto deverá preferir expressões como:

- registro de contribuição;
- unidade de reciprocidade;
- acesso comunitário;
- benefício não essencial;
- evidência de serviço;
- reconhecimento operacional.

Não serão adotados, para descrever a Agape Network, conceitos de pagamento, investimento, rendimento, cotação, liquidez, mercado ou enriquecimento.

## 41. Emissão e representações digitais

Esta ADR não autoriza emissão, distribuição, negociação ou conversão de qualquer representação digital, fungível ou não fungível.

Qualquer decisão futura sobre representação de registros sociais exigirá ADR própria, análise jurídica e econômica, modelo anti-especulação, regras de emissão e revogação, piloto controlado e aprovação humana.

## 42. Adesão ecumênica e interconfessional

O desenho deverá apoiar adesão voluntária de instituições católicas, espíritas e outras instituições religiosas sérias, sem:

- conversão;
- proselitismo coercitivo;
- exclusividade denominacional;
- discriminação por tradição;
- compra de autoridade por doação ou prestígio;
- declaração de reconhecimento canônico sem autoridade competente.

A rede não será apresentada como órgão de uma igreja, federação religiosa ou doutrina específica.

## 43. Validadores e custeio

O protótipo deverá permitir modelar regras de manutenção do validador sem exigir taxa, staking, contribuição, doação ou pagamento obrigatório para adesão ou voto.

Custos legítimos de energia, conectividade, hardware, hospedagem e recuperação deverão ser transparentes, auditáveis e incapazes de comprar voto ou autoridade.

## 44. Papel da inteligência artificial

IA poderá auxiliar:

- mapeamento de schemas;
- detecção de incompatibilidades;
- geração de documentação;
- classificação de evidências;
- testes;
- reconciliação assistida;
- detecção de anomalias.

IA não poderá decidir isoladamente autoridade, equivalência semântica, homologação, emissão, produção ou integração irreversível.

## 45. Cloud e PC dedicado

A arquitetura deverá ser portátil entre PC dedicado e eventual hospedagem externa.

Uma opção externa só poderá ser considerada candidata se for verificadamente permanente, sem cartão, sem faturamento obrigatório, sem trial, sem crédito promocional e sem cobrança oculta.

Na ausência dessa evidência, o PC dedicado permanecerá o fallback de bootstrap, sem criar dependência constitucional.

## 46. Redundância de bootstrap

O desenho poderá testar a retirada do PC da condição de único ponto de hospedagem depois de dois nós validadores externos independentes estarem comprovadamente capazes de manter serviço, estado, observabilidade, backup e recuperação em bootstrap ou piloto.

Esse marco não constituirá produção, tolerância BFT completa, gênese federativa ou independência constitucional.

## 47. Produção e transição federativa

Produção e transição continuarão subordinadas às ADR-006, ADR-007 e ADR-012.

A existência de dashboards, APIs, dois nós ou uma demonstração pública não autorizará produção.

O mínimo de quatro domínios validadores independentes e os demais gates permanecerão exigidos quando aplicáveis.

## 48. Testes e dados sintéticos

O primeiro protótipo deverá testar:

- navegação por papel;
- leitura de estado;
- simulação de voto;
- isolamento de tenants;
- observabilidade de validador;
- falhas de rede;
- repetição e reconciliação;
- exportação e recuperação;
- acessibilidade e compreensão humana.

Os testes não deverão emitir registros sociais reais nem afetar instituições candidatas.

## 49. Segurança arquitetural

O protótipo deverá aplicar autenticação, autorização, criptografia, integridade, proteção contra replay, limitação, monitoramento, resposta a incidentes e recuperação conforme a ADR-010.

Segredos, dados pessoais desnecessários e topologia sensível não serão exibidos nos dashboards.

## 50. Privacidade e direitos

Qualquer coleta deverá observar finalidade, necessidade, minimização, base legítima, retenção, acesso, correção, revogação e eliminação quando cabível.

Pessoa assistida não poderá perder assistência por não participar do dashboard, da votação ou da interoperabilidade.

## 51. Portabilidade e reversibilidade

O protótipo deverá permitir exportar configurações, schemas, registros de teste, evidências, decisões e versões sem dependência de fornecedor único.

Migrações deverão preservar origem, contexto, autorização, correções, revogações e histórico.

## 52. Validação red-to-green

Antes de implementar qualquer componente de risco médio ou alto deverá existir baseline pertinente, hipótese, escopo e teste RED identificável.

Depois da alteração, a validação deverá alcançar GREEN ou registrar a razão objetiva do bloqueio.

## 53. GREEN independente

Código, backend, interface, operação, implantação, publicação e experiência humana serão avaliados como dimensões separadas.

Um dashboard visualmente funcional não provará segurança, governança, integração ou produção.

## 54. Gates e autorização

Cada mutação deverá possuir autorização vinculada ao objetivo, workspace, risco e fronteiras.

Serão exigidos gates adicionais para:

- dados reais;
- credenciais externas;
- alteração destrutiva;
- publicação;
- integração operacional;
- produção;
- emissão ou mudança de representação social;
- ampliação de autoridade.

## 55. Evidência de conclusão

Uma etapa só será concluída quando houver evidência física verificável do artefato, ambiente, testes, estado e pós-condição declarados.

Relato do executor sem evidência independente será `NÃO_EXECUTADO`.

## 56. Riscos reconhecidos

Persistem riscos de:

- usar material operacional como norma;
- confundir dashboard com autoridade;
- vazamento de dados;
- dependência de fornecedor;
- mapeamento semântico incorreto;
- duplicidade e atraso;
- proselitismo ou exclusão institucional;
- linguagem financeira indevida;
- antecipação de produção;
- custo oculto de infraestrutura.

## 57. Bloqueios de implementação

A implementação e qualquer integração permanecem com os seguintes itens `BLOCKED`:

1. identificação do pacote canônico do BH-SMC;
2. confirmação da semântica oficial do BônusHora;
3. contrato de interoperabilidade aprovado pelos dois projetos;
4. escolha tecnológica concreta;
5. qualquer uso de dados reais;
6. qualquer emissão, homologação federativa ou produção.

## 58. Itens adiados

Permanecem `DEFERRED` até ADR própria ou decisão posterior:

- seleção de Cosmos SDK, Substrate ou alternativa;
- implementação do consenso;
- desenho definitivo de registros sociais;
- representação fungível ou não fungível;
- publicação externa;
- contratação de nuvem;
- integração efetiva com APIs do BH-SMC;
- admissão de instituições reais.

## 59. Próxima decisão

Após a revisão do pacote canônico do BH-SMC, a próxima decisão deverá:

- confirmar ou corrigir o vocabulário;
- reconciliar semântica e limites com ADR-009 e ADR-011;
- selecionar a alternativa técnica do protótipo;
- aprovar o contrato de interoperabilidade;
- definir os testes de aceitação dos dashboards;
- liberar, manter ou ampliar os gates de implementação conforme a evidência.

Nenhum desses atos ocorrerá automaticamente por esta ADR.

## 60. Estado da decisão

Esta ADR-013 foi expressamente aprovada e congelada por decisão humana em 11 de setembro de 2026.

O escopo aprovado limita-se à arquitetura técnica do protótipo, dashboards de usuários e validadores, sandbox de votação, observabilidade e desenho contratual de interoperabilidade.

Não estão autorizados por esta ADR: produção, gênese, emissão, conversão, integração operacional, alteração das ADRs congeladas, coleta de dados reais, homologação definitiva ou publicação irreversível.

O material operacional do BH-SMC poderá orientar a descoberta, mas somente um pacote canônico identificável, versionado e aprovado poderá fundamentar decisões semânticas ou contratos de interoperabilidade.
