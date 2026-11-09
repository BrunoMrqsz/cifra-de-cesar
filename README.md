# Cifra de César

Projeto de estudo para a matéria de Algoritmo e pensamento computacional em linguagem C que aplica uma variação da Cifra de César utilizando um deslocamento adicional baseado na sequência de Fibonacci.

## Como funciona

1. O programa solicita uma palavra secreta.
2. Solicita um valor inteiro de `SHIFT`.
3. Gera uma sequência de Fibonacci iniciada em `1, 1, 2, 3, 5...`.
4. Para cada caractere, soma o valor de `SHIFT` ao respectivo número da sequência.
5. Desloca a letra no alfabeto (26 posições), produzindo a palavra criptografada.

A regra aplicada a cada posição é:

```
deslocamento = SHIFT + Fibonacci[i]
letra_criptografada = ((letra - 'a' + deslocamento) % 26) + 'a'
```

## Requisitos e limitações da versão atual

- Implementado em C.
- Entrada de até 15 caracteres, sem espaços.
- A implementação atual considera letras minúsculas de `a` a `z`.
- O programa realiza a criptografia; não implementa a descriptografia.
- Trata-se de um exercício didático. A cifra não deve ser utilizada para proteger informações reais.

## Como compilar e executar

Com GCC:

```bash
gcc src/cifra_de_cesar.c -o cifra-de-cesar
./cifra-de-cesar
```

No Windows, usando MinGW:

```bash
gcc src/cifra_de_cesar.c -o cifra-de-cesar.exe
.cifra-de-cesar.exe
```

## Estrutura

```
cifra-de-cesar/
├── src/
│   └── cifra_de_cesar.c
├── .gitignore
└── README.md
```

## Próximas melhorias

- Validar se a entrada contém apenas letras minúsculas.
- Permitir palavras maiores e entradas com espaços.
- Implementar a descriptografia.
- Tratar valores negativos de SHIFT.
