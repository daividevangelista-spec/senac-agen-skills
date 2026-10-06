---
name: senac-ui
description: Orienta a análise, definição, construção e revisão de interfaces web de estudantes do SENAC, priorizando identidade visual, coerência, usabilidade, responsividade, acessibilidade e decisões de design justificáveis. Use para evitar interfaces genéricas ou visualmente desconectadas do contexto do projeto sem substituir as decisões formativas do estudante.
---

# SENAC UI

## Papel

Esta Skill orienta a análise, definição, construção e revisão da interface de projetos web de estudantes do SENAC.

Seu objetivo é ajudar a construir interfaces que tenham identidade, coerência, clareza e propósito, evitando soluções genéricas ou decisões visuais sem justificativa.

A interface deve responder ao contexto real do projeto, ao público, ao conteúdo e aos objetivos definidos.

## Governança

Analisar, propor, construir ou alterar a interface somente dentro do escopo e nível de autonomia definidos por \`senac-vibe-coding\`.

Esta Skill não concede a si mesma autorização para modificar o projeto.

Respeite:

1. instruções explícitas do usuário;
2. requisitos e contexto do projeto;
3. \`senac-vibe-coding\`;
4. regras desta Skill;
5. \`senac-code-review\` como camada de integração e priorização.

Quando houver conflito relevante, torne o trade-off explícito em vez de assumir que uma preferência visual deve vencer automaticamente.

## Diagnosticar antes de redesenhar

Não redesenhe uma interface apenas porque ela parece genérica, antiga ou diferente de uma preferência pessoal.

Antes de alterar:

1. identifique o objetivo da tela;
2. entenda o público;
3. observe o conteúdo;
4. identifique a hierarquia atual;
5. verifique o sistema visual existente;
6. localize inconsistências;
7. determine o impacto;
8. defina o menor escopo necessário.

Uma auditoria pode concluir que uma interface está adequada.

Não transforme uma auditoria em autorização automática para redesign.

## Contexto antes da estética

Considere, quando disponíveis:

- finalidade do produto;
- público;
- contexto de uso;
- identidade do projeto;
- conteúdo;
- tom de comunicação;
- requisitos pedagógicos;
- dispositivos utilizados;
- tecnologias e componentes existentes.

Uma solução visual deve fazer sentido no contexto em que será usada.

Não imponha um estilo visual apenas porque está em tendência.

## Identidade da interface

Uma interface com identidade não precisa ser extravagante.

Identidade pode surgir de decisões coerentes sobre:

- cor;
- tipografia;
- composição;
- espaçamento;
- formas;
- imagens;
- iconografia;
- componentes;
- conteúdo;
- microinterações;
- ritmo visual.

O conjunto deve parecer pertencente ao projeto.

Evite combinações genéricas produzidas apenas para "deixar bonito".

## Ordem das decisões

Quando for necessário construir ou melhorar uma interface, prefira esta ordem:

1. objetivo e conteúdo;
2. hierarquia da informação;
3. arquitetura da tela;
4. layout;
5. tipografia;
6. cores;
7. componentes;
8. estados;
9. responsividade;
10. interação e movimento;
11. refinamento visual.

Não tente compensar uma estrutura ruim com efeitos visuais.

## Design system e tokens

Quando existir um design system, reutilize seus tokens e componentes.

Quando não existir, estabeleça uma base proporcional ao tamanho do projeto.

Considere:

- cores principais e semânticas;
- tipografia;
- escala de tamanhos;
- espaçamento;
- raios;
- sombras;
- bordas;
- breakpoints;
- estados;
- componentes reutilizáveis.

Evite criar valores arbitrários repetidos.

Não transforme um projeto pequeno em um sistema de design excessivamente complexo.

Tokens devem existir para resolver consistência real, não para demonstrar sofisticação.

## Cores

Escolha cores considerando:

- identidade do projeto;
- hierarquia;
- legibilidade;
- significado;
- contraste;
- estados de interface;
- contexto de uso.

Não use cores aleatórias para preencher espaços.

Evite excesso de gradientes, brilhos, sombras ou cores de destaque sem função.

Cores de estado devem comunicar seu significado de maneira consistente e não depender somente da cor.

## Tipografia

A tipografia deve estabelecer hierarquia e legibilidade.

Considere:

- família;
- tamanho;
- peso;
- altura de linha;
- largura do texto;
- contraste;
- hierarquia entre títulos, corpo, rótulos e informações auxiliares.

Não use muitas famílias tipográficas sem necessidade.

A tipografia deve ajudar o usuário a compreender a interface, não competir com ela.

## Layout e composição

Construa o layout a partir da importância do conteúdo.

Considere:

- alinhamento;
- agrupamento;
- espaço em branco;
- largura de leitura;
- hierarquia;
- repetição;
- contraste;
- proximidade;
- ritmo visual.

Evite seções artificiais criadas apenas para ocupar espaço.

Uma tela não precisa preencher cada área disponível.

## Componentes e estados

Componentes devem possuir comportamento e estados coerentes.

Considere, quando aplicável:

- padrão;
- hover;
- focus;
- active;
- disabled;
- loading;
- vazio;
- erro;
- sucesso;
- seleção;
- validação.

Não considere uma interface pronta apenas porque o estado principal funciona.

Estados importantes devem fazer parte do projeto desde a concepção, e não apenas aparecer como correção posterior.

## Conteúdo

Conteúdo faz parte do design.

Evite:

- textos genéricos;
- lorem ipsum como conteúdo definitivo;
- títulos que não explicam a função da seção;
- botões sem intenção clara;
- mensagens vagas;
- conteúdo-placeholder deixado como final.

O texto deve ajudar o usuário a entender o que fazer e o que aconteceu.

Não invente conteúdo específico do projeto.

Quando faltar conteúdo real, sinalize o placeholder.

## Responsividade

A interface deve ser pensada para os contextos de uso relevantes, e não apenas reduzida de desktop para celular.

Considere:

- largura disponível;
- navegação;
- hierarquia;
- tamanho de controles;
- leitura;
- imagens;
- tabelas;
- formulários;
- menus;
- estados;
- teclado;
- zoom.

Use breakpoints quando o layout realmente precisar mudar.

Não crie dezenas de breakpoints sem necessidade.

## Movimento

Motion deve comunicar, orientar ou dar retorno ao usuário.

Pode ser usado para:

- transições;
- feedback;
- entrada e saída;
- mudança de estado;
- hierarquia;
- continuidade espacial.

Evite animações decorativas que aumentem distração ou custo sem benefício.

Respeite preferências de movimento reduzido e mantenha a interface funcional sem animação.

## Desempenho visual

Uma decisão visual não deve comprometer desnecessariamente o desempenho.

Considere:

- tamanho das imagens;
- fontes;
- efeitos pesados;
- animações;
- blur;
- sombras;
- recursos externos;
- quantidade de elementos;
- renderização.

Quando o problema for de desempenho mensurável, acione \`senac-performance\`.

Não declare que um efeito é "pesado" apenas por preferência. Procure evidência proporcional.

## Acessibilidade

A interface deve considerar acessibilidade desde a construção.

Considere:

- contraste;
- foco;
- teclado;
- nomes acessíveis;
- textos alternativos;
- estrutura semântica;
- tamanho de controles;
- mensagens de erro;
- estados;
- zoom;
- movimento reduzido;
- leitura e compreensão.

Para análise especializada de acessibilidade, acione \`senac-accessibility\`.

Acessibilidade não é uma etapa estética opcional.

## Auditoria não é redesign

Uma auditoria deve separar:

- problema real;
- oportunidade de melhoria;
- preferência pessoal;
- hipótese;
- recomendação.

Não transforme toda oportunidade em alteração obrigatória.

Quando a interface já atende ao objetivo, preserve as decisões válidas.

## Preferência pessoal não é defeito

Não classifique como problema apenas porque:

- você escolheria outra cor;
- prefere outro estilo;
- usaria outra fonte;
- gosta de outro espaçamento;
- considera outro layout mais bonito.

Uma diferença só deve ser tratada como problema quando houver relação com:

- requisito;
- usabilidade;
- acessibilidade;
- consistência;
- legibilidade;
- conteúdo;
- responsividade;
- desempenho;
- manutenção;
- objetivo do projeto.

## Participação do estudante

Quando uma decisão visual tiver valor formativo, favoreça que o estudante:

- compreenda o problema;
- escolha entre alternativas;
- justifique a escolha;
- teste a solução;
- avalie o resultado;
- modifique quando necessário.

A IA pode ajudar a executar uma decisão autorizada, mas não deve apagar a participação do estudante nas decisões que fazem parte do aprendizado.

## Verificação

Depois de uma alteração visual, verifique:

- coerência;
- estados;
- responsividade;
- acessibilidade;
- conteúdo;
- interação;
- desempenho quando relevante;
- regressões em telas relacionadas.

Quando necessário, combine esta Skill com:

- \`senac-accessibility\`;
- \`senac-testing\`;
- \`senac-performance\`;
- \`senac-code-review\`.

## Critérios de conclusão

Uma interface está concluída quando, dentro do escopo definido:

- o objetivo da tela está claro;
- a hierarquia é compreensível;
- as decisões visuais são coerentes;
- os componentes possuem estados relevantes;
- o conteúdo não depende de placeholders indevidos;
- a responsividade foi considerada;
- acessibilidade relevante foi considerada;
- efeitos visuais são proporcionais;
- a alteração foi verificada;
- decisões válidas anteriores foram preservadas;
- o resultado pode ser explicado pelo estudante quando houver valor formativo.

"Concluído" não significa "perfeito".

## Checklist de revisão

- [ ] O contexto do projeto foi considerado.
- [ ] O objetivo da tela está claro.
- [ ] A hierarquia da informação funciona.
- [ ] O layout tem intenção.
- [ ] Tipografia e cores são coerentes.
- [ ] Tokens e componentes existentes foram reutilizados.
- [ ] Os estados relevantes foram considerados.
- [ ] O conteúdo é específico ou os placeholders estão identificados.
- [ ] A interface funciona nos contextos responsivos relevantes.
- [ ] Movimento é funcional e proporcional.
- [ ] Acessibilidade foi considerada.
- [ ] O desempenho visual não foi prejudicado sem justificativa.
- [ ] Preferências pessoais não foram tratadas como defeitos.
- [ ] A alteração está dentro do escopo.
- [ ] O estudante participou das decisões formativas quando aplicável.
- [ ] O resultado foi verificado.

## Regra de ouro

> **Não faça a interface parecer diferente apenas para provar que ela não foi feita por IA. Faça-a parecer pertencente ao projeto porque as decisões de design têm contexto, propósito, coerência e justificativa.**
