 1. O que o programa faz

Esse programa serve para cadastrar e avaliar o desempenho de alunos com base em suas duas notas.
Ele:

Pede o número de alunos;

Para cada aluno, solicita:

Nome

RGM (ou matrícula)

Duas notas

Calcula a média das duas notas;

Exibe o resultado final, mostrando se o aluno está:

Aprovado (média ≥ 6)

Em recuperação (média > 4 e < 6)

Reprovado (média ≤ 4)

 2. Tecnologias e recursos utilizados

Linguagem: C

Bibliotecas:

<stdio.h> → usada para entrada e saída de dados (funções como printf e scanf).

<string.h> → incluída, mas não está sendo utilizada no código atual.

Estruturas e recursos de C:

struct → para agrupar informações do estudante (nome, matrícula, notas, média etc.).

for → para repetição, percorrendo os alunos.

Condicionais if/else → para verificar resultados e validar o número de alunos.

💻 3. Como instalar, compilar e executar o código
🧩 Pré-requisitos

Ter um compilador C instalado, como:

GCC (Linux/Mac/Windows com MinGW)

Code::Blocks

Dev-C++

Visual Studio Code com extensão C/C++ da Microsoft

 Compilação via terminal

Salve o código com o nome alunos.c

No terminal, vá até o diretório do arquivo e digite:

gcc alunos.c -o alunos


Depois execute:

./alunos

 4. Exemplos de uso
Entrada:
Numero de alunos: 2
Digite seu nome: Ana
Digite seu rgm: 123
sua primeira nota: 8
sua segunda nota: 7

Digite seu nome: João
Digite seu rgm: 456
sua primeira nota: 5
sua segunda nota: 3

Saída:
-----------------------------------------
Media do Ana: 7.50 
Aprovado(a)!
-----------------------------------------
Media do João: 4.00 
Reprovado(a)!

 5. Informações adicionais

A estrutura struct Estudante está sendo usada para um aluno por vez, mesmo dentro do for.
Para armazenar vários alunos, seria melhor usar um vetor de estruturas, como:

struct Estudante alunos[50];


Assim, cada aluno teria seus próprios dados guardados.

O limite de alunos é entre 1 e 49, conforme a validação no if.

Para ler nomes com espaços (como “Maria Silva”), é melhor usar:

scanf(" %[^\n]", aluno.nome);


em vez de scanf("%s", &aluno.nome);
