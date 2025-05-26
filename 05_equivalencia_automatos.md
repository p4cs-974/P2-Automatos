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
2. Minimize um AFD e verifique se ele é equivalente ao original.
3. Converta um AFN simples em AFD e compare as linguagens reconhecidas.

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
