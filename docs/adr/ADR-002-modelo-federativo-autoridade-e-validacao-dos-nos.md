# ADR-002 — Modelo Federativo, Autoridade e Validação dos Nós

- **Status:** Aprovada e congelada
- **Data:** 20 de agosto de 2026
- **Projeto:** Agape Network
- **Repositório:** `bonushora/agape-network`
- **Classificação:** Decisão institucional e arquitetural
- **Escopo:** Federação, autoridade, ingresso, validação, suspensão e exclusão de nós
- **Precedência:** Subordinada à ADR-001
- **Dependência:** ADR-001 — Fundamento Constitucional, Ético e Institucional

## 1. Contexto

A ADR-001 estabeleceu que a Agape Network será uma rede federativa de confiança inspirada nos ensinamentos de Nosso Senhor Jesus Cristo e destinada à caridade verificável, à cooperação institucional, à instrução, à transparência e à proteção da dignidade humana.

Também estabeleceu que:

- nenhuma instituição isolada será proprietária da missão espiritual;
- a autoridade de um nó representará responsabilidade verificável;
- os nós validarão fatos e operações, não fé ou mérito espiritual;
- a rede deverá impedir domínio baseado em riqueza, mineração ou influência pessoal;
- decisões técnicas deverão permanecer subordinadas ao fundamento constitucional;
- a tecnologia blockchain ainda não foi selecionada.

Torna-se necessário definir quem poderá operar nós, quais papéis existirão, como a autoridade será concedida, limitada, auditada, suspensa e eventualmente revogada.

## 2. Decisão

A Agape Network adotará um modelo federativo permissionado.

A participação pública nos serviços da rede não implicará autoridade automática sobre seu consenso ou sua governança.

A autoridade de validação será concedida somente a instituições identificáveis, independentes e admitidas mediante processo verificável.

Nenhuma pessoa, instituição, denominação, empresa, mantenedor técnico ou fundador poderá validar unilateralmente operações críticas ou controlar permanentemente a rede.

## 3. Princípio fundamental

> Um nó recebe autoridade para proteger a integridade da rede, nunca para governar consciências, medir fé ou estabelecer superioridade espiritual.

A autoridade de um nó será:

- limitada;
- revogável mediante devido processo;
- auditável;
- vinculada a uma identidade institucional;
- condicionada ao cumprimento constitucional;
- separada de riqueza, prestígio ou influência religiosa;
- tecnicamente verificável;
- sujeita a prestação de contas.

## 4. O que é um nó

Um nó é uma instância técnica operada sob responsabilidade institucional identificável e autorizada a desempenhar um ou mais papéis na Agape Network.

Um nó não se confunde com:

- a instituição que o opera;
- seus dirigentes;
- seus responsáveis técnicos;
- a comunidade religiosa vinculada;
- seus usuários;
- a autoridade espiritual reconhecida internamente pela instituição.

O software executa funções técnicas. A instituição responde pela operação autorizada do nó.

## 5. Instituições elegíveis

Poderão candidatar-se, entre outras:

- igrejas;
- centros espíritas;
- organizações religiosas;
- instituições beneficentes;
- associações comunitárias;
- organizações da sociedade civil;
- fundações;
- entidades educacionais;
- instituições de assistência social;
- comunidades formalmente organizadas;
- entidades independentes de auditoria;
- instituições técnicas comprometidas com o pacto ético.

A denominação religiosa não produzirá superioridade, preferência automática ou direito adquirido de validação.

Instituições não religiosas poderão participar quando aderirem integralmente à Constituição da Agape Network.

## 6. Requisitos institucionais mínimos

Uma instituição candidata deverá apresentar:

1. existência jurídica ou forma organizacional verificável;
2. identidade de seus responsáveis legais;
3. identidade de seus responsáveis técnicos;
4. chave criptográfica institucional própria;
5. declaração de independência em relação aos demais validadores;
6. adesão formal à ADR-001 e ao pacto ético;
7. política de proteção de dados;
8. política de proteção de crianças e pessoas vulneráveis;
9. compromisso contra discriminação;
10. compromisso contra conversão forçada;
11. compromisso contra exploração econômica da fé;
12. declaração de conflitos de interesses;
13. histórico institucional verificável;
14. infraestrutura técnica mínima;
15. capacidade de responder por incidentes;
16. aceitação de auditoria proporcional ao papel exercido.

A inexistência de grande capacidade financeira não será motivo suficiente para exclusão.

A rede poderá apoiar tecnicamente instituições idôneas que não disponham inicialmente de infraestrutura própria.

## 7. Independência institucional

Um conjunto de nós controlados direta ou indiretamente pela mesma autoridade será considerado um único domínio de controle.

Não será permitido multiplicar artificialmente votos ou influência por meio de:

- empresas coligadas;
- filiais sem autonomia;
- organizações de fachada;
- chaves distintas sob o mesmo controlador;
- infraestrutura formalmente separada, mas administrada pela mesma autoridade;
- acordos ocultos de voto;
- financiamento condicionante não declarado;
- identidade institucional falsa ou fragmentada.

A independência será avaliada por controle jurídico, técnico, financeiro, administrativo e operacional.

## 8. Papéis dos nós

A rede deverá separar, no mínimo, os seguintes papéis:

### 8.1 Nó observador

Poderá:

- acompanhar registros autorizados;
- verificar integridade;
- produzir auditorias;
- observar o funcionamento da rede;
- participar do período probatório.

Não poderá votar no consenso.

### 8.2 Nó proponente

Poderá:

- receber operações;
- realizar validações preliminares;
- propor operações elegíveis;
- encaminhá-las aos validadores.

Não poderá confirmar sozinho uma operação.

### 8.3 Nó validador

Poderá:

- verificar operações;
- votar em propostas;
- participar da confirmação por quórum;
- rejeitar operações inválidas;
- contribuir para a continuidade da rede.

Não poderá alterar unilateralmente políticas constitucionais.

### 8.4 Nó auditor

Poderá:

- verificar registros;
- produzir provas e relatórios;
- identificar inconsistências;
- acompanhar decisões institucionais;
- fiscalizar conflitos de interesses.

A auditoria não implicará voto automático no consenso.

### 8.5 Nó de arquivo

Poderá:

- preservar histórico autorizado;
- verificar encadeamento e integridade;
- apoiar recuperação;
- fornecer material para auditorias.

Dados sensíveis permanecerão sujeitos às regras de privacidade da ADR-001.

## 9. Separação de poderes

A arquitetura deverá evitar que uma única instituição concentre simultaneamente:

- proposição;
- validação;
- auditoria;
- julgamento ético;
- administração técnica;
- controle das identidades;
- controle das políticas;
- custódia exclusiva do histórico.

Uma instituição poderá exercer mais de um papel quando isso for inevitável na fase inicial, mas a concentração deverá:

- ser declarada;
- ser temporária;
- possuir controles compensatórios;
- constar do registro de governança;
- não permitir confirmação unilateral;
- ser reduzida conforme a rede amadurecer.

## 10. Processo de ingresso

O ingresso ocorrerá progressivamente:

1. candidatura;
2. verificação documental;
3. declaração de responsáveis;
4. análise de independência;
5. análise ética;
6. validação técnica;
7. registro de conflitos de interesses;
8. admissão como observador;
9. período probatório;
10. avaliação de comportamento;
11. votação de promoção;
12. ativação limitada como validador;
13. revisão posterior.

Nenhum candidato será promovido diretamente a validador apenas por prestígio, riqueza, número de fiéis, influência política ou relação pessoal com o fundador.

## 11. Período probatório

Todo candidato deverá iniciar como observador, salvo nós de gênese expressamente documentados.

Durante o período probatório serão avaliados:

- disponibilidade;
- comportamento do software;
- segurança operacional;
- resposta a incidentes;
- respeito às políticas;
- consistência das assinaturas;
- independência real;
- qualidade da prestação de contas;
- ausência de comportamento discriminatório;
- proteção de dados;
- cooperação com auditorias.

A duração exata será definida por política operacional posterior e não poderá ser reduzida secretamente.

## 12. Promoção a validador

A promoção exigirá:

- validação técnica automatizada;
- parecer institucional documentado;
- ausência de impedimentos constitucionais;
- período probatório satisfatório;
- declaração atualizada de conflitos;
- aprovação por quórum qualificado dos validadores elegíveis;
- registro auditável da decisão.

Como regra constitucional inicial, a promoção exigirá aprovação de pelo menos dois terços dos validadores elegíveis, excluídos os impedidos por conflito de interesses.

A implementação matemática exata do quórum dependerá do mecanismo de consenso escolhido em ADR posterior.

## 13. Nós de gênese

Enquanto não existirem validadores suficientes para aplicar o processo ordinário, a rede poderá utilizar nós de gênese.

Nós de gênese:

- serão expressamente identificados;
- terão mandato provisório;
- não receberão superioridade permanente;
- deverão pertencer a domínios de controle independentes;
- estarão submetidos à ADR-001;
- terão suas decisões registradas;
- deverão promover a descentralização progressiva;
- perderão privilégios excepcionais após a transição definida.

O fundador não possuirá, por sua condição, voto permanente, poder de veto perpétuo ou autoridade espiritual.

A composição e a transição dos nós de gênese exigirão ADR específica antes da rede entrar em operação.

## 14. Validação das operações

Os validadores deverão verificar, conforme o tipo de operação:

- assinatura digital;
- identidade do emissor;
- autorização;
- integridade;
- formato;
- política aplicável;
- consentimento;
- ausência de duplicidade;
- sequência;
- referências;
- limites operacionais;
- conflitos;
- provas exigidas;
- proteção de dados;
- compatibilidade constitucional.

A confirmação exigirá quórum.

Nenhum nó isolado poderá confirmar, apagar ou reescrever uma operação crítica.

## 15. Modelo de quórum

A rede deverá utilizar quórum qualificado resistente a falhas e comportamento malicioso.

Como princípio inicial:

- decisões operacionais de consenso exigirão mais de dois terços do poder validador elegível;
- admissões e exclusões exigirão pelo menos dois terços dos validadores institucionais elegíveis;
- alterações constitucionais possuirão processo ainda mais rigoroso, definido em ADR própria;
- validadores impedidos não serão computados como votos favoráveis;
- ausência de quórum manterá a operação pendente ou rejeitada, conforme política explícita;
- falha de validação será tratada em modo fail-closed.

A seleção do algoritmo BFT permanece adiada.

## 16. Distribuição de autoridade

A autoridade não será distribuída proporcionalmente a:

- dinheiro;
- tokens;
- patrimônio;
- capacidade computacional;
- energia consumida;
- quantidade de seguidores;
- número de templos;
- volume de doações;
- prestígio religioso;
- influência política;
- proximidade com o fundador.

A regra inicial será uma autoridade institucional limitada por domínio de controle.

Modelos de ponderação somente poderão ser introduzidos por ADR posterior e não poderão permitir compra de domínio.

## 17. Conduta incompatível

Poderão fundamentar restrição, suspensão ou exclusão:

- falsificação;
- adulteração;
- exposição indevida de dados;
- discriminação;
- coerção religiosa;
- conversão forçada vinculada à assistência;
- exploração econômica da fé;
- tentativa de capturar a governança;
- operação de identidades institucionais falsas;
- ocultação de controle comum;
- conluio;
- censura arbitrária;
- violação criptográfica;
- quebra intencional de disponibilidade;
- recusa injustificada de auditoria;
- conflito de interesses oculto;
- descumprimento persistente das políticas;
- comprometimento de chaves;
- uso do nó para atividade ilícita;
- tentativa de registrar mérito espiritual.

## 18. Suspensão emergencial

Um nó poderá ser suspenso temporariamente quando houver risco imediato e material à rede, às pessoas ou aos dados.

A suspensão emergencial deverá:

- ter fundamento registrado;
- possuir escopo mínimo;
- ser temporária;
- preservar evidências;
- impedir dano adicional;
- acionar revisão colegiada;
- permitir contestação posterior;
- não apagar o histórico;
- não presumir culpa definitiva.

Comprometimento confirmado ou provável de chaves poderá provocar suspensão técnica automática, conforme política futura.

## 19. Devido processo

Nenhum nó será definitivamente excluído sem:

- notificação;
- descrição dos fatos;
- evidências verificáveis;
- identificação das políticas aplicáveis;
- oportunidade razoável de defesa;
- avaliação por participantes não impedidos;
- decisão colegiada;
- quórum qualificado;
- fundamentação;
- registro auditável;
- possibilidade de revisão nos casos previstos.

Medidas emergenciais não eliminarão o devido processo para decisão definitiva.

## 20. Conflitos de interesses

Participantes deverão declarar impedimento quando:

- forem parte diretamente interessada;
- controlarem ou financiarem a instituição analisada;
- possuírem relação capaz de comprometer independência;
- participarem dos fatos investigados;
- tiverem vantagem material ou institucional relevante no resultado.

Votos de participantes impedidos não contarão para formar aprovação.

Tentativa deliberada de ocultar impedimento constituirá violação grave.

## 21. Direito de saída

Uma instituição poderá deixar a rede voluntariamente.

A saída:

- não apagará registros legitimamente confirmados;
- não eliminará responsabilidades anteriores;
- exigirá transição segura das funções;
- deverá proteger chaves e dados;
- deverá ser registrada;
- não poderá bloquear a continuidade da rede;
- não transferirá automaticamente autoridade a terceiro.

## 22. Responsabilidade institucional

Cada instituição operadora responderá:

- pela custódia de suas chaves;
- por seus responsáveis autorizados;
- por sua infraestrutura;
- por suas declarações;
- por sua conformidade;
- por sua resposta a incidentes;
- por seus conflitos de interesses;
- pelo uso legítimo de sua autoridade.

A rede não reconhecerá anonimato institucional para nós validadores.

Pessoas assistidas e usuários comuns poderão receber proteção de identidade conforme finalidade, risco e legislação.

## 23. Transparência e privacidade

Serão publicamente auditáveis, conforme o modelo de acesso futuro:

- identidade institucional dos validadores;
- chaves públicas autorizadas;
- papéis;
- situação operacional;
- decisões de ingresso;
- suspensões;
- exclusões;
- políticas vigentes;
- conflitos declarados;
- registros de governança.

Não serão publicizados indiscriminadamente:

- dados sensíveis;
- documentos pessoais;
- credenciais;
- chaves privadas;
- informações de crianças;
- histórias de vulnerabilidade;
- dados protegidos por lei;
- informações cuja exposição produza risco.

## 24. Restrições constitucionais

Nenhum nó poderá:

- declarar quem possui fé legítima;
- medir santidade;
- conceder mérito espiritual;
- condicionar caridade à adesão religiosa;
- comprar votos;
- vender autoridade;
- impor doutrina à federação;
- usar a rede para perseguir dissidentes;
- apagar evidências de sua própria conduta;
- utilizar o nome de Cristo para garantir retorno financeiro.

Essas restrições prevalecem sobre regras operacionais incompatíveis.

## 25. Consequências

Esta decisão:

- reduz a possibilidade de captura unilateral;
- exige identidade institucional dos validadores;
- aumenta responsabilidade e auditabilidade;
- impede consenso baseado em riqueza;
- admite pluralidade religiosa e institucional;
- exige processo formal de ingresso;
- cria separação entre observação, proposição, validação e auditoria;
- exige devido processo;
- torna a implementação mais complexa;
- exige mecanismos de governança além do software;
- mantém aberta a escolha da tecnologia blockchain.

## 26. Riscos reconhecidos

Permanecem riscos de:

- conluio entre validadores;
- captura institucional;
- lentidão de governança;
- falsa independência;
- excesso de burocracia;
- indisponibilidade;
- comprometimento de chaves;
- divergência entre política e execução;
- discriminação velada;
- concentração durante a gênese;
- abuso de suspensão emergencial.

Esses riscos deverão ser tratados por políticas, auditorias, arquitetura técnica, diversidade institucional e futuras ADRs.

## 27. Decisões adiadas

Esta ADR não seleciona:

- blockchain;
- framework;
- algoritmo BFT;
- tecnologia de identidade;
- número definitivo de validadores;
- duração do período probatório;
- requisitos de hardware;
- localização de nós;
- modelo de custódia;
- modelo jurídico;
- conselho ético definitivo;
- comitê técnico definitivo;
- política completa de incidentes;
- procedimento constitucional de emendas;
- composição dos nós de gênese.

## 28. Próximas decisões necessárias

Antes da implementação serão necessárias ADRs sobre:

1. governança constitucional e separação institucional de poderes;
2. identidade, autorização e privacidade;
3. classificação de dados on-chain e off-chain;
4. modelo de consenso e tolerância a falhas;
5. gênese e transição para federação;
6. cadeia de custódia e auditoria;
7. unidade de reciprocidade, se houver;
8. segurança de chaves e recuperação;
9. modelo jurídico e regulatório;
10. interoperabilidade.

## 29. Compatibilidade com a ADR-001

Esta ADR implementa institucionalmente o princípio:

> A rede valida a integridade das ações humanas de serviço e caridade; não julga a fé, a consciência, a santidade ou o mérito espiritual de nenhuma pessoa.

Em caso de conflito interpretativo, prevalecerá a ADR-001.

## 30. Estado da decisão

Esta ADR foi expressamente aprovada e congelada por decisão humana em 20 de agosto de 2026.

A implementação da Agape Network deverá permanecer subordinada a esta decisão durante todo o seu ciclo de vida.

Nenhuma implementação técnica está autorizada exclusivamente por esta ADR. Cada fase continuará sujeita à Inspeção Declarativa, decisão arquitetural correspondente e autorização humana.
