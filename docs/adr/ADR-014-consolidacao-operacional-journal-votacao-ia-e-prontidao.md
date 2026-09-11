# ADR-014 — Consolidação Operacional, Journal, Votação, IA e Critérios de Prontidão

- **Status:** Aprovada e congelada
- **Data:** 11 de setembro de 2026
- **Projeto:** Agape Network
- **Classificação:** Decisão de consolidação operacional, governança, evidência, experiência humana e prontidão
- **Escopo:** Journal operacional, mecânica mínima de votação, autonomia soberana operacional, governança da IA, custos, adesão, eventos, equivalência bilíngue PT-BR/EN e transição progressiva
- **Precedência:** Subordinada às ADRs-001 até ADR-013 e compatível com BH-SEP/BH-SDP v2.3
- **Dependências:** ADRs-001 a 013, manifesto canônico, política operacional proposta e validação humana competente

## 1. Contexto

As ADRs-001 a 013 estabeleceram o fundamento ético e institucional, a federação, a separação de poderes, a identidade, a privacidade, os dados, o consenso, a gênese, as ações verificáveis, a reciprocidade, a segurança, a interoperabilidade, o ciclo de vida e o envelope técnico de dashboards.

A revisão geral identificou que o conjunto é coerente no propósito, mas ainda possui lacunas operacionais que impedem transformar suas regras em um processo repetível e auditável. As principais lacunas são:

- ausência de um journal operacional com schema explícito;
- mecânica incompleta para elegibilidade, denominadores, arredondamento e auditoria de votos;
- governança insuficiente para troca de modelo ou provedor de inteligência artificial;
- diferença entre ausência de cobrança obrigatória e inexistência de custos de operação;
- critérios ainda não operacionalizados para instituições, eventos e recursos de acesso comunitário;
- fotografia documental que precisa ser revalidada depois de cada publicação;
- ausência de um caminho único entre protótipo, piloto, homologação e produção.

## 2. Problema

Sem uma consolidação operacional, a rede poderá possuir princípios corretos e ainda assim produzir decisões difíceis de reconstruir, interfaces ambíguas, custos ocultos, conflitos de representação, troca não rastreada de IA ou alegações de prontidão sem evidência.

Também existe risco de que o termo “canônico” seja interpretado como chancela eclesiástica, que “autônomo” seja interpretado como governo sem autoridade humana, ou que uma unidade de reciprocidade seja confundida com moeda, pagamento ou investimento.

## 3. Decisão

A Agape Network adota esta ADR como consolidação dos controles operacionais necessários para transformar as ADRs-001 a 013 em um caminho verificável de descoberta, protótipo, piloto e eventual produção.

Esta decisão:

- não reescreve ADR congelada;
- não cria autoridade espiritual, jurídica ou técnica adicional;
- não autoriza runtime, emissão, dados reais, integração operacional ou produção;
- não escolhe Cosmos SDK, Substrate, blockchain, nuvem ou fornecedor;
- não considera o material operacional do BH-SMC como norma;
- mantém como `BLOCKED` qualquer interoperabilidade com o BH-SMC sem pacote canônico, glossário e contrato aprovados;
- define autonomia soberana como capacidade operacional da rede federada, sem criar autoridade autônoma para a blockchain, os validadores, a IA ou qualquer operador;
- exige voto elegível para decisões de governança e matérias sensíveis, com consolidação automática apenas de resultados válidos segundo regras previamente aprovadas;
- exige que cada implementação futura registre sua autoridade, evidência, risco e pós-condição.

## 4. Princípio de consolidação

As ADRs congeladas estabelecem limites. Esta ADR estabelece como esses limites deverão ser observados, registrados e demonstrados durante a evolução.

Quando houver conflito entre conveniência operacional e uma proteção constitucional, prevalecerá a proteção constitucional. Quando houver conflito entre esta proposta e uma ADR congelada, a implementação deverá permanecer `BLOCKED` até que a divergência seja resolvida por emenda ou nova decisão competente.

## 5. Estados operacionais

Toda proposta, mutação, candidatura, evento, alteração de configuração e transição de fase deverá possuir estado explícito.

Os estados mínimos são:

- `PROPOSTA`: conteúdo submetido, ainda sem autorização de execução;
- `PENDENTE`: decisão, evidência ou dependência aguardando manifestação ou verificação;
- `AUTORIZADA`: autoridade competente concedeu autorização limitada;
- `EM_EXECUÇÃO`: operação coberta pela autorização está em curso;
- `PASSOU`: requisito verificado com evidência suficiente;
- `WARNING`: risco ou limitação documentada sem bloqueio imediato;
- `DEFERRED`: melhoria autorizadamente adiada, com responsável e revisão futura;
- `BLOCKED`: autoridade, evidência, requisito ou dependência ausente;
- `NÃO_EXECUTADO`: nenhuma execução física foi realizada;
- `REVERTIDA`: efeito técnico revertido, preservando o histórico;
- `ENCERRADA`: operação finalizada conforme seus critérios.

Nenhum estado verbal poderá substituir o registro físico correspondente.

## 6. Journal operacional canônico

A rede deverá possuir um Journal Operacional Canônico, independente do estado da blockchain, para registrar a evolução, a operação, as decisões e as evidências do sistema.

O journal será um registro de evidência e continuidade. Ele não será órgão de governo, não substituirá votação, não concederá autoridade e não provará sozinho a verdade material de uma declaração.

O journal deverá permanecer disponível durante falhas da rede, em modo degradado quando necessário, e deverá permitir reconciliação posterior sem apagar registros legítimos.

## 7. Schema mínimo do journal

Cada entrada deverá conter, quando aplicável:

1. `journal_id` único;
2. sequência local e referência de predecessor;
3. momento declarado;
4. momento observado;
5. momento recebido;
6. momento processado;
7. momento confirmado;
8. ambiente e workspace;
9. identidade do ator ou pseudônimo autorizado;
10. domínio institucional de controle;
11. autoridade e escopo da operação;
12. tipo da ação;
13. finalidade declarada;
14. identificador de correlação;
15. referência de repetição, quando houver;
16. referências dos objetos de entrada;
17. hash anterior do objeto, quando houver;
18. hash posterior do objeto, quando houver;
19. estado resultante;
20. código de erro seguro, quando houver;
21. evidências vinculadas;
22. revisão ou decisão humana relacionada;
23. classificação de dados e regra de retenção;
24. assinatura ou prova de integridade, quando aplicável.

Campos ausentes deverão ser marcados como não aplicáveis, não executados ou não observados, conforme o caso. Não será permitido preencher ausência de evidência com inferência.

## 8. Integridade, correção e recuperação do journal

O journal deverá ser append-only no sentido lógico: correções serão novas entradas relacionadas ao fato anterior, e não sobrescritas silenciosas.

Uma correção deverá indicar:

- o registro original;
- o motivo;
- a autoridade;
- a evidência;
- o novo estado;
- o responsável;
- a data e os critérios de revisão.

O journal deverá possuir cópia de recuperação protegida e procedimento testável de reconstrução. A cópia de recuperação não deverá criar autoridade concorrente nem permitir alteração sem trilha.

Segredos, credenciais, dados pessoais desnecessários e topologia sensível não serão gravados em claro. O journal deverá registrar referências, hashes ou classificações adequadas quando o conteúdo integral não puder ser retido.

## 9. Relação entre journal e blockchain

O journal poderá registrar operações antes, durante e depois da confirmação blockchain. A confirmação blockchain será uma evidência específica de finalidade, não substituto de toda a cadeia operacional.

Quando a blockchain estiver indisponível:

- ações essenciais autorizadas poderão entrar em fila ou procedimento manual seguro;
- o journal deverá registrar a degradação;
- nenhuma operação pendente será apresentada como final;
- a reconciliação posterior deverá preservar ordem, origem, autorização e conflitos.

Quando uma decisão de governança for consolidada, a blockchain poderá registrar o compromisso criptográfico da proposta, do conjunto elegível, dos votos, do quórum e do resultado. Dados pessoais, segredos e evidências sensíveis permanecerão no journal ou em armazenamento protegido, com referência verificável, e não serão expostos no ledger por conveniência.

## 10. Identidade documental e manifesto

O manifesto canônico deverá possuir uma visão atual separada dos históricos “próxima decisão” presentes nas ADRs.

Após cada publicação documental, o manifesto ou um snapshot vinculado deverá registrar, quando observado:

- URL do remoto;
- branch;
- SHA antes;
- SHA depois;
- arquivos publicados;
- hashes de conteúdo;
- status da árvore;
- resultado de testes e validações;
- autoridade da publicação.

O relato anterior à publicação não deverá permanecer apresentado como estado atual sem indicação temporal.

Os nomes de arquivo deverão seguir uma convenção estável `ADR-NNN-descricao.md`. A normalização de nomes existentes será uma alteração documental controlada, com preservação do conteúdo, do hash de bytes e do histórico Git quando possível.

### 10.1 Equivalência bilíngue PT-BR/EN

Os artefatos canônicos destinados à governança, adesão, operação, APIs, schemas, dashboards, ajuda e comunicação pública — incluindo ADRs, manifesto e políticas — deverão possuir versões equivalentes em Português do Brasil (`pt-BR`) e Inglês (`en`).

A garantia bilíngue exigirá, para cada versão publicada:

- idioma, versão, data, origem e hash declarados;
- equivalência semântica revisada por pessoa competente;
- preservação de identificadores, campos, códigos, fórmulas e referências técnicas;
- indicação explícita do idioma exibido ao usuário;
- possibilidade de alternância de idioma sem perder estado, evidência, voto, contestação ou acessibilidade;
- registro da tradução, revisão, correção e aprovação no journal.

A IA poderá auxiliar a tradução e a comparação, mas não poderá decidir sozinha o significado normativo. As duas versões terão o mesmo valor normativo. Divergência relevante entre `pt-BR` e `en` produzirá `BLOCKED` para o uso afetado até reconciliação humana, com preservação das versões e dos hashes anteriores.

Essa exigência não afirma que as ADRs congeladas existentes já estejam traduzidas. A criação de suas edições bilíngues será uma tarefa documental controlada, sem reescrever silenciosamente o texto aprovado.

## 11. Votação e separação de autoridades

Votação de governança institucional, finalidade de consenso blockchain e consulta comunitária são fenômenos distintos.

- O consenso técnico confirma operações permitidas pelo protocolo.
- A governança institucional decide matérias dentro de sua competência.
- A consulta de usuários candidatos informa ou propõe, mas não adquire autoridade por mera participação.

Uma interface nunca poderá transformar uma consulta em decisão vinculante sem registrar a autoridade e a regra que conferem esse efeito.

### 11.1 Autonomia soberana e consolidação por voto

A autonomia da Agape Network significará autonomia operacional e institucional da rede federada: validadores independentes poderão manter o consenso, aplicar regras aprovadas, registrar resultados e continuar sem provedor externo obrigatório ou comando unilateral externo.

Autonomia não significará autoridade autônoma da blockchain, dos validadores, da IA, do fundador ou de qualquer operador para decidir sobre consciência, dignidade, admissão, exclusão, protocolo, custos, dados, finalidade, integração, emissão ou produção. O termo “soberana” descreve independência técnica e institucional dentro da lei; não transforma a rede em Estado, órgão público, igreja ou tribunal.

Toda decisão de governança ou matéria sensível deverá:

1. ser apresentada como proposta versionada, com finalidade, escopo, autoridade, evidências e efeito proibido;
2. fixar o universo elegível, conflitos, regra de quórum, modo de voto, abertura e encerramento;
3. receber votos de identidades elegíveis, sem voto da IA e sem aprovação por silêncio, prazo ou comando externo;
4. ser apurada por regra determinística, com prova de integridade e registro de divergências;
5. ser consolidada automaticamente na blockchain somente quando o quórum e as demais condições forem satisfeitos;
6. produzir estado explícito, hash do resultado, referências ao journal e caminho de contestação.

A consolidação automática será limitada à aplicação de regras previamente aprovadas. Ela não poderá criar autoridade, alterar o propósito constitucional, ampliar escopo, admitir instituição, trocar provedor, emitir representação social, iniciar produção ou revogar direitos sem a decisão competente.

O consenso técnico que ordena e confirma operações já autorizadas permanecerá distinto do voto de governança. Consenso não substituirá voto, e voto não dispensará a finalidade, a segurança e a validação técnica exigidas para execução.

Resultado inválido, quórum insuficiente, prova divergente, falha de finalidade ou interrupção da rede produzirá `PENDENTE` ou `BLOCKED`, nunca aprovação automática. Sistemas externos e IAs poderão formular propostas ou solicitações, mas não enviar comandos soberanos à rede.

## 12. Unidade de representação

Enquanto não houver ADR específica que estabeleça outra regra compatível, a representação institucional deverá ser baseada em domínios independentes e não em riqueza, saldo, token, capacidade computacional, quantidade de seguidores, doações ou prestígio religioso.

Filiais, pessoas jurídicas relacionadas ou nós sob controle comum não formarão automaticamente múltiplas autoridades independentes.

Usuários individuais poderão participar de consultas e propostas comunitárias. Seu papel vinculante, quando existir, deverá ser definido por regra própria, com proteção contra captura, coerção e exposição indevida.

## 13. Registro mínimo de uma proposta de voto

Toda proposta submetida a voto deverá registrar:

- identificador e versão;
- texto integral e hash;
- finalidade;
- escopo;
- classe de decisão;
- autoridade competente;
- ambiente;
- data de abertura e encerramento;
- universo elegível no momento da abertura;
- impedimentos e conflitos;
- quórum aplicável;
- opções de voto;
- efeito esperado;
- efeito proibido;
- evidências anexas;
- canal de contestação;
- regra de encerramento e revisão.

Uma proposta sem esses campos permanecerá `PROPOSTA` ou `BLOCKED` e não será apresentada como decisão.

## 14. Denominador, conflitos e arredondamento

O denominador de uma votação deverá ser fixado no snapshot de abertura, com a lista de participantes elegíveis e os impedimentos registrados.

Conflitos reais, potenciais ou aparentes deverão ser avaliados por autoridade competente e registrados antes da apuração. A exclusão de um voto não poderá ser usada para manipular silenciosamente o quórum.

Os limiares deverão usar arredondamento explícito para cima:

- maioria simples: mais de metade dos votos válidos exigidos pela regra;
- dois terços: `ceil(2N/3)`;
- finalidade superior a dois terços: `floor(2N/3)+1`;
- três quartos: `ceil(3N/4)`.

`N` deverá ser definido pela regra da instância e pelo snapshot de elegibilidade. Se a exclusão de conflitos ou a alteração do universo tornar o cálculo controverso, a matéria permanecerá pendente até revisão independente.

## 15. Resultado, empate e ausência de quórum

O resultado deverá registrar votos favoráveis, contrários, abstenções, inválidos, impedidos e ausentes, respeitando a privacidade aplicável.

Empate, quórum insuficiente, divergência de apuração ou conflito não resolvido produzirão `PENDENTE` ou `BLOCKED`. Nunca produzirão aprovação por decurso de prazo ou silêncio.

Uma maioria não poderá revogar dignidade humana, liberdade de consciência, assistência essencial, autoridade humana ou os limites materiais da ADR-001.

## 16. Sigilo, auditabilidade e coerção

O voto poderá ser secreto quando a exposição criar risco de coerção ou retaliação. O mecanismo deverá preservar prova de elegibilidade, integridade, apuração e ausência de duplicidade sem exigir publicidade indevida da escolha individual.

A escolha entre voto público e secreto deverá ser registrada antes da abertura. Não será permitido alternar o modo para favorecer um resultado.

## 17. Mecânica ainda dependente de decisão humana

Esta ADR consolida invariantes, mas não escolhe sozinha:

- a composição definitiva das câmaras;
- a duração de mandatos;
- a plataforma de votação;
- a forma criptográfica de sigilo;
- a representação final de usuários;
- a política completa de delegação;
- o procedimento de recurso externo.

Esses itens permanecem `DEFERRED` até proposta identificada, revisão e aprovação competente.

## 18. Governança da inteligência artificial

A IA poderá auxiliar a preparar propostas, resumir documentos, classificar evidências, comparar alternativas, detectar anomalias, sugerir testes e explicar estados aos usuários.

A IA não poderá, isoladamente:

- votar;
- aprovar ou rejeitar proposta;
- definir o resultado de votação;
- homologar instituição;
- julgar fé, mérito espiritual ou valor humano;
- decidir compartilhamento de dado sensível;
- escolher emissão, produção ou integração irreversível;
- substituir autoridade humana exigida.

## 19. Modo determinístico assistido

“Modo determinístico” significará execução dentro de um contrato limitado e verificável, não uma promessa de que modelos diferentes produzirão bytes idênticos.

Toda saída assistida deverá, quando aplicável, registrar:

- identificador e versão do modelo;
- provedor;
- modo e parâmetros relevantes;
- versão do prompt ou template;
- hash dos insumos autorizados;
- schema de saída;
- validações executadas;
- evidências utilizadas;
- revisão humana;
- decisão efetivamente tomada.

Saída sem validação de schema, proveniência ou escopo não poderá ser usada como autorização.

## 20. Troca de IA ou provedor

A arquitetura deverá permitir trocar o modelo sem transferir autoridade, identidade, dados ou histórico de forma silenciosa.

Uma troca deverá declarar:

- motivo;
- modelo e provedor anterior;
- modelo e provedor proposto;
- custo e condições de uso;
- dados que serão processados;
- diferenças esperadas;
- testes de regressão;
- plano de retorno;
- autoridade competente.

Mudança que afete custo institucional, dados sensíveis, decisões críticas, segurança ou comportamento público exigirá proposta e aprovação humana conforme a classe de risco. Troca emergencial para preservar disponibilidade deverá ser temporária, registrada e revisada.

Nenhum provedor, gratuito ou pago, poderá receber dados reais ou sensíveis sem finalidade legítima, base autorizada, proteção contratual e gate jurídico aplicável.

## 21. Assistência aos usuários candidatos

A IA poderá explicar regras, estados, pendências, critérios de candidatura, eventos e caminhos de recurso em linguagem acessível.

Toda explicação deverá distinguir:

- fato observado;
- regra aplicável;
- interpretação ou hipótese;
- recomendação;
- decisão humana;
- bloqueio.

O usuário deverá poder revisar a fonte, contestar a explicação, solicitar atendimento humano e sair sem perder assistência essencial.

## 22. Cloud, PC e permanência

Uma infraestrutura externa somente será candidata durante o período em que os termos oficiais verificáveis demonstrarem:

- ausência de cartão ou método de pagamento obrigatório;
- ausência de faturamento obrigatório;
- ausência de trial, crédito promocional ou conversão automática;
- ausência de cobrança oculta;
- capacidade, persistência, segurança, backups e recuperação compatíveis;
- controles contra excedentes e suspensão inesperada.

Nenhum plano gratuito será tratado como permanentemente garantido. A continuidade do fornecedor deverá ser reavaliada quando seus termos mudarem.

Se a opção externa não satisfizer os requisitos, o PC dedicado será o fallback de bootstrap, com energia, conectividade, manutenção, substituição, segurança física e contingência declaradas.

## 23. Custos dos validadores

“Sem custo para o validador” significará ausência de cobrança obrigatória da rede para aderir, permanecer ou votar. Não significará inexistência de custos de energia, internet, hardware, hospedagem, manutenção, suporte ou recuperação.

Cada validador deverá possuir registro de custeio indicando se o custo é:

- próprio;
- compartilhado;
- doado;
- patrocinado;
- apoiado por infraestrutura comum autorizada.

O custeio não poderá comprar voto, prioridade, quórum, reputação ou autoridade. A ativação deverá permanecer `BLOCKED` se a responsabilidade pelo custo e a continuidade não forem transparentes.

## 24. Dois validadores e quatro domínios

Dois validadores externos independentes poderão permitir a retirada do PC da condição de único ponto de hospedagem em bootstrap ou piloto, desde que serviço, estado, observabilidade, backup e recuperação tenham sido comprovados.

Esse marco não constitui produção, tolerância BFT completa, gênese federativa ou independência constitucional.

Produção e transição federativa continuarão exigindo pelo menos quatro domínios validadores independentes e os demais critérios das ADRs-006, 007, 012 e 013.

## 25. Adesão institucional ecumênica

O termo “instituição séria” será aplicado por critérios de conduta e capacidade, não por julgamento da verdade espiritual de uma tradição.

O checklist deverá avaliar, proporcionalmente ao papel:

- identidade e autoridade para aderir;
- finalidade compatível com dignidade e assistência;
- proteção de crianças e pessoas vulneráveis;
- privacidade e segurança;
- transparência e prestação de contas;
- declaração de conflitos;
- ausência de coerção, exploração, ódio e discriminação;
- ausência de conversão obrigatória ou proselitismo agressivo;
- capacidade de continuidade e resposta a incidentes;
- aceitação de auditoria, contestação, suspensão e saída.

O mesmo princípio de processo justo deverá valer para instituições católicas, espíritas, de outras tradições religiosas e não religiosas em estruturas equivalentes. Nenhuma instituição será admitida por proximidade religiosa, indicação unilateral ou autoridade espiritual presumida.

## 26. Eventos e instituições credenciadas

Um evento cultural, religioso, educativo ou de entretenimento poderá ser apresentado como acesso comunitário não essencial, quando houver autorização e homologação aplicáveis.

O registro mínimo deverá conter:

- instituição responsável;
- propósito;
- natureza do evento;
- público e período;
- capacidade;
- acessibilidade;
- salvaguardas;
- critérios de acesso;
- conflitos;
- autoridade;
- estado de homologação;
- validade;
- canal de contestação;
- regra de encerramento.

O acesso não será compra, preço, pagamento, investimento, remuneração, conversão, prova de mérito ou condição para assistência essencial. A instituição candidata poderá indicar um evento, mas não poderá homologá-lo sozinha.

## 27. Vocabulário protegido

Para comunicação pública, interfaces e contratos da Agape Network, deverão ser preferidos:

- registro de contribuição;
- unidade de reciprocidade;
- acesso comunitário;
- benefício não essencial;
- reconhecimento operacional;
- evidência de serviço;
- proposta de governança.

Termos financeiros poderão aparecer somente quando necessários para negar equivalência jurídica ou econômica, sempre com contexto explícito. A rede não deverá usar “moeda”, “investimento”, “cotação”, “liquidez”, “rendimento”, “pagamento” ou “mercado” para descrever sua finalidade social.

## 28. Bônus-Hora e representações sociais

O Bônus-Hora e o BH-SMC permanecerão referências externas ou dependências futuras até a obtenção de pacote canônico, glossário, contrato e aprovação dos dois projetos.

Esta ADR não autoriza emissão fungível, não fungível, saldo, conversão, transferência, integração econômica ou representação social efetiva.

Qualquer representação futura exigirá ADR própria, análise jurídica, modelo anti-especulação, emissão e revogação verificáveis, piloto controlado, privacidade, correção e aprovação humana.

## 29. Pacote canônico do BH-SMC

Antes de qualquer contrato ou mapeamento normativo, o BH-SMC deverá fornecer ou identificar um pacote contendo, no mínimo:

- identidade do projeto;
- versão;
- autoridade de aprovação;
- hashes e integridade;
- finalidade;
- glossário semântico;
- schemas e versões;
- políticas de identidade, autorização e privacidade;
- garantias de entrega, idempotência e correlação;
- evidências de testes e aprovação;
- limites de uso, encerramento e revogação.

Até essa verificação, endpoints, dashboards, textos e código do BH-SMC serão evidências de descoberta, não normas ou contratos.

## 30. Dados reais e responsabilidade jurídica

Nenhum dado real de pessoa assistida, instituição ou usuário será usado no protótipo sem:

- finalidade legítima;
- base jurídica aplicável;
- minimização;
- classificação;
- retenção;
- controle de acesso;
- correção e revogação;
- procedimento de saída;
- responsável pelo tratamento;
- avaliação de riscos;
- autorização humana e jurídica aplicável.

Antes de piloto externo deverão ser definidos, para a jurisdição aplicável, papéis de controlador e operador, responsabilidade por eventos, incidentes, recursos, contratos e atendimento às pessoas.

## 31. Protótipo mínimo permitido

Depois da autorização específica da tarefa, o primeiro protótipo poderá conter somente:

- máquina de estados local e determinística;
- journal com dados sintéticos;
- schemas e APIs locais versionadas;
- sandbox de votação sem efeito canônico;
- dashboards por papel;
- observabilidade de nós simulados;
- simulação de falhas, retry, reconciliação e recuperação;
- exportação e reimportação de evidências de teste.

O protótipo não poderá:

- usar dados reais;
- emitir representação social;
- integrar operacionalmente o BH-SMC;
- admitir instituições reais;
- criar autoridade por interface;
- declarar produção;
- usar chaves ou endpoints de produção.

## 32. Comparação tecnológica

Antes de selecionar uma tecnologia, deverá ser comparado, pelo menos:

- ledger permissionado com consenso BFT;
- registro federado append-only com provas de integridade;
- alternativa de estado assinado com auditoria independente;
- Cosmos SDK, Substrate ou alternativa equivalente, somente se atenderem aos requisitos.

A comparação deverá avaliar segurança, finalidade, recuperação, privacidade, operação, custo, portabilidade, dependências, maturidade e experiência humana. A escolha não será feita por moda, nome de fornecedor ou semelhança superficial com outro projeto.

Também deverá ser demonstrado que a alternativa escolhida permite autonomia operacional sem dependência de comando externo, votação determinística, consolidação verificável no ledger, recuperação sem autoridade concorrente e separação entre consenso técnico e governança humana.

## 33. GREEN independente

O protótipo somente poderá ser declarado GREEN por dimensão, com evidência separada de:

- código;
- backend;
- interface;
- operação;
- implantação;
- publicação;
- experiência humana.

Um dashboard bonito não provará segurança, governança, consenso, interoperabilidade ou produção.

## 34. Experiência humana

Antes de qualquer piloto deverão ser avaliados, com participantes representativos e dados sintéticos:

- compreensão do propósito;
- distinção entre simulação e decisão;
- compreensão de custos e responsabilidades;
- leitura de bloqueios e pendências;
- revisão e contestação;
- acessibilidade;
- recuperação após falha;
- compreensão da natureza não financeira da reciprocidade;
- ausência de coerção religiosa ou econômica.

Melhorias opcionais não necessárias para o gate poderão ser classificadas como `DEFERRED`, com escopo e revisão futura.

## 35. Critérios de transição

Uma transição de fase exigirá evidência do estado anterior, autorização, testes, riscos residuais, plano de retorno, responsáveis, custo, experiência humana e pós-condição física.

Os estados mínimos são:

1. fundamentação;
2. descoberta técnica;
3. protótipo isolado;
4. validação interna;
5. piloto controlado;
6. homologação;
7. prontidão para produção;
8. produção progressiva;
9. produção estável;
10. encerramento ou substituição.

Nenhuma fase será inferida da existência de código, domínio, dashboard, nó, commit ou demonstração.

## 36. Critérios de falha e parada

A execução deverá parar em caso de:

- autoridade ausente;
- hash ou identidade divergente;
- dado real não autorizado;
- conflito de escopo;
- fornecedor ou credencial inesperada;
- perda de integridade;
- falha de recuperação;
- risco de coerção ou exposição;
- dependência BH-SMC sem pacote canônico;
- limiar de custo não controlado;
- comportamento de IA sem proveniência;
- duas tentativas equivalentes sem progresso verificável.

O estado será `BLOCKED`, com registro no journal e caminho de decisão humana.

## 37. Proibições

A Agape Network não poderá:

- apresentar inspiração cristocêntrica como certificação divina ou eclesiástica;
- permitir que uma maioria elimine direitos fundamentais;
- transformar consulta de usuário em autoridade automática;
- ocultar o denominador ou os conflitos de uma votação;
- permitir que custo compre voto ou prioridade;
- trocar modelo de IA sem identidade e revisão;
- usar IA para julgar fé, mérito espiritual ou valor humano;
- usar dados reais no protótipo;
- chamar dois validadores de produção BFT;
- chamar cloud promocional de permanência garantida;
- tratar evento como compra, pagamento ou recompensa espiritual;
- importar semântica do BH-SMC sem contrato;
- tratar hash como prova suficiente de verdade material;
- apagar correções, contestação ou histórico legítimo;
- usar o dashboard como autoridade autônoma;
- alterar ADR congelada sem emenda identificável.

## 38. Responsabilidades

Cada operação deverá possuir responsável humano ou institucional, autoridade, escopo, prazo e caminho de revisão.

O software poderá executar ações já autorizadas e verificadas. Não poderá ampliar a autorização por interpretação, conveniência ou ausência de resposta.

O responsável pelo journal deverá preservar integridade e disponibilidade. O responsável pela governança deverá preservar devido processo. O responsável pela operação deverá preservar segurança, continuidade e recuperação. Nenhum papel isolado poderá acumular todas essas funções sem declaração, mitigação e revisão.

## 39. Evidências de aprovação e manutenção desta ADR

A aprovação e a manutenção desta decisão deverão ser sustentadas por:

- revisão institucional e votação registrada pela instância competente;
- confirmação de que nenhuma ADR congelada foi reescrita;
- manifesto atualizado com os hashes e o snapshot de publicação;
- schema do journal revisado;
- especificação mínima de voto revisada;
- política de IA e troca de provedor revisada;
- checklist institucional e catálogo de eventos revisados;
- versões `pt-BR` e `en` equivalentes dos artefatos normativos publicados;
- prova testável de apuração e consolidação on-chain de uma votação sintética, sem efeito canônico;
- registro das pendências jurídicas e de privacidade;
- confirmação de que BH-SMC permanece `BLOCKED` sem pacote canônico;
- hashes e validação estrutural do artefato final.

## 40. Itens `PASSOU`

No estado documental desta decisão, são considerados consolidados no fundamento. Isso não é GREEN técnico, não comprova execução física e não autoriza transição de fase:

- proteção da dignidade e liberdade de consciência;
- autoridade humana sobre decisões críticas;
- separação entre governança, consenso técnico e interface;
- distinção entre bootstrap com dois nós e produção com quatro domínios;
- adesão voluntária e ecumênica baseada em conduta;
- eventos apenas como acesso comunitário não essencial;
- reciprocidade sem equivalência financeira presumida;
- interoperabilidade contratual e independente;
- evolução progressiva e GREEN independente.

## 41. Itens `DEFERRED`

Permanecem adiados até decisões ou artefatos próprios:

- composição final das câmaras de votação;
- plataforma e criptografia do voto;
- política completa de delegação;
- tecnologia de ledger ou blockchain;
- configuração final dos validadores;
- política de apoio a custos dos operadores;
- matriz teológica e ecumênica de fontes;
- catálogo definitivo de eventos;
- representação fungível ou não fungível;
- contratação de cloud;
- admissão de instituições reais;
- responsabilidade jurídica por jurisdição;
- traduções controladas `pt-BR`/`en` das ADRs e políticas existentes, sem alteração silenciosa do texto aprovado.

## 42. Itens `BLOCKED`

Continuam bloqueados:

- interoperabilidade operacional com o BH-SMC;
- uso de semântica externa como norma interna;
- dados reais no protótipo;
- emissão, conversão ou negociação de representações sociais;
- homologação federativa real;
- produção ou declaração de prontidão;
- troca de IA sem governança e proveniência;
- declaração de disponibilidade bilíngue sem equivalência semântica e hashes verificados;
- qualquer ação sem autoridade ou evidência suficiente.

## 43. Próximas decisões delimitadas

1. Realizar revisão institucional periódica e registrar os votos elegíveis de manutenção.
2. Consolidar o schema do journal em artefato técnico testável.
3. Definir a mecânica final de representação e votação.
4. Obter o pacote canônico do BH-SMC.
5. Preparar, depois dessa obtenção, a ADR específica de interoperabilidade como proposta.
6. Comparar alternativas tecnológicas sem antecipar escolha.
7. Autorizar separadamente o protótipo local com dados sintéticos.
8. Testar a consolidação on-chain de votos sintéticos somente após a especificação e autorização técnica correspondentes.

## 44. Estado da decisão

Esta ADR foi aprovada e congelada por decisão humana em 11 de setembro de 2026.

Sua criação não autoriza software executável, cloud, nó validador, integração, emissão, coleta de dados reais, admissão institucional ou produção.

A autonomia soberana aqui definida permanece um requisito de arquitetura e governança a ser demonstrado por evidência; não é alegação de independência técnica já implementada.

Qualquer alteração futura deverá registrar autoridade humana, versão, hash, quórum, conflitos, resultado e data. Sem quórum, a matéria permanecerá pendente ou `BLOCKED`.

O critério cristocêntrico continuará sendo uma diretriz normativa humilde, sujeita a fontes verificáveis, interpretação humana e discernimento ecumênico. Nenhum artefato técnico poderá declarar-se espelho perfeito, intérprete exclusivo ou chancela religiosa.
