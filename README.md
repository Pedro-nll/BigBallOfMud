# Resenha do artigo Big Ball of Mud

[PDF](mud.pdf)

O artigo feito pela Universidade de Illinois, em 1997, discute o que eles denominam a arquitetura de software mais comum, "A grande bola de lama". Isso contrasta com a maioria das discussões em torno dos padrões arquiteturais de alto nível, em que, **enquanto falam sobre sistemas bem projetados, entregam sistemas funcionais.** Diante desse cenário, os autores exploram uma hipótese simples, mas poderosa: se essa abordagem é tão popular, ela deve estar, pelo menos parcialmente, correta. Assim, busca-se entender o que leva ao surgimento de uma arquitetura indescritível, por que ela é tão eficaz e como gerenciá-la. E, para atingir esse objetivo, é necessário entender o que é a arquitetura "*BIG BALL OF MUD*".

Em contraste com a arquitetura em camadas ou com uma pipeline arquitetural bem definida, que todos os sistemas em um mundo perfeito seguiriam, a "bola de lama" é definida por todos os atalhos tomados com pressa e reparos feitos com urgência. Estamos acostumados, especialmente em ambientes acadêmicos, a lidar com softwares bem definidos, a estudar diagramas de classe, implantação, entidade e relacionamento. Vemos contextos e domínios bem definidos, temos questões objetivas e, mesmo com prazos marcados em pedra, há uma recompensa por ter uma estrutura interna elegante.

Contudo, no mundo real, existem problemas e temos apenas que apresentar soluções. O cliente, o mercado ou o usuário final são, na maioria das vezes, cegos para as tecnologias utilizadas ou para as dívidas técnicas acumuladas; sendo assim, há um benefício em uma entrega rápida. Esta minha opinião está de acordo com o que o autor do artigo coloca: a "bola de lama" mostra sinais de crescimento desregulado. Se existia uma definição de contexto, domínio e elementos, ela há muito tempo foi erodida, e a realidade é que toda informação no sistema deixa de ser encapsulada, que o código é, em sua maioria, duplicado e, **ainda assim, essa arquitetura predomina.**

Com isso, o artigo passa a explorar seis padrões de design que buscam aproximar a realidade das arquiteturas na maioria dos ecossistemas de software ao que é visto como a arquitetura ideal, a arquitetura debatida e estudada. Esses não são antipadrões, são apenas estruturas que surgem a partir da prática em sistemas com um ciclo de vida longo e sem constante planejamento e reestruturação em prol de um desenvolvimento ágil. Eles são: *BIG BALL OF MUD*, *THROWAWAY CODE*, *PIECEMEAL GROWTH*, *KEEP IT WORKING*, *SWEEPING IT UNDER THE RUG* e *RECONSTRUCTION*.

Com o entendimento do que seria a grande bola de lama, conseguimos entender de onde ela surge a partir desses padrões. Começando com o "código descartável" (*Throwaway code*), que muitas vezes dá início à acumulação de lama, onde um pequeno trecho de código é escrito para resolver um problema pequeno de forma rápida. A famosa gambiarra. O problema é que, muitas vezes, esse código toma vida própria. Se funciona, por que alterá-lo? Assim, ele passa a ser reutilizado e, rapidamente, um pedaço significativo do sistema passa a depender desse trecho.

Isso leva a outro padrão da lama, o "crescimento gradual" (*Piecemeal growth*). O sistema pode até ter uma arquitetura bem definida no seu começo, mas sua estrutura tende a sofrer com a constante mudança de requisitos, mudanças e adições graduais. Vemos isso o tempo todo, até em ambientes acadêmicos, e nos acostumamos com esse fenômeno. O desenvolvimento de software é um processo vivo, e se, a cada problema resolvido, a cada linha adicionada, fosse necessário voltar atrás e refazer todos os diagramas e repetir a fase de planejamento, estaríamos presos em um loop infinito de indecisão. **Com isso, de pouco em pouco, a arquitetura do sistema passa a ser apenas uma sombra da boa definição arquitetural. E o contexto bem definido, apenas uma maquiagem para a solução.**

Em virtude disso, chegamos aos outros padrões definidos no artigo. "*Sweeping it under the rug*" busca aplicar uma fachada bem feita, uma interface bem definida, para uma estrutura decadente. Reconstruction busca refazer o sistema, abandonando o caos que se instaurou. "*Keeping it working*" busca aplicar os bons padrões em pequenos pedaços manejáveis do sistema.

Contudo, mesmo entendendo que esses padrões existem e seus efeitos, ainda há de surgir uma resposta para o "por que eles existem?". Como disse anteriormente, essa arquitetura predomina por uma necessidade de venda. Resolver um problema na hora certa, aproveitar uma janela de oportunidade, entregar uma solução é agnóstico a como isso será feito. Assim, definimos, em concordância com o autor do artigo, a primeira força primordial no surgimento da bola de lama: **tempo**.

Ademais, a experiência dos desenvolvedores no time, a taxa de turnover e rotatividade, a habilidade individual, a complexidade inerente do problema e o custo da boa arquitetura e refatoração. Todos são fatores que levam à aderência a esses padrões de design; todos levam à acumulação de reparos rápidos, de decisões imprudentes e não planejadas. Todos pendem a balança entre qualidade e funcionalidade para um lado.

Para exemplificar todos esses conceitos, o autor faz uma metáfora interessante, a qual vou adaptar para a realidade do brasileiro. O surgimento dessa arquitetura desenha um paralelo com incrível semelhança ao surgimento das favelas. Há uma necessidade urgente de moradia, elas são construídas a partir de materiais baratos e ferramentas simples. A construção é rápida e a mão de obra não precisa ser especializada; a arquitetura é um luxo de tempo e dinheiro. Porém, as reformas e manutenções que serão inevitavelmente necessárias são caras e extremamente difíceis de serem feitas. O foco é primariamente em funcionalidade, e não em qualidade.

Um último ponto relevante a ser considerado é que, em alguns casos, a liberdade dada a partes do código — um pequeno pedaço de caos em meio à ordem arquitetural imposta — pode ser interessante. Existem domínios complexos demais para serem modelados seguindo uma abordagem "top-down"; a busca pela perfeição é cara e há o argumento de que não vale a pena. Permitir que o sistema passe por um período mais instável, para que a informação flua naturalmente para sua posição no sistema, sem barreiras arbitrárias, pode resultar em uma arquitetura saudável com suas devidas refatorações depois que o problema for melhor entendido. Mas, mesmo assim, a bola de lama deve ser tratada com cuidado para que não saia do controle.
