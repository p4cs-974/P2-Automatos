# Máquinas de Turing

## 1. Introdução ao Tema

Máquinas de Turing são modelos matemáticos de computação capazes de reconhecer linguagens mais complexas que os autômatos finitos e de pilha. Elas são fundamentais para entender o conceito de computabilidade e limites do que pode ser resolvido por algoritmos.

---

## 2. Módulos Temáticos

### Módulo 1: Definição e Funcionamento

- **Meta:** Compreender o que é uma máquina de Turing e como ela opera.
- **Conteúdo:**
  - Definição formal
  - Componentes: fita, cabeçote, estados, função de transição
- **Exemplo:**
  - Máquina de Turing que reconhece a linguagem {a^n b^n | n ≥ 1}
- **Exercício sugerido:**
  - Descreva a configuração de uma máquina de Turing para uma palavra de exemplo.

### Módulo 2: Construção de Máquinas de Turing

- **Meta:** Aprender a projetar máquinas de Turing para linguagens específicas.
- **Conteúdo:**
  - Estratégias de construção
  - Exemplos passo a passo
- **Exemplo:**
  - Máquina de Turing para inverter uma palavra
- **Exercício sugerido:**
  - Construa uma máquina de Turing para reconhecer palíndromos.

### Módulo 3: Computabilidade e Decidibilidade

- **Meta:** Entender o que é computável e o que não é.
- **Conteúdo:**
  - Problemas decidíveis e indecidíveis
  - Exemplos clássicos (problema da parada)
- **Exemplo:**
  - Explique por que o problema da parada é indecidível.
- **Exercício sugerido:**
  - Dê exemplos de problemas decidíveis e indecidíveis.

---

## 3. Exemplos Práticos

- Máquina de Turing para somar dois números unários
- Máquina de Turing para reconhecer a linguagem {ww | w ∈ {a, b}\*}

---

## 4. Exercícios de Fixação

1. Descreva a configuração de uma máquina de Turing para a palavra "aabb".

<!-- RESOLUÇÃO E EXPLICAÇÃO DIDÁTICA -->

**Resolução:**

- Exemplo: MT para {a^n b^n | n ≥ 1}
- Configuração inicial: fita = "aabb", cabeçote no primeiro símbolo, estado inicial q0.
- A MT marca o primeiro 'a', procura o primeiro 'b', marca, volta ao início, repete até não restar 'a' ou 'b'.

---

2. Construa uma máquina de Turing para inverter uma palavra.

<!-- RESOLUÇÃO E EXPLICAÇÃO DIDÁTICA -->

**Resolução:**

- Estratégia: use símbolos auxiliares para marcar o início e o fim, trocando os extremos até inverter toda a palavra.
- Exemplo de passos:
  1. Marque o primeiro símbolo, vá até o fim, troque com o último, volte ao início, repita.

---

3. Explique a diferença entre problemas decidíveis e indecidíveis.

<!-- RESOLUÇÃO E EXPLICAÇÃO DIDÁTICA -->

**Resolução:**

- Problemas **decidíveis**: existe uma máquina de Turing que sempre para e responde sim ou não para toda entrada (ex: verificar se uma palavra pertence a uma linguagem regular).
- Problemas **indecidíveis**: não existe máquina de Turing que resolva o problema para toda entrada (ex: problema da parada).

---

## 5. Autoavaliação

- [ ] Sei descrever e construir máquinas de Turing
- [ ] Entendo o conceito de computabilidade
- [ ] Sei identificar problemas decidíveis e indecidíveis

---

## 6. Recursos Adicionais

- [JFLAP](http://www.jflap.org/)
- Hopcroft, Motwani & Ullman, Cap. 8
- Sipser, Cap. 3
