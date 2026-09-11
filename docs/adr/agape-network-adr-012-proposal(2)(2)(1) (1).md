# ADR-012 — Ciclo de Vida, Implantação Progressiva, Pilotos, Métricas e Critérios de Maturidade

- **Status:** Aprovada e congelada
- **Data:** 11 de setembro de 2026
- **Projeto:** Agape Network
- **Repositório:** `bonushora/agape-network`
- **Classificação:** Decisão constitucional, arquitetural, institucional e operacional
- **Escopo:** Ciclo de vida, fases, gates, pilotos, homologação, produção, métricas, maturidade e encerramento
- **Precedência:** Subordinada à ADR-001 até ADR-011
- **Dependências:** ADR-001 a ADR-011

## 1. Contexto

As ADRs-001 a 011 definiram o fundamento ético e institucional, o modelo federativo, a separação de poderes, a identidade, a privacidade, a arquitetura híbrida, o consenso permissionado, a gênese, as ações de caridade verificável, o modelo econômico, a segurança operacional e a interoperabilidade da Agape Network.

Essas decisões estabelecem limites constitucionais, mas ainda não definem como o projeto passará da fundamentação para protótipos, pilotos, homologação, produção, evolução e eventual encerramento.

## 2. Problema

Sem um ciclo de vida explícito, a pressão por construir ou publicar poderá antecipar:

- capacidades não validadas;
- uso de dados reais sem proteção suficiente;
- escolha tecnológica incompatível;
- promessa de tolerância ou finalidade não demonstrada;
- expansão de escopo sem decisão;
- confusão entre protótipo, piloto e produção;
- dependência institucional antes da homologação;
- operação sem recuperação testada;
- métricas que incentivem exposição ou especulação.

## 3. Decisão

A Agape Network adotará um ciclo de vida progressivo, reversível quando possível, baseado em evidências e dividido em estados explícitos.

Nenhuma fase será considerada concluída por intenção, demonstração isolada, narrativa comercial ou sucesso parcial. Cada transição exigirá critérios de entrada, evidências proporcionais ao risco, decisão da autoridade competente e critérios objetivos de saída.

Esta ADR encerra a fundamentação constitucional das doze ADRs fundamentais, mas não escolhe uma tecnologia concreta, não autoriza produção irrestrita, não constitui sozinha a rede federativa e não substitui ADRs técnicas, jurídicas ou operacionais posteriores.

Fica congelada a seguinte postura inicial: o sistema poderá operar de forma autônoma no sentido operacional, como serviço contínuo instalado em ambiente autorizado, sem transferir para software, IA ou fornecedor qualquer autoridade constitucional, institucional ou de governança. Decisões críticas continuarão sujeitas à autoridade humana e aos gates desta ADR.

A primeira instalação deverá avaliar uma infraestrutura cloud sem cobrança recorrente dentro dos limites documentados. Se nenhuma opção cloud demonstrar custo zero de provedor, controle de custos, persistência, segurança, recuperação, conectividade e capacidade compatíveis com a fase, a instalação inicial será feita em PC físico dedicado, ligado continuamente, com seus custos de energia, conectividade, manutenção e substituição declarados.

## 4. Princípio fundamental

A rede evoluirá na velocidade da evidência, não na velocidade da expectativa.

Cada capacidade deverá ser introduzida em ambiente e escopo compatíveis com o que foi realmente validado. Uma limitação conhecida deverá ser declarada; uma capacidade não demonstrada não poderá ser apresentada como existente.

## 5. Estados do ciclo de vida

Os estados canônicos serão:

1. fundamentação;
2. descoberta técnica;
3. protótipo isolado;
4. validação interna;
5. piloto controlado;
6. homologação federativa;
7. prontidão para produção;
8. produção limitada ou progressiva;
9. produção estável;
10. suspensão, substituição ou encerramento.

Um artefato deverá declarar seu estado atual. Estados não poderão ser pulados por conveniência administrativa.

## 6. Fundamentação constitucional

O estado de fundamentação compreende as ADRs-001 a 012 aprovadas e congeladas, seus conflitos resolvidos e suas decisões adiadas explicitamente inventariadas.

O encerramento desta fase não significa que todos os requisitos técnicos, jurídicos ou operacionais estejam resolvidos.

## 7. Descoberta técnica e infraestrutura inicial

Após a aprovação desta ADR, poderão ser estudadas alternativas de blockchain, framework, linguagem, identidade, armazenamento, consenso, observabilidade e implantação.

A infraestrutura inicial deverá ser avaliada em ordem cloud-primeiro e PC-fallback. Uma oferta cloud somente será candidata se, cumulativamente:

- for infraestrutura terceirizada/externa sob responsabilidade contratual identificável;
- possuir permanência ou duração indefinida nos termos oficiais vigentes, sem depender de trial, crédito promocional ou renovação discricionária de benefício;
- não exigir cartão de crédito, cartão de débito, método de pagamento ou vínculo obrigatório de faturamento;
- não permitir cobrança recorrente, cobrança de excedentes, conversão automática para plano pago ou débito não autorizado;
- oferecer capacidade, persistência, conectividade, armazenamento, backups, monitoramento e recuperação compatíveis com a fase;
- declarar limites, disponibilidade regional, risco de suspensão, retomada de recursos ociosos e procedimento de saída.

A avaliação cloud deverá conferir, na data da decisão técnica, preço efetivo, prazo do benefício, quotas, região, capacidade, persistência, egress, endereçamento, backups, monitoramento, recuperação, risco de suspensão ou retomada de recursos e possibilidade de impedir cobrança acidental.

Uma oferta divulgada como Always Free ou equivalente será considerada apenas candidata até que suas condições reais sejam verificadas para o uso da Agape Network. A disponibilidade de uma VM gratuita não prova que uma rede blockchain, seus dados, backups, observabilidade e recuperação possam operar sem custo ou com segurança suficiente. Qualquer exigência de cartão, faturamento ou pagamento desqualificará a oferta segundo esta ADR.

Se a avaliação não demonstrar todos os requisitos sem cobrança do provedor e sem vínculo obrigatório de cobrança, o primeiro ambiente será um PC dedicado ligado continuamente. Esse ambiente deverá possuir energia estável, conectividade, armazenamento protegido, backups, controle físico, monitoramento e plano de substituição. A escolha do PC não elimina a necessidade de homologação nem transforma a máquina em autoridade da rede.

O PC dedicado poderá deixar de ser o único ponto de hospedagem somente depois de pelo menos dois nós validadores independentes, externos ao PC, estarem habilitados e comprovadamente capazes de manter o serviço, o estado, a observabilidade, os backups e a recuperação necessários. Esse marco será classificado como redundância operacional de bootstrap ou piloto. Ele não autorizará declarar produção, tolerância BFT a uma falha, gênese federativa ou independência constitucional da rede. Produção e transição federativa continuarão exigindo pelo menos quatro domínios validadores independentes e os demais critérios das ADRs-006 e 007.

A descoberta deverá comparar alternativas contra critérios verificáveis das ADRs anteriores. Estudo não equivale a seleção, e seleção não equivale a autorização de implantação. A seleção concreta será objeto da ADR-013.

## 8. Protótipo isolado

O protótipo deverá testar o menor conjunto de capacidades necessário para reduzir incerteza técnica.

Ele deverá operar com dados sintéticos ou autorizados, validadores de laboratório e isolamento suficiente para não ser confundido com rede federativa, serviço de assistência ou ambiente de produção.

## 9. Validação interna

A validação interna verificará determinismo, integridade, identidade, autorização, classificação de dados, consenso, auditoria, recuperação, observabilidade e experiência humana no escopo do protótipo.

Falhas deverão ser registradas como falhas do escopo testado, sem extrapolação para capacidades não examinadas.

## 10. Piloto controlado e adesão institucional

O piloto controlado poderá envolver instituições ou participantes convidados, em quantidade, jurisdição, duração e capacidade limitadas. A adesão institucional deverá ser conduzida por uma trilha formal, ecumênica e interconfessional, capaz de acolher especialmente instituições católicas e espíritas sem criar privilégio teológico ou autoridade automática.

A expressão **adesão canônica** nesta ADR significa adesão formal pela autoridade competente segundo o direito canônico, estatuto, ato constitutivo, regulamento ou estrutura legítima da própria instituição. Ela não presume que instituições de tradições diferentes possuam a mesma forma jurídica ou eclesial, nem concede reconhecimento religioso à Agape Network.

O caminho de adesão deverá oferecer apresentação institucional, orientação sobre as ADRs, indicação de representante, ingresso inicial como observador, período probatório, participação progressiva e revisão independente. Outras instituições religiosas poderão aderir pela mesma via quando demonstrarem governança legítima, identidade verificável, finalidade compatível e conduta responsável.

A adesão institucional e a ativação como validador serão etapas distintas. A homologação da instituição não produzirá automaticamente voto, acesso privilegiado ou autoridade de validação. A ativação como validador dependerá de homologação técnica, período probatório, independência real, chaves institucionais, responsáveis identificados e aceitação dos deveres de operação, manutenção, segurança, auditoria, recuperação e comunicação de incidentes.

A propagação da rede e dos nós validadores significará divulgação técnica e institucional do propósito, das regras, dos limites e da forma voluntária de participação, além do convite a instituições qualificadas. Não poderá significar conversão, recrutamento coercitivo, recompensa por adesão, comissão por indicação, competição religiosa ou expansão acima dos critérios de segurança e governança.

O Bônus-Hora, quando e somente quando uma unidade social futura tiver sido autorizada por ADR específica, poderá ser utilizado como critério de concessão de acesso comunitário a eventos culturais, religiosos, educacionais ou de entretenimento não essenciais. Esse acesso será concessão de reciprocidade e não constituirá compra de bem ou serviço, pagamento de preço, aquisição de ingresso, troca comercial ou conversão financeira.

O acesso a eventos não poderá substituir assistência essencial, condicionar adesão, homologação, voto, reputação ou permanência na rede, nem exigir conversão, profissão de fé, contribuição, exposição ou alinhamento espiritual. A natureza religiosa de um evento deverá ser informada previamente e sua participação deverá ser livre.

O piloto deverá possuir plano, responsável, critérios de parada, suporte, consentimentos aplicáveis, tratamento de incidentes e procedimento de saída antes do primeiro dado operacional ser aceito.

## 11. Homologação federativa e reconhecimento de adesão

A homologação federativa verificará se instituições independentes conseguem operar os papéis previstos sem autoridade unilateral, dependência oculta ou perda de auditabilidade.

O processo deverá reconhecer como portas de entrada legítimas, entre outras, dioceses, paróquias, congregações, obras sociais e entidades católicas regularmente representadas; centros, casas, federações e entidades espíritas regularmente representadas; e instituições de outras tradições religiosas ou não religiosas que possuam estrutura equivalente de responsabilidade.

O reconhecimento será institucional e operacional: não afirmará superioridade doutrinária, autenticidade espiritual universal, sucessão religiosa ou aprovação por uma autoridade externa que não tenha participado formalmente. Uma instituição não poderá ser admitida apenas por usar linguagem religiosa, nem rejeitada apenas por pertencer a uma tradição minoritária.

A instituição candidata poderá indicar ou propor outra instituição e seus eventos para uma trilha de credenciamento. A indicação não equivalerá a homologação da rede, não produzirá confiança automática e não concederá acesso automático aos usuários. O evento e a instituição indicada somente poderão receber status de oferta da rede após verificação independente ou permanecerão claramente marcados como proposta externa não homologada.

Para qualquer oferta homologada deverão ser observáveis, no mínimo, a identidade e a autoridade responsável, o propósito institucional e do evento, a natureza não essencial da atividade, o público, o período, a capacidade, os critérios de concessão, as salvaguardas, a acessibilidade, os conflitos de interesse, o canal de contestação e o registro de auditoria. A instituição candidata não poderá credenciar sozinha uma instituição parceira em nome de toda a rede.

A instituição homologada como validadora participará da manutenção e da governança técnica somente dentro das competências delegadas, dos contratos, do consenso e dos quóruns aplicáveis. Seu voto confirmará operações permitidas pelo protocolo; não conferirá propriedade da rede, controle unilateral, poder de alterar a Constituição ou autoridade sobre outra instituição. Os deveres de manutenção, disponibilidade, segurança, atualização, backup, recuperação e resposta a incidentes deverão ser aceitos em instrumento verificável.

Ela deverá testar também ingresso, suspensão, contestação, rotação, perda de conectividade, recuperação e transição de autoridade.

## 12. Prontidão para produção

Prontidão para produção será um estado de evidência, não uma autorização automática de lançamento.

Antes de declarar prontidão deverão existir avaliações técnicas, de segurança, privacidade, governança, operação, continuidade, experiência humana, custos, requisitos legais e riscos residuais.

## 13. Produção progressiva

Qualquer produção deverá começar com exposição e capacidade limitadas, observabilidade reforçada e possibilidade de interrupção.

Novos domínios, instituições, dados, jurisdições ou capacidades deverão ser tratados como ampliações sujeitas a nova avaliação, mesmo quando a infraestrutura já estiver em produção.

## 14. Produção estável

Produção estável somente poderá ser declarada depois de período suficiente de operação progressiva, ausência de bloqueios críticos não tratados, recuperação demonstrada e revisão independente compatível com o risco.

Estabilidade não elimina os deveres de auditoria, transparência, revisão e resposta a incidentes.

## 15. Suspensão, substituição e encerramento

Uma capacidade, piloto, integração ou rede poderá ser suspensa, substituída ou encerrada por risco, falha, perda de autoridade, inviabilidade, mudança jurídica ou decisão institucional legítima.

O encerramento deverá preservar histórico legítimo, direitos das pessoas, exportação autorizada, revogação de credenciais, tratamento de pendências e auditoria final.

## 16. Critérios de entrada

Cada fase deverá declarar:

- objetivo;
- escopo;
- ambiente;
- participantes;
- dados permitidos;
- autoridade responsável;
- riscos conhecidos;
- evidência esperada;
- orçamento de custo e fricção;
- critérios de parada.

Sem esses elementos, a transição permanecerá `BLOCKED`.

Para adesão institucional, a entrada deverá acrescentar:

- identidade jurídica ou estatutária verificável;
- autoridade interna competente para aderir;
- instrumento formal de adesão;
- missão e finalidade declaradas;
- responsáveis identificados;
- prestação de contas proporcional;
- política de proteção de crianças e pessoas vulneráveis, quando aplicável;
- compromisso de assistência sem conversão ou exposição obrigatória;
- compromisso de não utilizar os canais da rede para proselitismo coercitivo;
- declaração de conflitos e vínculos relevantes.

## 17. Critérios de saída

Uma fase somente poderá avançar quando seus critérios de saída forem verificados fisicamente e os itens não concluídos estiverem classificados como `DEFERRED`, `NOT_APPLICABLE`, `WARNING` ou `BLOCKED`, com justificativa.

Uma pendência crítica não poderá ser escondida por média, percentual ou resultado agregado.

## 18. Gates de transição

As transições serão protegidas por gates proporcionais ao risco:

- gate constitucional;
- gate técnico;
- gate de segurança e privacidade;
- gate de governança e autoridade;
- gate operacional e de continuidade;
- gate de experiência humana;
- gate jurídico e regulatório, quando aplicável;
- gate de produção.

Um gate poderá ser combinado com outro quando a evidência e a autoridade forem realmente comuns, sem eliminar nenhuma dimensão necessária.

## 19. Autoridade dos gates

Cada gate deverá identificar quem pode decidir, quem deve revisar, quem executa e quem audita.

Nenhum operador técnico, fornecedor, fundador, IA ou órgão isolado poderá aprovar sozinho uma transição que exija competência institucional, jurídica, ética ou humana distinta.

Uma instituição católica, espírita ou de outra tradição deverá decidir sua adesão por sua própria autoridade legítima. A Agape Network verificará a competência declarada e os requisitos de conduta, mas não substituirá bispo, superior religioso, diretoria, conselho, federação ou órgão equivalente.

## 20. Evidência dos gates

O registro de cada gate deverá conter objetivo, escopo, versão, ambiente, participantes, evidências, limitações, decisão, autoridade, data, riscos residuais e próximo estado.

Relato verbal, captura isolada ou afirmação do executor não substituirá evidência observável.

## 21. Classificação de risco

Toda transição deverá classificar o risco como baixo, médio ou alto conforme impacto em pessoas, dados, autoridade, segurança, continuidade, contrato público, produção, custo e reversibilidade.

A governança poderá ser reforçada por risco real, mas não por ritual sem finalidade verificável.

## 22. Controle de escopo

O escopo de uma fase deverá ser congelado no início. Nova capacidade, integração, classe de dado, jurisdição ou consumidor relevante deverá ser registrada como mudança ou nova fase.

O sucesso de uma capacidade não autoriza capacidades vizinhas por inferência.

## 23. Controle de mudanças

Mudanças durante uma fase deverão preservar a rastreabilidade entre requisito, decisão, implementação, teste e resultado.

Mudança arquitetural, de segurança, de dados, de contrato público ou de autoridade exigirá nova análise e gate compatível, ainda que a mudança pareça pequena.

## 24. Reversibilidade

O plano de cada fase deverá indicar como desativar, reverter, substituir ou encerrar a capacidade quando isso for técnica e juridicamente possível.

Quando a reversão não for possível, a decisão deverá ser tratada como de alto risco e exigir autorização específica antes da execução.

## 25. Ativação gradual

Capacidades deverão ser ativadas gradualmente por escopo, instituição, ambiente, função ou volume, com critérios de avanço e recuo.

Ativação gradual não poderá servir para ocultar uma falha conhecida nem para contornar um gate.

## 26. Ambientes

Os ambientes de desenvolvimento, teste, piloto, homologação e produção deverão possuir identidade, dados, credenciais, autoridade e controles próprios.

Nenhum ambiente herdará automaticamente autoridade, segredo, evidência ou classificação de outro.

## 27. Isolamento

Protótipos e pilotos deverão ser isolados de serviços essenciais, dados não autorizados e redes federativas não participantes.

O isolamento deverá ser verificável e deverá gerar evidência suficiente para demonstrar que uma falha local não se tornou uma falha sistêmica.

## 28. Dados por fase

Dados sintéticos serão preferidos na descoberta, no protótipo e na validação interna.

Dados reais somente poderão entrar em piloto ou produção quando finalidade, base legítima, minimização, segurança, retenção, acesso, correção, revogação e saída estiverem definidos.

## 29. Proteção das pessoas

Nenhuma fase poderá expor pessoas assistidas, crianças ou pessoas vulneráveis a publicidade, conversão religiosa, discriminação, coleta desnecessária ou perda de assistência essencial.

A ausência de capacidade técnica não poderá ser compensada transferindo risco para a pessoa mais vulnerável.

## 30. Participantes do piloto

Participantes deverão ser selecionados por critérios explícitos, independência, capacidade operacional, diversidade relevante e ausência de conflito incompatível.

Quando houver adesão religiosa, a composição deverá buscar pluralidade real, incluindo instituições católicas e espíritas quando qualificadas e, progressivamente, outras tradições religiosas sérias. A presença de uma tradição não dará veto, voto superior, propriedade da missão ou direito de excluir outra instituição qualificada.

Para esta ADR, uma instituição religiosa séria é aquela que possui identidade e autoridade verificáveis, finalidade compatível com a proteção humana, prestação de contas proporcional, mecanismos de salvaguarda, disposição para auditoria e ausência de prática coercitiva ou exploratória. O critério não avaliará a verdade teológica da doutrina.

Instituições poderão iniciar como observadoras ou parceiras de assistência antes de solicitar funções de proposição, validação ou auditoria. Essa entrada de menor risco deverá reduzir barreiras legítimas sem reduzir os requisitos de proteção.

O convite deverá explicar objetivo, escopo, limitações, riscos, tratamento de dados, suporte, retirada e contato para contestação.

A comunicação de propagação deverá explicar que a participação de uma instituição católica, espírita ou de outra tradição qualificada não cria superioridade religiosa, exclusividade, propriedade da missão ou direito de excluir outras tradições. A rede deverá acolher cooperação séria sem avaliar a verdade teológica das doutrinas e sem transformar o crescimento do número de nós em prova de virtude.

## 31. Consentimento e direitos

Quando consentimento for a base aplicável, ele deverá ser livre, informado, específico, verificável e revogável sem retaliação.

Direitos legais ou institucionais não poderão ser substituídos por aceite genérico de termos técnicos.

## 32. Experiência humana

Cada fase deverá avaliar entrada, revisão, decisão, feedback, compreensão do estado, recuperação, acessibilidade e possibilidade de contestação.

Uma função tecnicamente correta, mas incompreensível ou insegura para seus usuários, não será considerada GREEN funcional.

A experiência de adesão deverá incluir linguagem acessível, apresentação não sectária, canal de esclarecimento, tempo razoável para deliberação interna e possibilidade de recusa sem penalidade. Nenhuma instituição deverá aceitar doutrina, propaganda, conversão ou alinhamento espiritual para participar da rede.

## 33. Acessibilidade e inclusão

Interfaces e procedimentos deverão considerar acessibilidade, idioma, conectividade limitada, capacidades diversas e alternativas manuais quando necessário.

Limitações de acesso não poderão ser convertidas automaticamente em suspeita, exclusão ou perda de dignidade.

## 34. Segurança

Antes de cada avanço relevante deverão ser avaliados identidade, autorização, privilégio mínimo, chaves, segredos, endpoints, dependências, rede, logs, detecção, resposta e preservação de evidências.

O nível de segurança reivindicado deverá ser limitado ao que os testes demonstraram.

## 35. Privacidade

Cada fase deverá manter inventário de dados, finalidade, classificação, localização, retenção, acesso, compartilhamento, correção, revogação e eliminação aplicável.

Dados proibidos pelas ADRs-004 e 005 não poderão ser introduzidos para acelerar um teste.

## 36. Consenso e finalidade

Qualquer implementação de consenso deverá demonstrar as propriedades reivindicadas no escopo correspondente, incluindo quórum, finalidade, tolerância, reconfiguração, partição, reinício e conflito.

Um protótipo limitado não poderá ser descrito como uma rede BFT de produção sem evidência adicional.

## 37. Governança e autoridade

Cada fase deverá demonstrar quais decisões permanecem humanas, quais funções são automatizadas e quais capacidades estão negadas por padrão.

Automação poderá verificar, registrar e executar política autorizada, mas não poderá criar autoridade, alterar a Constituição ou substituir deliberação exigida.

## 38. Operação e continuidade

Antes do avanço deverão existir procedimentos de implantação, observabilidade, suporte, incidentes, contenção, backup, recuperação, reconciliação e comunicação compatíveis com o ambiente.

Backup não testado, operador único ou procedimento conhecido apenas por uma pessoa não serão tratados como continuidade suficiente.

## 39. Interoperabilidade

Integrações de piloto ou produção deverão possuir contrato, identidade da origem, schema, versão, finalidade, idempotência, correlação, garantia de entrega, timeouts, isolamento, portabilidade e encerramento.

Compatibilidade sintática não provará equivalência semântica ou jurídica.

## 40. Economia e legalidade

Qualquer cobrança, unidade de reciprocidade, reconhecimento, doação, remuneração ou fluxo de recursos deverá permanecer compatível com a ADR-009 e com análise jurídica e contábil aplicável.

Nenhuma fase poderá prometer retorno financeiro, autoridade ou assistência em troca de participação.

Instituições religiosas não poderão comprar adesão, prioridade, validação, reconhecimento, voto, reputação ou acesso a pessoas assistidas. Doações, patrocínios e contribuições operacionais serão separados da decisão de ingresso e não poderão criar dependência ou captura.

Nenhum validador poderá ser obrigado a pagar taxa de adesão, taxa de manutenção, staking, token, doação, dízimo, comissão ou contribuição financeira para ingressar, permanecer ou votar. Custos legítimos de energia, conectividade, hardware, hospedagem, manutenção, substituição e recuperação deverão possuir fonte de custeio transparente, aprovada e auditável antes da ativação; o custeio não poderá comprar voto, prioridade, quórum, reputação ou autoridade.

O Bônus-Hora não poderá ser usado como pagamento, preço, aquisição ou revenda de bens, serviços, ingressos, taxas ou dívidas. Quando uma unidade social autorizada conceder acesso a evento, o registro deverá indicar que se trata de reciprocidade comunitária não essencial, com finalidade, instituição responsável, critérios, período, limites, situação de homologação e evidência de autorização. Nenhuma concessão poderá criar mercado, conversão financeira, expectativa de lucro ou poder de governança.

## 41. Métricas

Métricas deverão ser definidas antes da coleta e relacionadas ao objetivo da fase.

Poderão incluir integridade, disponibilidade, latência, finalidade, recuperação, incidentes, contestação, correção, acessibilidade, compreensão e custo, desde que não reidentifiquem pessoas nem convertam volume em prova de virtude.

## 42. Métricas de qualidade

Cada métrica deverá declarar definição, unidade, fonte, janela, versão, cobertura, limitações, responsável e ação associada.

Métrica sem método de observação verificável será apenas hipótese e não poderá sustentar um gate.

## 43. Critérios de sucesso

O sucesso de uma fase deverá ser definido por critérios objetivos, mínimos e verificáveis antes do início.

Critérios de sucesso deverão incluir também limites de dano, privacidade, segurança, operação, experiência humana e reversibilidade, não apenas desempenho ou adoção.

## 44. Critérios de falha

Serão falhas relevantes: violação de privacidade, autoridade indevida, estado conflitante não detectado, perda de evidência, recuperação não realizada, exposição não autorizada, erro silencioso ou incapacidade de explicar o resultado.

Falha relevante deverá impedir o avanço até ser corrigida, aceita por autoridade competente ou formalmente reclassificada.

## 45. Condições de parada

O projeto deverá parar, degradar ou recuar quando houver risco não contido, evidência contraditória, perda de quórum, comprometimento de chave, incidente relevante, falha de integridade, falta de autoridade ou expansão não autorizada.

Parar não significará apagar evidências nem abandonar pessoas que dependam de assistência essencial.

## 46. Incidentes

Cada piloto e ambiente produtivo deverá possuir classificação de severidade, comando de incidente, contenção, comunicação, preservação, investigação, devido processo e revisão pós-incidente.

Alertas automatizados poderão iniciar análise, mas não provarão culpa por si mesmos.

## 47. Reversão e recuperação

O plano de saída deverá definir desativação segura, tratamento de operações pendentes, restauração, reconciliação, revogação de credenciais, comunicação e relatório.

Uma transição não poderá avançar enquanto a recuperação necessária permanecer apenas teórica.

## 48. Registro e auditoria

Cada fase deverá produzir registro versionado das decisões, mudanças, participantes, evidências, resultados, falhas, exceções, correções e encerramento.

A auditoria local de cada instituição deverá ser preservada mesmo quando houver relatório compartilhado.

## 49. Transparência

A transparência deverá ser proporcional e compatível com privacidade, segurança, devido processo e independência institucional.

Deverão ser comunicados, conforme aplicável, o estado da fase, capacidades, limitações, riscos residuais, incidentes relevantes, critérios de avanço e critérios de saída.

Também deverão ser comunicados os critérios de adesão, as instituições admitidas em cada papel, os períodos probatórios, os conflitos declarados, as suspensões e as razões operacionais das decisões, preservando a privacidade e a segurança. A comunicação institucional poderá reconhecer a contribuição católica, espírita ou de outra tradição sem transformar reconhecimento operacional em propaganda religiosa.

## 50. Revisão independente

Transições de risco médio ou alto deverão possuir revisão independente adequada ao risco, sem que independência seja reduzida a uma assinatura nominal.

A revisão deverá poder registrar discordância, solicitar evidência adicional e recomendar bloqueio.

## 51. Inteligência artificial

A IA poderá auxiliar planejamento, documentação, classificação, geração de testes, análise de evidências, detecção de anomalias e reconciliação assistida.

Não poderá decidir isoladamente avanço de fase, confiança institucional, compartilhamento de dados sensíveis, autoridade, equivalência jurídica, produção ou encerramento.

## 52. Automação do ciclo de vida

Automação poderá verificar pré-condições, impedir combinações proibidas, coletar métricas, produzir relatórios e abrir gates.

Ela não poderá ocultar falha, converter ausência de evidência em sucesso, ampliar escopo, consumir autoridade futura ou impedir revisão humana legítima.

## 53. Fornecedores e dependências

Toda dependência crítica deverá possuir inventário, finalidade, escopo, risco, substituição possível, exportação, continuidade e responsável.

Fornecedor algum poderá deter sozinho a interpretação dos dados, a recuperação da rede, a operação das identidades ou a validação da integridade.

Nenhuma instituição religiosa poderá tornar-se fornecedora exclusiva, patrocinadora dominante ou porta obrigatória de assistência, identidade ou validação por causa de sua tradição, tamanho ou capacidade financeira.

## 54. Custo e sustentabilidade

Cada fase deverá declarar meta de custo, recursos necessários, custos recorrentes, custos de saída e responsáveis pelo custeio.

Restrições financeiras não autorizam reduzir proteção humana, privacidade, segurança, auditoria ou devido processo sem decisão explícita e análise de risco.

A meta de custo da primeira instalação será ausência de cobrança e de vínculo obrigatório de faturamento do provedor cloud, por prazo permanente ou indefinido segundo os termos oficiais vigentes, dentro dos limites documentados. A verificação deverá considerar também custos de armazenamento, tráfego, backup, endereçamento, monitoramento, recuperação, excedentes, inatividade, suspensão e saída. Se a meta não puder ser garantida com controles verificáveis, deverá ser aplicado o fallback para PC dedicado.

“Sem custo para o validador” significará ausência de desembolso obrigatório do operador para adesão, permanência ou voto, e não inexistência de custos do sistema. No PC dedicado deverão ser contabilizados energia, internet, manutenção, substituição, espaço físico e contingência. A operação de um validador somente poderá ser ativada quando esses custos tiverem responsável e custeio transparente; a falta de custeio não poderá ser ocultada como gratuidade.

## 55. Declaração de produção

Somente a autoridade institucional competente poderá declarar produção, após os gates correspondentes e a verificação da pós-condição física.

Código executável, domínio publicado, rede acessível ou demonstração pública não constituem, por si só, declaração de produção.

## 56. Níveis de maturidade

A maturidade será comunicada por capacidade e evidência, não por um único rótulo global.

Uma capacidade poderá estar madura para protótipo e imatura para produção; um componente GREEN não tornará automaticamente GREEN o backend, a interface, a operação, a implantação, a publicação ou a experiência humana.

## 57. Proibições constitucionais

A Agape Network não poderá:

- pular fases para obter aparência de lançamento;
- chamar protótipo de produção;
- usar pessoas vulneráveis como ambiente de teste sem proteção;
- publicar capacidade não validada como fato;
- ocultar falha sob métrica agregada;
- ampliar autoridade por sucesso técnico;
- tratar piloto como consentimento permanente;
- usar emergência para eliminar governança;
- apagar registros de fases, incidentes ou decisões;
- converter adoção, saldo ou volume em superioridade moral;
- permitir que uma IA ou fornecedor aprove sua própria transição;
- iniciar gênese federativa sem os critérios da ADR-007;
- admitir instituição religiosa apenas por prestígio, linguagem espiritual, promessa financeira ou proximidade pessoal;
- excluir instituição qualificada apenas por sua denominação ou por não pertencer à tradição majoritária;
- usar a adesão para conversão, pressão, propaganda ou recrutamento coercitivo;
- condicionar assistência, validação ou participação à profissão de fé;
- permitir que doação, lucro, dízimo, contribuição ou patrocínio compre autoridade;
- apresentar a Agape Network como órgão de uma igreja, federação religiosa ou doutrina específica;
- conferir reconhecimento canônico, eclesiástico ou espiritual que não tenha sido formalmente concedido pela autoridade competente;
- aceitar cloud que exija cartão, método de pagamento, vínculo obrigatório de faturamento, trial, crédito promocional ou conversão automática para plano pago;
- declarar que dois nós validadores, isoladamente, constituem produção, tolerância BFT, gênese federativa ou independência constitucional;
- exigir custo obrigatório do validador ou usar custeio para comprar voto, prioridade, quórum, reputação ou autoridade;
- usar a propagação da rede para conversão, proselitismo agressivo, recrutamento coercitivo, comissão por indicação ou exclusão de outras tradições sérias;
- usar o Bônus-Hora para comprar, pagar, precificar, revender ou converter bens, serviços, ingressos, taxas ou dívidas;
- liberar acesso a evento sem propósito, instituição responsável, critérios, situação de homologação, salvaguardas e registro observável;
- tratar a indicação de uma instituição candidata como credenciamento automático da rede;
- condicionar evento cultural, religioso, educacional ou de entretenimento a conversão, profissão de fé, contribuição, exposição ou exclusividade;
- declarar cloud gratuita sem verificar limites, cobrança de excedentes, capacidade, inatividade, persistência e recuperação;
- tratar autonomia operacional como autorização para decisões humanas críticas.

## 58. Consequências

Esta decisão:

- cria uma passagem verificável entre fundamento e operação;
- reduz pressão por lançamento prematuro;
- separa protótipo, piloto, homologação e produção;
- torna limitações e riscos comunicáveis;
- protege pessoas e dados durante a evolução;
- preserva autoridade humana e independência institucional;
- exige métricas com método e finalidade;
- torna recuperação e saída parte do desenho;
- permite evolução progressiva sem congelar tecnologia inadequada;
- mantém abertas as ADRs técnicas posteriores;
- cria uma porta de entrada segura e gradual para instituições católicas, espíritas e outras instituições qualificadas;
- favorece cooperação ecumênica e interconfessional sem transformar a rede em instrumento de proselitismo;
- separa adesão institucional, contribuição financeira, reconhecimento operacional e autoridade de validação;
- estabelece cloud como primeira alternativa a ser verificada e PC dedicado como fallback condicionado.
- permite retirar o PC da condição de único ponto de hospedagem após dois validadores externos independentes, somente em bootstrap ou piloto com capacidades comprovadas;
- preserva o mínimo de quatro domínios validadores independentes para produção e transição federativa;
- impede que a promessa de gratuidade do validador esconda custos ou compre autoridade;
- define propagação como convite técnico e institucional voluntário, sem conversão ou competição religiosa.
- permite concessão de acesso comunitário a eventos não essenciais sem transformar a unidade social em pagamento;
- exige propósito explícito, critérios observáveis e homologação independente para instituições e eventos indicados por candidatas;
- preserva a liberdade de consciência em eventos religiosos e impede que acesso substitua assistência essencial.

Permanecem custos de coordenação, documentação, revisão, auditoria e operação. Esses custos são reconhecidos como parte da responsabilidade institucional, não como autorização para remover controles essenciais.

## 59. Próxima decisão

Após a aprovação e o congelamento desta ADR, a próxima decisão deverá definir:

> ADR-013 — Seleção tecnológica, arquitetura técnica e critérios de implementação do primeiro protótipo.

Essa ADR deverá comparar alternativas concretas contra os requisitos das ADRs-001 a 012, sem presumir que blockchain própria, Cosmos SDK, Substrate, token, nuvem ou fornecedor específico sejam obrigatórios.

## 60. Estado da decisão

Esta ADR foi expressamente aprovada e congelada por decisão humana em 11 de setembro de 2026.

Fica aprovada a evolução progressiva e a postura operacional inicial de serviço autônomo contínuo, com avaliação cloud sem cobrança recorrente e fallback para PC físico dedicado ligado continuamente quando a opção cloud não satisfizer os requisitos de custo, controle, persistência, segurança, recuperação e capacidade.

Fica também aprovada a adesão institucional voluntária. Uma instituição somente poderá ser homologada à rede depois de adequar-se às regras aplicáveis, apresentar autoridade legítima, concluir a trilha de adesão, cumprir o período probatório e passar pela homologação correspondente. A adesão não exige conversão, profissão de fé, propaganda ou exclusividade religiosa.

Esta emenda, aprovada por manifestação humana expressa em 11 de setembro de 2026, incorpora os seguintes limites operacionais: cloud terceirizada somente sem cartão, sem faturamento obrigatório, sem trial, sem crédito promocional e sem cobrança oculta; fallback para PC dedicado; retirada do PC como único ponto de hospedagem somente após dois validadores externos independentes capazes de assumir o serviço em bootstrap ou piloto; e produção ou transição federativa somente após pelo menos quatro domínios validadores independentes, conforme as ADRs-006 e 007.

Fica ainda estabelecido que a adesão e a manutenção de um validador não exigem taxa, staking, token, doação ou contribuição financeira obrigatória. Custos necessários deverão ter custeio transparente e auditável, sem comprar voto ou autoridade. A propagação da rede deverá ser técnica e institucional, voluntária, ecumênica e interconfessional, sem conversão, proselitismo coercitivo, exclusividade ou discriminação contra outra instituição séria.

Fica também estabelecido que eventual uso do Bônus-Hora para eventos será exclusivamente uma concessão de reciprocidade comunitária não essencial, nunca compra, preço, pagamento, revenda ou conversão financeira. Instituições candidatas poderão indicar ofertas, mas somente a homologação independente e a autorização prevista em ADR específica poderão permitir sua apresentação como oferta da rede. Esta cláusula não autoriza emissão, integração com o BH-SMC ou operação em produção.

Esta ADR não seleciona o provedor cloud, não define a configuração do PC, não escolhe blockchain ou framework, não autoriza gênese, produção irrestrita, contratação, coleta de dados reais ou integração específica. Essas decisões continuarão sujeitas à ADR-013, à Inspeção Declarativa, à classificação de risco, aos gates correspondentes, à validação independente e à autoridade humana.
