# Respostas dos Exercícios: Evolução das Linguagens de Programação
**Referência:** Robert Sebesta — *Conceitos de Linguagens de Programação* (Capítulo 2)

---

### Questão 1
**Enunciado:** A genealogia das linguagens não é uma escada de progresso. Explique essa afirmação e apresente dois fatores históricos que fazem uma linguagem influenciar outra sem necessariamente substituí-la.

**Resposta:**
Dizer que a genealogia das linguagens não é uma "escada de progresso" significa que a história da computação não funciona como uma linha reta onde cada linguagem nova apaga ou é necessariamente melhor que a anterior. Em vez de substituição, o que acontece é uma divisão de nichos: as linguagens antigas continuam firmes onde funcionam bem, enquanto as novas surgem para atender a outras necessidades.

Dois fatores que mostram essa influência sem substituição:
* **Custo do código legado:** Reescrever sistemas gigantescos e críticos (como sistemas bancários em COBOL ou cálculos físicos em Fortran) custa muito caro e traz alto risco. Por isso, a linguagem original continua ativa e influenciando as novas.
* **Foco e objetivos diferentes:** Cada linguagem é pensada para resolver um problema específico. Uma linguagem nova pode pegar conceitos emprestados de uma clássica (como pegar ideias funcionais de Lisp), mas a pioneira continua sendo a mais adequada para o seu propósito original.

---

### Questão 2
**Enunciado:** Plankalkül não foi implementada em sua época. Ainda assim, por que ela é relevante para a história das linguagens? Cite três recursos antecipados por seu projeto e explique o valor de um deles.

**Resposta:**
A Plankalkül, criada por Konrad Zuse entre 1943 e 1945, é fundamental porque foi a primeira linguagem de programação de alto nível já proposta. Mesmo sem ter sido implementada na época, ela provou teoricamente que dava para programar de forma abstrata sem depender diretamente da arquitetura física do computador.

Três recursos antecipados por ela:
* Estruturas de dados complexas (arrays e tipos compostos semelhantes a registros/structs).
* Estruturas de repetição e condições lógicas bem definidas.
* Notação formal para tipos de dados (bits, inteiros e ponto flutuante).

Sobre o valor das estruturas de dados: ter tipos heterogêneos/registros permitiu agrupar dados relacionados em um único bloco lógico. Isso tirou o foco do programador de gerenciar endereços brutos de memória e abriu caminho para os tipos abstratos de dados e classes que usamos hoje.

---

### Questão 3
**Enunciado:** Compare Short Code, Speedcoding e os sistemas A-0/A-1/A-2 quanto ao problema enfrentado e à estratégia adotada. Por que chamá-los simplesmente de compiladores modernos seria impreciso?

**Resposta:**
O problema comum enfrentado por todos eles era a extrema dificuldade de programar diretamente em código de máquina puro (binário/octal), que era um processo demorado, propenso a falhas e sem suporte nativo das máquinas para operações de ponto flutuante.

Quanto às estratégias adotadas:
* O **Short Code** interpretava expressões matemáticas linha por linha durante a execução.
* O **Speedcoding** funcionava como um interpretador que simulava uma máquina virtual para facilitar operações numéricas e índices, sacrificando velocidade.
* Os **sistemas A-0, A-1 e A-2** de Grace Hopper eram sistemas de pseudocódigo que expandiam macros e juntavam rotinas prontas guardadas em fita magnética para montar o programa final.

Chamar essas ferramentas de compiladores modernos seria impreciso porque elas não faziam uma análise léxica, sintática e semântica completa a partir de gramáticas formais, tampouco geravam código de máquina otimizado. Eram basicamente interpretadores primitivos ou sistemas de junção e expansão de macros.

---

### Questão 4
**Enunciado:** Explique por que o projeto Fortran precisou convencer programadores de que código traduzido podia competir com código de máquina escrito à mão. Relacione desempenho, custo de programação e adoção.

**Resposta:**
Nos anos 1950, o aluguel dos computadores custava uma fortuna por hora e os programadores tinham receio de que uma linguagem de alto nível gerasse código lento e ineficiente, desperdiçando o investimento no hardware.

Por conta disso, a equipe do Fortran concentrou quase todo o esforço em construir um otimizador de código extremamente eficiente. Quando conseguiram demonstrar que o compilador gerava código quase tão rápido quanto o feito à mão em assembly, a resistência caiu por terra. A produtividade aumentou muito, o custo de desenvolvimento despencou e o Fortran foi rapidamente adotado como o primeiro grande padrão para a computação científica.

---

### Questão 5
**Enunciado:** Lisp surgiu em um contexto diferente de Fortran. Compare os domínios, a representação de dados e o estilo de computação favorecido pelas duas linguagens.

**Resposta:**
Enquanto o Fortran nasceu voltado para o cálculo numérico e científico de alta performance, o Lisp foi criado para o campo da Inteligência Artificial e a manipulação de símbolos e lógica formal.

Em relação aos dados, o Fortran trabalha principalmente com números primitivos (inteiros e ponto flutuante) e matrizes homogêneas, enquanto o Lisp organiza tudo em listas encadeadas dinâmicas e heterogêneas (*S-expressions*).

No estilo de computação, o Fortran segue o paradigma imperativo, focado em passos sequenciais, variáveis mutáveis e laços iterativos. Já o Lisp adota o paradigma funcional, baseando-se na avaliação de expressões matemáticas e chamadas de funções recursivas, evitando efeitos colaterais.

---

### Questão 6
**Enunciado:** Avalie três contribuições de ALGOL 60 que ultrapassaram sua adoção comercial. Por que uma linguagem pode ser muito influente sem dominar o mercado?

**Resposta:**
Três grandes contribuições do ALGOL 60:
* **Estrutura de blocos e escopo local:** A ideia de poder declarar variáveis válidas apenas dentro de blocos delimitados (`begin ... end`).
* **Suporte nativo à recursão:** Funções que chamam a si mesmas, o que exigiu a criação de pilhas de execução dinâmica na memória.
* **Formalização por BNF (Backus-Naur Form):** Primeira linguagem a ter sua gramática descrita formalmente, servindo de base para a teoria dos compiladores.

O ALGOL 60 não dominou comercialmente porque não possuía suporte nativo padronizado para operações de entrada e saída (I/O) e não teve o apoio da IBM, que preferiu investir no Fortran. Mesmo assim, foi extremamente influente porque quase todas as linguagens estruturadas modernas (como Pascal, C e Java) foram construídas com base nos conceitos que ela introduziu.

---

### Questão 7
**Enunciado:** COBOL foi desenhada para processamento comercial. Mostre como domínio e público influenciaram sua legibilidade, seus registros e sua relação com FLOW-MATIC.

**Resposta:**
O COBOL foi pensado para o ambiente corporativo e tinha como público gerentes e auditores que precisavam entender a lógica das regras de negócio. Por isso, a sintaxe foi feita para se parecer com frases em inglês, como no comando `ADD B TO C GIVING D`.

Para atender ao processamento de cadastros e folhas de pagamento, a linguagem introduziu o formato de registros hierárquicos (usando níveis numéricos como `01 CLIENTE`, `05 NOME`), separando a descrição dos dados da lógica dos procedimentos.

Essa abordagem veio diretamente do FLOW-MATIC, projeto pioneiro de Grace Hopper que já utilizava palavras em inglês e serviu de protótipo prático para a criação do COBOL.

---

### Questão 8
**Enunciado:** Compare Basic e PL/I como respostas ao desejo de ampliar o acesso ou o alcance da programação. Qual compromisso de projeto aparece em cada caso?

**Resposta:**
O BASIC e o PL/I tentaram expandir o uso da programação nos anos 1960 com caminhos bem diferentes:

* O **BASIC** buscou facilitar o **acesso** à computação para estudantes e iniciantes em terminais compartilhados. O compromisso de projeto foi priorizar a extrema simplicidade e o aprendizado rápido, deixando de lado o rigor sintático, a tipagem forte e a velocidade de execução.
* O **PL/I** tentou ampliar o **alcance** da programação ao criar uma linguagem unificada que servisse tanto para ciência quanto para comércio e sistemas. O compromisso de projeto foi abraçar a generalidade e colocar o máximo de recursos possíveis, o que tornou a linguagem muito complexa, difícil de implementar e cheia de comportamentos confusos.

---

### Questão 9
**Enunciado:** APL, SNOBOL e SIMULA 67 seguiram direções distintas. Associe cada linguagem ao seu foco e identifique uma contribuição duradoura de cada uma.

**Resposta:**
* **APL:** Focou em cálculo matemático conciso e operações com matrizes e vetores. Sua contribuição duradoura foi o processamento orientado a arranjos, que serviu de base para ferramentas modernas como MATLAB, R e a biblioteca NumPy em Python.
* **SNOBOL:** Focou na manipulação de texto e strings. Sua grande contribuição foi o mecanismo de busca por padrões (*pattern matching*) com retrocesso (*backtracking*), conceito que originou as Expressões Regulares modernas.
* **SIMULA 67:** Focou na simulação de eventos discretos e processos concorrentes. Sua contribuição definitiva foi a criação dos conceitos de classes, objetos e herança, dando origem a todo o paradigma da Programação Orientada a Objetos.

---

### Questão 10
**Enunciado:** Defina ortogonalidade no projeto de linguagens e use ALGOL 68 para discutir a diferença entre regularidade e simplicidade. Uma linguagem muito ortogonal é automaticamente fácil de usar?

**Resposta:**
Ortogonalidade é a característica de uma linguagem onde um conjunto pequeno de comandos e tipos primitivos pode ser combinado livremente, de maneira uniforme e sem restrições ou exceções dependendo do contexto.

No ALGOL 68, os criadores buscaram o nível máximo de ortogonalidade, permitindo que qualquer tipo de dado fosse combinado com qualquer operador ou estrutura. Isso garantiu **regularidade** (tudo seguia as mesmas regras lógicas sem exceção), mas não trouxe **simplicidade**, pois gerou expressões combinatórias extremamente abstratas e difíceis de compreender.

Portanto, uma linguagem muito ortogonal não é automaticamente fácil de usar. Quando a liberdade de combinação é excessiva, o código pode ficar ilegível e propenso a erros conceituais por parte do programador.

---

### Questão 11
**Enunciado:** Construa uma cadeia de influência que passe por ALGOL, Pascal e C. Depois contraste essa linhagem imperativa com a proposta declarativa de Prolog.

**Resposta:**
A cadeia de influência imperativa começa no **ALGOL 60**, que definiu a estrutura de blocos e o controle estruturado de fluxo. O **Pascal** refinou essas ideias focando no ensino e reforçando a segurança e a verificação estrita de tipos. Em seguida, o **C** aproveitou as estruturas de controle do modelo algólico e adicionou o acesso direto à memória com ponteiros, focando no desenvolvimento de sistemas operacionais.

O contraste com o **Prolog** está no paradigma:
* A linhagem do ALGOL, Pascal e C é **imperativa**, focada em **"como fazer"**, onde o desenvolvedor escreve passo a passo a sequência de operações e alterações de estado na memória.
* O Prolog é **lógico e declarativo**, focado em **"o que é verdade"**, onde o desenvolvedor apenas define fatos e regras, e o próprio motor da linguagem deduz as respostas por inferência sem a necessidade de comandos de repetição manuais.

---

### Questão 12
**Enunciado:** Modele em linguagem natural uma pequena base Prolog com dois fatos, uma regra e uma consulta. Explique por que isso representa programação lógica, não apenas armazenamento de dados.

**Resposta:**
* **Dois Fatos:**
  * Sócrates é humano: `humano(socrates).`
  * Platão é humano: `humano(platao).`
* **Uma Regra:**
  * Todo humano é mortal: `mortal(X) :- humano(X).`
* **Uma Consulta:**
  * Sócrates é mortal? `?- mortal(socrates).` $\to$ Retorno: `true`.

Isso representa programação lógica porque o sistema não está apenas fazendo uma busca por um valor fixo salvo em uma tabela. Ele usa **inferência lógica** e substituição de variáveis (*unificação*) para deduzir ativamente uma nova conclusão que não estava gravada de forma direta, conectando o fato à regra.

---

### Questão 13
**Enunciado:** Ada resultou de requisitos e projeto em grande escala. Analise como confiabilidade, tipos, pacotes e concorrência se relacionam ao domínio de sistemas críticos.

**Resposta:**
A linguagem Ada foi criada por encomenda militar para sistemas embarcados e missões críticas, onde qualquer falha de software pode causar acidentes graves:
* **Confiabilidade:** Possui tratamento de exceções rigoroso para garantir que o software não trave inesperadamente durante a operação.
* **Tipos:** Permite definir limites e faixas de valores válidos já em tempo de compilação (como limitar uma variável de temperatura de -50 a 100), evitando entradas inválidas.
* **Pacotes (*Packages*):** Garante modularidade ao separar a especificação pública da implementação interna, ajudando equipes gigantescas a manter o código organizado e seguro.
* **Concorrência:** Traz controle de tarefas (*tasks*) e sincronização nativos da linguagem, evitando erros comuns de acesso concorrente à memória.

---

### Questão 14
**Enunciado:** Compare o papel dos objetos em Smalltalk, C++ e Java. Inclua na resposta o compromisso de C++ com C e a estratégia de portabilidade de Java.

**Resposta:**
O papel dos objetos varia bastante entre essas três linguagens:
* No **Smalltalk**, a orientação a objetos é pura: absolutamente tudo no sistema é tratado como um objeto e as operações acontecem estritamente por envio de mensagens.
* No **C++**, a orientação a objetos é híbrida. A linguagem manteve **total compatibilidade com o C tradicional**, preservando tipos primitivos, controle manual de ponteiros e foco em desempenho de baixo nível sem camadas extras de execução.
* No **Java**, o modelo de objetos é obrigatório para estruturar o código, mas a linguagem abriu mão dos ponteiros manuais de C++ por segurança. Sua estratégia foi compilar o código para **bytecode**, que roda em qualquer sistema que possua a Máquina Virtual Java (JVM), garantindo portabilidade total.

---

### Questão 15
**Enunciado:** A primeira aplicação de Java não foi a Web, mas a Web impulsionou sua adoção. Explique como mudanças de contexto podem reposicionar uma linguagem.

**Resposta:**
O Java começou como um projeto chamado Oak, voltado para pequenos aparelhos eletrônicos e decodificadores de TV, um segmento que não teve tração no início dos anos 1990.

No entanto, com o surgimento da Web gráfica, o mercado passou a precisar com urgência de programas que pudessem rodar de forma segura em qualquer navegador e sistema operacional. Como o Java já contava com uma máquina virtual independente, segurança de memória e código portável, ele se encaixou perfeitamente nessa nova demanda com os Applets. Isso mostra como o sucesso de uma tecnologia depende diretamente de se alinhar às transformações e oportunidades do mercado.

---

### Questão 16
**Enunciado:** Compare Perl, JavaScript, PHP, Python, Ruby e Lua usando três eixos: domínio inicial, estruturas de dados e estratégia de implementação.

**Resposta:**
Embora todas sejam frequentemente chamadas de linguagens de script, cada uma nasceu com focos e arquiteturas bem distintas:

* **Perl:** Começou na administração de sistemas UNIX e tratamento de relatórios. Tem como estruturas marcantes os escalares, arrays indexados e hashes associativos, operando por compilação rápida de opcodes em tempo de execução.
* **JavaScript:** Nasceu para dar interatividade client-side aos navegadores. Baseia-se em objetos por protótipos e arrays dinâmicos, sendo executado nos motores dos navegadores com interpretadores e compiladores JIT.
* **PHP:** Criado para gerar páginas web dinâmicas do lado do servidor. Sua estrutura central é o array associativo híbrido (que funciona como lista e tabela de busca), rodando interpretado e acoplado ao servidor Web.
* **Python:** Focou no ensino e na automação geral com sintaxe limpa. Usa listas dinâmicas, dicionários, tuplas e conjuntos nativos, compilando o código para bytecode antes de rodar na VM padrão (CPython).
* **Ruby:** Projetado para a produtividade e expressividade no desenvolvimento com orientação a objetos pura. Trabalha com objetos puros, hashes, arrays e blocos de código (*closures*), sendo executado via máquina virtual de bytecode.
* **Lua:** Criada como linguagem leve para ser embutida dentro de programas em C/C++ (muito usada em jogos). Utiliza uma estrutura única e flexível chamada tabela (*table*), rodando em uma máquina virtual compacta baseada em registradores.

---

### Questão 17
**Enunciado:** C# foi apresentada como evolução no ambiente .NET. Compare duas decisões de C# com suas correspondentes em Java ou C++ e explique o problema que pretendem resolver.

**Resposta:**
Duas decisões importantes no design do C#:

1. **Uso de Propriedades (*Properties*) em vez de getters/setters repetitivos (Java):**
   * *Problema:* Em Java, encapsular atributos privados exige a escrita manual de vários métodos auxiliares `getNome()` e `setNome()`.
   * *Solução no C#:* Criou a sintaxe nativa de propriedades com acessores `get` e `set`, permitindo proteger os dados mantendo a simplicidade visual de uma atribuição direta (`obj.Nome = "Valor"`).

2. **Blocos `unsafe` em vez do modelo fechado do Java ou aberto do C++:**
   * *Problema:* O C++ permite ponteiros em qualquer lugar (aumentando o risco de erros de memória), enquanto o Java eliminou ponteiros totalmente (dificultando a integração de alta performance com rotinas de baixo nível).
   * *Solução no C#:* Mantém o ambiente gerenciado e seguro por padrão, mas permite isolar trechos específicos como `unsafe` onde o uso de ponteiros é liberado para tarefas que exigem velocidade máxima.

---

### Questão 18
**Enunciado:** Diferencie XSLT e JSP quanto a entrada, processamento e saída. Por que ambas podem ser chamadas de linguagens híbridas de marcação e programação?

**Resposta:**
A diferença entre elas está no fluxo de trabalho:
* **XSLT:** Recebe como entrada um documento estruturado em **XML**, aplica transformações declarativas baseadas em regras e caminhos XPath, e gera como saída um novo arquivo estruturado (HTML, texto ou outro XML).
* **JSP:** Recebe uma requisição web contendo templates em **HTML**, processa a lógica de negócio convertendo a página em um Servlet Java no servidor e devolve como saída a página HTML pronta para renderização no cliente.

Ambas são chamadas de híbridas porque combinam em um mesmo arquivo tags de **marcação estática** (XML/HTML) com **lógica de programação executável** (como laços, desvios condicionais e chamadas de código).

---

### Questão 19
**Enunciado:** Crie uma linha do tempo com oito linguagens de pelo menos quatro paradigmas. Para cada ligação, escreva o tipo de influência.

**Resposta:**
* **1957 — Fortran (Imperativo / Procedural):** Pioneira em expressões matemáticas e tipos numéricos básicos.
  * *Influenciou o ALGOL 60 ao demonstrar a viabilidade de sintaxes estruturadas de alto nível.*
* **1958 — Lisp (Funcional):** Pioneira na avaliação de expressões sem efeitos colaterais e processamento de listas.
  * *Influenciou a maioria das linguagens dinâmicas modernas com suas noções de funções de primeira classe.*
* **1960 — ALGOL 60 (Imperativo Estruturado):** Introduziu estrutura de blocos e escopo de variáveis.
  * *Influenciou o C ao fornecer o modelo de controle de fluxo e escopos locais.*
  * *Influenciou o SIMULA 67 na estrutura de blocos que deu origem ao encapsulamento.*
* **1967 — SIMULA 67 (Orientado a Objetos):** Criou as ideias de classes e herança.
  * *Influenciou diretamente o C++ ao sugerir a adição de classes sobre a base do C.*
* **1972 — C (Imperativo / Baixo Nível):** Focado em controle de memória e desenvolvimento de sistemas.
  * *Influenciou o C++ fornecendo a base sintática e o modelo de execução direta na máquina.*
* **1972 — Prolog (Lógico / Declarativo):** Pioneiro em dedução automática por regras e fatos.
* **1983 — C++ (Multiparadigma / OOP):** Combinou orientação a objetos com desempenho em código nativo.
  * *Influenciou o Java no formato sintático e no modelo geral de classes.*
* **1995 — Java (Orientado a Objetos com VM):** Focou em portabilidade com bytecode e gerenciamento automático de memória.
* **1995 — JavaScript (Multiparadigma / Protótipos e Funcional):** Uniu sintaxe parecida com C e conceitos funcionais herdados de Lisp/Scheme para a Web.

---

### Questão 20
**Enunciado:** Estudo de caso: uma equipe precisa escolher tecnologias para cálculo científico, regras declarativas, aplicação Web interativa e firmware restrito. Proponha famílias de linguagens, justifique historicamente cada escolha e explicite dois trade-offs.

**Resposta:**
Para atender aos quatro cenários, as famílias de linguagens mais adequadas são:

* **Cálculo Científico $\to$ Família Fortran / Julia / Python (com extensões numéricas em C/C++):** Historicamente essa linhagem foi aperfeiçoada para manipular matrizes contíguas na memória e conta com bibliotecas numéricas otimizadas há décadas.
* **Regras Declarativas $\to$ Família Prolog / Motores de Regras Lógicas (como CLIPS ou Drools):** Criadas especificamente para resolver problemas baseados em axiomas e inferência lógica sem precisar de laços manuais.
* **Aplicação Web Interativa $\to$ Família JavaScript / TypeScript:** Linguagens concebidas nativamente para interagir com o DOM e executadas pelos motores de todos os navegadores modernos.
* **Firmware Restrito $\to$ Família C / Rust / Assembly:** Linguagens sem coletor de lixo que permitem manipular registradores e posições de memória diretamente com o menor consumo de recursos.

Dois compromissos de projeto (*trade-offs*) dessa escolha:
1. **Velocidade de desenvolvimento vs. Consumo de recursos:** Usar linguagens dinâmicas na Web e na análise de dados acelera a escrita do código, mas aumenta o uso de memória e a dependência de interpretadores pesados.
2. **Segurança de memória vs. Controle em tempo real:** No firmware restrito não podemos utilizar linguagens com Coletor de Lixo (*Garbage Collector*), como Java ou Go, porque as pausas na limpeza de memória travam a execução em tempo real, exigindo o gerenciamento manual ou estático de C e Rust.