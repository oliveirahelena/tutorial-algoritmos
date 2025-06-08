# Tutorial: A Tartaruga Artista e a Sequência Mágica!

Bem-vindo, jovem programador(a)!

Hoje, vamos aprender algo muito importante no mundo da programação: **algoritmos**. Um algoritmo nada mais é do que uma **sequência de comandos claros e ordenados** que damos a um computador (ou, no nosso caso, à nossa amiga Tartaruga Artista!) para que ela realize uma tarefa específica e alcance um objetivo.

Nosso objetivo hoje? Ensinar a Tartaruga a desenhar um lindo **quadrado azul** na tela! Para isso, vamos pensar juntos em cada pequeno passo que ela precisa seguir.

Preparado(a)? Vamos começar!

---

## Entendendo Nosso Desafio: O Algoritmo do Quadrado

Antes de tocar nos blocos, vamos pensar como *nós* desenharíamos um quadrado no papel com uma caneta:

1.  Preparar a área de desenho (limpar a tela).
2.  Pegar a caneta e escolher a cor azul.
3.  Colocar a ponta da caneta no papel, apontando para cima.
4.  Desenhar uma linha reta para frente (para cima).
5.  Virar a caneta (e o papel, ou nós mesmos) em 90 graus para a direita.
6.  Desenhar outra linha reta do mesmo tamanho.
7.  Virar novamente 90 graus para a direita.
8.  Desenhar a terceira linha reta.
9.  Virar mais uma vez 90 graus para a direita.
10. Desenhar a última linha reta para fechar o quadrado.

Percebeu? Essa é uma sequência de comandos! É um algoritmo! Agora, vamos traduzir isso para a linguagem da nossa Tartaruga Artista no MakeCode Arcade.

---

## Passo 1: Preparando o Palco e a Artista

Assim como um artista prepara sua tela e seus pincéis, precisamos preparar o ambiente para nossa Tartaruga.

1.  **Reiniciando a Tartaruga:** Para começar com uma tela limpa e a tartaruga na posição inicial (no centro, virada para CIMA), vamos usar o bloco de reinício.
    *   Na caixa de ferramentas à esquerda, procure a categoria de blocos chamada `Turtle`.
    *   Encontre o bloco `turtle reset`.
    *   Arraste este bloco para dentro do bloco `ao iniciar`, que já deve estar na sua área de programação. Se não estiver, você pode encontrá-lo na categoria `Loops`.

    ```blocks
    // Dentro do bloco "ao iniciar"
    turtle.reset()
    ```
    *Este é o primeiro comando da nossa sequência: "Tartaruga, prepare-se e limpe a tela!"*

2.  **Escolhendo a Cor da Tinta:** Nosso quadrado será azul.
    *   Ainda na categoria `Turtle`, procure o bloco `turtle pen color [cor]`.
    *   Arraste-o para baixo do bloco `turtle reset`.
    *   Clique no espaço da cor (que deve ser um seletor de cores) e escolha a cor **azul**.

    ```blocks
    // Dentro do bloco "ao iniciar"
    turtle.reset()
    turtle.pencolor(Colors.Blue) // O bloco mostrará um seletor de cores
    ```
    *Segundo comando: "Tartaruga, use a tinta azul!"*

---

## Passo 2: Desenhando o Primeiro Lado do Quadrado

Agora que a Tartaruga está pronta e com a cor certa, vamos dar o comando para ela desenhar a primeira linha do nosso quadrado. Lembre-se, ela começa virada para CIMA.

1.  **Movendo para Frente:**
    *   Na categoria `Turtle`, encontre o bloco `turtle forward [distância] pixels`.
    *   Arraste-o para baixo do bloco de definir a cor.
    *   No espaço do número para `distância`, digite `50`. Isso fará a Tartaruga andar 50 pixels para frente (para cima), desenhando uma linha.

    ```blocks
    // Dentro do bloco "ao iniciar"
    turtle.reset()
    turtle.pencolor(Colors.Blue)
    turtle.forward(50)
    ```
    *Terceiro comando: "Tartaruga, ande 50 passos para frente desenhando!"*

    **Teste!** Clique no botão de "Play" (parece um triângulo) abaixo da tela do jogo. Você deve ver uma linha azul aparecer, indo do centro da tela para cima! Este é o poder de dar comandos em sequência!

---

## Passo 3: Virando para o Próximo Lado

Para fazer um canto do quadrado, a Tartaruga precisa virar. Um quadrado tem cantos de 90 graus.

1.  **Virando à Direita:**
    *   Na categoria `Turtle`, procure o bloco `turtle right [ângulo] degrees`.
    *   Arraste-o para baixo do bloco `turtle forward`.
    *   No espaço do número para `ângulo`, digite `90`.

    ```blocks
    // Dentro do bloco "ao iniciar"
    turtle.reset()
    turtle.pencolor(Colors.Blue)
    turtle.forward(50)
    turtle.right(90)
    ```
    *Quarto comando: "Tartaruga, vire 90 graus para a sua direita!"*

    Se ela estava virada para CIMA e virou 90 graus à direita, agora ela está apontando para a DIREITA na tela, pronta para o próximo lado!

---

## Passo 4: Completando o Quadrado - A Sequência se Repete!

Você já deu os comandos para desenhar um lado (para cima) e fazer uma virada (para a direita). Um quadrado tem quatro lados iguais e quatro cantos iguais. Isso significa que a **sequência de comandos `turtle forward 50 pixels` e `turtle right 90 degrees` vai se repetir!**

Para completar o quadrado, você precisa adicionar os seguintes comandos, na ordem correta:

2.  `turtle forward 50 pixels` (para o segundo lado, que será desenhado para a direita)
3.  `turtle right 90 degrees` (agora ela apontará para BAIXO)
4.  `turtle forward 50 pixels` (para o terceiro lado, desenhado para baixo)
5.  `turtle right 90 degrees` (agora ela apontará para a ESQUERDA)
6.  `turtle forward 50 pixels` (para o quarto e último lado, desenhado para a esquerda, fechando o quadrado)
7.  (Opcional) `turtle right 90 degrees` (para a Tartaruga voltar à orientação para CIMA, como começou)

**Seu desafio é montar essa sequência completa!** Seu bloco `ao iniciar` deverá ficar parecido com isto no final:

```blocks
// Dentro do bloco "ao iniciar"
turtle.reset()
turtle.pencolor(Colors.Blue)

// Primeiro lado (para CIMA) e virada
turtle.forward(50)
turtle.right(90)

// Segundo lado (para DIREITA) e virada
turtle.forward(50)
turtle.right(90)

// Terceiro lado (para BAIXO) e virada
turtle.forward(50)
turtle.right(90)

// Quarto lado (para ESQUERDA)
turtle.forward(50)
// turtle.right(90) // Opcional: para a tartaruga olhar para CIMA novamente
```