# Linguagens Formais e Autômatos

Este repositório contém o material de estudo para a disciplina de Linguagens Formais e Autômatos, organizado nos seguintes tópicos:

1. [Linguagens Regulares](01_linguagens_regulares.md)
2. [Construção de Autômatos](02_construcao_automatos.md)
3. [Operações com Autômatos](03_operacoes_automatos.md)
4. [Séries Regulares](04_series_regulares.md)
5. [Equivalência de Autômatos](05_equivalencia_automatos.md)
6. [Transformação entre Autômatos e Expressões Regulares](06_expressoes_regulares.md)
7. [Gramáticas](07_gramaticas.md)
   - Derivar
   - Autômatos com Pilha
   - Reconhecimento de Cadeias
8. [Máquinas de Turing](08_maquinas_turing.md)

## Aprendizados

### Linguagens regulares

- **Estrela de Kleene**: o que estiver à esquerda da estrela pode se repetir zero ou mais vezes.
  > Obs: a estrela de Kleene sempre inclui a palavra vazia.

### Construção de Autômatos

- **Transições Epsilon (ε):** Transições "espontâneas" em AFNs que não consomem símbolos de entrada. Úteis na construção de AFNs a partir de operações com linguagens (união, concatenação, estrela de Kleene) e para simplificação.
