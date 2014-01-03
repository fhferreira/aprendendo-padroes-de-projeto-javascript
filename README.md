![logo](http://i.imgur.com/p52KGBW.png)

## Um livro de [Addy Osmani](http://twitter.com/addyosmani) - Volume 1.5.2

**Copyright © Addy Osmani 2012.**

**Livro Original:** http://addyosmani.com/resources/essentialjsdesignpatterns/book

**Tradução:** [Eric Oliveira](https://github.com/eoop/eo_op)


<br>
Aprendendo Padrões de Projeto Javascript é liberado pela [Creative Commons Attribution-Noncommercial-No Derivative Works 3.0.](http://creativecommons.org/licenses/by-nc-nd/3.0/) Está também disponível para compra via [O'Reilly](http://shop.oreilly.com/product/0636920025832.do) porém irá permanecer disponível gratuitamente online e como livro físico (ou digital) para compra de leitores que desejam apoiar o projeto.


# Prefácio

Padrões de projeto são soluções reutilizáveis para problemas que frequentemente ocorrem no desenvolvimento de softwares. Padrões estes com tópicos empolgantes e fascinantes a serem explorados em qualquer linguagem de programação.

Uma razão para isso é que eles nos ajudam a construir sobre a experiência combinada de vários desenvolvedores que vieram antes de nós, assegurando que estamos estruturando nosso código de forma otimizada, indo de encontro as necessidades dos problemas que estamos tentando resolver.

Padrões de projeto também nos fornece um vocabulário comum para descrever soluções. Isso pode ser muito mais simples que descrever sintaxe e semântica quando estivermos tentando transmitir uma maneira de estruturar uma solução em forma de código para outras pessoas.

Neste livro nós vamos explorar a aplicação de ambos padrões de pojeto, clássico e moderno, para programação JavaScript.



# Público Alvo

Este livro é destinado aos desenvolvedores profissionais que desejam melhorar seus conhecimentos sobre padrões de projeto e como eles podem ser aplicados na linguagem de programação JavaScript.

Alguns dos conceitos abordados (closures, herança prototípica) necessitam de um conhecimento e entendimento básico prévio. Se você se encontrar precisando de ler mais sobre alguns destes tópicos, uma lista de títulos sugeridos é fornecida por conveniência.

Se você deseja aprender como escrever um código bonito, estruturado e organizado, eu acredito que este livro é para você.



# Agradecimentos

Eu sempre vou ser grato pela talentosa revisão técnica que ajudou a melhorar este livro, incluindo a comunidade em geral. O conhecimento e entusiasmo que eles trouxeram foi simplesmente fantástico. Os tweets e blogs oficias dos revisores técnicos foram fontes regulares tanto para ideias como inspiração e eu recomendo de coração que vocês os chequem.

* [Nicholas Zakas](http://nczonline.net) @slicknet
* [Andrée Hansson](http://andreehansson.se), @peolanha
* [Luke Smith](http://lucassmith.name), @ls_n
* [Eric Ferraiuolo](http://ericf.me/), @ericf
* [Peter Michaux](http://michaux.ca), @petermichaux
* [Alex Sexton](http://alexsexton.com), @slexaxton

Eu também gostaria de agradecer a [Rebecca Murphey](http://rebeccamurphey.com), @rmurphey por fornecer inspiração para este livro e o mais importante, continuar a fazê-lo ambamente disponível no GitHub e via O'Reilly.

Finalmente, eu gostaria de agradecer minha maravilhosa esposa Ellie, por todo o suporte enquanto eu montava esta publicação.



# Créditos

Embora alguns dos padrões abordados no livro foram implementados baseados na experiência pessoal, muitos deles podem ser previamente identificados na comunidade JavaScript. Este trabalho é fruto da experiência combinada de inúmeros desenvolvedores. Similar a abordagem lógica de prevenir interrupções do texto com créditos (em Padrões Javascript), eu listei créditos e leituras recomendadas para todo conteúdo abordado, na seção de referências.

Se algum artigo ou link estiver faltando na lista de referências, por favor aceite minhas sinceras desculpas. Se você contatar-me eu irei atualizá-la e o incluir na lista.



# Leitura

Por este livro ser destinado a desenvolvedores iniciantes e intermediários, um entendimento básico dos fundamentos JavaScript é assumido. Caso você queira saber mais sobre a linguagem, fico feliz de recomendar os seguintes títulos:

* JavaScript: O guia definitivo por David Flanagan
* Eloquent JavaScript por Marijin Haverbeke
* Padrões JavaScript por Stoyan Stefanov
* Writing Maintainable JavaScript por Nicholas Zakas
* JavaScript: As melhores partes por Douglas Crockford



# Tabela de Conteúdo

* <a href="#01">↡</a> Introdução
* [O que é Padrão?](https://github.com/eoop/aprendendo-padroes-de-projeto-javascript#o-que-%C3%A9-um-padr%C3%A3o)
* [Teste de Padronicidade, Proto-padrões e A Regra dos Três](https://github.com/eoop/aprendendo-padroes-de-projeto-javascript#teste-de-padronicidade-proto-padr%C3%B5es-e-a-regra-dos-tr%C3%AAs)
* [A Estrutura de um Padrão de Projeto](https://github.com/eoop/aprendendo-padroes-de-projeto-javascript#a-estrutura-de-um-padr%C3%A3o-de-projeto)
* [Escrevendo Padrões de Projeto](https://github.com/eoop/aprendendo-padroes-de-projeto-javascript#escrevendo-padr%C3%B5es-de-projeto)
* [Anti-Padrões](https://github.com/eoop/aprendendo-padroes-de-projeto-javascript#anti-padr%C3%B5es)
* [Categorias de Padrão de Projeto](https://github.com/eoop/aprendendo-padroes-de-projeto-javascript#categorias-de-padr%C3%A3o-de-projeto)
* [Tabela-Resumo de Categorias de Padrão de Projeto](https://github.com/eoop/aprendendo-padroes-de-projeto-javascript#categoriza%C3%A7%C3%A3o-de-padr%C3%B5es-de-projeto)
* [Padrões de Projeto JavaScript]()
	* [Constructor Pattern (Padrão "Construtor")]()
	* [Revealing Module Pattern (Padrão "de Módulo")]()
	* [Module Pattern (Padrão "de Revelação de Módulo")]()
	* [Singleton Pattern (Padrão "Única Coisa")]()
	* [Observer Pattern (Padrão "Observador")]()
	* [Mediator Pattern (Padrão "Mediador")]()
	* [Prototype Pattern (Padrão "de Protótipo")]()
	* [Command Pattern (Padrão "de Comando")]()
	* [Facade Pattern (Padrão "de Fachada")]()
	* [Factory Pattern (Padrão "de Fábrica")]()
	* [Mixin Pattern (Padrão "Combinado")]()
	* [Decorator Pattern (Padrão "Decorador")]()
	* [Flyweight Pattern]()
* [Padrões JavaScript MV*]()
	* [Padrão MVC]()
	* [Padrão MVP]()
	* [Padrão MVVM]()
* [Padrões de Projeto Modernos de JavaScript Modular]()
	* [AMD]()
	* [CommonJS]()
	* [ES Harmony]()
* [Padrões de Projeto no jQuery]()
	* [Composite Pattern (Padrão "de Composição")]()
	* [Adapter Pattern (Padrão "de Adaptação")]()
	* [Facade Pattern (Padrão "de Fachada")]()
	* [Observer Pattern (Padrão "Observador")]()
	* [Iterator Pattern (Padrão "Iterador")]()
	* [Lazy Initialization Pattern (Padrão "de Inicialização Preguiçoso")]()
	* [Proxy Pattern (Padrão "Procurador")]()
	* [Builder Pattern (Padrão "Construtor")]()
* [Padrões de Projeto para plugin jQuery]()
* [Padrões de Namespacing JavaScript]()
* [Conclusões]()
* [Referências]()



<h1 id="01">◈ <span>Introdução</span></h1>

Um dos mais importantes aspectos de escrever código manutenível é se tornar capaz de notar partes recorrentes neste código e otimizá-los. Esta é uma área onde o conhecimento de padrões de projeto pode ser inestimável.

Na primeira parte do livro, nós vamos explorar a história e importância dos padrões de projeto que podem ser aplicados em qualquer linguagem de programação. Se você se sente familiar com esta história, sinta-se livre para pular para o capítulo "O que é um Padrão?" para continuar lendo.

Padrões de projeto nos leva aos trabalhos iniciais de um arquiteto chamado Christopher Alexander. Ele costumava escrever publicações sobre sua experiência na resolução de problemas de projeto e como eles se relacionam com construções e cidades. Um dia, ocorreu a Alexander que quando usado uma ou outra vez, certos padrões de projeto levam a um efeito ideal desejado.

Em colaboração com Sara Ishikawa e Murray Silverstein, Alexander produziu uma linguagem de projeto que permitia a qualquer um projetar e construir em qualquer escala. Isto foi publicado em 1977 em um artigo entitulado "A Pattern Language" (Uma Linguagem de Projeto), que mais tarde foi publicado como um livro.

Há cerca de 30 anos atrás, os engenheiros de software começaram a incorporar os princípios que Alexander escreveu na primeira documentação a respeito dos padrões de projeto, que se tornou um guia para desenvolvedores iniciantes que buscavam aperfeiçoar suas habilidades em codificar. É importante notar que os conceitos por trás dos padrões de projeto estavam em torno da indústria de programação desde a sua criação, embora fosse de forma menos formalizada.

Um dos primeiros e indiscutivelmente mais emblemático trabalho publicado em relação aos padrões de projeto na engenharia de software foi o livro lançado em 1995 chamado "Design Patterns: Elements of Reusable Object-Oriented Software" (Padrões de Projeto: Elementos de Reutilização de Softwares Orientados a Objetos). Este foi escrito por Erich Gamma, Richard Helm, Ralph Johnson e John Vlissides - um grupo que veio a ser conhecido como "Gang of Four" (Gangue dos Quatro, ou GoF para encurtar).

A publicação da GoF é considerada fundamental para o entendimento do conceito de padrões de projeto voltados a nossa área, descrevendo inúmeras técnicas de desenvolvimento e armadilhas, bem como o fornecimento de 23 núcleos de padrões de projeto orientados a objeto usados frequentemente nos dias de hoje. Nós vamos abordar estes padrões com mais detalhe na seção "Categorias de Padrões de Projeto".

Neste livro, iremos ver inúmeros padrões de projeto populares de JavaScript e explorar porque certos padrões são mais adequados para seus projetos que outros. Lembre-se que padrões podem ser aplicados não somente no vanilla JavaScript (i.e código JavaScript padrão), mas também pode ser abstraído para bibliotecas como jQuery e Dojo se desejado. Antes de iniciarmos, dê uma olhada na definição exata de "padrão" em projetos de software.




# O que é um Padrão?

Um padrão é uma solução reutilizável que pode ser aplicada nos problemas que frequentemente ocorrem nos projetos de software - no nosso caso - escrevendo aplicações web JavaScript. Outro meio de olhar para os padrões são como modelos de como nós podemos resolver problemas - sendo alguns possíveis de serem aplicados em diferentes situações.

Então, porque é importante entender os padrões e se tornar familiar com eles? Padrões de projeto tem 3 principais benefícios:

1. **Padrões são soluções comprovadas:** Eles fornecem abordagens para solucionar questões no desenvolvimento de software usando técnicas comprovadas que refletem a experiência e conhecimento dos desenvolvedores que ajudaram a definí-lo e torná-lo um padrão.

2. **Padrões podem ser facilmente reutilizados:** Um padrão usualmente reflete em uma solução "out of the box" (fora da caixa, além do comum) que pode ser adaptada para atender as nossas próprias necessidades. Essa característica faz com que os padrões sejam muito robustos.

3. **Padrões podem ser expressivos:** Quando nós olhamos para um padrão, ele geralmente é um conjunto de estruturas e vocabulários para a apresentação de uma solução que pode nos ajudar a expressar soluções extensas de uma forma muito elegante.

Padrões não são exatamente uma solução. É importante que lembremos que a função do padrão é meramente nos fornecer um esquema para a solução. Padrões não resolvem todos os problemas de projeto nem tampouco substituem bons projetistas de software, porém, eles **ajudam-os.** Vamos agora ver algumas outras vantagens que os padrões nos oferecem.

* **Padrões reutilizáveis ajudam a prevenir pequenos problemas que podem causar grandes problemas no processo de desenvolvimento da aplicação.** Isso significa que quando o código é feito sobre padrões comprovados, nós podemos nos dar ao luxo de gastar menos tempo se preocupando com a estrutura do nosso código, e focar na qualidade da solução em geral. Isto porque os padrões nos encorajam a programar de forma mais estruturada e de modo organizado evitando a necessidade de refatorar nosso código para fins de limpeza no futuro.

* **Padrões podem fornecer soluções generalizadas, que são documentadas de uma forma onde o mesmo não seja vinculado a um problema em específico.** Esta abordagem geral significa que independentemente da aplicação (e em vários casos da linguagem de programação) que estamos trabalhando, os padrões de projeto podem ser aplicados para a melhoria da estrutura do nosso código.

* **Certos padrões podem efetivamente diminuir o tamanho do arquivo do nosso código evitando repetição.** Encorajando aos desenvolvedores a olhar mais atentamente para suas soluções nas áreas onde uma redução instantânea na repetição pode ser feita, e.g. (exempli gratia = por exemplo) reduzindo o número de funções que realizam processos similares em favor de uma função geral única, o tamanho total do nosso código base pode ser diminuído. Isso também é conhecido como 'fazer seu código mais DRY'. DRY = Don't repeat yourself (não repita a si mesmo).

* **Padrões adicionam aos desenvolvedores vocabulário, o qual permite uma comunicação mais rápida.**

* **Padrões usados frequentemente podem ser melhorados com o tempo, através das experiências de outros desenvolvedores que usam e contribuem com a comunidade de padrões de projeto.** Em alguns casos isto leva a criação de padrões inteiramente novos, embora em outros, tenhamos uma melhoria das diretrizes de quão específico e como o padrão pode ser melhor usado. Isto pode garantir que a base da solução do padrão continue sendo mais robusta que uma solução "ad-hoc" pode ser. (ad-hoc = é uma expressão latina cuja tradução literal é "para isto" ou "para esta finalidade")

### Nós já Usamos Padrões todos os dias

Para entender o quão útil os padrões podem ser, vamos revisar um simples problema de seleção de elementos que a biblioteca jQuery resolve para nós.

Imagine que temos um script onde para cada elemento DOM encontrado na página com a classe "foo", nós desejamos incrementar um contador. Qual o meio mais eficiente de consultar esta coleção de elementos? Bem, temos algumas diferentes formas para que este problema seja combatido:

1. Selecione todos os elementos na página e então armazene as referências a eles. Depois, filtre esta coleção e use expressões regulares (ou outras formas) para somente armazenar aqueles que contém a classe "foo".

2. Use um recurso nativo dos navegadores modernos tal como `querySelectorAll()` para selecionar todos os elementos com a classe 'foo'.

3. Use um recurso nativo como `getElementsByClassName()` para pegar a coleção desejada similarmente.

Então, qual destas opções é a mais rápida? Atualmente é a opção 3, de 8 a 10 vezes mais rápida. Veja os [teste](http://jsperf.com/getelementsbyclassname-vs-queryselectorall/59). Em um mundo real das aplicações, porém, a opção 3 não irá funcionar em versões abaixo do Internet Explorer 9 sendo assim necessário usar a primeira opção, pois a segunda e terceira não são suportadas.

Desenvolvedores usando jQuery não precisam se preocupar com este problema, pois felizmente ele é abstraído usando o Padrão Façade. Nos iremos revisá-lo futuramente com mais detalhes. Este padrão proporciona um simples conjunto de interfaces abstratas (e.g `$el.css()`, `$el.animate()`) para muitos outros corpos de código subjacentes mais complexos.

Nos bastidores, a biblioteca simplesmente opta pela abordagem mais otimizada para selecionar elementos dependendo de qual nosso navegador atual e nós somente consumimos a camada de abstração.

Nós todos estamos, provavelmente, acostumados também com o `$("selector")` do jQuery. Isto é significantemente mais fácil de usar para selecionar elementos HTML na página do que ter que lidar manualmente para optar por `getElementById()`, `getElementsByClassName()`, `getElementByTagName()` e assim por diante.

Embora saibamos que querySelectorAll() tenta resolver este problema, compare o esforço envolvido na utilização de interfaces de fachada do jQuery contra selecionar o caminho ideal nós mesmos. Não há contestação! Abstrações usando padrões podem oferecer valores do mundo real.

Nós vamos ver este e mais padrões de projeto mais tarde neste livro.



# Teste de Padronicidade, Proto-padrões e A Regra dos Três 

Lembre-se que nem todo algoritmo, melhores práticas ou solução representa o que pode ser considerado um padrão completo. Pode haver ingredientes aqui que foram perdidos e a comunidade de padrões é geralmente cautelosa em dizer que há um padrão específico para algo a menos que ele seja fortemente comprovado e testado. Mesmo que algo nos seja apresentado como um padrão e pareça satisfazer os critérios para assim ser denominado, ele não deve ser considerado um padrão até que passe por um períodos de testes e exames minunciosos.

Olhe novamente para o trabalho de Alexander, ele afirma que um padrão deve ser um processo e uma "coisa". Essa definição é coerente com o que ele seguia por dizer que o processo deve ser criar a "coisa". Esta é a razão pela qual os padrões geralmente focam em direcionar uma identidade estrutural da estrutura, i.e. nós devemos ser capazes de descrever visualmente (ou desenhar) uma figura representando a estrutura que retrata o padrão de uma forma prática.

Estudando padrões de projeto, não é incomum depararmos com o termo "proto-padrão" (proto-pattern). O que é isso? Bem, um padrão que ainda não passou por todos os testes necessários é usualmente referido como um proto-padrão. Eles podem ser resultados do trabalho de alguém que tenha demonstrado uma solução particular que seja digna de compartilhamento com a comunidade, porém ainda não tivera a oportunidade de ser examinado minunciosamente por causa de ser algo muito recente.

Alternativamente, o(s) indivíduo(s) que compartilham o padrão podem não ter tempo ou interesse em ingressar no processo de "padronização" e soltam uma pequena descrição de seu proto-padrão ao invés disso. Breves descrições ou fragmentos deste padrão são conhecidos como 'patlets'.

O trabalho envolvido em uma documentação completad para qualificação de um padrão pode ser muito assustador. Olhando para alguns dos mais recentes trabalhos no campo dos padrões de projeto, um padrão pode ser considerado "bom" se seguir as seguintes condições:

**Resolva um problema em particular:** Padrões não devem apenas capturar princípios ou estratégias. Eles precisam de capturar soluções. Este é um dos mais essenciais ingredientes para um bom padrão.
**A solução para esse padrão não deve ser óbvia:** Podemos achar que as técnicas de resolução de problemas frequentemente tentam derivar os mesmos para uma solução baseada em um conhecimento inicial. Os melhores padrões de projeto usualmente fornecem soluções para os problemas indiretamente - isto é considerado uma abordagem necessária para os maiores problemas relacionados aos padrões.

**O conceito descrito deve ter sido comprovado:** Padrões de projeto requerem provas que suas funções descritas e sem estas provas o padrão não podem ser considerado seriamente. Se um padrão é de natureza altamente especulativa, somente os corajosos podem tentar usá-lo.

**Deve descrever um relacionamento:** Em alguns casos, isso pode parecer um padrão que descreve um módulo. Embora a implementação possa se parecer com essa forma, a descrição oficial do padrão deve dizer muito mais a fundo suas estruturas e seus mecanismos que explicam sua relação com o código. 

Poderíamos pensar que um proto-padrão que não cumpra este guia não valha a pena ser aprendido, porém, isso estaria longe de ser verdade. Vários proto-padrões são muito bons. Eu não estou dizendo que todos os proto-padrões devem ser vistos, mas existem alguns que nos podem ser úteis em projetos futuros. Use bom senso com a lista acima em mente e você irá ficar bem no seu processo de seleção.

Um dos requisitos adicionais para um padrão ser válido é que ele deve mostrar alguns fenômenos recorrentes. Isto é frequentemente algo que pode ser qualificado em pelo menos 3 áreas chave, referenciadas como * A regra dos Três*. Para mostrar recorrência usando esta regra, temos esta demonstração:

1. **Aptidão do propósito** - O quão bem sucedido é considerado este padrão?
2. **Utilidade** - Por que este padrão é considerado bem sucedido?
3. **Aplicabilidade** - O projeto é digno de ser um padrão, por ter uma aplicabilidade mais ampla? Caso seja, isso deve ser explicado. Ao rever ou definir um padrão, é importante manter o que foi dito acima em mente.

# A Estrutura de um Padrão de Projeto	

Você deve estar curioso sobre como um autor de padrão aborda a estrutura definida, a implementação e o propósito de um novo padrão. Um padrão é inicialmente apresentado na forma de uma regra que estabelece uma relação entre:

* Um contexto
* Um sistema de forças que surge neste contexto e
* Uma configuração que permite que estas forças resolvam por si mesmo o contexto

Com isto em mente, vamos agora olhar o sumário dos elementos componentes de um padrão de projeto. Um padrão de projeto deve ter:

* **Nome do padrão** e uma **descrição**.
* **Esboço do contexto** - o contexto em que o padrão é efetivo em responder a necessiade dos usuários.
* **Declaração do problema** - uma definição do problema a ser tratado para que possamos entender a intenção do padrão.
* **Solução** - uma descrição de como os problemas dos usuários vão ser resolvidos em uma lista compreensível de passos e percepções.
* **Projeto** - uma descrição do padrão do projeto e em particular, o comportamento do usuário em interagir com o mesmo.
* **Implementação** - um guia de como o padrão pode ser implementado.
* **Ilustrações** - uma representação visual das classes no padrão. (e.g. um diagrama)
* **Exemplos** - uma implementação do padrão em uma forma mínima.
* **Co-requisitos** - outros padrões são necessários para o dar suporte ao uso do padrão descrito?  
* **Relações** - Quais outros padrões que este se assemelha? Ele imita algum outro?
* **Uso Conhecido** - o padrão está sendo usado *na natureza*? Se sim, onde e como?
* **Discussões** - os pensamentos da equipe ou do autor dizendo emocionantemente os benefícios do padrão

Padrões de projeto são uma abordagem bastante poderosa para se ter todos os desenvolvedores em uma organização na mesma página quando estiverem criando ou mantendo soluções. Se considerando trabalhando em um padrão por si mesmo, lembre-se que embora ele parece ter um alto custo inicial no planejamento e fases seguintes, o valor recebido deste investimento é muito recompensador. Sempre pesquise a fundo antes de trabalhar em novos padrões, pois você sabe que é mais benéfico usar ou construir em cima de padrões consolidados do que começar do zero.

# Escrevendo Padrões de Projeto

Embora este livro destina-se aos novos padrões de projeto, um entendimento básico de como um padrão de projetos é escrito pode oferecer alguns úteis benefícios. Para começar, nós podemos aprofundar na apreciação do raciocínio por trás do motivo da necessidade do padrão. Nós podemos também aprender como dizer se um padrão (ou proto-padrão) é erguido do zero quando os revisamos para nossas próprias necessidades.

Escrever bons padrões é uma tarefa desafiadora. Padrões não precisam somente de (idealmente) fornecer uma quantia substancial de referências para os usuários finais, eles também precisam ser capazes de defender porque são necessários.

Tendo lido a seção anterior sobre o quê um padrão é, nós podemos pensar que isso por si só é o suficiente para nos ajudar a identificar os padrões que vemos no dia a dia. Isso não é completamente verdade. Não está sempre claro se um pedaçõ de código que estamos olhando está seguindo um padrão ou acidentalmente se parece com o que ele faz.

Quando nós olhamos para um corpo de códgo nós pensamos que podemos usar um padrão, nós precisamos considerar escrever do início alguns dos aspectos do código que acreditamos falhar em uma particularidade existente do padrão ou conjunto de padrões.

Em vários casos de análise de padrões, nós podemos achar que estamos apenas olhando para um código que segue bons princípios e práticas de design que podem ajudar no que poderia sobrepor às regras de um padrão por acidente. Lembre-se - soluções em que nem interações nem regras definidas aparecem não são padrões.

Se estiver interessado em escrever seus próprio padrão de projeto eu recomendo que você aprenda com outros que já tenham passado pelo processo e feito isso corretamente. Despenda tempo absorvendo a informação de várias descrições padrões de projeto diferentes e pegue o que for significativo para você.

Explore a estrutura e a semântica - isto pode ser feito examinando as interações e o contexto dos padrões que você esteja interessado, então você pode identificar os princípios que assistem de forma organizada estes padrões conjuntos com configurações úteis.

Uma vez que nós expomos a riqueza da informação da literatura do padrão, nós podemos desejar começar a escrever nosso padrão usando um formato *existente* e vendo se nós podemos ter novas ideias para melhorá-lo ou integrar nossas ideias nele.

Um exemplo de um desenvolvedor que fez isso recentemente é Christian Heilmann, quem pegou o existente *Module pattern* e fez algumas mudanças fundamentais úteis para criar o *Revealing Module pattern* (este é um dos padrões discutidos posteriormente neste livro).

As perguntas seguintes são minhas sugestões se você tiver interesse em criar um novo padrão de projeto:

* **Quão prático é o padrão?:** Verifique se o padrão descreve soluções comprovadas para problemas recorrentes, e não apenas soluções especulativas que não foram qualificadas.
* **Mantenha boas práticas em mente:** As decisões de projeto que tomamos devem ser baseadas nos princípios de onde derivamos, entendendo das melhores práticas.
* **Nossos padrões de projeto devem ser transparentes para o usuário:** Padrões de projeto devem ser inteiramente transparentes para qualquer tipo de usuário. Eles lá principalmente para servir os desenvolvedores que forem usá-los e não devem forçar mudanças de comportamento na experiência do usuário, que não seriam incorridos sem o uso de um padrão.

* **Lembre-se que originalidade NÃO é fundamental em um padrão de projeto:** Quando escrevemos um padrão, nós não precisamos de ser o descobridor original das soluções que estão sendo documentadas nem precisamos nos preocupar se o nosso projeto coincide com pedaços menores de outros padrões. Se a abordagem é forte o suficiente para ter ampla e útil aplicabilidade, o padrão tem chance de ser reconhecido como um padrão válido.

* **Padrões precisam de um forte grupo de exemplos:** Uma boa descrição de um padrão precisa ser seguida por um igualmente bom número de exemplos demonstrando o sucesso da aplicação do padrão em questão. Para mostrar o amplo uso, exemplos que exibem bons princípios de projeto são ideais.

Escrever um padrão é um cuidadoso balanço entre a criação de um projeto que é geral, específico e sobre tudo, útil. Tente assegurar-se de quando for escrever um padrão você cubra aamplamente as possíveis áreas e você se sairá bem. Eu espero que esta breve introdução de como escrever padrões tenha dado a você alguns *insights* que vão ajudá-lo no processo de aprendizado para as próximas seções deste livro.

# Anti-padrões

Se nós considerarmos que um padrão representa uma boa prática, um anti-padrão representa uma lição que foi aprendida. O termo anti-padrão foi cunhado em 1995 por Andrew Koenig no *November C++ Report* daquele ano, inspirado pelo livro GoF's *Design Patterns*. No artigo do Koenig, temos duas notações de anti-padrões representadas. Anti-padrões:

* Descrevem uma má solução para um problema particular que resulta em uma situação ruim ocorrida
* Descrevem como sair da situação citada e como ir para uma boa solução

Neste tópico, Alexander escreve sobre as dificuldades de alcançar um bom balanço entre uma boa estrutura de projeto e um bom contexto:

> Estas notas são sobre os processos de projeto; o processo de inventar coisas físicas que mostram uma nova ordem física, organização, forma, em resposta à função... todo problema do projeto começa com um esforço para conseguir a aptidão entre duas entidades: a forma em questão e o contexto. A forma é a solução do problema; o contexto define o problema.

Embora seja muit importante estar ciente de padrões de projeto, pode ser igualmente importante entender de anti-padrões. Vamos qualificar a razão por trás disso. Quando criamos uma aplicação, um ciclo de vida de um projeto começa com a construção, no entanto uma vez que você tem a versão inicial feita, ela precisa ser mantida. A qualidade de uma solução final vai ser boa ou ruim, dependendo do nível de habilidade e o tempo que o time investiu nesta. Aqui *bom* e *ruim* são considerados no contexto - um projeto "perfeito" deve qualificar como um anti-padrão se aplicado no contexto errado.

Os maiores desafios acontecem depois que uma aplicação atingiu a produção e está pronta para entrar em modo de manutenção. Um desenvolvedor trabalhando em um sistema desse tipo, que não trabalhou no aplicativo antes pode introduzir uma solução ruim para este projeto por acidente. Se *más* práticas forem criadas como anti-padrões, elas permitem aos desenvolvedores uma maneira de reconhecê-las com antecedência, para que possam evitar os erros mais comuns que possam aparecer - está uma forma paralela na qual os padrões de projeto nos fornecem um meio para reconhecer técnicas comuns que são úteis.

Para resumir, um anti-padrão é um projeto ruim que é válido para documentação. Exemplos de anti-padrões em JavaScript são os seguintes:

* Poluir o namespace global definindo um grande número de variáveis no contexto global.
* Passar strings em vez de funções, quer seja com setTimeout ou setInterval, desencadeando o uso de `eval()` internamente.
* Modificar a classe prototípica `Object` (isto é particularmente um ruim anti-padrão).
* Usar JavaScript de forma *inline* pois está é inflexível.
* O uso de `document.write` onde temos alternativas DOM nativas como `document.createElement` mais apropriadas. `document.write` tem sido grosseiramente mal utilizado ao longo dos anos e tem algumas desvantagens incluindo que se ele é executado depois que a página foi carregada, ele pode realmente subtituir a página que está, enquanto `document.createElement` não. Nós podemos ver [aqui](http://jsfiddle.net/addyosmani/6T9vX/) para um exemplo real desta ação. Ele também não funciona com XHTML que é outra razão de optar por métodos mais amigáveis ao DOM como `document.createElement` que é favorável.

Conhecer os anti-padrões é crítico para o sucesso. Uma vez que estivermos aptos a reconhecê-los, estaremos aptos a refatorar nosso código para negá-los, de modo que a qualidade global das nossas soluções melhorarão instantaneamente.

# Categorias de Padrão de Projeto

Um glossário do livro conhecido de projetos, *Domain-Driven Terms*, afirma com razão que:

> "Um padrão de projeto nomeia, abstra e identifica os aspectos de uma comum estrutura de projeto que faz isto útil para criação e reutilização de projetos orientados a objeto. O padrão de projeto identifica as classes participantes e suas instâncias, suas funções e colaborações, e a distribuição de responsabilidades.

> Cada padrão de projeto foca em um problema ou questão particular de projetos orientados a objetos. Ele descreve quando se aplica, ou não pode ser aplicado em vista de outras restrições de projeto, e as consequências e os compromissos de se usá-lo. Desde que nós eventualmente implementemos nossos padrões, um padrão de projeto também fornece código de exemplo para ilustrar uma implementação.

> Embora padrões de projeto descrevam padrões orientado a objetos, eles são baseados em soluções práticas que devem ser implementadas em linguagens de programação orientada a objetos tradicionais..."

Padrões de projeto pode ser divididos em um número de diferentes categorias. Nesta seção vamos revisar 3 destas categorias e mencionar brevemente alguns exemplos de padrões que caem nestas categorias antes de explorar especificamente alguns com maiores detalhes.

### Padrões de projetos Criacionais

Padrões de projetos Criacionais focam em lidar com os mecanismos de criação de objetos onde os objetos são criados de maneira adequada para a situação que estamos trabalhando. A abordagem básica para criação de objeto pode legar a adicionar complexidade ao projeto, enquanto esses padrões têm como objetivo resolver problemas através do controle do processo de criação.

Alguns padrões que se encaixam nesta categoria são: Constructor, Factory, Abstract, Prototype, Singleton e Builder.

### Padrões de Projetos Estruturais

Padrões de projetos estruturais estão preocupados com composição de objetos e, normalmente, identificar maneiras simples de realizar as relações entre diferentes objetos. Eles ajudam a assegurar que quando uma parte do sistema muda, toda a estrutura do sistema não precisa fazer o mesmo. Eles também auxiliam na reformulação de partes do sistema que não encaixam em uma proposta particular dentro do que eles fazem.

Padrões que entram nesta categoria: Decorator, Facade, Flyweight, Adapter e Proxy.

### Padrões de projetos Comportamentais

Padrões de projetos comportamentais focam em melhorar ou simplificar a comunicação entre os objetos díspares em um sistema.

Alguns padrões comportamentais são: Iterator, Mediator, Observer e Visitor.

# Categorização de Padrões de Projeto

Em minhas primeiras experiências de aprendizado sobre padrões de projeto, eu encontrei a tabela a seguir um lembrete muito útil do que uma série de padrões tem a oferecer - ela cobre os 23 padrões de projeto mencionados pela GoF. A tabela original foi resumida por Elyse Nielsen em 2004 e eu a modifiquei onde foi necessário de acordo com nossa discussão nessa seção do livro.

Eu recomendo usar esta tabela como referência, mas lembre-se que existem padrões adicionais que não foram mencionados aqui mas vão ser discutidos depois no livro.

### Uma breve nota sobre as classes

Tenha em mente que haverá padrões nesta tabela que fazem referência ao conceito de "classes". JavaScript é uma linguagem sem classes, entretanto classes podem ser simuladas usando funções.

A abordagem mais comum para conseguir isto é definindo uma função JavaScript onde nós então criamos um objeto usando a palavra-chave `new`. `this` pode ser usado para ajudar a definir novas propriedades e métodos para o objeto como no exemplo seguinte:

<pre>
<code>
// Uma "classe" carro
function Car ( model ) {
	
	this.model = model;
	this.color = "silver";
	this.year  = "2012";

	this.getInfo = function () {
		return this.model + " " + this.year;
	};
}	
</code>
</pre>

Nós podemos então instanciar o objeto usando o construtor Car que definimos acima:

<pre>
<code>
var myCar = new Car("ford");

myCar.year = "2010";

console.log( myCar.getInfo() );
</code>
</pre>

Para mais formas de definir "classes" usando JavaScript, veja [este](http://www.phpied.com/3-ways-to-define-a-javascript-class/) útil post de Stoyan Stefanov.

Vamos agora analisar a tabela.

### Criacional

|Criacional|Baseada no conceito de criar um objeto.|
| :-------------: |:-------------:|
| **Classe** |
| Método Factory | Faz uma instância de diversas classes derivadas baseadas em dados ou eventos interligados. |
| **Objeto** |
| Factory Abstrata | Cria uma instância de diversas famílias de classes sem detalhar classes concretas. |
| Builder | Separa a construção de objetos de sua representação, sempre criando o mesmo tipo de objeto. |
| Prototype | Uma inicialização completa usada para copiar ou clonar. |
| Singleton | Uma classe com somente uma instância com pontos de acesso global. |


### Estrutural

|Estrutural|Baseada na ideia de construir blocos de objetos.|
| :-------------: |:-------------:|
| **Classe** |  |
| Adapter | Liga interfaces de diferentes classes, portanto as classes podem trabalhar juntas apesar das incompatibilidades das interfaces |
|**Objeto**||
|Adapter|Liga interfaces de diferentes classes, portanto as classes podem trabalhar juntas apesar das incompatibilidades das interfaces|
|Bridge|Separa uma interface de objeto a partir de sua implementação, assim os dois podem variar independentemente|
|Composite|Uma estrutura dos objetos simples e compostos que torna o objeto total mais que a soma de suas partes.|
|Decorator|Adiciona dinâmicamente processamento alternativo para objetos.|
|Facade|Uma única classe que esconde a complexidade de todo subsistema.|
|Flyweight|Um exemplo refinado usado para o compartilhamento eficiente de informações que estão contidas em outro lugar.|
|Proxy|Um objeto de espaço reservado que representa o verdadeiro objeto.|


### Comportamental

|Comportamental|Baseado na forma como os objetos desempenham e trabalham em conjunto.|
| :-------------: |:-------------:|
|**Classe**||
|Interpreter|Uma forma de incluir elementos da linguagem em um aplicativo para coincidir com a gramática da língua pretendida.|
|Template Método|Cria o *shell* de um algoritmo em um método, em seguida, adia as etapas exatas para uma subclasse. |
|**Objeto**||
|Chain of Responsibility|Uma forma de passar uma requisição entre uma cadeia de objetos para encontrar o objeto que pode manipular a requisição.|
|Command|Encapsula uma requisição de comando como um objeto para permitir, login ou fila de pedidos, e fornece tratamento de erros para os pedidos não tratados.|
|Iterator|Acessa sequencialmente os elementos de uma coleção sem conhecer o funcionamento interno da coleção.|
|Mediator|Define simples comunicações entre classes para prevenir um grupo de classes de se referir explicitamente uma a outra.|
|Memento|Captura o estado interno de um objeto para poder restaurá-lo mais tarde.|
|Observer|Uma forma de notificar a mudança para um número de classes para assegurar a consistência entre as classes.|
|State|Altera o comportamento do objeto quando seu estado muda.|
|Strategy|Encapsula um algoritmo dentro de uma classe separano a seleção a partir da implementação.|
|Visitor|Adiciona uma nova operação para uma classe sem mudar a classe.|


# Padrões de Projeto JavaScript

Nesta seção, vamos explorar implementações JavaScript de uma série de ambos os padrões de projetos, clássicos e modernos.

Desenvolvedores normalmente se perguntam se existe um padrão *ideal* ou conjunto de padrões que eles devem usar em seu *workflow*. Não uma única reposta verdadeira para essa questão. cada script e aplicação web que trabalhamos tem suas necessidades individuais e nós precisamos pensar e sentir onde um padrão pode oferecer um valor real para uma implementação.

Por exemplo, alguns projetos podem beneficiar das vantagens oferecidas pela dissociação do padrão *Observer* (que reduz quão dependente as partes da aplicação são da outra) enquanto outros podem simplesmente ser bem pequenos para uma dissociação ser algo a se preocupar.

