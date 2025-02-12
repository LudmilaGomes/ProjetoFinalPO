# Trabalho Final para a disciplina de Pesquisa Operacional
## Equipe: Arthur Henrique da Silva @ArthurH35 - Ludmila Vinólia Guimarães Gomes @LudmilaGomes

### Conceito
Resumo do Funcionamento - Branch-and-Bound: o algoritmo Branch-and-Bound foi pensado para vencer a dificuldade existente nas resoluções de problemas de programação linear inteira (onde as variáveis a serem encontradas são obrigatoriamente valores inteiros) ao utilizar uma 'relaxação linear', em que o modelo de PI proposto se torna um modelo de programação linear apenas, ou seja, a restrição de integralidade das variáveis é retirada para que seja encontrada a solução. Com a solução, o polígono de soluções viáveis para o modelo PL encontrado é dividido em duas partes, devido à inclusão de restrições que limitam o espaço (Branch) e retiram uma região em que uma das variáveis assume valores não inteiros. Esse processo é realizado de forma cíclica até que um valor ótimo com variáveis de valores inteiros seja encontrado. O algoritmo para de executar quando os modelos relaxados não podem ser solucionados, devido às podas que podem ocorrer (Bounds):

 - por Limitante: o valor objetivo atual encontrado é menor que outros valores ótimos e possíveis (e não faz sentido buscar abaixo desse nó, pois os valores objetivos serão menores que o atual).
 - por Integralidade: os valores das variáveis são números inteiros (e o valor objetivo pode ser ótimo ou não).
 - por Inviabilidade: o polígono de soluções viáveis está 'vazio' e não pode ser encontrada solução para o modelo.
O presente projeto tem o objetivo de utilizar o algoritmo Branch-and-Bound, mas apenas na resolução de problemas de programação linear inteira binária. Assim, o modelo relaxado apresenta variáveis com valores reais no intervalo de 0 a 1 e a solução ótima procurada deve apresentar um valor binário (inteiro, claro), 0 ou 1.

Assim, é realizada a implementação do algoritmo de Branch-and-Bound para problemas de programação linear inteira binária usando Python e o pacote Mip, este usado para encontrar as soluções dos modelos relaxados.

Modelos de entrada aceitos: função objetivo de maximização, restrições de “menor ou igual” (com exceção das que definem o domı́nio das variáveis).

Saída gerada: para um caso de teste, o programa exibe em uma célula os resultados dos modelos dos nós, com valores para as variáveis e seus valores objetivos. Na célula seguinte, é exibida a solução ótima encontrada para esse caso de teste.
