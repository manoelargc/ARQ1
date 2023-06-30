## Trabalho Final - Arquitetura e Organização de Computadores I - Ciência da Computação - 23.1
# Processador MIPS Monociclo no Logisim
- Manoela Resende
- Eduarda Sifuentes

Este trabalho é propriedade de Manoela Resende, perfil [manoelargc](https://github.com/manoelargc). Ele foi desenvolvido como parte do Trabalho Final da disciplina de Arquitetura e Organização de Computadores I do 3º Semestre de Ciência da Computação - 23.1.

## Descrição
O projeto consiste na implementação de um processador MIPS monociclo utilizando o software Logisim-evolution. O processador é capaz de executar instruções MIPS básicas, como operações aritméticas, desvios condicionais e acesso à memória.

#### O processador inclui os seguintes componentes:

- Unidade Lógico-Aritmética (ULA): realiza operações lógicas e aritméticas, como adição, subtração e operações bit a bit.
- Registradores: armazenam os dados temporários durante as operações do processador.
- Memória de Programa: contém as instruções do programa a serem executadas.
- Memória de Dados: armazena os dados utilizados pelo programa.
  
### Instruções de uso
Para utilizar o projeto, siga as seguintes etapas:

- Faça o download do software Logisim-evolution em: https://github.com/reds-heig/logisim-evolution.
- Abra o Logisim-evolution e carregue o arquivo XML do projeto.
- Utilize as ferramentas disponíveis no Logisim-evolution para interagir com o processador, como inserir instruções, visualizar registros e observar o comportamento do processador durante a execução.


## Referências
Logisim-evolution: https://github.com/reds-heig/logisim-evolution
O restante está no codigo

## Componentes do processador

1.	Registrador de Programa (PC): Ele mantém o controle do endereço de memória da instrução atualmente sendo executada. Incrementa 4 unidades a cada ciclo de clock .
2.	Memória de Programa: Responsável por armazenar o código em assembly do MIPS. A instrução é decodificada em uma sequência de 32 bits, dividida em partes menores, e a saída é distribuída para os componentes correspondentes.
3.	MUX (Multiplexador): É responsável por selecionar qual entrada será utilizada para leitura ou escrita.
4.	Banco de Registradores: Armazena os dados dos registradores utilizados pelo processador. O sinal de escrita (rw) indica o endereço no banco de dados onde a informação de entrada será registrada.
5.	ULA (Unidade Lógica e Aritmética): Realiza as operações aritméticas e lógicas nos dados fornecidos pelas saídas A e B do Banco de Registradores.
6.	MUX 2: Define se a entrada B da ULA será o valor do registrador (vindo do Banco de Registradores) ou um valor imediato.
7.	Extensor de Sinal: Transforma um valor imediato de 16 bits em um valor de 32 bits para que a ULA possa operar corretamente.
9.	Memória RAM: Uma memória de acesso aleatório utilizada pelo processador para ler e escrever dados.
10.	Branch: Utilizado nas instruções BEQ (branch if equal) e BNE (branch if not equal) para controlar os desvios condicionais. Realiza a soma do PC com um endereço para o salto.


__Funções de Controle__: São responsáveis por controlar o funcionamento dos diferentes componentes do processador. Algumas dessas funções são:
-	REGWRITE: Define se o valor gerado na saída W do Banco de Registradores será registrado novamente no banco.
-	RESET: Sinal de reset utilizado para reinicializar o processador.
-	REGDST: Indica qual sequência de bits no Banco de Registradores será usada como endereço, sendo 0 para instruções do tipo I e 1 para instruções do tipo R.
-	ALUSCR: Define se a entrada B da ULA virá do Banco de Registradores (0) ou do valor imediato (1).
-	ALUOP: Define a operação a ser realizada pela ULA, como soma (0010) ou subtração (0110).
-	MEMWRITE: Habilita a escrita na memória.
-	MEMREAD: Habilita a leitura na memória.
-	MEMTOREG: Define se o dado a ser escrito no registrador vem da memória.

É possível acompanhar as operações do processador e verificar os resultados nas saídas apropriadas, como registradores e memória de dados.

---------------
O projeto depende do software Logisim-evolution para ser executado. Certifique-se de ter o Logisim-evolution instalado em seu sistema antes de utilizar o projeto.
Certifique-se de consultar a documentação e o projeto específico para obter mais detalhes sobre a implementação do processador MIPS monociclo no Logisim.
