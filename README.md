# 🗺️ Busca A* (A-Star) em Mapa de RPG Procedural

 **Disciplina:** Inteligência Artificial (Unidade I)  
 **Grupo:**
 - Fabyo Hunter Costa Sá
 - Alana Mayara Silva Monteiro
 - Raí Abreu Machado

Este projeto implementa o algoritmo de busca **A* (A-Star)** aplicado a um problema de navegação em um mapa gerado proceduralmente (aleatório). O objetivo é demonstrar como um agente inteligente toma decisões baseadas em **custo de terreno** e **heurística espacial**.

## 🧠 Sobre o Projeto

Diferente de labirintos simples onde apenas existem "paredes" e "caminhos", este projeto simula um ambiente de RPG com terrenos de dificuldades variadas. O agente deve encontrar o caminho até o objetivo minimizando o **esforço total**, não apenas a distância.

### Funcionalidades
- **Geração Procedural:** A cada execução, um novo mapa 20x20 é criado aleatoriamente.
- **Terrenos com Pesos:**
  - 🟩 **Grama (Custo 1):** Caminho padrão, rápido.
  - 🌲 **Floresta (Custo 5):** Terreno difícil, o agente evita se possível.
  - 🟦 **Água (Custo 20):** Terreno muito custoso, o agente só entra em último caso.
  - ⬛ **Muros:** Obstáculos intransponíveis.
- **Visualização Gráfica:** Renderização do grafo e da rota usando `matplotlib`.

---

## 📐 A Lógica do Algoritmo

O A* utiliza a função de avaliação $f(n) = g(n) + h(n)$, onde:

1. **$g(n)$ (Custo Real):** É a soma dos pesos das arestas percorridas.
   - *Exemplo:* Andar 3 casas na grama custa 3. Andar 3 casas na água custa 60. O algoritmo "sente" esse peso.
   
2. **$h(n)$ (Heurística):** Estimativa do custo restante até o objetivo.
   - Utilizamos a **Distância de Manhattan** ($|x_1 - x_2| + |y_1 - y_2|$), pois o agente se move apenas na vertical e horizontal (grade).

---

## 🚀 Como Rodar

### Pré-requisitos
Certifique-se de ter o Python instalado. Instale as bibliotecas necessárias:

```bash
pip install networkx matplotlib
```

---

## 🎥 Demonstração em Vídeo
Confira a explicação detalhada do código e a demonstração de execução no link abaixo:

```bash
https://youtu.be/7r7LKm5wt4g
```
