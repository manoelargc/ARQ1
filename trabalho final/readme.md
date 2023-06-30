Título do Projeto
Processador MIPS Monociclo no Logisim

Descrição
Este projeto consiste em um processador MIPS monociclo implementado no software Logisim. O processador é capaz de executar um subconjunto de instruções da arquitetura MIPS (Microprocessor without Interlocked Pipeline Stages) em um ciclo de clock.

O processador inclui os seguintes componentes:

Unidade de Controle: responsável por controlar as operações do processador e gerar os sinais de controle adequados para cada instrução.
Unidade Lógico-Aritmética (ULA): realiza operações lógicas e aritméticas, como adição, subtração e operações bit a bit.
Registradores: armazenam os dados temporários durante as operações do processador.
Memória de Instruções: contém as instruções do programa a serem executadas.
Memória de Dados: armazena os dados utilizados pelo programa.
Pré-requisitos
Antes de executar o projeto, certifique-se de ter os seguintes pré-requisitos:

Software Logisim instalado em seu computador.
Instalação
Siga as etapas abaixo para instalar e executar o projeto:

Faça o download do arquivo do projeto.
Abra o Logisim em seu computador.
No Logisim, abra o arquivo do projeto baixado.
Uso
Para utilizar o processador no Logisim, siga as instruções abaixo:

Adicione o programa desejado à memória de instruções.
Configure os registradores e a memória de dados, se necessário.
Inicie a simulação no Logisim para que o processador execute as instruções.
Monitore os resultados nas saídas apropriadas (registradores, memória de dados, etc.).
Contribuição
Se você deseja contribuir para este projeto, siga as etapas abaixo:

Faça um fork do projeto.
Crie um branch para sua contribuição (git checkout -b feature/MinhaContribuicao).
Faça as alterações desejadas no Logisim.
Faça o commit das suas alterações (git commit -m 'Adicionando minha contribuição').
Faça o push para o branch (git push origin feature/MinhaContribuicao).
Abra um pull request descrevendo suas alterações.
Licença
Este projeto está licenciado sob a [Nome da Licença]. Consulte o arquivo LICENSE.md para obter mais detalhes.

Contato
Em caso de dúvidas ou sugestões, entre em contato com [Nome do Contato] por e-mail em [Email do Contato].

Anotações Adicionais
Aqui estão algumas anotações que podem ser úteis ao trabalhar com o processador MIPS monociclo no Logisim:

Registrador PC: O contador do programa (PC) é incrementado a cada ciclo de clock por 4 unidades. O somador recebe a saída do PC constante 4 e sua saída está conectada à entrada do PC.

Memória de Programa: Responsável por armazenar o código em assembly do MIPS. A instrução é decodificada em uma sequência de 32 bits, dividida em sequências menores. Por isso, na saída, há um distribuidor que realiza a divisão.

MUX: Define qual entrada será selecionada para escrita (RW).

Banco de Registradores: O RW define o endereço dentro do banco de dados em que as informações de entrada serão registradas, de acordo com o endereço.

ULA: Recebe as saídas A e B do Banco de Dados (BD).

MUX 2: Define se a entrada B será o valor do registrador (BD) ou o valor imediato.

Extensor de Sinal: Transforma 16 bits em 32 bits, já que a ULA trabalha com 32 bits.

Funções de Controle: Essas funções incluem REGWRITE (define se o valor W será registrado no BD), RESET, REGDST (qual sequência de bits guarda o endereço - 0 para I, 1 para R), ALUSCR (define 0 para R - vindo do BD, 1 para I - imediato) e ALUOP (operador da ULA).

Instruções de Memória: As instruções do tipo lw (load) e sw (store) são usadas para leitura e escrita na memória, respectivamente.

BRANCH: Utilizado nas instruções beq e bne. Define se a soma do PC será a mesma do circuito passado. Para beq, ocorre um salto quando os valores são iguais. Para bne, ocorre um salto quando os valores são diferentes.

MEMWRITE: Habilita a escrita na memória.

MEMREAD: Habilita a leitura na memória.

MEMTOREG: Define se o dado a ser escrito no registrador vem da memória.

Diversas instruções do tipo R e I são suportadas pelo processador MIPS monociclo implementado no Logisim.

É possível acompanhar as operações do processador e verificar os resultados nas saídas apropriadas, como registradores e memória de dados.

Certifique-se de consultar a documentação e o projeto específico para obter mais detalhes sobre a implementação do processador MIPS monociclo no Logisim.