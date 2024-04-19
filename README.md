# Minesweeper

Este é um jogo de campo minado (Minesweeper) escrito em C# com MonoGame. O repositório utilizado para o trabalho foi o seguinte: https://github.com/lunacys/Minesweeper

## Descrição

O Minesweeper é um jogo em que o jogador deve descobrir as células do campo de jogo que não contêm minas. O objetivo é revelar todas as células sem minas, evitando clicar nas células que as contêm. O jogo termina quando todas as células sem minas são reveladas ou quando uma célula com uma mina é clicada.

## Funcionalidades

1. **`CreateBoard(rows, cols, mines)`:** Este método cria um novo tabuleiro do jogo com o número especificado de linhas, colunas e minas. Retorna um tabuleiro inicializado com células ocultas e minas posicionadas aleatoriamente.

2. **`PrintBoard(board, reveal=false)`:** Este método imprime o tabuleiro atual do jogo. Se `reveal` for verdadeiro, todas as células serão reveladas, mostrando as minas e os números que indicam o número de minas adjacentes a cada célula.

3. **`RevealCell(board, row, col)`:** Este método revela o conteúdo de uma célula específica do tabuleiro. Se a célula contiver uma mina, o jogo termina. Se a célula estiver vazia, todas as células adjacentes vazias serão reveladas recursivamente.

4. **`MarkCell(board, row, col)`:** Este método marca ou desmarca uma célula como suspeita de conter uma mina. As células marcadas são exibidas como bandeiras quando o tabuleiro é impresso.

5. **`CheckWin(board)`:** Este método verifica se o jogador ganhou o jogo, ou seja, se todas as células sem minas foram reveladas.

6. **`PlayGame(rows, cols, mines)`:** Este método inicia e controla o fluxo do jogo. Permite ao jogador interagir com o tabuleiro, revelando células, marcando-as como suspeitas de conter minas e verifica se o jogo terminou com vitória ou derrota.

7. **`RestartGame()`:** Este método reinicia o jogo, permitindo ao jogador jogar novamente sem precisar reiniciar o aplicativo.

8. **`SaveGame()`:** Este método permite ao jogador salvar o estado atual do jogo para retomá-lo mais tarde.

9. **`LoadGame()`:** Este método permite ao jogador carregar um jogo salvo anteriormente para continuar jogando.

10. **`Options()`:** Este método permite ao jogador ajustar as configurações do jogo, como tamanho do tabuleiro e número de minas, durante o jogo.

11. Temos níveis de dificuldade, que influenciam em quantas bombas serão colocadas no tabuleiro.

12. Podemos alterar o tamanho do grid, definindo sua altura e largura.

13. Botões para refazer a jogada e até mesmo resolver o "puzzle".

14. Contadores de minas, espaços disponíveis, células vazias, tempo, etc.

## Como Jogar

1. Certifique-se que possui .NET Core na versão 3.1 ou superior. O MonoGame instalado também é essencial.
2. Através do CMD, aceda à pasta ./Source e digite o seguinte comando:
dotnet run --project .\Minesweeper.DesktopGL\Minesweeper.DesktopGL.csproj