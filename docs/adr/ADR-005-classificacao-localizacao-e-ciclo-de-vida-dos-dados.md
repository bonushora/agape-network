# ADR-005 — Classificação, Localização e Ciclo de Vida dos Dados On-chain e Off-chain

- **Status:** Aprovada e congelada
- **Data:** 20 de agosto de 2026
- **Projeto:** Agape Network
- **Repositório:** `bonushora/agape-network`
- **Classificação:** Decisão constitucional, arquitetural, de segurança e privacidade
- **Escopo:** Classificação, armazenamento, referência, retenção, correção, revogação e destruição de dados
- **Precedência:** Subordinada à ADR-001, ADR-002, ADR-003 e ADR-004
- **Dependências:** ADR-001 a ADR-004

## 1. Contexto

A Agape Network utilizará uma infraestrutura distribuída para comprovar ações, decisões, autorizações, integridade e prestação de contas.

A blockchain poderá replicar registros entre instituições independentes e preservar evidências por longo período. Essa característica é útil para confiança e auditoria, mas torna perigoso o armazenamento indiscriminado de dados pessoais, sensíveis, secretos ou sujeitos a correção.

A ADR-004 determinou que dados pessoais e sensíveis permanecerão preferencialmente fora da blockchain.

Esta ADR define quais classes de informação poderão ser consideradas para registro on-chain, quais deverão permanecer off-chain e como todo dado deverá percorrer seu ciclo de vida.

## 2. Decisão

A Agape Network adotará arquitetura híbrida:

- blockchain para provas, compromissos, estados autorizados e registros institucionais mínimos;
- armazenamento off-chain protegido para conteúdo pessoal, sensível, volumoso, corrigível ou sujeito a exclusão;
- referências criptográficas para vincular os dois ambientes quando necessário;
- políticas explícitas de retenção, correção, revogação e destruição;
- classificação obrigatória antes de qualquer gravação.

Nenhum dado será registrado on-chain apenas porque isso é tecnicamente possível.

## 3. Princípio fundamental

> A blockchain deverá provar o que precisa ser verificável sem transformar a vida, a fé ou a vulnerabilidade das pessoas em registro público permanente.

## 4. Autoridade de classificação

Todo tipo de dado deverá possuir classificação aprovada antes de entrar em produção.

A classificação deverá identificar:

- proprietário institucional responsável;
- finalidade;
- sujeitos envolvidos;
- sensibilidade;
- localização;
- replicação;
- acesso;
- retenção;
- correção;
- revogação;
- destruição;
- risco de correlação;
- fundamento aplicável.

A aplicação não poderá decidir silenciosamente a classificação durante a execução.

## 5. Classes de dados

A rede adotará inicialmente as classes:

1. público institucional;
2. federativo restrito;
3. operacional protegido;
4. pessoal;
5. pessoal sensível;
6. segredo institucional;
7. segredo criptográfico;
8. evidência;
9. metadado técnico;
10. dado derivado.

A classificação final será atribuída por esquema e finalidade, não apenas pelo nome do campo.

## 6. Dados públicos institucionais

Poderão ser públicos, conforme política:

- Constituição e ADRs;
- políticas vigentes;
- identidade de instituições validadoras;
- chaves públicas autorizadas;
- papéis dos nós;
- situação dos validadores;
- decisões de governança publicáveis;
- versões de software autorizadas;
- relatórios agregados;
- auditorias sem dados protegidos.

Mesmo dados públicos deverão observar integridade, autenticidade e finalidade.

## 7. Dados federativos restritos

Serão acessíveis apenas às instituições ou órgãos autorizados, podendo incluir:

- candidaturas de nós;
- avaliações institucionais;
- conflitos declarados não públicos;
- relatórios internos;
- investigações;
- planos de resposta;
- informações técnicas de segurança;
- deliberações ainda não publicadas.

A restrição federativa não autoriza replicação ilimitada.

## 8. Dados operacionais protegidos

Poderão incluir:

- solicitações de assistência;
- fluxos de aprovação;
- encaminhamentos;
- registros de atendimento;
- autorizações operacionais;
- detalhes de execução;
- informações logísticas;
- contatos necessários;
- documentos de suporte.

Esses dados permanecerão off-chain por padrão.

## 9. Dados pessoais

São informações relacionadas a pessoa identificada ou identificável.

Incluem, entre outras:

- nome;
- documento;
- endereço;
- contato;
- imagem;
- voz;
- localização;
- identificadores;
- relações familiares;
- histórico de atendimento;
- dados financeiros individualizados.

Dados pessoais não serão gravados diretamente on-chain por padrão.

## 10. Dados pessoais sensíveis

Serão protegidos com nível reforçado, incluindo informações sobre:

- religião;
- crença;
- ausência de crença;
- saúde;
- deficiência;
- origem racial ou étnica;
- biometria;
- vida sexual;
- opinião política;
- filiação;
- condição de vulnerabilidade;
- crianças e adolescentes.

Esses dados deverão permanecer off-chain e não poderão ser incorporados a hashes previsíveis sem análise específica de reidentificação.

## 11. Segredos institucionais

Incluem:

- credenciais;
- planos internos de segurança;
- vulnerabilidades ainda não corrigidas;
- dados de investigação;
- configurações sensíveis;
- material de autenticação;
- informações protegidas por dever jurídico.

Segredos institucionais não serão armazenados em texto aberto on-chain.

## 12. Segredos criptográficos

Chaves privadas, seeds, senhas, tokens de sessão, fatores de recuperação e material equivalente nunca serão registrados on-chain.

Também não serão incluídos em:

- logs;
- eventos;
- mensagens de erro;
- snapshots públicos;
- repositórios;
- relatórios;
- backups desprotegidos.

Somente chaves públicas e provas adequadas poderão ser publicadas.

## 13. Evidências

Uma evidência poderá possuir:

- conteúdo original off-chain;
- hash criptográfico;
- identificador;
- origem;
- custodiante;
- momento autorizado;
- cadeia de custódia;
- situação;
- referências;
- assinaturas.

O registro on-chain deverá comprovar integridade e estado sem necessariamente revelar o conteúdo.

Requisitos completos de cadeia de custódia serão definidos na ADR-009.

## 14. Metadados técnicos

Metadados podem produzir exposição mesmo sem conteúdo explícito.

Deverão ser avaliados:

- horários;
- frequência;
- origem de rede;
- identificadores;
- tamanho;
- sequência;
- relacionamento entre operações;
- localização;
- padrão de atividade;
- chaves públicas.

Metadados capazes de revelar assistência, religião ou vulnerabilidade serão protegidos.

## 15. Dados derivados

Inferências, pontuações, classificações, perfis e resultados produzidos por sistemas também serão classificados.

Dado derivado não será considerado inofensivo apenas por não ter sido fornecido diretamente pela pessoa.

Ficam proibidos derivados destinados a medir:

- fé;
- santidade;
- mérito espiritual;
- merecimento moral;
- probabilidade de conversão;
- valor humano.

## 16. Critérios para registro on-chain

Um dado somente poderá ser registrado on-chain quando houver necessidade demonstrável de:

- consenso;
- integridade compartilhada;
- não repúdio institucional;
- prova de existência;
- prova de autorização;
- prova de sequência;
- estado federativo comum;
- prevenção de duplicidade;
- auditoria distribuída.

Além disso, deverá:

- ser mínimo;
- possuir risco aceitável;
- não expor pessoa vulnerável;
- não exigir correção destrutiva;
- ser compatível com retenção prolongada;
- possuir esquema aprovado.

## 17. Conteúdo permitido on-chain

Poderão ser elegíveis, conforme política posterior:

- identificadores opacos de operação;
- hashes ou compromissos seguros;
- assinaturas;
- chaves públicas institucionais;
- estados de nós;
- decisões de governança;
- versões de políticas;
- provas de autorização;
- referências a evidências;
- registros mínimos de auditoria;
- marcadores de revogação;
- estados agregados não reidentificáveis.

Elegibilidade não significa autorização automática.

## 18. Conteúdo proibido on-chain

Fica proibido registrar diretamente:

- nomes de pessoas assistidas;
- documentos pessoais;
- endereços;
- telefones;
- e-mails pessoais;
- diagnósticos;
- prontuários;
- fotografias pessoais;
- biometria;
- religião individual;
- relatos de sofrimento;
- histórias familiares;
- dados de crianças;
- localização precisa de vulneráveis;
- credenciais secretas;
- chaves privadas;
- conteúdo integral de documentos;
- denúncias identificáveis;
- material ilícito;
- dados destinados a avaliar mérito espiritual.

Exceção futura exigirá ADR específica e não poderá contrariar a ADR-001 ou ADR-004.

## 19. Hashes e compromissos

Hash não será tratado automaticamente como dado anônimo.

Antes de registrar um hash serão avaliados:

- entropia do original;
- previsibilidade;
- uso de salt;
- uso de segredo;
- possibilidade de força bruta;
- correlação;
- tamanho do universo;
- risco futuro;
- necessidade de prova pública;
- possibilidade de desligamento da referência.

Hashes de CPF, telefone, e-mail, diagnóstico ou respostas religiosas sem proteção adequada serão proibidos.

## 20. Armazenamento off-chain

O conteúdo protegido deverá permanecer em repositórios off-chain com:

- criptografia em trânsito;
- criptografia em repouso;
- controle granular;
- segregação institucional;
- logs de acesso;
- retenção definida;
- backups protegidos;
- correção;
- exclusão;
- recuperação;
- resposta a incidentes.

A tecnologia específica será definida posteriormente.

## 21. Referências entre ambientes

Uma referência on-chain para conteúdo off-chain deverá ser:

- opaca;
- não enumerável;
- incapaz de revelar diretamente a pessoa;
- vinculada a política;
- verificável;
- revogável logicamente;
- resistente a correlação desnecessária.

URLs públicas contendo identificadores pessoais não serão utilizadas.

## 22. Criptografia e separação

Dados protegidos deverão utilizar separação adequada entre:

- conteúdo;
- índices;
- chaves;
- metadados;
- backups;
- ambientes;
- instituições;
- finalidades.

A mesma chave não deverá proteger indiscriminadamente todos os dados e contextos.

Detalhes de custódia serão definidos na ADR-008.

## 23. Ciclo de vida

Todo dado deverá atravessar estados controlados:

1. proposta de coleta;
2. classificação;
3. autorização;
4. coleta ou geração;
5. validação;
6. armazenamento;
7. utilização;
8. compartilhamento;
9. atualização;
10. arquivamento;
11. revogação ou expiração;
12. destruição ou preservação justificada.

Nenhuma etapa será presumida pelo simples fato de a anterior ter ocorrido.

## 24. Coleta

Antes da coleta deverão existir:

- finalidade;
- classificação;
- campos autorizados;
- responsável;
- fundamento;
- prazo;
- política de acesso;
- localização;
- forma de informação à pessoa;
- mecanismo de correção.

Coleta exploratória indiscriminada será proibida.

## 25. Validação

A validação de dados deverá verificar:

- formato;
- integridade;
- origem;
- autorização;
- necessidade;
- consistência;
- ausência de conteúdo proibido;
- classificação;
- destino correto.

Dados reprovados não poderão ser enviados silenciosamente à blockchain.

## 26. Retenção

Cada categoria possuirá prazo ou critério de retenção.

A retenção considerará:

- finalidade;
- obrigações aplicáveis;
- defesa de direitos;
- segurança;
- risco;
- necessidade de auditoria;
- capacidade de correção;
- expectativa legítima da pessoa.

“Para sempre” não será política padrão para dados off-chain.

## 27. Correção

Dados off-chain deverão permitir correção controlada.

A correção deverá:

- preservar autoria;
- registrar motivo;
- impedir apresentação do estado antigo como atual;
- manter histórico somente quando necessário;
- atualizar referências autorizadas;
- comunicar sistemas dependentes.

Registros on-chain incorretos serão tratados por evento de correção ou substituição lógica, nunca por ocultação do erro.

## 28. Revogação lógica

Quando um registro imutável perder validade, a rede deverá registrar estado posterior que indique:

- revogado;
- expirado;
- substituído;
- contestado;
- inválido;
- suspenso.

Consumidores deverão consultar o estado vigente, não apenas a existência histórica.

## 29. Exclusão off-chain

Quando aplicável, a exclusão deverá remover:

- conteúdo principal;
- réplicas não necessárias;
- índices;
- caches;
- temporários;
- filas;
- exportações controladas;
- backups após seu ciclo autorizado.

A exclusão deverá produzir evidência mínima de cumprimento sem reproduzir o dado eliminado.

## 30. Destruição criptográfica

Quando adequada, a destruição de chaves poderá tornar conteúdo inacessível.

Ela deverá:

- possuir autoridade;
- ser registrada;
- afetar somente o escopo correto;
- considerar backups;
- impedir reconstrução indevida;
- ser validada;
- respeitar preservação obrigatória.

Destruição criptográfica não será anunciada como apagamento físico universal sem comprovação.

## 31. Backups

Backups estarão sujeitos às mesmas classificações do dado original.

Deverão possuir:

- criptografia;
- inventário;
- controle de acesso;
- retenção;
- teste de recuperação;
- expiração;
- destruição;
- segregação;
- rastreabilidade.

Backup não será justificativa para retenção ilimitada.

## 32. Replicação

A replicação será mínima e proporcional.

Antes de replicar serão avaliados:

- necessidade;
- instituições destinatárias;
- jurisdições;
- classificação;
- finalidade;
- segurança;
- retenção;
- capacidade de revogação;
- impacto de comprometimento.

Participar da federação não concederá acesso automático a todos os dados off-chain.

## 33. Compartilhamento

Compartilhamento exigirá:

- emissor autorizado;
- destinatário autorizado;
- finalidade;
- conjunto mínimo;
- prazo;
- proteção;
- registro;
- restrições de reutilização.

Exportações em massa serão operações críticas.

## 34. Portabilidade e interoperabilidade

A portabilidade deverá utilizar formatos documentados e seguros.

A interoperabilidade não poderá:

- reduzir classificação;
- eliminar finalidade;
- expor identificadores;
- transformar dados protegidos em públicos;
- ignorar revogação;
- contornar autorização.

Contratos de interoperabilidade serão definidos na ADR-011.

## 35. Agregação e estatísticas

Dados agregados poderão ser publicados quando houver proteção contra reidentificação.

Serão avaliados:

- tamanho dos grupos;
- raridade;
- combinação de atributos;
- localização;
- séries temporais;
- possibilidade de subtração;
- acesso a fontes auxiliares.

Pequenos grupos vulneráveis não serão expostos em nome da transparência.

## 36. Logs

Logs deverão evitar:

- conteúdo pessoal completo;
- segredos;
- tokens;
- documentos;
- diagnósticos;
- relatos;
- respostas religiosas;
- payloads integrais desnecessários.

Logs terão classificação, acesso, retenção e descarte próprios.

## 37. Ambientes não produtivos

Dados reais protegidos não serão copiados indiscriminadamente para:

- desenvolvimento;
- testes;
- demonstrações;
- treinamento;
- suporte;
- protótipos.

Serão preferidos dados sintéticos ou adequadamente desidentificados.

## 38. Inteligência artificial

Dados não poderão ser enviados a sistemas de IA apenas por conveniência.

O uso exigirá:

- finalidade aprovada;
- classificação compatível;
- minimização;
- contrato adequado;
- controle de retenção;
- impedimento de treinamento não autorizado;
- supervisão;
- auditoria;
- avaliação de inferências.

A IA não será autorizada a reconstruir identidades protegidas.

## 39. Incidentes

Incidentes deverão permitir identificar:

- classe afetada;
- localização;
- sujeitos;
- réplicas;
- chaves;
- acessos;
- impacto;
- obrigações;
- contenção;
- recuperação;
- comunicação;
- prevenção de recorrência.

A fragmentação federativa não eliminará coordenação de resposta.

## 40. Inventário e linhagem

A rede deverá manter inventário dos tipos de dados e sua linhagem.

A linhagem deverá indicar, conforme aplicável:

- origem;
- transformações;
- derivações;
- responsáveis;
- destinos;
- versões;
- compartilhamentos;
- retenção;
- estado vigente.

Inventário não deverá reproduzir dados sensíveis.

## 41. Esquemas e contratos

Cada operação deverá declarar esquema de dados.

O esquema definirá:

- campo;
- tipo;
- obrigatoriedade;
- classificação;
- localização;
- validação;
- retenção;
- possibilidade de publicação;
- regra de correção;
- versão.

Campo sem classificação aprovada será rejeitado em modo fail-closed.

## 42. Mudança de classificação

Reclassificação exigirá:

- justificativa;
- análise de impacto;
- autoridade;
- revisão;
- registro;
- migração segura;
- reavaliação de acessos;
- reavaliação de réplicas;
- comunicação quando aplicável.

Dados protegidos não poderão ser tornados públicos por decisão operacional simples.

## 43. Responsabilidade institucional

Cada conjunto de dados deverá possuir responsável identificável.

A responsabilidade incluirá:

- classificação;
- qualidade;
- acesso;
- retenção;
- correção;
- incidentes;
- compartilhamento;
- destruição;
- atendimento de direitos.

Descentralização não significará ausência de responsável.

## 44. Auditoria

A auditoria deverá verificar:

- aderência à classificação;
- localização real;
- acessos;
- replicações;
- retenções;
- exclusões;
- referências on-chain;
- hashes;
- backups;
- reclassificações;
- incidentes.

A auditoria preservará a minimização e não criará cópia paralela irrestrita.

## 45. Proibições constitucionais

Fica proibido:

- publicar vulnerabilidade individual para atrair doações;
- tornar assistência condicionada à exposição;
- registrar religião individual on-chain;
- armazenar segredo criptográfico na blockchain;
- usar hash previsível como falsa anonimização;
- manter dados indefinidamente sem fundamento;
- replicar todos os dados para todos os nós;
- ignorar correções;
- apresentar estado revogado como vigente;
- utilizar imutabilidade para negar direitos;
- criar mercado de dados de pessoas assistidas;
- ocultar responsabilidade sob o argumento de descentralização.

## 46. Consequências

Esta decisão:

- estabelece arquitetura híbrida;
- reduz exposição permanente;
- restringe conteúdo on-chain;
- exige armazenamento off-chain protegido;
- exige classificação por esquema;
- cria ciclo de vida explícito;
- preserva correção e revogação lógica;
- limita replicação;
- aumenta complexidade operacional;
- prepara a escolha de consenso sem sacrificar privacidade.

## 47. Riscos reconhecidos

Permanecem riscos de:

- correlação;
- reidentificação;
- perda de vínculos off-chain;
- comprometimento de chaves;
- divergência entre estado on-chain e off-chain;
- retenção indevida;
- exclusão incompleta;
- replicação não autorizada;
- esquemas incorretos;
- agregados reidentificáveis;
- logs excessivos;
- dependência de armazenamento externo.

Esses riscos deverão possuir controles e testes específicos.

## 48. Decisões adiadas

Esta ADR não define:

- banco de dados;
- armazenamento de objetos;
- algoritmo de hash;
- criptografia;
- formato de compromisso;
- mecanismo de prova;
- política temporal completa;
- jurisdição dos servidores;
- padrão de esquema;
- tecnologia blockchain;
- estratégia de backup;
- implementação de destruição criptográfica.

## 49. Próximas decisões necessárias

A próxima decisão será:

> ADR-006 — Modelo de Consenso, Finalidade e Tolerância a Falhas.

As decisões criptográficas específicas continuarão adiadas até que seus requisitos estejam suficientemente definidos.

## 50. Compatibilidade

Esta ADR deverá ser interpretada conforme a ADR-001 a ADR-004.

Em caso de dúvida, prevalecerá a alternativa que:

- reduza exposição humana;
- preserve integridade;
- permita responsabilização;
- limite autoridade;
- respeite finalidade;
- mantenha a tecnologia subordinada à dignidade.

## 51. Estado da decisão

Esta ADR foi expressamente autorizada, aprovada e congelada por decisão humana em 20 de agosto de 2026.

A classificação, a localização e o ciclo de vida dos dados da Agape Network deverão permanecer subordinados a esta decisão durante todo o ciclo de vida do projeto.

Nenhuma implementação técnica está autorizada exclusivamente por esta ADR. Cada fase continuará sujeita à Inspeção Declarativa, decisão arquitetural correspondente e autorização humana.
