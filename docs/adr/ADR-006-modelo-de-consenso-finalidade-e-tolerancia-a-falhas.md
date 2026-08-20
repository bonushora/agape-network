# ADR-006 — Modelo de Consenso, Finalidade e Tolerância a Falhas

- **Status:** Aprovada e congelada
- **Data:** 20 de agosto de 2026
- **Projeto:** Agape Network
- **Repositório:** `bonushora/agape-network`
- **Classificação:** Decisão arquitetural, distribuída e de segurança
- **Escopo:** Consenso, finalidade, quórum, falhas, validadores e segurança distribuída
- **Precedência:** Subordinada à ADR-001 até ADR-005
- **Dependências:** ADR-001 a ADR-005

## 1. Contexto

A Agape Network foi definida como rede federativa permissionada, composta por instituições independentes e submetida a governança multiparte.

A ADR-002 determinou que nenhuma instituição isolada poderá confirmar operações críticas e que decisões de consenso exigirão quórum qualificado.

A rede deverá continuar íntegra mesmo quando alguns nós:

- falharem;
- ficarem indisponíveis;
- enviarem mensagens divergentes;
- atrasarem mensagens;
- tentarem confirmar estados conflitantes;
- forem comprometidos;
- agirem maliciosamente.

Esta ADR define os requisitos do consenso sem selecionar blockchain, framework ou implementação.

## 2. Decisão

A Agape Network adotará consenso permissionado com finalidade determinística e tolerância a falhas bizantinas.

O modelo deverá:

- utilizar conjunto conhecido de validadores;
- exigir quórum superior a dois terços;
- garantir interseção segura entre quóruns;
- impedir confirmação unilateral;
- produzir finalidade explícita;
- priorizar segurança sobre disponibilidade quando ambas não puderem ser preservadas;
- interromper confirmações diante de ambiguidade crítica;
- registrar evidências de comportamento conflitante;
- separar consenso técnico de governança institucional.

## 3. Princípio fundamental

> É preferível interromper temporariamente a confirmação de operações a confirmar dois estados incompatíveis como verdadeiros.

A Agape Network priorizará segurança e integridade em situações de partição, ambiguidade ou perda de quórum.

## 4. Propriedades obrigatórias

O consenso deverá buscar:

### Segurança

Dois estados conflitantes não poderão ser finalizados legitimamente para a mesma posição do histórico.

### Vivacidade

Operações válidas deverão progredir quando houver rede suficientemente estável e quórum honesto disponível.

### Finalidade

Uma operação finalizada não dependerá de confirmações probabilísticas crescentes.

### Consistência

Nós honestos deverão convergir para o mesmo histórico finalizado.

### Integridade

Somente operações válidas, autorizadas e compatíveis com as políticas poderão ser finalizadas.

## 5. Modelo de falhas

O modelo deverá considerar:

- falha por parada;
- reinicialização;
- perda de conectividade;
- atraso;
- duplicação de mensagens;
- mensagens fora de ordem;
- mensagens conflitantes;
- equivocation;
- nó comprometido;
- chave comprometida;
- comportamento arbitrário;
- conluio dentro do limite tolerado;
- partição de rede.

Falhas físicas, humanas, institucionais e maliciosas serão consideradas.

## 6. Limite bizantino

Para tolerar até `f` validadores bizantinos, o conjunto deverá satisfazer:

> `n ≥ 3f + 1`

em que:

- `n` é o número de validadores independentes elegíveis;
- `f` é o número máximo de validadores bizantinos tolerados.

A finalidade exigirá quórum de votos válidos estritamente superior a dois terços do poder total elegível.

Nas configurações canônicas em que `n = 3f + 1`, esse quórum corresponde a:

> `2f + 1` votos válidos

Quando `n` for superior ao mínimo `3f + 1`, o quórum não poderá ser reduzido a `2f + 1` se esse valor deixar de representar poder de voto estritamente superior a dois terços do total elegível.

## 7. Exemplos de configuração

| Validadores independentes | Falhas bizantinas toleradas | Quórum mínimo |
|---:|---:|---:|
| 1 | 0 | 1 |
| 4 | 1 | 3 |
| 7 | 2 | 5 |
| 10 | 3 | 7 |
| 13 | 4 | 9 |

Uma rede com menos de quatro validadores independentes não poderá afirmar tolerância a uma falha bizantina.

Ambiente de desenvolvimento com um validador não será apresentado como rede BFT de produção.

## 8. Independência dos validadores

A contagem considerará domínios reais de controle, conforme a ADR-002.

Vários nós sob o mesmo controle:

- jurídico;
- administrativo;
- técnico;
- financeiro;
- operacional;
- criptográfico;

não serão considerados independentes apenas por utilizarem máquinas ou chaves diferentes.

A tolerância anunciada deverá refletir independência real.

## 9. Poder de voto

O poder de voto não será adquirido por:

- riqueza;
- token;
- mineração;
- patrimônio;
- quantidade de seguidores;
- volume de doações;
- capacidade computacional;
- prestígio religioso;
- proximidade com o fundador.

A regra inicial será autoridade institucional por domínio independente.

Qualquer ponderação futura exigirá ADR específica e não poderá permitir compra de controle.

## 10. Quórum

Somente votos de validadores:

- ativos;
- elegíveis;
- autenticados;
- não revogados;
- não expirados;
- pertencentes à configuração vigente;
- válidos para a rodada;
- compatíveis com a proposta;

poderão formar quórum.

Votos duplicados não aumentarão o quórum.

Votos de identidades desconhecidas ou suspensas serão rejeitados.

## 11. Interseção de quóruns

A configuração deverá assegurar que dois quóruns válidos possuam interseção suficiente de validadores honestos para impedir finalidade conflitante dentro do limite de falhas.

Mudanças de configuração não poderão criar conjuntos sem sobreposição segura.

A prova de segurança do protocolo escolhido deverá demonstrar essa propriedade.

## 12. Finalidade determinística

Uma operação será considerada final somente após satisfazer todas as fases exigidas pelo protocolo e obter certificado verificável de quórum.

Antes da finalidade, uma operação poderá estar:

- recebida;
- validada preliminarmente;
- proposta;
- votada;
- preparada;
- comprometida em processamento.

Esses estados não serão apresentados como confirmação definitiva.

## 13. Certificado de finalidade

A finalidade deverá produzir evidência verificável contendo, conforme o protocolo:

- identificador da operação ou bloco;
- altura ou posição;
- rodada ou época;
- hash do estado;
- configuração de validadores;
- votos ou prova agregada;
- quórum alcançado;
- política ou versão aplicável;
- assinaturas;
- referência temporal autorizada quando necessária.

A evidência não deverá conter dados pessoais proibidos.

## 14. Estado finalizado

Depois da finalidade:

- o estado será canônico;
- nós honestos não aceitarão estado conflitante na mesma posição;
- reprocessamento não produzirá efeito duplicado;
- reinicialização deverá reconstruir o mesmo resultado;
- recuperação deverá preservar a finalidade comprovada;
- expiração posterior de credencial não invalidará retroativamente realidade legitimamente finalizada.

Fraude comprovada poderá gerar medida compensatória posterior, nunca reescrita secreta do histórico.

## 15. Conflito de finalidade

Se forem detectados certificados válidos para estados incompatíveis na mesma posição:

- a rede deverá considerar o evento violação crítica de segurança;
- novas finalizações afetadas deverão ser interrompidas;
- evidências deverão ser preservadas;
- validadores envolvidos deverão ser identificados;
- governança e resposta a incidentes deverão ser acionadas;
- nenhuma versão será escolhida silenciosamente por conveniência.

A recuperação exigirá processo extraordinário auditável.

## 16. Segurança acima da vivacidade

Durante partição de rede, a Agape Network não tentará manter disponibilidade sacrificando consistência.

Partes minoritárias poderão:

- receber solicitações;
- preservar dados locais autorizados;
- operar consultas seguras;
- manter fila pendente;

mas não poderão declarar finalidade sem quórum válido.

## 17. Perda de quórum

Na ausência de quórum:

- novas operações permanecerão pendentes ou serão rejeitadas conforme política;
- nenhum nó assumirá autoridade emergencial automática;
- o estado finalizado anterior será preservado;
- filas não serão apresentadas como finalizadas;
- a governança será notificada;
- a restauração seguirá processo autorizado.

Ausência de quórum não autoriza redução silenciosa do limiar.

## 18. Rede parcialmente síncrona

O protocolo deverá preservar segurança mesmo com atrasos não limitados.

A vivacidade poderá depender de um período em que a comunicação entre nós honestos volte a respeitar limites operacionais suficientes.

Timeouts:

- não provarão que um nó é malicioso;
- não autorizarão finalidade sem quórum;
- poderão provocar mudança de rodada;
- serão configuráveis por política técnica;
- deverão usar fonte temporal apropriada.

## 19. Autoridade temporal

Horário fornecido pelo cliente não será autoridade para consenso, validade ou expiração.

Quando tempo for relevante, a arquitetura deverá utilizar fonte autorizada e regras determinísticas.

Relógio de parede isolado não decidirá ordenação canônica quando a ordem depender do consenso.

Anomalias temporais deverão provocar tratamento fail-closed quando afetarem segurança.

## 20. Determinismo da máquina de estados

Todos os validadores honestos deverão obter o mesmo resultado ao executar a mesma operação finalizada sobre o mesmo estado anterior.

A execução não poderá depender diretamente de:

- horário local não autorizado;
- aleatoriedade não consensual;
- ordem de mapa não determinística;
- idioma ou localidade;
- sistema operacional;
- resposta externa mutável;
- rede externa não incorporada ao consenso;
- estado oculto;
- comportamento indefinido.

Entradas externas deverão ser transformadas em dados verificáveis antes da execução consensual.

## 21. Validação antes do voto

Antes de votar, cada validador deverá verificar, conforme aplicável:

- assinatura;
- identidade;
- autorização;
- validade da credencial;
- esquema;
- classificação dos dados;
- política;
- sequência;
- duplicidade;
- limites;
- referências;
- compatibilidade constitucional;
- resultado determinístico.

Falha de validação resultará em rejeição, não em correção silenciosa.

## 22. Proposição

O proponente de uma rodada não possuirá autoridade superior permanente.

Ele poderá ordenar propostas dentro das regras, mas não poderá:

- alterar operações;
- forjar autorizações;
- excluir indefinidamente operações por discriminação;
- confirmar sozinho;
- reduzir quórum;
- alterar a configuração vigente.

Censura persistente deverá ser detectável e tratável.

## 23. Mudança de rodada

O protocolo deverá permitir substituição de proponente ou avanço de rodada quando não houver progresso.

A mudança deverá:

- preservar bloqueios ou provas de segurança;
- impedir votos conflitantes;
- transportar o estado necessário;
- manter rastreabilidade;
- não reiniciar a história;
- não reduzir o quórum.

## 24. Ordenação

A ordem canônica será definida pelo consenso.

A ordem de chegada a um único nó não será autoridade global.

Quando duas operações conflitarem, o protocolo deverá aplicar regra determinística e auditável.

A ordenação não poderá ser manipulada para discriminar pessoas ou instituições.

## 25. Idempotência

Cada operação crítica possuirá identidade única e chave de idempotência adequada.

Repetições idênticas deverão convergir para o mesmo resultado comprovado.

Reutilização conflitante da mesma identidade deverá ser rejeitada.

Reenvio após falha de comunicação não poderá duplicar efeitos.

## 26. Duplicidade e replay

O consenso deverá prevenir:

- inclusão duplicada;
- gasto ou benefício duplicado;
- reaplicação de operação finalizada;
- replay entre redes;
- replay entre épocas incompatíveis;
- reutilização de assinatura fora de contexto.

Assinaturas deverão estar vinculadas ao domínio, rede, versão e finalidade necessários.

## 27. Configuração de validadores

A configuração vigente deverá possuir:

- identificador;
- membros;
- chaves;
- poder de voto;
- início de validade;
- regra de quórum;
- versão;
- decisão de governança correspondente.

Nós não poderão inventar localmente uma configuração alternativa.

## 28. Entrada e saída de validadores

Mudanças de validadores serão operações governadas e finalizadas.

A transição deverá:

- ser aprovada conforme ADR-002 e ADR-003;
- ser registrada na configuração anterior;
- indicar ativação;
- preservar interseção segura;
- impedir ativação prematura;
- impedir voto simultâneo indevido;
- permitir auditoria.

O mecanismo exato de reconfiguração será escolhido com o protocolo.

## 29. Suspensão emergencial

Comprometimento grave poderá justificar suspensão emergencial conforme as ADRs anteriores.

A suspensão não poderá reduzir o conjunto a uma configuração que declare tolerância inexistente.

Se a remoção impedir quórum seguro, a rede deverá interromper finalidade até reconfiguração válida.

## 30. Chaves comprometidas

Suspeita de chave comprometida exigirá:

- interrupção do uso;
- preservação de evidências;
- notificação;
- avaliação;
- rotação ou revogação;
- reconfiguração quando necessária;
- investigação de votos anteriores.

Uma chave nova não apagará evidências produzidas pela chave anterior.

A custódia detalhada será tratada na ADR-008.

## 31. Persistência

Um nó deverá persistir informações suficientes para não violar segurança após reinício.

O protocolo deverá especificar:

- votos persistentes;
- bloqueios;
- certificados;
- configuração;
- altura;
- rodada;
- estado finalizado;
- dados necessários à recuperação.

Reiniciar não poderá permitir que o nó vote contraditoriamente.

## 32. Recuperação

Ao retornar, um nó deverá:

- autenticar pares;
- descobrir configuração vigente;
- obter certificados;
- verificar histórico;
- reconstruir estado;
- detectar divergência;
- sincronizar somente a partir de fontes verificáveis;
- recusar snapshot sem prova suficiente.

Velocidade de recuperação não prevalecerá sobre integridade.

## 33. Sincronização de estado

Snapshots poderão acelerar sincronização quando vinculados a:

- estado finalizado;
- hash;
- altura;
- configuração;
- certificado de quórum;
- origem verificável;
- formato versionado.

Snapshot não será autoridade isolada.

## 34. Disponibilidade de dados

Finalidade não deverá depender de dados necessários que nenhum participante autorizado consiga recuperar.

Antes da finalidade, o protocolo deverá assegurar disponibilidade suficiente do conteúdo ou das provas exigidas para validar o estado.

Dados protegidos continuarão sujeitos às ADRs de privacidade e classificação.

## 35. Comportamento bizantino comprovável

Deverão ser preservadas evidências de:

- votos conflitantes;
- propostas conflitantes;
- assinaturas inválidas;
- configuração indevida;
- tentativa de replay;
- certificado forjado;
- censura tecnicamente demonstrável;
- mensagens incompatíveis.

Sanções institucionais dependerão de devido processo.

Não haverá “slashing” financeiro presumido, pois a rede não adota token especulativo.

## 36. Observabilidade

A rede deverá observar:

- altura finalizada;
- rodada;
- latência;
- quórum;
- validadores ativos;
- mudanças de configuração;
- falhas;
- divergências;
- operações pendentes;
- certificados;
- tempo sem progresso.

Métricas não deverão expor dados pessoais.

## 37. Atualizações do protocolo

Mudanças que afetem consenso serão decisões técnicas críticas.

Exigirão:

- especificação;
- análise de segurança;
- compatibilidade;
- testes;
- versão;
- quórum institucional;
- plano de ativação;
- critério de abortar;
- recuperação;
- auditoria.

Atualizações incompatíveis não poderão ser ativadas unilateralmente.

## 38. Partições e reconciliação

Após partição, nós honestos deverão reconciliar-se pelo histórico com finalidade válida.

Operações apenas pendentes na partição minoritária poderão ser repropostas, mas não tratadas como já finalizadas.

Estados conflitantes sem certificado válido serão descartados ou mantidos apenas como evidência.

## 39. Ataques de maioria

Nenhum protocolo BFT protege a segurança quando o limite assumido de comportamento bizantino é excedido.

A arquitetura deverá reduzir esse risco por:

- diversidade institucional;
- independência real;
- separação geográfica;
- custódia segura;
- auditoria;
- governança;
- detecção de conluio;
- transparência dos validadores;
- limitação de poder.

A limitação deverá ser comunicada honestamente.

## 40. Ataques de negação de serviço

A rede deverá proteger consenso contra:

- inundação;
- propostas inválidas;
- conexões abusivas;
- consumo de memória;
- operações excessivas;
- mensagens repetidas;
- pares não autorizados.

Controles de capacidade não poderão ser usados para discriminação religiosa ou institucional.

## 41. Ambientes

A arquitetura distinguirá:

- desenvolvimento;
- teste;
- homologação;
- piloto;
- produção.

Finalidade em ambiente de teste não produzirá autoridade na produção.

Chaves, identificadores e domínios deverão impedir replay entre ambientes.

## 42. Critérios de produção

Antes da produção deverão existir:

- pelo menos quatro domínios validadores independentes para tolerar uma falha bizantina;
- protocolo formalmente especificado;
- testes de segurança;
- testes de partição;
- testes de reinício;
- testes de reconfiguração;
- recuperação validada;
- observabilidade;
- resposta a incidentes;
- governança operacional;
- auditoria;
- cerimônia de gênese.

O piloto poderá possuir limitações explícitas, sem alegações falsas de tolerância.

## 43. Proibições constitucionais

Fica proibido:

- consenso baseado em riqueza;
- mineração competitiva como fonte de autoridade;
- venda de poder validador;
- finalidade unilateral;
- redução secreta de quórum;
- uso de horário do cliente como autoridade;
- confirmação probabilística apresentada como determinística;
- reescrita secreta do histórico;
- autoridade técnica transformada em autoridade espiritual;
- disponibilidade obtida pela aceitação de estados conflitantes;
- configuração falsa de independência;
- alegação de tolerância superior à matematicamente suportada.

## 44. Consequências

Esta decisão:

- seleciona a família BFT permissionada;
- exige finalidade determinística;
- estabelece `n ≥ 3f + 1`;
- exige quórum superior a dois terços;
- prioriza segurança sobre vivacidade;
- exige execução determinística;
- impede consenso baseado em riqueza;
- exige no mínimo quatro domínios independentes para tolerar uma falha bizantina;
- aumenta complexidade operacional;
- restringe as tecnologias elegíveis;
- mantém aberta a escolha do framework.

## 45. Riscos reconhecidos

Permanecem riscos de:

- conluio acima do limite;
- falsa independência;
- censura;
- indisponibilidade;
- erros de implementação;
- configuração incorreta;
- comprometimento de chaves;
- falhas de persistência;
- reconfiguração insegura;
- dependência de rede;
- atualização incompatível;
- complexidade de recuperação.

Esses riscos exigirão testes, auditoria e governança contínua.

## 46. Decisões adiadas

Esta ADR não define:

- algoritmo BFT específico;
- blockchain;
- framework;
- linguagem;
- biblioteca criptográfica;
- formato de bloco;
- duração de bloco;
- timeout;
- tamanho inicial definitivo;
- agregação de assinaturas;
- rede peer-to-peer;
- armazenamento;
- mecanismo exato de reconfiguração;
- composição dos nós de gênese.

## 47. Critérios para seleção tecnológica

A futura tecnologia deverá demonstrar:

- consenso BFT permissionado;
- finalidade determinística;
- reconfiguração segura;
- execução determinística;
- identidade dos validadores;
- certificados verificáveis;
- recuperação;
- observabilidade;
- interoperabilidade;
- ausência de dependência obrigatória de token;
- maturidade de segurança;
- possibilidade de auditoria.

A seleção será documentada após a conclusão das 12 ADRs fundamentais.

## 48. Próxima decisão

A próxima decisão será:

> ADR-007 — Gênese da Rede e Transição da Autoridade Provisória para a Federação.

Essa ADR definirá a formação inicial sem transformar o fundador ou os nós de gênese em autoridades permanentes.

## 49. Compatibilidade

Esta ADR será interpretada conforme a ADR-001 a ADR-005.

Em caso de tensão entre disponibilidade e integridade, prevalecerá a preservação do estado seguro.

Em caso de tensão entre transparência técnica e privacidade humana, prevalecerão classificação e acesso proporcional.

## 50. Estado da decisão

Esta ADR foi expressamente aprovada e congelada por decisão humana em 20 de agosto de 2026.

O modelo de consenso, finalidade determinística, quórum e tolerância a falhas da Agape Network deverá permanecer subordinado a esta decisão durante todo o ciclo de vida do projeto.

Nenhuma implementação técnica está autorizada exclusivamente por esta ADR. A seleção do algoritmo, da blockchain ou do framework continuará sujeita à Inspeção Declarativa, ADR específica e autorização humana.
