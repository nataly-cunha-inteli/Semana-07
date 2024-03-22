# Instruções

- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 6 questões objetivas assinalando a alternativa correta
- Resolva as 4 questões dissertativas escrevendo no próprio arquivo .md
  - lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com ChatGPT e afins: entregar algo só para ganhar nota não faz você aprender e ficar mais inteligente. Não seja dependente da máquina! (E não se envolva em plágio!)
- ao final, publique seu arquivo lista_02.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas

**1)** Considere o seguinte código JavaScript:

```javascript
//EX01
let x = 17
let y = 5
let z = 8

resultadoBooleano =  (x < y) && (z > x) || (x - y > z)
console.log(resultadoBooleano)

const listaDeNumeros = [1, 2, 3, 4, 5];
let soma = 0;

for (let i = 0; i < listaDeNumeros.length; i++) {
  soma += listaDeNumeros[i];
}

console.log("A soma dos números é:", soma);

```
Qual das seguintes alternativas melhor descreve o que o código faz?

A) O código avalia a expressão booleana, imprime o resultado `false`, calcula a soma dos números de 1 a 5 e imprime o resultado no console.

B) O código avalia a expressão booleana, imprime o resultado `true`, calcula a soma dos números de 1 a 5 e imprime o resultado no console.

C) O código avalia a expressão booleana, imprime o resultado `true` e verifica se o número 5 está presente na lista de números.

D) O código avalia a expressão booleana, imprime o resultado `false` e ordena a lista de números em ordem crescente.


______

**2)** Analise as funções calcularOrcamento() e calcularOrcamento2(). Num cenário em que a lista gastos fosse incializada como var gastos = [3600, 950, 620, 38] em ambas funções.

```javascript
//Versão 1 da função que calcula orçamento
function calculaOrcamento(){

    var gastos = [1800, 950, 620, 38];
    var totalGastos = gastos[0];
    var salario = 3500;
    var saldo = 0; 
    var statusSaldo =  'positivo';
    var i = 1;

    do{
        totalGastos += gastos[i];
        i++;
    } while(salario >= totalGastos && i<gastos.length)
    
    saldo = salario - totalGastos;

    if (saldo < 0 ){
        statusSaldo = 'negativo';
    } 
    console.log (`Seu saldo é ${statusSaldo} de ${saldo}. `);
}
```

```javascript
//Versão 2 da função que calcula orçamento
function calculaOrcamento2(){

    var gastos = [1800, 950, 620, 38];
    var totalGastos = gastos[0];
    var salario = 3500;
    var statusSaldo =  'positivo';
    var saldo = 0;
    var i = 1;

    while(salario >= totalGastos && i<gastos.length){
        totalGastos += gastos[i];
        i++;
    }

    saldo = salario - totalGastos;
    if (saldo < 0 ){
        statusSaldo = 'negativo';
    } 
    console.log (`Seu saldo é ${statusSaldo} de ${saldo}. `);
}
```

Escolha a opção que responde corretamente qual seria a saída após a execução de cada função:

A) As funções calcularOrcamento() e calcularOrcamento2() teriam a mesma saída: 'Seu saldo é negativo de -1050.'

B) A saída de calcularOrcamento() seria: 'Seu saldo é negativo de -1050.' e a de calcularOrcamento2() seria: 'Seu saldo é negativo de -100.'

C) A saída de calcularOrcamento() seria: 'Seu saldo é negativo de -100.' e a de calcularOrcamento2() seria: 'Seu saldo é negativo de -1050.'

D) As funções calcularOrcamento() e calcularOrcamento2() teriam a mesma saída: 'Seu saldo é negativo de -100.'

______

**3)** Considere o seguinte trecho de código em JavaScript:
```javascript
//EX03
const numero = 10;

if (numero % 2 === 0) {
  console.log("O número é par!");
} else if (numero % 3 === 0) {
  console.log("O número é divisível por 3!");
} else {
  console.log("O número é ímpar e não é divisível por 3!");
}
```

 Qual das seguintes alternativas é a descrição mais precisa do que o código faz?


A) O código verifica se o número é divisível por 3 e, se for, exibe a mensagem "O número é divisível por 3!".

B) O código verifica se o número é par ou ímpar. Se for par, exibe a mensagem "O número é par!". Se for ímpar, exibe a mensagem "O número é ímpar!".

C) O código verifica se o número é par, ímpar ou divisível por 3. Se for par, exibe a mensagem "O número é par!". Se for divisível por 3, exibe a mensagem "O número é divisível por 3!". Se for ímpar, exibe a mensagem "O número é ímpar e não é divisível por 3!".

D) O código verifica se o número é par, se é divisível por 3 ou se é ímpar. Se for par, exibe a mensagem "O número é par!". Se for divisível por 3 (e não for par), exibe a mensagem "O número é divisível por 3!". Se for ímpar (e não for divisível por 3), exibe a mensagem "O número é ímpar e não é divisível por 3!".


______

**4)** Qual será o resultado impresso no console após a execução desse código?
```javascript
//EX04
var saldo = 1000;
var limiteCredito = 500;
var valorCompras = [200, 800, 300, 400, 600];

for (var i = 0; i < valorCompras.length; i++) {
    var valorCompra = valorCompras[i];

    if (valorCompra <= saldo) {
        console.log("Compra " + (i+1) + " aprovada. Saldo restante: " + (saldo - valorCompra));
        saldo -= valorCompra;
    } else if (valorCompra <= saldo + limiteCredito) {
        console.log("Compra " + (i+1) + " aprovada com limite de crédito. Saldo restante: " + ((saldo + limiteCredito) - valorCompra));
        saldo = 0;
        limiteCredito -= (valorCompra - saldo);
    } else {
        console.log("Compra " + (i+1) + " negada. Saldo insuficiente e limite de crédito excedido.");
    }
}
```

Escolha a opção que responde corretamente:

A)
Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 400

Compra 4 aprovada com limite de crédito. Saldo restante: 0

Compra 5 aprovada. Saldo restante: -200


B)
Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 200

Compra 4 negada. Saldo insuficiente e limite de crédito excedido.

Compra 5 negada. Saldo insuficiente e limite de crédito excedido.


C)
Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 400

Compra 4 negada. Saldo insuficiente e limite de crédito excedido.


D)

Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada. Saldo restante: 0

Compra 3 aprovada com limite de crédito. Saldo restante: 200

Compra 4 negada. Saldo insuficiente e limite de crédito excedido.

Compra 5 negada. Saldo insuficiente e limite de crédito excedido.

______

**5)** Qual é o principal ciclo de vida de um jogo em Phaser.js?

Escolha a opção que responde corretamente:

A) Setup -> Update -> Draw

B) Preload -> Create -> Update

C) Load -> Initialize -> Render

D) Begin -> Play -> End
______

**6)** Qual é o objetivo principal do módulo Arcade Physics em Phaser.js?

Escolha a opção que responde corretamente:

A) Renderizar gráficos 3D para jogos em HTML5.

B) Simular interações físicas realistas, como colisões e movimentos, em jogos 2D.

C) Criar efeitos de áudio para melhorar a experiência do usuário em jogos.

D) Gerenciar a lógica do jogo e a sincronização de eventos em jogos multiplayer.

______

# Questões dissertativas

**7)** Implemente o pseudocódigo para o algoritmo representado no fluxograma da imagem.
![Uma imagem](assets/image.png)

**Resposta:**

```
algoritmo "voto"

#criação de variáveis
var
inteiro idade = entrada("Insira sua idade: ");

inicio

#condição 1
SE (idade < 16) ENTAO:

#impressão de mensagem para o usuário
escreva("Não pode votar!)

FIM SE

#condição 2
SE (idade >= 16 e idade < 18) ENTAO:

#impressão de mensagem para o usuário
escreva("Voto facultativo!)

FIM SE

#condição else, caso todas as outras não sejam verdadeiras
SENAO:

#impressão de mensagem para o usuário
escreva("Voto obrigatório)

FIM SE

fimalgoritmo
```

______

**8)** Considere a implementação da classe base FormaGeometrica em um sistema de modelagem de formas geométricas. Sua tarefa é implementar, utilizando pseudocódigo, as classes derivadas Retangulo e Circulo, que herdam da classe FormaGeometrica, adicionando atributos específicos e métodos para calcular a área de um retângulo e de um círculo, respectivamente.

```
Classe FormaGeometrica:
    Atributos:
        - cor

    Método Construtor(cor):
        Define o valor do atributo cor com o valor passado como parâmetro.

    Método CalcularArea():
        # Implementação genérica para cálculo de área, a ser sobrescrita pelas subclasses.

```

MINHA RESPOSTA:
```
classe FormaGeometrica: 
    
    # método construtor que pode ser, por padrão, vazio, mas neste caso o configuro manualmente
    MÉTODO construtor(cor, pi, area): 

        #inserção de atributos da classe FormaGeometrica
        atribuir cor a cor
        atribuir pi a pi
        atribuir area a area
    FIM MÉTODO

    #criação de método que recebe um parâmetro area e mostra ao usuário a área
    MÉTODO calcularArea(area):
        escreva area
    FIM MÉTODO

FIM CLASSE

 #criação de classe-filha
classe Retangulo estende de FormaGeometrica:
    
    # configuração de atributos
    MÉTODO construtor(cor, base, altura):
        chamar construtor de FormaGeometrica passando cor # inclusão de atributos da classe-pai, como no super() em JavaScript

        # novos atributos
        atribuir base a base
        atribuir altura a altura
    FIM MÉTODO

    #método que calcula a área e mostra ao usuário
    MÉTODO calcularArea():
        escreva base multiplicada por altura
    FIM MÉTODO

FIM CLASSE

# criação de outra classe-filha
classe Circulo estende FormaGeometrica:
    
     # configuração de atributos
    MÉTODO construtor(cor, pi, raio):
        chamar construtor de FormaGeometrica passando cor e pi # inclusão de atributos da classe-pai, como no super() em JavaScript
        atribuir raio a raio
    FIM MÉTODO

    #método que calcula a área e mostra ao usuário
    MÉTODO calcularArea():
        escreva pi multiplicado por raio ao quadrado
    FIM MÉTODO

FIM CLASSE

#criação de novos objetos da classe-pai e das classes-filhas
retangulo = novo retangulo com parâmetros 'verde', 5, 10
circulo = novo circulo com parâmetros 'vermelho', 3.14, 2
forma = nova forma com parâmetros 'roxo', 3.14, 2

#utilização dos métodos de cada classe
escreva o método calcularArea de forma passando parâmetro área
escreva o método calcularArea de retangulo
escreva o método calcularArea de circulo

```

______

**9)** Você foi contratado(a) como estagiário(a) da Tesla e está participando do desenvolvimento de um programa para simular o desempenho de um carro elétrico em uma corrida. Seu objetivo é determinar em quantos minutos o carro levará para completar uma determinada distância, levando em consideração uma velocidade inicial e uma taxa de aceleração constante. No entanto, você deseja garantir que o carro não exceda uma velocidade máxima nem que a corrida demore mais do que um tempo máximo. Implemente a lógica dessa simulação em pseudocódigo.

```
algoritmo "corrida";

#criação de variáveis
var
real distancia, velocidadeInicial = 0, aceleracao, velocidadeMaxima, tempoMaximo, minutos = 0
logico ida = verdadeiro

#função que simula a corrida
função simularDesempenho()

    # loop infinito de tipo while até que a corrida seja concluída ou as condições sejam violadas
    ENQUANTO caminho == verdadeiro FAÇA  
        minutos += 1  # incremento do tempo de 1 em 1 minuto
        
        # cálculo da velocidade atual do carro usando a equação da cinemática v = v0 . a . t
        velocidade = velocidadeInicial + aceleracao * minutos
        
        # condição que verifica se a velocidade máxima foi excedida
        SE velocidade = velocidadeMaxima:
            velocidade <- velocidadeMaxima  # limitação da velocidade à velocidade máxima
        FIM SE
        
        # Calcular a distância percorrida até o momento usando a equação S = v0 + V . t 
        distanciaPercorrida = velocidadeInicial + velocidade * aceleracao
        
        # Verificar se a distância total foi percorrida
        SE distanciaPercorrida >= distancia:
            retorno minutos  # Retornar o tempo total da corrida

        FIM SE
        
        # verificação de se o tempo máximo foi excedido
        SE minutos == tempoMaximo:
            escreva("O carro percorreu a distância em " + minutos + "minutos.")
            ida == falso # irá parar o loop 

        FIM SE
FIM FUNÇÃO

#utilização da função de simular corrida
tempoCorrida = simularCorrida(distancia, velocidadeInicial, aceleracao, velocidadeMaxima, tempoMaximo)

```

______

**10)** Uma matriz é uma coleção bidimensional de elementos, organizados em linhas e colunas. A seguir, é fornecida a implementação da função SomaDeMatrizes(matrizA, matrizB), que calcula a soma de duas matrizes. Sua tarefa é implementar uma função semelhante, porém que realize a multiplicação de duas matrizes.

```
Função SomaDeMatrizes(matrizA, matrizB):
    # Verifica se as duas matrizes têm o mesmo número de linhas e colunas
    Se tamanho(matrizA) ≠ tamanho(matrizB) então:
        Retornar "As matrizes não podem ser somadas. Elas têm dimensões diferentes."
    Senão:
        linhas <- tamanho(matrizA)
        colunas <- tamanho(matrizA[0]) # Considerando que todas as linhas têm o mesmo número de colunas
        matrizResultado <- novaMatriz(linhas, colunas)

        # Loop para percorrer cada elemento das matrizes e calcular a soma
        Para i de 0 até linhas-1 faça:
            Para j de 0 até colunas-1 faça:
                matrizResultado[i][j] <- matrizA[i][j] + matrizB[i][j]

        Retornar matrizResultado

# Exemplo de uso da função
matrizA <- [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
matrizB <- [[9, 8, 7], [6, 5, 4], [3, 2, 1]]

matrizSoma <- SomaDeMatrizes(matrizA, matrizB)
Escrever("Soma das matrizes:")
ImprimirMatriz(matrizSoma)

```

MINHA RESPOSTA:

```
função MultiplicacaoDeMatrizes(matrizA, matrizB):
    # Verifica se as duas matrizes têm o mesmo número de linhas e colunas
    SE tamanho(matrizA) ≠ tamanho(matrizB) ENTÃO:
        Retornar "As matrizes não podem ser multiplicadas. Elas são de diferentes ordens."
    FIM SE

    # condição favorável ao cálculo, pois acontece quando as matrizes são de mesma ordem
    SENÃO:
        # configuração de leitura do tamanho padrão para as matrizes, e de uma variável que guarda estes dados
        linhas <- tamanho(matrizA)
        colunas <- tamanho(matrizA[0])
        matrizResultado <- novaMatriz(linhas, colunas)

        # loop para percorrer cada elemento das matrizes e calcular a multiplicação
        Para i de 0 até linhas-1 FAÇA:
            Para j de 0 até colunas-1 faça:
                matrizResultado[i][j] <- (matrizA[i][j] * matrizB[i][j])+matrizA[i][j+1]*matrizB[i+1][j]
        FIM PARA
        retornar matrizResultado
    FIM SE

# Exemplo de uso da função
matrizA <- [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
matrizB <- [[9, 8, 7], [6, 5, 4], [3, 2, 1]]

#inicialização da função de multiplicação, guardada em uma variável
matrizMult <- MultiplicacaoDeMatrizes(matrizA, matrizB)

#impressão do resultado da multiplicação
escreva("Multiplicação das matrizes: " + matrizMult)
```