# Operações com Autômatos

## 1. Introdução às Operações com Autômatos

### 1.1 O que são operações sobre linguagens?

- **Operações sobre linguagens** são formas de combinar, modificar ou transformar linguagens, resultando em novas linguagens.
- As principais operações estudadas em linguagens regulares são:
  - **União** (L1 ∪ L2): palavras que pertencem a L1 ou L2
  - **Interseção** (L1 ∩ L2): palavras que pertencem a L1 e L2
  - **Complemento** (L̅): palavras que não pertencem a L
  - **Diferença** (L1 - L2): palavras que pertencem a L1 mas não a L2
  - **Concatenação** (L1L2): palavras formadas por uma palavra de L1 seguida de uma de L2
  - **Fechamento de Kleene** (L\*): todas as concatenações finitas de palavras de L (incluindo a palavra vazia)
  - **Reversão** (L^R): todas as palavras de L escritas ao contrário

### 1.2 Por que estudar operações com autômatos?

- Permite construir autômatos para linguagens mais complexas a partir de autômatos simples.
- Ajuda a entender as propriedades de fechamento das linguagens regulares.
- É fundamental para resolver problemas de decisão e análise de linguagens.

---

## 2. Exemplos de Operações

### 2.1 União

Seja L1 = {palavras com número par de 'a'} e L2 = {palavras que terminam com 'b'}.

- L1 ∪ L2 = {palavras que têm número par de 'a' **ou** terminam com 'b'}

**Exemplo:**

- "aab" (número par de 'a' e termina com 'b') ∈ L1 ∪ L2
- "ab" (número ímpar de 'a', mas termina com 'b') ∈ L1 ∪ L2
- "aa" (número par de 'a', não termina com 'b') ∈ L1 ∪ L2
- "aba" (número par de 'a', não termina com 'b') ∈ L1 ∪ L2

### 2.2 Interseção

L1 ∩ L2 = {palavras com número par de 'a' **e** que terminam com 'b'}

**Exemplo:**

- "aab" ∈ L1 ∩ L2
- "ab" ∉ L1 ∩ L2 (número ímpar de 'a')
- "aa" ∉ L1 ∩ L2 (não termina com 'b')

### 2.3 Complemento

Se L = {palavras que contêm pelo menos um 'a'}, então L̅ = {palavras que **não** contêm 'a'}

**Exemplo:**

- "bbb" ∈ L̅
- "ab" ∉ L̅

### 2.4 Diferença

L1 - L2 = {palavras com número par de 'a' **e** que **não** terminam com 'b'}

> obs: a ordem dos conjuntos é importante, L1 - L2 != L2 - L1

**Exemplo:**

- "aa" ∈ L1 - L2
- "aab" ∉ L1 - L2 (termina com 'b')

### 2.5 Concatenação

Se L1 = {a, aa}, L2 = {b, bb}, então L1L2 = {ab, abb, aab, aabb}

### 2.6 Fechamento de Kleene

Se L = {ab}, então L\* = {ε, ab, abab, ababab, ...}

### 2.7 Reversão

Se L = {ab, ba}, então L^R = {ba, ab}

---

## 3. Exercícios Práticos

1. Dê exemplos de união e interseção de linguagens sobre {a, b}:

   - L1 = {palavras que começam com 'a'}
   - L2 = {palavras que terminam com 'b'}
   - Liste 2 palavras que pertencem a L1 ∪ L2 e 2 que pertencem a L1 ∩ L2.

```
L1 ∪ L2 = {palavras que começam com 'a' ou terminam com 'b'}
L1 ∩ L2 = {palavras que começam com 'a' e terminam com 'b'}

Palavras que pertencem a L1 ∪ L2:
- "aabab" (começa com 'a')
- "bbbab" (termina com 'b')

Palavras que não pertencem a L1 ∪ L2:
- "bba" (não começa com 'a' nem termina com 'b')
- "ba" (não começa com 'a' nem termina com 'b')

Palavras que pertencem a L1 ∩ L2:
- "aab" (começa com 'a' e termina com 'b')
- "abab" (começa com 'a' e termina com 'b')

Palavras que não pertencem a L1 ∩ L2:
- "bba" (não começa com 'a')
- "aaa" (não termina com 'b')
```

**Explicação:**

- Para L1 ∪ L2, basta que a palavra comece com 'a' ou termine com 'b'.
- Para L1 ∩ L2, a palavra deve começar com 'a' **e** terminar com 'b'.
- Os exemplos acima ilustram corretamente cada caso.

2. Dado um AFD para L, descreva como construir o AFD para o complemento de L.

```
Passo a passo para construir o complemento de um AFD:
1. Certifique-se de que o AFD é completo (todas as transições estão definidas para cada símbolo em cada estado). Se não estiver, adicione um estado de erro e complete as transições.
2. Inverta o conjunto de estados finais: os estados que eram finais deixam de ser, e os que não eram finais passam a ser finais.
3. O autômato resultante reconhece o complemento da linguagem original.

Exemplo:
Se o AFD original tem estados finais F, o complemento terá como estados finais Q \ F (todos os estados que não estão em F).
```

3. Construa um AFN para a concatenação das linguagens L1 = {a, aa} e L2 = {b, bb}.

```
Passo a passo:
- L1 = {a, aa}
- L2 = {b, bb}
- L1L2 = {ab, abb, aab, aabb}

Construção do AFN:
- Estados: q0 (inicial), q1, q2, q3 (finais)
- Transições:
  - q0 --a--> q1
  - q0 --a--> q2 (para aceitar 'aa')
  - q1 --b--> q3 (aceita 'ab')
  - q1 --b--> q3 (aceita 'abb' via transição epsilon para q2)
  - q2 --a--> q1 (para formar 'aa')
  - q2 --b--> q3 (aceita 'aab')
  - q2 --b--> q3 (aceita 'aabb')

AFN simplificado:
- q0 --a--> q1 (para 'a')
- q0 --a--> q2 (para 'aa')
- q1 --b--> q3 (para 'ab')
- q1 --b--> q3 (para 'abb' via q2)
- q2 --b--> q3 (para 'aab')
- q2 --b--> q3 (para 'aabb')
- q3 é final

Exemplo de aceitação:
- "ab": q0 --a--> q1 --b--> q3
- "abb": q0 --a--> q1 --b--> q3 (q3 aceita mais um 'b' se for necessário)
- "aab": q0 --a--> q2 --b--> q3
- "aabb": q0 --a--> q2 --b--> q3 (q3 aceita mais um 'b' se for necessário)

Obs: Como as linguagens são finitas, o AFN pode ser construído explicitamente para cada palavra. Além disso, vale notar que o estado q0 não deve aceitar "b".
```

4. Dado um AFN para L, explique como construir o AFN para L\*.

```
Passo a passo para construir o AFN para L*:
1. Crie um novo estado inicial q_new, que também será estado final.
2. Adicione uma transição epsilon de q_new para o estado inicial do AFN original.
3. Para cada estado final do AFN original, adicione uma transição epsilon de volta para o estado inicial do AFN original.
4. O novo autômato aceita qualquer número de repetições (inclusive zero) de palavras de L.

Exemplo:
- Se o AFN original reconhece L, o novo AFN reconhece L\*.
- A palavra vazia é aceita diretamente em q_new.
```

---

## 4. Autoavaliação

### Checklist de Competências

- [x] Entendo o conceito de operações sobre linguagens
- [x] Sei construir autômatos para união, interseção e complemento
- [x] Consigo construir autômatos para concatenação e fechamento de Kleene
- [x] Sei aplicar operações em exemplos práticos

### Exercícios de Fixação

1. Dado o alfabeto Σ = {a, b}, construa um autômato para a linguagem das palavras que contêm número par de 'a' **ou** terminam com 'b'.
2. Dado um AFD para L, construa o AFD para o complemento de L.
3. Construa um AFN para a linguagem (ab)\*.
4. Dado um AFN para L, construa o AFN para L^R (reverso).

---

## 5. Recursos Adicionais

- [JFLAP](http://www.jflap.org/) - Para desenhar e simular autômatos
- [Regex101](https://regex101.com/) - Para testar expressões regulares
- Hopcroft, J. E., Motwani, R., & Ullman, J. D. (2006). Introduction to Automata Theory, Languages, and Computation
- Sipser, M. (2012). Introduction to the Theory of Computation

## Dicas de Estudo e Autoavaliação

- Sempre desenhe os diagramas dos autômatos para cada operação.
- Teste exemplos práticos: crie palavras e verifique se o autômato resultante aceita ou rejeita corretamente.
- Explique para si mesmo cada passo da construção.
- Ao final de cada semana, tente criar um exercício próprio e resolvê-lo.
