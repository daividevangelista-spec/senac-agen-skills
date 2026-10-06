---
name: senac-accessibility
description: Orienta a análise, construção, teste e revisão de acessibilidade em projetos web de estudantes do SENAC. Use para avaliar semântica HTML, teclado, foco, contraste, nomes acessíveis, imagens, formulários, componentes dinâmicos, responsividade, movimento e outros critérios de acessibilidade, priorizando soluções nativas e verificáveis sem substituir as decisões formativas do estudante.
---

# SENAC Accessibility

## Papel

Esta Skill orienta a análise, construção, teste e revisão de acessibilidade em projetos web de estudantes do SENAC.

Seu objetivo é tornar a acessibilidade parte da qualidade do projeto, considerando pessoas com diferentes necessidades de interação, percepção, compreensão e acesso ao conteúdo.

Acessibilidade deve ser considerada durante a construção e não apenas como uma correção final.

## Governança

Trabalhe dentro do escopo e do nível de autonomia definidos por \`senac-vibe-coding\`.

Esta Skill não concede a si mesma autorização para modificar o projeto.

Antes de alterar qualquer coisa:

1. entenda o objetivo;
2. identifique o problema;
3. reúna evidências;
4. avalie o impacto;
5. determine o menor escopo necessário;
6. proponha ou execute somente o que estiver autorizado.

Quando houver conflito entre acessibilidade e outra decisão do projeto, explicite o trade-off e procure uma solução que preserve a maior qualidade possível.

## HTML nativo antes de ARIA

Prefira elementos HTML semânticos e nativos quando eles já fornecem o comportamento necessário.

Exemplos:

- \`button\` para ações;
- \`a\` para navegação;
- \`label\` associado a campos;
- \`input\`, \`select\` e \`textarea\` adequados ao conteúdo;
- headings em ordem lógica;
- landmarks semânticos quando apropriados.

ARIA deve complementar a semântica quando necessário.

Não use ARIA para simular um componente nativo que já resolve o problema.

## ARIA é uma promessa

Ao usar ARIA, confirme que o componente realmente oferece o comportamento correspondente.

Não adicione atributos ARIA apenas para eliminar alertas automáticos.

Verifique:

- papel;
- nome acessível;
- estado;
- propriedade;
- valor quando aplicável;
- comportamento de teclado;
- atualização dinâmica.

Um papel acessível sem comportamento correspondente pode criar uma experiência enganosa.

## Teclado

Todo fluxo relevante deve poder ser operado por teclado quando a interação não depender essencialmente de uma entrada física específica.

Verifique:

- ordem de tabulação;
- elementos focáveis;
- ativação por teclado;
- ausência de armadilhas de foco;
- navegação em menus;
- diálogos;
- dropdowns;
- componentes personalizados;
- formulários;
- controles dinâmicos.

Não crie \`tabindex\` positivos sem necessidade.

Prefira a ordem natural do documento.

## Foco

O foco deve ser:

- visível;
- previsível;
- coerente;
- preservado quando a interface muda.

Ao abrir um modal, considere:

- mover o foco para o contexto apropriado;
- impedir interação indevida com o conteúdo de fundo;
- permitir fechamento por teclado quando aplicável;
- devolver o foco ao elemento de origem quando adequado.

Ao fechar ou remover elementos, evite deixar o usuário sem contexto de foco.

## Contraste e cor

Verifique contraste suficiente entre conteúdo e fundo.

Não use cor como único meio de transmitir:

- erro;
- sucesso;
- alerta;
- seleção;
- estado;
- prioridade.

Quando a cor tiver função semântica, complemente-a com texto, ícone, estrutura ou outro sinal apropriado.

Não declare que uma combinação falha em contraste sem evidência ou medição quando uma afirmação precisa for necessária.

## Nomes acessíveis

Controles interativos devem possuir nomes acessíveis compreensíveis.

Verifique especialmente:

- botões somente com ícone;
- links;
- campos;
- controles personalizados;
- menus;
- diálogos;
- elementos que mudam de estado.

O nome deve comunicar a ação ou finalidade, e não apenas repetir informação visual irrelevante.

## Imagens e conteúdo não textual

Para imagens, determine a função:

- informativa;
- decorativa;
- funcional;
- complexa;
- parte de conteúdo.

Use texto alternativo apropriado ao propósito.

Imagens decorativas podem precisar ser ignoradas por tecnologias assistivas.

Não invente descrição de uma imagem quando o contexto real não estiver disponível.

## Formulários

Formulários devem fornecer:

- rótulos claros;
- instruções quando necessárias;
- associação entre campo e rótulo;
- identificação de erro;
- mensagens compreensíveis;
- indicação de estado;
- ordem lógica;
- feedback acessível.

Não dependa apenas de placeholder como rótulo.

Quando houver erro, ajude o usuário a localizar e corrigir o problema.

## Componentes dinâmicos

Mudanças de interface precisam ser perceptíveis para quem não depende exclusivamente de visão ou interação por mouse.

Considere:

- mensagens;
- alertas;
- atualizações de conteúdo;
- carregamento;
- erros;
- sucesso;
- resultados de pesquisa;
- filtros;
- mudanças de estado.

Quando apropriado, use mecanismos como regiões vivas com cuidado.

Não transforme toda alteração visual em anúncio automático.

## Menus, diálogos e componentes personalizados

Componentes complexos exigem comportamento coerente.

Verifique:

- semântica;
- teclado;
- foco;
- estados;
- fechamento;
- leitura;
- relacionamento entre controle e conteúdo.

Quanto mais um componente se afasta de um elemento nativo, maior a responsabilidade de reproduzir corretamente seu comportamento acessível.

## Tamanho e área de interação

Controles interativos devem possuir área de interação suficiente para uso confortável.

Considere:

- tamanho;
- espaçamento entre controles;
- dispositivos de toque;
- contexto de uso.

Não reduza controles importantes apenas para obter uma composição visual mais compacta.

## Zoom e responsividade

A interface não deve depender de um único tamanho de tela.

Verifique:

- zoom;
- reflow;
- leitura;
- navegação;
- formulários;
- tabelas;
- menus;
- conteúdo que pode ficar oculto;
- sobreposição de elementos.

Não trate uma interface como acessível apenas porque ela funciona em uma largura específica.

## Movimento

Movimentos, transições e animações devem ser proporcionais e não impedir o uso da interface.

Considere a preferência de movimento reduzido quando disponível.

Evite:

- movimento contínuo desnecessário;
- efeitos que dificultem leitura;
- animações que escondam informação;
- interações que dependam exclusivamente de movimento.

A interface deve continuar funcional quando animações forem reduzidas ou removidas.

## Conteúdo, compreensão e cognição

Acessibilidade também envolve compreensão.

Considere:

- linguagem clara;
- instruções objetivas;
- consistência;
- mensagens previsíveis;
- identificação de erros;
- organização do conteúdo;
- redução de ambiguidades.

Não simplifique conteúdo de maneira que elimine informações necessárias.

## Tabelas e conteúdo estruturado

Quando houver tabelas:

- use estrutura semântica apropriada;
- diferencie cabeçalhos e dados;
- preserve relações entre células;
- evite usar tabelas apenas para layout.

Conteúdo estruturado deve manter relações compreensíveis sem depender exclusivamente da posição visual.

## Ordem e estrutura do documento

A ordem visual deve, quando possível, corresponder à ordem lógica do conteúdo.

Verifique:

- headings;
- landmarks;
- sequência de leitura;
- ordem dos controles;
- relações entre títulos e seções.

Não altere a ordem semântica apenas para obter uma composição visual específica.

## Multimídia

Quando houver áudio ou vídeo, considere:

- controles acessíveis;
- legendas quando necessárias;
- alternativas textuais quando apropriadas;
- identificação do conteúdo;
- operação por teclado.

Não invente transcrições, legendas ou descrições que não estejam disponíveis.

## Diagnóstico antes da correção

Classifique o que foi encontrado antes de alterar.

Um achado pode ser:

- problema real;
- risco;
- melhoria recomendada;
- hipótese;
- limitação de teste.

Avalie também:

- severidade;
- impacto;
- frequência;
- contexto;
- evidência disponível.

Não trate todo alerta automatizado como falha crítica.

## Testes automatizados e manuais

Ferramentas automatizadas são úteis, mas não cobrem toda a experiência de acessibilidade.

Combine, conforme o risco:

- inspeção semântica;
- testes automatizados;
- navegação por teclado;
- inspeção de foco;
- zoom;
- contraste;
- testes com diferentes larguras;
- inspeção de nomes acessíveis;
- testes com tecnologias assistivas quando disponíveis.

Não declare acessibilidade completa apenas porque uma ferramenta automatizada não encontrou erros.

## Teste com leitor de tela

Quando apropriado, use um leitor de tela ou inspeção equivalente para verificar:

- ordem de leitura;
- nomes;
- estados;
- mensagens;
- navegação;
- relacionamentos.

O objetivo é observar a experiência, não apenas procurar atributos no código.

## Preservar decisões válidas

Não remova uma decisão de design apenas porque existe uma alternativa acessível diferente.

Procure adaptar a solução preservando:

- identidade;
- conteúdo;
- intenção;
- funcionamento.

Quando a decisão existente realmente impedir acessibilidade, explique o problema e proponha alternativas.

## Integração com outras Skills

Acione outras Skills quando necessário:

- \`senac-ui\` para decisões de interface;
- \`senac-testing\` para estratégia e execução de testes;
- \`senac-performance\` quando uma solução de acessibilidade tiver impacto mensurável no desempenho;
- \`senac-code-review\` para integração e priorização.

A integração não elimina as regras de governança de \`senac-vibe-coding\`.

## Estudante e aprendizagem

Quando o problema de acessibilidade tiver valor formativo, favoreça que o estudante:

- observe o problema;
- compreenda o impacto;
- teste a interface;
- compare alternativas;
- escolha uma solução;
- justifique a decisão;
- valide o resultado.

A IA pode ajudar na implementação autorizada, mas não deve transformar acessibilidade em uma caixa-preta.

## Critérios de conclusão

Dentro do escopo definido, uma tarefa de acessibilidade está concluída quando:

- problemas relevantes foram identificados;
- evidências foram reunidas;
- correções necessárias foram implementadas ou encaminhadas;
- teclado e foco foram considerados quando aplicáveis;
- semântica e nomes acessíveis foram considerados;
- contraste e uso de cor foram considerados;
- conteúdo não textual foi tratado adequadamente;
- formulários e componentes dinâmicos foram considerados;
- responsividade, zoom e movimento foram considerados quando aplicáveis;
- testes proporcionais ao risco foram realizados;
- regressões relevantes foram verificadas.

"Concluído" não significa conformidade absoluta ou perfeição.

## Checklist

- [ ] HTML nativo foi priorizado.
- [ ] ARIA é necessário e corresponde ao comportamento real.
- [ ] Navegação por teclado foi considerada.
- [ ] Foco é visível e previsível.
- [ ] Contraste foi considerado.
- [ ] Cor não é o único meio de transmitir informação.
- [ ] Controles possuem nomes acessíveis.
- [ ] Imagens foram classificadas por função.
- [ ] Formulários possuem rótulos e feedback adequados.
- [ ] Componentes dinâmicos comunicam mudanças relevantes.
- [ ] Menus e diálogos possuem comportamento adequado.
- [ ] Área de interação foi considerada.
- [ ] Zoom e responsividade foram considerados.
- [ ] Movimento reduzido foi considerado quando aplicável.
- [ ] Conteúdo é compreensível e consistente.
- [ ] Estrutura e ordem do documento são coerentes.
- [ ] Testes automatizados não foram tratados como prova suficiente.
- [ ] Testes manuais foram realizados quando necessários.
- [ ] O escopo e a autonomia foram respeitados.
- [ ] O estudante participou das decisões formativas quando aplicável.

## Regra de ouro

> **Acessibilidade não é um conjunto de atributos adicionados no final. É a garantia de que a interface e seu conteúdo possam ser percebidos, compreendidos e utilizados por mais pessoas, preservando o propósito e a identidade do projeto.**
