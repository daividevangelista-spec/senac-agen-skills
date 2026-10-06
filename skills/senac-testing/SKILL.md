---
name: senac-testing
description: Orienta a estratégia, execução, diagnóstico e documentação de testes em projetos web de estudantes do SENAC. Use para validar comportamentos, componentes, integrações, APIs, fluxos E2E, acessibilidade, responsividade e regressões, escolhendo o nível de teste adequado ao risco e ao objetivo. Ajuda a transformar requisitos em evidências verificáveis, investigar falhas antes de corrigi-las e manter o estudante envolvido na interpretação dos resultados.
---

# SENAC Testing

## Papel

Esta Skill orienta a estratégia, execução, diagnóstico e documentação de testes em projetos web de estudantes do SENAC.

Seu objetivo é transformar requisitos e comportamentos esperados em evidências verificáveis, escolhendo testes proporcionais ao risco e ao objetivo do projeto.

Testar não significa provar que o projeto é perfeito. Significa produzir evidências sobre o comportamento observado e aumentar a confiança nas partes verificadas.

## Governança

Trabalhe dentro do escopo e do nível de autonomia definidos por \`senac-vibe-coding\`.

Esta Skill não concede a si mesma autorização para modificar o projeto.

Antes de alterar código em resposta a uma falha:

1. identifique o comportamento esperado;
2. reproduza ou confirme a falha;
3. reúna evidências;
4. classifique a causa provável;
5. determine o menor escopo necessário;
6. corrija somente quando houver autorização;
7. execute novamente o teste.

## Requisitos → critérios de aceitação → testes

Sempre que possível, transforme requisitos em critérios observáveis.

Um bom critério deve responder:

- o que deve acontecer;
- em qual condição;
- qual resultado é esperado;
- como verificar.

Exemplo:

**Requisito:** o usuário deve conseguir enviar uma atividade.

**Critério:** com dados válidos, o envio deve ser aceito, persistido e refletido na interface.

A partir disso, defina cenários de sucesso, erro e limites relevantes.

Não invente critérios que não estejam apoiados pelo requisito ou pelo contexto do projeto.

## Estratégia baseada em risco

Priorize testes conforme:

- impacto da falha;
- probabilidade;
- frequência de uso;
- complexidade;
- dependências;
- dados envolvidos;
- criticidade do fluxo;
- dificuldade de detectar a falha manualmente.

Não busque cobertura numérica como objetivo isolado.

Um teste simples de um fluxo crítico pode ser mais valioso que muitos testes de partes de baixo risco.

## Níveis de teste

Escolha o nível adequado ao problema:

### Teste manual

Útil para:

- exploração;
- experiência;
- inspeção visual;
- fluxos rápidos;
- investigação inicial.

### Teste unitário

Útil para:

- funções;
- regras isoladas;
- transformações;
- cálculos;
- validações.

### Teste de componente

Útil para:

- estados de componentes;
- interações;
- renderização;
- comportamento local.

### Teste de integração

Útil para:

- comunicação entre módulos;
- APIs;
- banco;
- autenticação;
- persistência;
- serviços.

### Teste E2E

Útil para:

- fluxos completos;
- navegação;
- autenticação;
- formulários;
- entregas;
- cenários críticos de usuário.

Não use E2E para tudo quando um teste menor fornece evidência suficiente.

## Cenários

Para cada fluxo relevante, considere quando aplicável:

- caminho feliz;
- entrada inválida;
- ausência de dados;
- limites;
- estado de carregamento;
- erro de rede;
- erro de servidor;
- permissões;
- sessão expirada;
- repetição;
- concorrência;
- atualização da interface.

Não crie cenários artificiais apenas para aumentar a quantidade de testes.

## Playwright e testes E2E

Quando o projeto usar Playwright, prefira localizadores orientados ao comportamento e à semântica.

Prioridade geral:

1. papel acessível;
2. nome acessível;
3. texto ou rótulo quando apropriado;
4. atributos de teste estáveis;
5. seletores estruturais somente quando necessário.

Evite seletores frágeis baseados em:

- classes visuais que mudam;
- posições;
- estrutura interna desnecessária;
- seletores gerados automaticamente.

O teste deve refletir como o usuário encontra e utiliza o elemento quando isso for apropriado.

## Assertions

Asserções devem verificar resultados relevantes.

Prefira verificar:

- estado;
- conteúdo;
- URL;
- visibilidade;
- acessibilidade;
- persistência;
- resposta;
- comportamento.

Evite asserções excessivamente acopladas à implementação interna.

Um teste deve falhar quando o comportamento importante deixa de funcionar, não apenas porque um detalhe visual irrelevante mudou.

## Esperas e flakiness

Não use esperas fixas como solução padrão para sincronização.

Prefira:

- auto-waiting;
- espera por estado;
- espera por elemento;
- espera por resposta ou evento relevante.

Quando um teste oscilar entre passar e falhar:

1. reproduza;
2. identifique a condição de corrida;
3. observe rede, estado e tempo;
4. corrija a causa do flakiness;
5. execute novamente.

Não aumente arbitrariamente o timeout apenas para esconder uma falha de sincronização.

## Isolamento

Testes devem ser suficientemente isolados para que a ordem de execução não determine o resultado.

Considere:

- dados independentes;
- limpeza;
- fixtures;
- estado inicial;
- autenticação;
- banco;
- armazenamento;
- sessão.

Um teste que depende silenciosamente de outro é frágil.

## Fixtures e dados de teste

Use dados controlados e seguros.

Evite depender de:

- dados reais desnecessários;
- contas pessoais;
- informações sensíveis;
- estado manual criado fora do teste.

Dados de teste devem ser reproduzíveis sempre que possível.

Não invente resultados de dados que não foram realmente executados.

## Mocking e interceptação

Use mocks ou interceptação quando isso aumentar isolamento e previsibilidade, especialmente para:

- serviços externos;
- APIs instáveis;
- respostas de erro;
- cenários difíceis de reproduzir.

Não use mocks para esconder uma integração que deveria ser realmente validada.

Diferencie claramente:

- teste isolado;
- teste de integração real;
- teste E2E com serviços reais.

## Autenticação

Para fluxos autenticados, considere:

- login;
- sessão;
- permissões;
- usuário sem acesso;
- sessão expirada;
- logout.

Não coloque credenciais reais no código de teste.

Quando houver mecanismos seguros de autenticação para testes, prefira-os.

## Persistência e banco

Quando o comportamento envolver persistência, verifique quando relevante:

- criação;
- atualização;
- leitura;
- exclusão;
- consistência;
- estados intermediários;
- tratamento de erro.

Não confunda atualização visual com persistência confirmada.

Quando a tarefa depender do banco, a evidência deve distinguir o que ocorreu na interface do que foi realmente persistido.

## Console e rede

Durante a investigação, observe quando relevante:

- erros no console;
- requisições falhas;
- códigos HTTP;
- payloads;
- tempos;
- respostas;
- erros de JavaScript.

Um fluxo que "parece funcionar" pode esconder erros no console ou chamadas de rede defeituosas.

Não trate toda mensagem de console como defeito crítico sem analisar seu impacto.

## Responsividade

Teste os contextos de tela relevantes ao projeto.

Considere:

- desktop;
- tablet quando aplicável;
- celular;
- orientação;
- largura de conteúdo;
- navegação;
- formulários;
- tabelas;
- menus;
- imagens;
- overflow.

Não limite o teste a uma única largura se o projeto precisar funcionar em várias.

## Acessibilidade

Testes de acessibilidade devem combinar automação e verificação manual.

Considere:

- teclado;
- foco;
- contraste;
- nomes acessíveis;
- semântica;
- formulários;
- mensagens;
- zoom;
- movimento;
- componentes dinâmicos.

Use \`senac-accessibility\` para análise especializada.

Uma ferramenta automatizada sem violações não significa acessibilidade completa.

## Testes visuais

Quando a aparência fizer parte do requisito, verifique:

- hierarquia;
- estados;
- alinhamento;
- conteúdo;
- responsividade;
- componentes importantes.

Snapshots visuais podem ser úteis, mas devem ser usados com critério.

Não transforme diferenças visuais irrelevantes em falhas automáticas.

## Regressão

Depois de uma correção, teste:

1. o cenário que falhou;
2. fluxos diretamente relacionados;
3. áreas de risco afetadas pela mudança.

Não é necessário executar toda a suíte para toda alteração, mas a extensão da regressão deve ser proporcional ao impacto.

## Classificação de falhas

Quando um teste falhar, diferencie:

- falha do produto;
- falha do teste;
- ambiente;
- dado;
- configuração;
- dependência externa;
- flakiness;
- comportamento esperado alterado.

Não corrija o código da aplicação automaticamente só porque um teste falhou.

## Evidência e confiança

Registre, quando relevante:

- teste executado;
- cenário;
- resultado;
- evidência;
- ambiente;
- limitações;
- confiança.

Diferencie:

- **passou:** o comportamento observado correspondeu ao esperado;
- **falhou:** o comportamento observado não correspondeu ao esperado;
- **bloqueado:** não foi possível testar;
- **não aplicável:** o cenário não pertence ao escopo.

Não transforme "não testado" em "passou".

## CI e execução repetível

Quando houver integração contínua, priorize testes:

- determinísticos;
- reproduzíveis;
- isolados;
- com tempo proporcional;
- sem dependência desnecessária de estado local.

Uma suíte lenta ou instável pode reduzir a confiança em vez de aumentá-la.

## Segurança

Durante os testes, considere riscos relevantes como:

- controle de acesso;
- exposição de dados;
- entradas maliciosas;
- autenticação;
- autorização;
- armazenamento indevido de segredos.

Não use testes como justificativa para expor credenciais ou dados reais.

Quando uma falha de segurança for identificada, trate sua severidade adequadamente e evite ações que possam causar dano.

## Pedagogia

Quando o projeto estiver em contexto de aprendizagem, o estudante deve ser envolvido na interpretação dos testes.

Favoreça que ele:

- leia o resultado;
- reproduza a falha;
- formule hipóteses;
- escolha a correção;
- teste novamente;
- explique por que o teste é relevante.

A IA pode ajudar a executar testes e organizar evidências, mas não deve transformar os resultados em uma caixa-preta.

## Integração com outras Skills

Use outras Skills quando necessário:

- \`senac-vibe-coding\` para governança e autonomia;
- \`senac-ui\` para questões de interface;
- \`senac-accessibility\` para acessibilidade;
- \`senac-performance\` para desempenho;
- \`senac-code-review\` para revisão integrada e priorização.

Uma falha descoberta por testes pode ser encaminhada para a Skill especializada correspondente antes da correção.

## Critérios de conclusão

Dentro do escopo definido, os testes estão concluídos quando:

- requisitos relevantes foram convertidos em comportamentos verificáveis;
- riscos principais foram considerados;
- o nível de teste escolhido é proporcional ao problema;
- cenários relevantes foram executados;
- falhas foram investigadas antes da correção;
- resultados foram registrados corretamente;
- regressões relevantes foram verificadas;
- limitações conhecidas foram registradas;
- o estudante participou da interpretação quando aplicável.

"Concluído" não significa cobertura total ou ausência absoluta de defeitos.

## Checklist

- [ ] O requisito ou comportamento esperado está claro.
- [ ] Critérios de aceitação são verificáveis.
- [ ] Os testes foram priorizados por risco.
- [ ] O nível de teste é adequado.
- [ ] Cenários de sucesso e erro relevantes foram considerados.
- [ ] Localizadores são estáveis quando aplicável.
- [ ] Assertions verificam comportamento relevante.
- [ ] Esperas não escondem problemas de sincronização.
- [ ] Dados de teste são controlados e seguros.
- [ ] Mocks são usados com propósito.
- [ ] Autenticação e permissões foram consideradas.
- [ ] Persistência foi diferenciada de atualização visual.
- [ ] Console e rede foram observados quando relevantes.
- [ ] Responsividade foi considerada.
- [ ] Acessibilidade foi considerada.
- [ ] Regressões relevantes foram verificadas.
- [ ] Falhas foram classificadas antes de corrigir.
- [ ] "Não testado" não foi tratado como "passou".
- [ ] Evidências e limitações foram registradas.
- [ ] O estudante participou da interpretação quando aplicável.

## Regra de ouro

> **Teste não é para provar que a aplicação é perfeita; é para produzir evidência confiável sobre o que ela realmente faz, revelar riscos e permitir que o estudante compreenda, corrija e valide o próprio trabalho.**
