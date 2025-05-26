# Linguagens Regulares

## 1. Introdução às Linguagens Regulares

### 1.1 Conceitos Básicos

- Alfabeto (Σ): conjunto finito de símbolos
- Palavra: sequência finita de símbolos do alfabeto
- Linguagem: conjunto de palavras sobre um alfabeto
- Linguagem Regular: linguagem que pode ser reconhecida por um autômato finito

### 1.2 Propriedades das Linguagens Regulares

- Fechamento sob:
  - União
  - Concatenação
  - Estrela de Kleene (\*)
  - Complemento
  - Interseção
  - Diferença

## 2. Expressões Regulares

### 2.1 Operadores Básicos

- Concatenação (ab)
- União (a|b)
- Estrela de Kleene (a\*)
- Opcional (a?)
- Positivo (a+)

### 2.2 Exemplos de Expressões Regulares

1. Palavras que começam com 'a' e terminam com 'b':

   ```
   a(a|b)*b
   ```

2. Palavras com comprimento par:

   ```
   ((a|b)(a|b))*
   ```

3. Palavras que contêm pelo menos um 'a':
   ```
   (a|b)*a(a|b)*
   ```

## 3. Exercícios Práticos

### Exercício 1: Identificação de Linguagens

Para cada linguagem abaixo, escreva uma expressão regular e mostre:

- 2 palavras que pertencem à linguagem
- 2 palavras que não pertencem à linguagem

1. Linguagem de todas as palavras sobre {a,b} que começam com 'a' e terminam com 'b'

   - Pertencem: "ab", "aab"
   - Não pertencem: "ba", "bb"

```
começa com a -> a
termina com b -> a___b
qualquer coisa pode estar entre eles -> a(a|b)*b
```

```
a(a|b)*b
```

> **Correção:** Sua expressão regular `a(a|b)*b` está correta para essa linguagem! Os exemplos de palavras pertencentes ("ab", "aab") e não pertencentes ("ba", "bb") também estão corretos. Muito bem!

2. Linguagem de todas as palavras sobre {0,1} que contêm pelo menos dois '1's consecutivos

   - Pertencem: "011", "1100"
   - Não pertencem: "0101", "1000"

```
coném dois '1's consecutivos -> __11__
pode ter qualquer coisa antes -> (0|1)*11__
pode ter qualquer coisa depois -> (0|1)*11(0|1)*
```

```
(0|1)*11(0|1)*
```

> **Correção:** Sua expressão regular `(0|1)*11(0|1)*` está perfeita! Ela captura corretamente a ideia de ter "11" em qualquer posição da string, com qualquer combinação de 0s e 1s antes e depois. Os exemplos também estão corretos. Excelente!

3. Linguagem de todas as palavras sobre {a,b} que terminam com 'a'
   - Pertencem: "a", "ba"
   - Não pertencem: "b", "ab"

```
terminam com a -> __a
pode ter qualquer coisa antes -> (a|b)*a
```

```
(a|b)*a
```

> **Correção:** Sua expressão regular `(a|b)*a` está correta. Ela representa qualquer sequência de 'a's ou 'b's seguida por um 'a', garantindo que termine com 'a'. No entanto, revise seus exemplos de palavras que NÃO pertencem. A palavra "ab" _não_ pertence a essa linguagem (termina com 'b'), então está correta como "Não pertencem". Mas a palavra "b" _não_ pertence a essa linguagem (termina com 'b'), então também está correta como "Não pertencem". Seus exemplos de palavras que _pertencem_ ("a", "ba") estão corretos. O exemplo de palavra que _não_ pertence "ab" está correto. O exemplo de palavra que _não_ pertence "b" está correto. Parece que você listou os exemplos corretamente, apenas a minha interpretação inicial foi confusa. Desculpe! Seus exemplos estão OK.

### Exercício 2: Construção de Expressões Regulares

Construa expressões regulares para as seguintes linguagens:

1. Todas as palavras sobre {a,b} que contêm exatamente dois 'a's
2. Todas as palavras sobre {0,1} que representam números binários pares
3. Todas as palavras sobre {a,b} que não contêm a subpalavra "aba"

### Exercício 3: Análise de Linguagens

Para cada expressão regular abaixo, descreva em português a linguagem que ela representa:

1. `(a|b)*a(a|b)*`

```
Palavras dessa linguagem devem conter pelo menos uma letra 'a' em qualquer posição.
```

> **Correção:** Sua descrição está **correta**! A expressão `(a|b)*` representa qualquer sequência de 'a's e 'b's (incluindo a vazia), e o 'a' no meio garante que a palavra contenha pelo menos um 'a'. Muito bom!

2. `(0|1)*00(0|1)*`

```
Palavras dessa linguagem devem conter a sequência '00' em qualquer posição.
```

> **Correção:** Sua descrição está **correta** novamente! A expressão `(0|1)*` antes e depois do `00` permite qualquer combinação de 0s e 1s nos extremos, enquanto o `00` garante a subpalavra. Excelente!

3. `(a|b)*aba(a|b)*`

```
Palabras dessa linguagem devem conter a sequência 'aba' em qualquer posiçãp
```

> **Correção:** Sua descrição está **quase perfeita**! A ideia está certa: a linguagem contém palavras que possuem a subpalavra "aba". A pequena correção é apenas na grafia da palavra "posição". Fora isso, a análise está correta!

## 4. Autoavaliação

### Checklist de Competências

- [x] Entendo o conceito de alfabeto e palavra
- [x] Compreendo o que é uma linguagem regular
- [x] Sei construir expressões regulares básicas
- [x] Consigo identificar palavras que pertencem/não pertencem a uma linguagem
- [x] Entendo as propriedades de fechamento das linguagens regulares

### Exercícios de Fixação

1. Dado o alfabeto Σ = {a,b}, liste todas as palavras de comprimento 2

```
aa
ab
ba
bb
```

> **Correção:** Lista completa e **correta**! Essas são exatamente todas as palavras de comprimento 2 sobre o alfabeto {a,b}.

2. Construa uma expressão regular para a linguagem de todas as palavras sobre {0,1} que terminam com '01'

```
(0|1)*01
```

> **Correção:** Sua expressão regular `(0|1)*01` está **correta**! Ela representa qualquer sequência de 0s ou 1s seguida pela sequência "01".

3. Mostre que a linguagem L = {a^n b^n | n ≥ 0} não é regular

```
// Resolução do Exercício de Fixação nº 3:
// Para provar que a linguagem L = {a^n b^n | n ≥ 0} não é regular, utilizaremos o Lema do Bombeamento (Pumping Lemma) para linguagens regulares.
// O Lema do Bombeamento afirma que, se uma linguagem L é regular, então existe um número p (o comprimento do bombeamento) tal que qualquer palavra s em L com |s| >= p pode ser dividida em três partes, s = xyz, satisfazendo as seguintes condições:
// 1. |y| > 0 (a parte do meio, y, não é vazia)
// 2. |xy| <= p (as duas primeiras partes juntas não excedem o comprimento do bombeamento)
// 3. Para todo i >= 0, a palavra xy^i z pertence a L (podemos 'bombear' a parte y qualquer número de vezes, e a palavra resultante ainda estará na linguagem)

// Vamos escolher uma palavra s em L tal que |s| >= p. Uma escolha conveniente é s = a^p b^p.
// O comprimento de s é |s| = p + p = 2p, que é >= p.

// Agora, de acordo com o Lema do Bombeamento, s = a^p b^p pode ser dividida em xyz, onde |y| > 0 e |xy| <= p.
// Dado que |xy| <= p, as partes x e y devem consistir apenas de 'a's, pois as primeiras p letras de s são 'a's.
// Portanto, y deve ter a forma a^k para algum k >= 1 (já que |y| > 0).
// Assim, x = a^j e y = a^k e z = a^(p-j-k) b^p, onde j+k <= p e k >= 1.

// Agora vamos aplicar a terceira condição do Lema: xy^i z deve pertencer a L para todo i >= 0.
// Considere o caso i = 2. A palavra resultante é xy^2 z = (a^j)(a^k)^2(a^(p-j-k) b^p) = a^j a^(2k) a^(p-j-k) b^p = a^(j + 2k + p - j - k) b^p = a^(p+k) b^p.

// A palavra a^(p+k) b^p tem p+k ocorrências de 'a' e p ocorrências de 'b'.
// Para que esta palavra pertença à linguagem L = {a^n b^n | n ≥ 0}, o número de 'a's deve ser igual ao número de 'b's, ou seja, p+k = p.
// No entanto, sabemos que k >= 1, o que implica que p+k > p.
// Portanto, a^(p+k) b^p não pertence à linguagem L para i = 2.

// Isso contradiz a terceira condição do Lema do Bombeamento. Como encontramos uma contradição, a suposição inicial de que L é regular deve ser falsa.

// Conclusão: A linguagem L = {a^n b^n | n ≥ 0} não é regular.
```

## 5. Recursos Adicionais

### Ferramentas Online

- [Regex101](https://regex101.com/) - Para testar expressões regulares
- [JFLAP](http://www.jflap.org/) - Para visualizar autômatos

### Referências

- Hopcroft, J. E., Motwani, R., & Ullman, J. D. (2006). Introduction to Automata Theory, Languages, and Computation
- Sipser, M. (2012). Introduction to the Theory of Computation
