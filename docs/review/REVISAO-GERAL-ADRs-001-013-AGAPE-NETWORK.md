# Revisão Geral das ADRs-001 a 013 — Agape Network

- **Status:** Aprovação parcial do encaminhamento; propostas sob revisão institucional e votação elegível
- **Data:** 11 de setembro de 2026
- **Escopo:** ADRs-001 a 013, limites aprovados para infraestrutura, adesão, eventos, dashboards e interoperabilidade com o BH-SMC
- **Autoridade:** Informativo e propositivo; não cria autorização adicional
- **Objetivo:** Verificar coerência do conjunto e propor correções ou consolidações conforme o propósito constitucional e o critério cristocêntrico declarado da Agape Network

## Aprovação parcial registrada

A manifestação humana atual aprova parcialmente o encaminhamento deste relatório, do manifesto documental e da política operacional: os artefatos podem circular como propostas para revisão das instituições e votação dos participantes elegíveis.

Essa aprovação não transforma os documentos em norma final, não altera ADRs congeladas e não autoriza implementação. O desejo coletivo deverá prevalecer dentro das regras constitucionais já aprovadas: maioria simples somente para decisões ordinárias; pelo menos dois terços para admissões, promoções, suspensões prolongadas, exclusões, alterações relevantes de política e nomeações críticas; e quórum superior a dois terços para finalidade de consenso. Participantes impedidos por conflito não votam.

Nenhuma maioria poderá revogar dignidade humana, liberdade de consciência, proibição de coerção, proteção das pessoas assistidas, autoridade humana ou a precedência da ADR-001. Sem quórum ou diante de conflito não resolvido, a decisão permanece pendente ou `BLOCKED`.

## Critério normativo cristocêntrico solicitado

A solicitação atual corrige o critério de leitura do projeto: a Agape Network não deverá ser apresentada como espelho do pensamento pessoal do fundador, do usuário ou da IA. Seu critério normativo declarado deverá ser a busca de fidelidade estrita e humilde aos ensinamentos canônicos de Nosso Senhor Jesus Cristo.

Essa afirmação precisa ser tratada com precisão. Um software, um fundador ou uma ADR não conseguem provar por si mesmos que uma regra reproduz integralmente o pensamento de Cristo. Portanto, o projeto deverá separar:

- fonte primária explicitamente identificada;
- interpretação humana, católica, espírita ou de outra tradição participante;
- regra institucional verificável;
- implementação técnica subordinada à regra.

Nenhuma instituição, fundador, algoritmo ou dashboard poderá declarar-se intérprete exclusivo de Cristo. A participação ecumênica continuará voluntária e não poderá exigir conversão, uniformidade doutrinária ou submissão espiritual. A formulação “espelho estrito” deverá permanecer como critério normativo sujeito a validação humana, teológica e ecumênica, não como fato técnico já comprovado.

Também deverá ser revisada a atribuição de frases religiosas na ADR-001. As expressões citadas ali não possuem, no próprio arquivo, capítulo e versículo identificados; até a verificação de fonte, não deverão ser tratadas como citações literais de Jesus. Uma futura emenda poderá classificá-las como formulações interpretativas ou substituí-las por referências evangélicas verificáveis, sem alterar diretamente a ADR congelada.

## 1. Resultado executivo

O conjunto das ADRs-001 a 013 está coerente com o objetivo central do projeto:

> A tecnologia deve servir à caridade, à cooperação, à dignidade humana e à liberdade de consciência, sem transformar fé, necessidade ou reputação em instrumento de poder.

Não foi identificado conflito material entre as decisões aprovadas. Foram identificadas, contudo, lacunas que impedem declarar o sistema tecnicamente pronto:

- o pacote canônico do BH-SMC ainda não foi verificado;
- a interoperabilidade permanece `BLOCKED`;
- a seleção tecnológica permanece `DEFERRED`;
- dashboards, consenso, nós e APIs ainda não foram implementados ou validados;
- a publicação Git e a convergência remota não foram verificadas neste workspace.

Conclusão: **fundamentação constitucional PASSOU; implementação e produção NÃO EXECUTADAS**.

## 2. Base física revisada

Foram considerados:

1. ADR-001 até ADR-011, presentes no pacote extraído do projeto e marcadas como `Aprovada e congelada`;
2. ADR-012 aprovada e congelada, com as regras de ciclo de vida, cloud sem cartão, PC dedicado, dois validadores de bootstrap, quatro domínios para produção, adesão voluntária e eventos não essenciais;
3. ADR-013 aprovada e congelada, com o envelope técnico, dashboards, sandbox de voto, observabilidade e adaptador contratual;
4. material operacional disponível do BH-SMC, contendo backend, endpoints, implantação, dashboards e textos públicos.

O material operacional do BH-SMC é evidência de descoberta técnica. Não foi localizado, nesse material, um pacote canônico de ADRs ou uma especificação semântica oficial, versionada e aprovada que possa autorizar integração.

## 3. Âncoras observadas

| Artefato | Estado observado | Evidência |
|---|---|---|
| ADR-001 a ADR-011 | Aprovadas e congeladas | Arquivos extraídos do pacote das ADRs |
| ADR-012 | Aprovada e congelada | SHA-256 `50922f785b89e0eec46fe8a472300fc97fa5130169d8a61779bf0b1b94c8a851` |
| ADR-013 | Aprovada e congelada | SHA-256 `1a322a871cad43c3da2a337565fab27f894c35d685eaa83ce416e50162df9041` |
| BH-SMC | Referência operacional não normativa | Materiais de backend, dashboards, implantação e textos públicos |
| Git remoto | Não verificado nesta revisão | Nenhuma operação de commit, push ou conferência remota foi executada aqui |

## 4. Matriz de alinhamento constitucional

| Princípio | ADRs relacionadas | Resultado | Observação |
|---|---|---|---|
| Dignidade e liberdade de consciência | 001, 004, 012, 013 | `PASSOU` | Assistência e participação não dependem de saldo, fé ou filiação |
| Autoridade humana | 001, 003, 010, 012, 013 | `PASSOU` | IA, dashboard e automação não aprovam decisões críticas sozinhos |
| Adesão ecumênica voluntária | 001, 002, 007, 012, 013 | `PASSOU` com refinamento pendente | Faltam artefatos operacionais para comprovar os critérios em cada candidatura |
| Separação de poderes | 002, 003, 006, 007 | `PASSOU` | Quórum, impedimentos e independência estão definidos |
| Privacidade e proteção | 004, 005, 010, 012, 013 | `PASSOU` no desenho | Validação prática ainda `NÃO_EXECUTADA` |
| Consenso e validadores | 002, 006, 007, 012, 013 | `PASSOU` no fundamento | Quatro domínios continuam exigidos para produção |
| Ações verificáveis | 008, 012, 013 | `PASSOU` no desenho | Provas, eventos e testes ainda não implementados |
| Reciprocidade não especulativa | 009, 012, 013 | `PASSOU` com dependência externa | O vocabulário do BH-SMC ainda precisa ser reconciliado |
| Segurança e recuperação | 010, 012, 013 | `PASSOU` no desenho | Exercícios de falha e recuperação ainda `NÃO EXECUTADOS` |
| Independência entre projetos | 011, 013 | `PASSOU` | Nenhuma integração automática ou autoridade compartilhada foi criada |
| Evolução progressiva | 012, 013 | `PASSOU` | Protótipo, piloto, homologação e produção permanecem separados |
| Dashboards e experiência humana | 013 | `DEFERRED` | Escopo aprovado, implementação ainda inexistente |

## 5. Divergências resolvidas

### 5.1 Dois validadores e quatro domínios

Não há conflito entre:

- dois validadores externos para retirar o PC da condição de único ponto de hospedagem em bootstrap ou piloto;
- pelo menos quatro domínios independentes para tolerância BFT, produção e transição federativa.

O primeiro é redundância operacional limitada. O segundo é requisito de segurança e federação. A distinção está corretamente registrada nas ADR-012 e ADR-013.

### 5.2 Aprovação da ADR-013 e bloqueio da implementação

Também não há conflito entre aprovar e congelar o envelope arquitetural e manter `BLOCKED` a escolha tecnológica, o contrato BH-SMC, os dados reais, a emissão e a produção.

A aprovação congela limites; não declara capacidade executável.

### 5.3 Eventos e reciprocidade

O acesso a eventos foi corretamente limitado a concessão de reciprocidade comunitária não essencial. Permanece proibida a interpretação como compra, preço, pagamento, revenda, conversão, condição de assistência ou mecanismo de proselitismo.

### 5.4 Governança e dashboard

O dashboard é superfície de leitura, simulação e coordenação. Não é órgão de governo, validador isolado ou fonte autônoma de autoridade.

## 6. Pontos que exigem correção ou consolidação

### 6.1 Pacote canônico do BH-SMC — prioridade ALTA — `BLOCKED`

Os materiais disponíveis mostram um piloto operacional, com backend, rotas, dashboards, registros de horas e textos de utilidade social. Isso não prova que exista um contrato constitucional canônico.

Correção proposta:

- obter ADRs ou pacote versionado, assinado e aprovado pelo BH-SMC;
- registrar identidade, versão, autoridade e hash do pacote;
- separar material normativo, documentação técnica, código, dados de demonstração e evidência de execução;
- não importar semântica, campos ou regras do piloto diretamente para a Agape Network.

Até essa correção, qualquer integração permanece `BLOCKED`.

### 6.2 Vocabulário e semântica — prioridade ALTA — `BLOCKED`

O material público do BH-SMC contém expressões como ativo de utilidade, `$BH$`, saldo, resgate, compra, meio de troca e linguagem de emissão. Essas expressões não podem ser adotadas pela Agape Network sem reconciliação semântica, jurídica e institucional.

Correção proposta:

- adotar no projeto os termos registro de contribuição, unidade de reciprocidade, acesso comunitário, benefício não essencial e reconhecimento operacional;
- manter qualquer divergência terminológica como campo não equivalente;
- proibir tradução automática de um registro externo em autoridade, preço, pagamento, investimento, rendimento ou superioridade humana;
- criar um glossário canônico antes do contrato de interoperabilidade.

### 6.3 Critérios de instituição religiosa séria — prioridade MÉDIA/ALTA — `DEFERRED`

As ADRs protegem a adesão católica, espírita e de outras tradições sérias contra coerção e discriminação. Falta ainda um artefato operacional único para aplicar os critérios de forma repetível.

Correção proposta:

- checklist de identidade e autoridade legítima;
- finalidade compatível com dignidade e assistência;
- prestação de contas proporcional;
- salvaguardas para pessoas vulneráveis;
- aceitação de auditoria;
- declaração de conflitos;
- ausência de conversão, exploração, propaganda coercitiva ou discriminação;
- decisão registrada por instância competente, sem julgamento da verdade teológica.

O mesmo checklist deverá valer para instituições religiosas e não religiosas em estruturas equivalentes.

### 6.4 Eventos indicados por instituições — prioridade MÉDIA — `DEFERRED`

As regras constitucionais estão corretas, mas o catálogo técnico ainda precisa de campos obrigatórios:

- instituição responsável;
- propósito;
- natureza não essencial;
- público e período;
- capacidade;
- critérios de acesso;
- acessibilidade;
- salvaguardas;
- conflitos;
- estado de homologação;
- canal de contestação;
- evidência de autorização.

Sem esses campos, o evento deverá permanecer como proposta externa não homologada.

### 6.5 Infraestrutura gratuita e permanência — prioridade MÉDIA — `WARNING`

É legítimo exigir cloud sem cartão, sem cobrança obrigatória e sem custos ocultos. Nenhum fornecedor pode garantir, por si só, permanência indefinida de um plano gratuito.

Correção proposta para futura emenda textual:

> Uma opção externa só será candidata enquanto os termos oficiais verificáveis demonstrarem ausência de cartão, faturamento obrigatório e cobrança não autorizada. A continuidade futura do fornecedor não será presumida; qualquer alteração de termos reativa o fallback para PC dedicado ou outra opção aprovada.

Essa redação preserva a meta de custo sem transformar uma promessa externa em certeza.

### 6.6 Custeio dos validadores — prioridade MÉDIA — `WARNING`

“Sem custo para o validador” já foi corretamente interpretado como ausência de desembolso obrigatório para aderir, permanecer ou votar. Isso não elimina energia, conectividade, hardware, hospedagem, manutenção e recuperação.

Consolidação proposta:

- registrar o responsável por cada custo;
- indicar se o custeio é próprio, compartilhado, doado ou patrocinado;
- impedir que o custeio compre voto, prioridade ou autoridade;
- suspender a ativação quando não houver custeio transparente;
- publicar apenas agregados que não exponham dados pessoais ou estratégicos.

### 6.7 Fonte canônica das ADRs — prioridade MÉDIA — `NÃO EXECUTADO`

As ADRs possuem históricos e seções de “próxima decisão” que são corretos como registro temporal, mas podem parecer um roteiro atual depois que ADRs posteriores foram aprovadas.

Consolidação proposta:

- criar um manifesto atual das ADRs-001 a 013;
- registrar status, data, escopo, precedência, dependências e hash de cada arquivo;
- marcar “próxima decisão” histórica como histórica;
- manter no manifesto a única visão atual de gates, bloqueios e próximos passos;
- verificar publicação local e remota separadamente.

Não é necessário reescrever todas as ADRs congeladas.

### 6.8 Implementação e GREEN independente — prioridade MÉDIA — `NÃO EXECUTADO`

O envelope da ADR-013 está aprovado, mas ainda não há evidência de:

- código;
- backend;
- interface;
- operação;
- implantação;
- publicação;
- experiência humana.

Cada dimensão deverá possuir teste e evidência independente. Um dashboard renderizado não será considerado GREEN do sistema inteiro.

### 6.9 Fidelidade à fonte cristocêntrica — prioridade ALTA — `BLOCKED`

As ADRs já declaram inspiração nos ensinamentos de Nosso Senhor Jesus Cristo e estabelecem salvaguardas contra coerção, exploração, julgamento espiritual e supremacia denominacional. Ainda não existe, porém, uma matriz de fontes e interpretações que permita sustentar a formulação mais forte solicitada: que a proposta seja um espelho estrito do pensamento de Cristo.

Correção proposta:

- criar um registro de fontes evangélicas e referências verificáveis;
- distinguir texto fonte, interpretação institucional e regra operacional;
- submeter a matriz a revisão humana, teológica e ecumênica;
- registrar divergências de interpretação sem convertê-las em autoridade técnica;
- impedir que qualquer pessoa ou instituição fale em nome exclusivo de Cristo;
- manter a rede limitada à verificação de ações, consentimentos, integridade e governança, nunca de salvação, fé, santidade ou mérito espiritual.

Até essa validação, a afirmação de fidelidade estrita permanece `BLOCKED` como alegação de conformidade, embora o propósito cristocêntrico continue sendo a diretriz declarada.

## 7. Consolidação recomendada

Recomenda-se consolidar sem alterar diretamente as ADRs congeladas:

### Frente A — Manifesto canônico

Artefato de baixa mutação contendo a situação atual de ADRs, hashes, dependências, estados `PASSOU`, `BLOCKED`, `DEFERRED` e `NÃO EXECUTADO`, além da distinção entre fonte cristocêntrica, interpretação humana e regra técnica. “Canônico” aqui significa canônico para o controle documental do projeto; não significa aprovação eclesiástica automática.

### Frente B — Emenda textual controlada

Uma futura ADR de emenda poderá harmonizar apenas:

- permanência não presumida de cloud gratuita;
- definição de “sem custo obrigatório” para validadores;
- dados reais somente após todos os gates;
- distinção entre redundância de bootstrap e produção;
- vocabulário neutro da Agape Network.

### Frente C — ADR específica do BH-SMC

Depois da obtenção do pacote canônico, uma nova ADR deverá tratar:

- glossário;
- finalidade;
- identidade dos dois projetos;
- schema e versão;
- equivalência e não equivalência;
- origem e prova;
- autorização;
- idempotência;
- privacidade;
- revogação;
- encerramento;
- ausência de conversão automática.

Essa ADR não deverá ser criada como se o material operacional atual fosse norma suficiente.

### Frente D — Política operacional de adesão e eventos

O checklist institucional e o registro de eventos poderão ser uma política operacional vinculada às ADRs-002, 007, 012 e 013, evitando criar uma ADR constitucional para cada formulário ou tela. A política deverá aplicar o pacto ético comum sem transformar a adesão em prova de superioridade teológica.

## 8. Estados de governança atuais

### `PASSOU`

- fundamento ético e liberdade de consciência;
- autoridade humana;
- separação institucional;
- identidade e privacidade no desenho;
- consenso e quórum no fundamento;
- gênese e transição como decisões distintas;
- registro de ações verificáveis;
- reciprocidade não especulativa;
- segurança como obrigação arquitetural;
- independência entre Agape Network e BH-SMC;
- ciclo de vida progressivo;
- envelope de dashboards e sandbox.

### `BLOCKED`

- pacote canônico do BH-SMC;
- contrato de interoperabilidade;
- dados reais;
- emissão ou representação social efetiva;
- homologação federativa;
- produção;
- publicação remota não verificada;
- seleção tecnológica com efeito de implantação.

### `DEFERRED`

- Cosmos SDK, Substrate ou alternativa;
- algoritmo e implementação de consenso;
- configuração definitiva de nós;
- catálogo técnico de eventos;
- política operacional final de adesão;
- representação fungível ou não fungível;
- contratação de cloud;
- admissão de instituições reais.

### `NÃO EXECUTADO`

- código da Agape Network;
- backend;
- dashboards reais;
- sandbox executável;
- observabilidade de validadores;
- testes de falha e recuperação;
- deploy;
- commit, push e convergência remota.

## 9. Ordem recomendada dos próximos passos

1. Obter o pacote canônico do BH-SMC.
2. Criar o manifesto canônico das ADRs-001 a 013.
3. Reconciliar o glossário e registrar não equivalências.
4. Preparar a ADR específica de interoperabilidade, ainda como proposta.
5. Formalizar o checklist institucional e o registro de eventos.
6. Comparar tecnologias sem selecionar fornecedor por inferência.
7. Implementar somente o protótipo isolado, com dados sintéticos.
8. Validar código, backend, interface, operação, implantação, publicação e experiência humana separadamente.

## 10. Parecer final

As decisões aprovadas formam uma base constitucional consistente e rara em três aspectos: protegem a pessoa antes do mecanismo, separam cooperação de subordinação e impedem que reputação, fé, saldo ou conectividade comprem autoridade.

As correções necessárias são de consolidação e operacionalização, não de mudança do propósito. A prioridade é impedir que o material operacional do BH-SMC, a promessa de cloud gratuita ou uma interface funcional sejam interpretados como autorização para alterar a natureza da rede.

Nenhuma ADR congelada deverá ser reescrita diretamente. As mudanças futuras deverão ocorrer por emenda identificável, nova ADR ou política operacional claramente subordinada.

## 11. Snapshot BH-SDP v2.3

```json
{
  "nome_do_projeto": "Agape Network",
  "versao_do_protocolo": "BH-SDP v2.3",
  "tipo_de_arquitetura": "Rede federativa permissionada, independente, multi-institucional e interoperável por contratos explícitos",
  "meta_de_custo": "Cloud sem cartão e sem cobrança obrigatória enquanto verificável; PC dedicado como fallback",
  "fase_atual": "Fundamentação constitucional aprovada; envelope técnico aprovado; implementação não iniciada",
  "nivel_de_risco": "ALTO",
  "contagem_de_gates": 1,
  "tentativas_equivalentes": 0,
  "acoes_manuais": [
    "aprovação humana das ADRs-012 e 013",
    "obtenção do pacote canônico do BH-SMC",
    "revisão humana antes de qualquer emenda ou implementação"
  ],
  "ambiente": "localhost",
  "destino_fisico": {
    "url": "workspace local",
    "branch": "NÃO_APLICÁVEL",
    "sha_antes": "NÃO_EXECUTADO",
    "sha_depois": "NÃO_EXECUTADO"
  },
  "estado_green": {
    "codigo": "PASSOU",
    "backend": "NÃO_EXECUTADO",
    "interface": "NÃO_EXECUTADO",
    "operacao": "NÃO_EXECUTADO",
    "implantacao": "NÃO_EXECUTADO",
    "publicacao": "NÃO_EXECUTADO",
    "experiencia_humana": "NÃO_EXECUTADO"
  },
  "itens_deferred": [
    "pacote canônico e contrato BH-SMC",
    "seleção tecnológica",
    "política operacional de adesão e eventos",
    "representações sociais futuras",
    "dados reais e produção"
  ],
  "ancoras_fisicas": {
    "hash_do_commit": "NÃO_EXECUTADO",
    "status_dos_testes": "PASSOU",
    "ultimas_linhas_inspecionadas": "ADRs-001 a 013; estados finais; dependências; seções de compatibilidade; material operacional BH-SMC"
  },
  "componentes_validados": [
    "coerência constitucional entre ADRs-001 a 013",
    "separação entre aprovação documental e implementação",
    "distinção entre dois validadores de bootstrap e quatro domínios de produção",
    "adesão voluntária e ecumênica",
    "reciprocidade comunitária não especulativa",
    "independência contratual entre Agape Network e BH-SMC",
    "dashboards sem autoridade autônoma",
    "bloqueios de produção e emissão"
  ],
  "proximo_passo": "Obter o pacote canônico do BH-SMC e preparar a ADR específica de interoperabilidade como proposta"
}
```
