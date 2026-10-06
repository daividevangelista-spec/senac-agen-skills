---
name: senac-performance
description: Orienta a medição, diagnóstico e otimização de desempenho em projetos web de estudantes do SENAC. Use para investigar carregamento, Core Web Vitals, JavaScript, CSS, imagens, fontes, rede, renderização, memória, componentes e recursos de terceiros, sempre estabelecendo evidências antes da otimização e verificando o resultado depois da alteração. Priorize melhorias proporcionais ao impacto e preserve funcionalidade, acessibilidade, experiência do usuário, legibilidade e simplicidade do projeto.
---

# SENAC Performance

## Papel

Esta Skill orienta a medição, diagnóstico e otimização de desempenho em projetos web de estudantes do SENAC.

Seu princípio central é:

**medir → diagnosticar → priorizar → otimizar → medir novamente → verificar regressões.**

Desempenho não deve ser tratado como uma coleção de otimizações genéricas. Uma melhoria deve responder a um problema observado ou a um risco relevante e mensurável.

## Governança

Trabalhe dentro do escopo e do nível de autonomia definidos por \`senac-vibe-coding\`.

Esta Skill não concede a si mesma autorização para modificar o projeto.

Antes de alterar:

1. identifique o objetivo;
2. estabeleça uma referência;
3. reúna evidências;
4. localize a causa;
5. estime impacto;
6. escolha a menor intervenção adequada;
7. altere somente dentro da autorização;
8. meça novamente;
9. verifique regressões.

Não otimize por hábito.

## Medir antes de otimizar

Não declare que algo está lento sem evidência proporcional.

Quando possível, registre uma linha de base:

- tempo de carregamento;
- LCP;
- INP;
- CLS;
- tamanho de recursos;
- JavaScript transferido;
- CSS;
- imagens;
- fontes;
- requisições;
- uso de memória;
- métricas específicas do projeto.

Compare resultados em condições equivalentes sempre que possível.

Uma medição isolada pode variar. Considere o contexto do ambiente e repita quando necessário.

## Core Web Vitals

Quando forem aplicáveis, use como referência:

### LCP — Largest Contentful Paint

- até 2,5 s: bom;
- acima de 2,5 s até 4 s: precisa melhorar;
- acima de 4 s: ruim.

### INP — Interaction to Next Paint

- até 200 ms: bom;
- acima de 200 ms até 500 ms: precisa melhorar;
- acima de 500 ms: ruim.

### CLS — Cumulative Layout Shift

- até 0,1: bom;
- acima de 0,1 até 0,25: precisa melhorar;
- acima de 0,25: ruim.

Esses valores orientam diagnóstico; não substituem o contexto real do projeto.

## Laboratório e campo

Diferencie:

- **dados de laboratório:** resultados de ferramentas e ambientes controlados;
- **dados de campo:** comportamento observado em usuários e ambientes reais.

Não trate uma medição de laboratório como representação perfeita de todas as experiências.

Quando dados de campo estiverem disponíveis, considere-os no diagnóstico.

## Ferramentas

Use ferramentas adequadas ao problema, como:

- Lighthouse;
- DevTools;
- análise de rede;
- profiler;
- métricas de navegador;
- testes automatizados;
- ferramentas de build;
- métricas do projeto.

Escolha a ferramenta pelo problema, não pela popularidade.

## LCP

Para investigar LCP, considere:

- recurso principal;
- imagem principal;
- texto renderizado;
- fontes;
- CSS bloqueante;
- JavaScript que atrasa a renderização;
- tempo de servidor;
- rede;
- renderização.

Não aplique lazy loading indiscriminadamente ao elemento que determina o LCP.

Quando uma imagem for o elemento principal, considere tamanho, formato, compressão e carregamento apropriados.

## INP e interatividade

Para investigar INP, considere:

- tarefas longas;
- JavaScript excessivo;
- handlers pesados;
- renderizações desnecessárias;
- trabalho síncrono;
- componentes grandes;
- processamento durante interação.

Prefira reduzir trabalho desnecessário antes de introduzir complexidade de otimização.

## CLS e estabilidade visual

Para investigar CLS, procure:

- imagens sem dimensões reservadas;
- conteúdo inserido depois do carregamento;
- fontes que alteram layout;
- banners;
- anúncios ou recursos externos;
- componentes que mudam de tamanho inesperadamente.

A interface deve permanecer visualmente estável durante o carregamento.

## JavaScript

Considere:

- tamanho do bundle;
- código não utilizado;
- dependências;
- imports;
- code splitting;
- lazy loading;
- hidratação quando aplicável;
- tarefas longas;
- renderizações;
- execução inicial.

Não divida código indiscriminadamente.

Code splitting só é melhoria quando reduz trabalho relevante no contexto real.

## React e componentes

Quando o projeto usar React, investigue evidências de:

- renderizações desnecessárias;
- estado excessivamente amplo;
- componentes grandes;
- efeitos que executam repetidamente;
- dependências incorretas;
- polling desnecessário;
- listeners duplicados;
- consultas repetidas;
- dados buscados várias vezes.

Não use memoização ou otimizações complexas automaticamente.

Primeiro confirme que existe custo relevante.

## CSS

Considere:

- tamanho do CSS;
- CSS crítico;
- estilos duplicados;
- regras não utilizadas;
- efeitos caros;
- seletores excessivamente complexos;
- animações;
- filtros e blur;
- layout e pintura.

Não remova estilos apenas porque parecem pouco usados sem verificar seus estados e contextos.

## Imagens

Para imagens, considere:

- dimensões adequadas;
- compressão;
- formato;
- responsive images;
- lazy loading quando apropriado;
- preload somente quando justificado;
- dimensões reservadas;
- conteúdo acima da dobra.

Não comprima uma imagem de maneira que prejudique significativamente sua finalidade visual.

## Fontes

Considere:

- número de famílias;
- pesos;
- tamanho;
- carregamento;
- formatos;
- fontes externas;
- fallback;
- impacto no texto visível inicialmente.

Evite carregar pesos e famílias que o projeto não utiliza.

## Rede

Investigue:

- quantidade de requisições;
- tamanho das respostas;
- latência;
- chamadas repetidas;
- recursos bloqueantes;
- cache;
- APIs;
- terceiros.

Quando houver requisições repetidas, identifique a causa antes de criar uma camada de cache.

Cache deve considerar:

- validade;
- consistência;
- invalidação;
- concorrência;
- custo de memória;
- risco de dados obsoletos.

## Recursos de terceiros

Recursos externos podem afetar:

- carregamento;
- privacidade;
- estabilidade;
- desempenho;
- disponibilidade.

Considere se cada recurso é necessário.

Não introduza uma biblioteca ou serviço externo apenas para obter um efeito visual simples.

## Memória

Quando houver evidência de uso excessivo ou crescimento contínuo, investigue:

- listeners;
- timers;
- subscriptions;
- conexões;
- objetos retidos;
- caches;
- componentes desmontados;
- recursos que não são liberados.

Não declare vazamento de memória sem evidência suficiente.

## Polling, listeners e conexões

Para atualizações em tempo real ou periódicas, procure:

- polling duplicado;
- listeners duplicados;
- conexões abertas sem necessidade;
- subscriptions não removidas;
- atualizações fora de contexto;
- múltiplos componentes consultando o mesmo recurso.

Prefira compartilhamento quando houver evidência de duplicação e quando a arquitetura permitir.

Ao desmontar componentes, encerre recursos que não devem continuar ativos.

Considere o estado da aba quando isso for relevante.

## Recursos de carregamento

Use recursos como preload, prefetch ou preconnect somente quando houver justificativa.

Eles também podem aumentar:

- concorrência;
- consumo de rede;
- competição por recursos;
- complexidade.

Um recurso prioritário deve ser realmente prioritário.

## Performance e interface

Não sacrifique:

- acessibilidade;
- legibilidade;
- identidade visual;
- funcionalidade;
- responsividade;
- manutenção;

por uma melhoria de desempenho pequena e não significativa.

Quando uma otimização alterar a interface, envolva \`senac-ui\`.

Quando afetar acessibilidade, envolva \`senac-accessibility\`.

Quando precisar de validação comportamental, envolva \`senac-testing\`.

Quando o problema exigir avaliação ampla, envolva \`senac-code-review\`.

## Performance e pedagogia

Quando o projeto estiver em contexto de aprendizagem, favoreça que o estudante compreenda:

- qual métrica mudou;
- por que estava ruim;
- qual era a causa;
- qual solução foi escolhida;
- qual foi o trade-off;
- como o resultado foi verificado.

Não transforme otimização em uma sequência de comandos que o estudante não consegue explicar.

## Priorização

Priorize melhorias considerando:

- impacto;
- confiança na causa;
- esforço;
- risco;
- alcance;
- relevância para o usuário.

Uma correção pequena e comprovada pode ser mais valiosa que uma grande refatoração especulativa.

## Verificação após otimização

Depois de qualquer otimização relevante:

1. execute novamente a medição;
2. compare com a linha de base;
3. confirme se a métrica melhorou;
4. verifique funcionalidade;
5. verifique acessibilidade;
6. verifique interface;
7. procure regressões;
8. registre o resultado.

Não declare sucesso apenas porque o código ficou "mais limpo".

## Regressão

Uma otimização pode criar:

- bugs;
- layout quebrado;
- dados obsoletos;
- acessibilidade reduzida;
- maior complexidade;
- problemas de memória;
- pior desempenho em outro cenário.

Teste as áreas afetadas proporcionalmente ao risco.

## Diagnóstico antes de correção

Classifique a causa provável antes de agir.

Exemplos:

- rede;
- servidor;
- JavaScript;
- CSS;
- imagem;
- fonte;
- componente;
- consulta;
- terceiro;
- memória;
- renderização.

Se a causa não puder ser determinada com confiança, declare a incerteza.

Não aplique uma lista genérica de "otimizações padrão".

## Critérios de conclusão

Dentro do escopo definido, uma tarefa de desempenho está concluída quando:

- existe evidência suficiente do problema;
- uma linha de base foi estabelecida quando possível;
- a causa foi investigada;
- a melhoria foi priorizada proporcionalmente;
- a alteração foi executada dentro da autorização;
- a medição foi repetida;
- o resultado foi comparado;
- funcionalidade e qualidade foram preservadas;
- regressões relevantes foram verificadas;
- limitações foram registradas quando necessário.

"Concluído" não significa atingir uma métrica perfeita.

## Checklist

- [ ] O problema foi medido antes da otimização.
- [ ] A linha de base foi registrada quando possível.
- [ ] Laboratório e campo foram diferenciados quando aplicável.
- [ ] A causa foi investigada.
- [ ] LCP, INP e CLS foram considerados quando relevantes.
- [ ] JavaScript foi analisado antes de otimizações complexas.
- [ ] CSS foi analisado.
- [ ] Imagens foram avaliadas.
- [ ] Fontes foram avaliadas.
- [ ] Rede e requisições repetidas foram investigadas.
- [ ] Recursos de terceiros foram considerados.
- [ ] Memória foi analisada quando havia evidência.
- [ ] Cache, polling e listeners não foram alterados sem diagnóstico.
- [ ] A otimização foi proporcional ao impacto.
- [ ] A interface foi preservada ou revisada quando necessário.
- [ ] Acessibilidade foi preservada ou revisada quando necessário.
- [ ] Testes de regressão foram realizados.
- [ ] A métrica foi medida novamente.
- [ ] O resultado foi documentado.
- [ ] O estudante consegue explicar a melhoria quando aplicável.

## Regra de ouro

> **Não otimize porque o código parece poder ficar mais rápido. Meça, encontre a causa, faça a menor mudança adequada, meça novamente e confirme que a melhoria realmente valeu o custo.**
