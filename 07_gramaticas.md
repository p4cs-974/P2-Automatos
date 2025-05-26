# Gramáticas e Autômatos com Pilha

## 1. Introdução ao Tema

Gramáticas formais são sistemas de regras para gerar linguagens. Elas permitem descrever linguagens mais complexas que as regulares. O estudo de gramáticas e autômatos com pilha (AP) é essencial para entender análise sintática e reconhecimento de linguagens livres de contexto.

---

## 2. Módulos Temáticos

### Módulo 1: Definição e Tipos de Gramáticas

- **Meta:** Compreender o conceito de gramática formal e seus tipos.
- **Conteúdo:**
  - Definição de gramática
  - Gramáticas regulares, livres de contexto, sensíveis ao contexto e irrestritas
- **Exemplo:**
  - Gramática para a linguagem (a^n b^n)
- **Exercício sugerido:**
  - Classifique gramáticas dadas quanto ao tipo.

### Módulo 2: Derivação e Reconhecimento de Cadeias

- **Meta:** Saber derivar cadeias e reconhecer se pertencem à linguagem da gramática.
- **Conteúdo:**
  - Derivação à esquerda e à direita
  - Árvores de derivação
- **Exemplo:**
  - Derive a cadeia "aabb" em uma gramática para (a^n b^n)
- **Exercício sugerido:**
  - Dada uma gramática, derive cadeias e construa árvores de derivação.

### Módulo 3: Autômatos com Pilha (AP)

- **Meta:** Relacionar gramáticas livres de contexto com autômatos com pilha.
- **Conteúdo:**
  - Definição de AP
  - Conversão de gramática para AP
- **Exemplo:**
  - Construa um AP para a linguagem (a^n b^n)
- **Exercício sugerido:**
  - Dada uma gramática, construa o AP correspondente.

---

## 3. Exemplos Práticos

- Gramática para palíndromos sobre {a, b}
- Derivação de "abba" em uma gramática livre de contexto

---

## 4. Exercícios de Fixação

1. Classifique as gramáticas abaixo quanto ao tipo.

<!-- RESOLUÇÃO E EXPLICAÇÃO DIDÁTICA -->

**Resolução:**

- Exemplo 1: S → aSb | ε
  - É uma gramática livre de contexto (GLC), pois a produção tem uma variável à esquerda.
- Exemplo 2: S → aS | bS | ε
  - Também é GLC.
- Exemplo 3: S → aA, A → b
  - É regular, pois as produções têm uma variável à esquerda e no máximo uma variável à direita.

---

2. Derive a cadeia "aaabbb" em uma gramática para (a^n b^n).

<!-- RESOLUÇÃO E EXPLICAÇÃO DIDÁTICA -->

**Resolução:**

- Gramática: S → aSb | ε
- Derivação:
  - S ⇒ aSb
  - ⇒ aaSbb
  - ⇒ aaaSbbb
  - ⇒ aaabbb

---

3. Construa um AP para a linguagem de palíndromos.

<!-- RESOLUÇÃO E EXPLICAÇÃO DIDÁTICA -->

**Resolução:**

- Alfabeto: {a, b}
- Estratégia: empilhar símbolos da primeira metade, desempilhar e comparar na segunda metade.
- O AP aceita se, ao final, a pilha estiver vazia e todos os símbolos corresponderem.

---

## 5. Autoavaliação

- [ ] Sei classificar gramáticas
- [ ] Sei derivar cadeias e construir árvores de derivação
- [ ] Sei construir APs a partir de gramáticas

---

## 6. Recursos Adicionais

- [JFLAP](http://www.jflap.org/)
- Hopcroft, Motwani & Ullman, Cap. 5
- Sipser, Cap. 2
