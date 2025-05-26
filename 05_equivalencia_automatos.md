# Equivalência de Autômatos (AFD e AFN)

## 1. Introdução ao Tema

A equivalência de autômatos é o estudo de quando dois autômatos reconhecem a mesma linguagem. Saber provar equivalência é fundamental para simplificação, otimização e transformação de autômatos.

---

## 2. Módulos Temáticos

### Módulo 1: Conceito de Equivalência

- **Meta:** Entender o que significa dois autômatos serem equivalentes.
- **Conteúdo:**
  - Definição formal de equivalência
  - Exemplos de autômatos equivalentes
- **Exemplo:**
  - Dois AFDs diferentes que reconhecem a linguagem das palavras com número par de 'a'.
- **Exercício sugerido:**
  - Dê exemplos de autômatos equivalentes e não equivalentes.

### Módulo 2: Prova de Equivalência

- **Meta:** Aprender métodos para provar equivalência de autômatos.
- **Conteúdo:**
  - Teste de equivalência por simulação
  - Minimização de AFDs
  - Construção do produto para diferença de linguagens
- **Exemplo:**
  - Minimize um AFD e compare com outro.
- **Exercício sugerido:**
  - Dado dois autômatos, verifique se são equivalentes usando minimização.

### Módulo 3: Equivalência entre AFD e AFN

- **Meta:** Compreender que todo AFN tem um AFD equivalente.
- **Conteúdo:**
  - Algoritmo de determinização (construção do subconjunto)
  - Prova de equivalência entre AFD e AFN
- **Exemplo:**
  - Converta um AFN em AFD e mostre que reconhecem a mesma linguagem.
- **Exercício sugerido:**
  - Dado um AFN, construa o AFD equivalente.

---

## 3. Exemplos Práticos

- Dois autômatos para (ab)\*: um AFD e um AFN.
- Minimização de AFD para a linguagem das palavras que terminam com '0'.

---

## 4. Exercícios de Fixação

1. Dê um exemplo de dois autômatos não equivalentes.

<!-- RESOLUÇÃO E EXPLICAÇÃO DIDÁTICA -->

**Resolução:**

- AFD1: reconhece palavras sobre {a, b} com número par de 'a'.
- AFD2: reconhece palavras sobre {a, b} que terminam com 'a'.

Exemplo:

- Palavra "ba":
  - AFD1: "ba" tem 1 'a' (ímpar) → rejeita.
  - AFD2: termina com 'a' → aceita.
- Portanto, AFD1 e AFD2 não são equivalentes.

---

2. Minimize um AFD e verifique se ele é equivalente ao original.

<!-- RESOLUÇÃO E EXPLICAÇÃO DIDÁTICA -->

**Resolução:**

- Considere o AFD para palavras sobre {0,1} que terminam com "01":

Estados: q0 (inicial), q1, q2 (final)

- δ(q0, 0) → q1
- δ(q0, 1) → q0
- δ(q1, 0) → q1
- δ(q1, 1) → q2
- δ(q2, 0) → q1
- δ(q2, 1) → q0

Esse AFD já está minimizado, pois todos os estados têm comportamento distinto para o sufixo "01".
**Verificação:** Teste palavras como "01", "1001", "0001" e veja que o comportamento é igual no original e no minimizado.

---

3. Converta um AFN simples em AFD e compare as linguagens reconhecidas.

<!-- RESOLUÇÃO E EXPLICAÇÃO DIDÁTICA -->

**Resolução:**

- AFN: reconhece palavras sobre {a, b} que contêm "ab" como subpalavra.
- Estados: q0 (inicial), q1, q2 (final)
  - δ(q0, a) → {q0, q1}
  - δ(q0, b) → {q0}
  - δ(q1, b) → {q2}
  - δ(q2, a) → {q2}
  - δ(q2, b) → {q2}

**Construção do AFD (por subconjuntos):**

- Estados do AFD: subconjuntos dos estados do AFN.
- Estado inicial: {q0}
- Transições:
  - {q0} --a--> {q0, q1}
  - {q0} --b--> {q0}
  - {q0, q1} --a--> {q0, q1}
  - {q0, q1} --b--> {q0, q2}
  - {q0, q2} --a--> {q0, q1, q2}
  - {q0, q2} --b--> {q0, q2}
  - etc.

**Conclusão:** O AFD reconhece a mesma linguagem do AFN, pois todo caminho aceito no AFN é simulado no AFD.

---

## 5. Autoavaliação

- [ ] Sei identificar autômatos equivalentes
- [ ] Consigo provar equivalência por simulação ou minimização
- [ ] Sei converter AFN em AFD equivalente

---

## 6. Recursos Adicionais

- [JFLAP](http://www.jflap.org/)
- Hopcroft, Motwani & Ullman, Cap. 4
- Sipser, Cap. 1 e 2
