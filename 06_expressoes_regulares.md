# Transformação entre Autômatos e Expressões Regulares

## 1. Introdução ao Tema

A relação entre autômatos e expressões regulares é fundamental: toda linguagem regular pode ser descrita por ambos. Saber transformar um autômato em expressão regular (e vice-versa) é essencial para análise e projeto de sistemas de reconhecimento de padrões.

---

## 2. Módulos Temáticos

### Módulo 1: De Expressão Regular para Autômato

- **Meta:** Aprender a construir um AFN a partir de uma expressão regular.
- **Conteúdo:**
  - Algoritmo de construção de Thompson
  - Exemplos de conversão
- **Exemplo:**
  - Construa um AFN para a expressão (a|b)\*abb
- **Exercício sugerido:**
  - Dada uma expressão regular, construa o AFN correspondente.

### Módulo 2: De Autômato para Expressão Regular

- **Meta:** Aprender a obter uma expressão regular a partir de um autômato.
- **Conteúdo:**
  - Algoritmo de eliminação de estados
  - Exemplos de conversão
- **Exemplo:**
  - Dado um AFD simples, derive a expressão regular equivalente.
- **Exercício sugerido:**
  - Dado um autômato, obtenha a expressão regular correspondente.

### Módulo 3: Propriedades e Aplicações

- **Meta:** Entender aplicações práticas e propriedades das transformações.
- **Conteúdo:**
  - Propriedades de equivalência
  - Aplicações em análise léxica
- **Exemplo:**
  - Mostre que a linguagem reconhecida por um autômato é regular.
- **Exercício sugerido:**
  - Dê exemplos de uso prático das transformações.

---

## 3. Exemplos Práticos

- Construa um AFN para (a|b)\*a.
- Dado um AFD para (01)\*, obtenha a expressão regular equivalente.

---

## 4. Exercícios de Fixação

1. Construa um AFN para a expressão regular (ab|ba)\*.
2. Dado um AFD, derive a expressão regular correspondente.
3. Explique por que toda linguagem reconhecida por um AFD é regular.

---

## 5. Autoavaliação

- [ ] Sei converter expressões regulares em autômatos
- [ ] Sei converter autômatos em expressões regulares
- [ ] Entendo as aplicações práticas dessas transformações

---

## 6. Recursos Adicionais

- [JFLAP](http://www.jflap.org/)
- Hopcroft, Motwani & Ullman, Cap. 3
- Sipser, Cap. 1
