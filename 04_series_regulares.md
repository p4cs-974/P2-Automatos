# Séries Regulares

## 1. Introdução ao Tema

As séries regulares são subconjuntos de linguagens regulares com propriedades específicas, frequentemente usadas para descrever padrões e resolver problemas clássicos de reconhecimento de cadeias. Estudar séries regulares ajuda a consolidar o entendimento sobre autômatos e expressões regulares.

---

## 2. Módulos Temáticos

### Módulo 1: Definição e Exemplos de Séries Regulares

- **Meta:** Compreender o conceito de série regular e identificar exemplos clássicos.
- **Conteúdo:**
  - O que é uma série regular?
  - Diferença entre linguagem regular e série regular
  - Exemplos de séries regulares sobre {a, b}
- **Exemplo:**
  - Série das palavras que começam com 'a'
  - Série das palavras que contêm número par de 'b'
- **Exercício sugerido:**
  - Liste 2 palavras que pertencem e 2 que não pertencem a cada série regular apresentada.

### Módulo 2: Construção e Análise de Séries Regulares

- **Meta:** Saber construir e analisar séries regulares a partir de descrições.
- **Conteúdo:**
  - Como descrever uma série regular usando expressão regular ou autômato
  - Como testar se uma palavra pertence à série
- **Exemplo:**
  - Dada a série das palavras que terminam com 'ab', construa um autômato correspondente.
- **Exercício sugerido:**
  - Para cada série dada, construa um autômato e teste 2 palavras que pertencem e 2 que não pertencem.

### Módulo 3: Propriedades e Aplicações

- **Meta:** Entender propriedades e aplicações práticas das séries regulares.
- **Conteúdo:**
  - Propriedades de fechamento
  - Aplicações em reconhecimento de padrões
- **Exemplo:**
  - Mostre que a união de duas séries regulares é uma série regular.
- **Exercício sugerido:**
  - Dê exemplos de aplicações práticas de séries regulares.

---

## 3. Exemplos Práticos

- Série: Palavras sobre {0,1} com número ímpar de '1'.
  - Pertencem: "1", "011"
  - Não pertencem: "0", "1100"
- Série: Palavras sobre {a,b} que não contêm "bb".
  - Pertencem: "ab", "ba"
  - Não pertencem: "bb", "abb"

---

## 4. Exercícios de Fixação

1. Dada a série das palavras que contêm exatamente dois 'a's, liste 2 palavras que pertencem e 2 que não pertencem.

<!-- RESOLUÇÃO E EXPLICAÇÃO DIDÁTICA -->

**Resolução:**

- A série é composta por todas as palavras sobre {a, b} que contêm exatamente dois 'a's (ou seja, qualquer quantidade de 'b', mas apenas dois 'a').
- Exemplos que **pertencem**:
  - "aba" (tem dois 'a's e um 'b')
  - "baa" (tem dois 'a's e um 'b')
- Exemplos que **não pertencem**:
  - "abbb" (tem apenas um 'a', não pertence)
  - "aaa" (tem três 'a's, não pertence)

---

2. Construa um autômato para a série das palavras que terminam com 'b'.

<!-- RESOLUÇÃO E EXPLICAÇÃO DIDÁTICA -->

**Resolução:**

- Alfabeto: {a, b}
- Precisamos de um autômato que aceite qualquer palavra que termine com 'b'.

**Construção:**

- Estados: q0 (inicial), q1 (final)
- Transições:
  - q0 --a--> q0 (lendo 'a', permanece em q0)
  - q0 --b--> q1 (lendo 'b', vai para q1)
  - q1 --a--> q0 (se depois de um 'b' vier um 'a', volta para q0)
  - q1 --b--> q1 (se vier outro 'b', permanece em q1)
- Estado inicial: q0
- Estado final: q1

**Tabela de transição:**

| Estado | a   | b   |
| ------ | --- | --- |
| q0     | q0  | q1  |
| q1     | q0  | q1  |

**Explicação:**
O autômato aceita qualquer palavra que termine com 'b', pois só estará em q1 ao final se o último símbolo for 'b'.

---

3. Explique por que toda série regular é uma linguagem regular.

<!-- RESOLUÇÃO E EXPLICAÇÃO DIDÁTICA -->

**Resolução:**

- Por definição, uma série regular é um subconjunto de uma linguagem regular que pode ser descrito por uma expressão regular ou reconhecido por um autômato finito.
- Toda série regular pode ser reconhecida por um autômato finito, pois é construída a partir de operações regulares (união, concatenação, estrela de Kleene, etc).
- Portanto, toda série regular é, por definição, uma linguagem regular.

**Resposta:**
Toda série regular é uma linguagem regular porque pode ser descrita por uma expressão regular ou reconhecida por um autômato finito, ou seja, satisfaz exatamente a definição de linguagem regular.

---

## 5. Autoavaliação

- [ ] Sei identificar e construir séries regulares
- [ ] Consigo testar se uma palavra pertence a uma série
- [ ] Entendo as propriedades de fechamento das séries regulares

---

## 6. Recursos Adicionais

- [JFLAP](http://www.jflap.org/)
- Hopcroft, Motwani & Ullman, Cap. 2
- Sipser, Cap. 1
