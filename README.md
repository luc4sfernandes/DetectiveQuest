# 🔍 Detective Quest: Algoritmos de Investigação Criminal

Bem-vindo ao **Detective Quest**, um simulador de mistério desenvolvido em C. Este projeto foi desenhado para ensinar como organizar informações não lineares. Aqui, os dados não estão em uma lista simples; eles estão escondidos em ramificações e conexões lógicas.

---

## 🏛️ A Engenharia do Mistério

O desafio utiliza três estruturas de elite para resolver o crime:

### 🎮 Nível Novato: O Mapa da Mansão (Árvore Binária)
Como representar uma casa onde cada sala leva a dois novos caminhos? Usamos uma **Árvore Binária de Navegação**.
* **O Conceito:** Cada nó da árvore é um `Comodo`. O ponteiro `esquerda` leva a uma sala, e o `direita` a outra. 
* **A Lógica:** Você aprenderá a **Recursividade de Travessia**. Chegar ao fim de um corredor significa alcançar um "Nó Folha" (onde os ponteiros são `NULL`).



### 🛡️ Nível Aventureiro: O Arquivo de Evidências (BST)
Encontrar pistas é fácil; organizá-las para busca rápida é o desafio. Entra a **Árvore Binária de Busca (BST)**.
* **O Diferencial:** Diferente da árvore do mapa, aqui a posição de cada nó depende do seu valor (ordem alfabética). 
* **A Eficiência:** Buscar uma pista em uma BST é muito mais rápido do que em uma lista comum, pois a cada comparação você descarta metade da árvore.
* **Função Educativa:** O uso do percurso `Em-Ordem` (In-Order Traversal) para listar todas as evidências perfeitamente alfabetizadas.



### 🏆 Nível Mestre: O Quadro de Suspeitos (Tabela Hash)
O ápice da investigação. Como ligar uma "Pista" a um "Suspeito" instantaneamente? Usamos uma **Tabela Hash**.
* **O Conceito:** Uma Tabela Hash transforma o nome da pista (string) em um índice numérico (endereço de memória) através de uma **Função de Espalhamento**.
* **A Lógica de Ligação:** É um dicionário de alta performance. Em vez de procurar em toda a lista quem é o dono da "Faca", o computador calcula o endereço e vai direto ao suspeito.
* **Desafio Técnico:** Lidar com **Colisões** (quando duas pistas geram o mesmo índice) usando encadeamento (listas ligadas nos índices).



---

## 📋 Tabela de Ferramentas do Detetive

| Estrutura | Função no Jogo | Complexidade (Busca) |
| :--- | :--- | :--- |
| **Árvore Binária** | Navegação física entre salas. | O(n) |
| **BST (Busca)** | Organizar pistas alfabeticamente. | O(log n) |
| **Tabela Hash** | Associar Evidência → Suspeito. | O(1) - Quase instantâneo |

---

## 💡 Dicas de Perícia (ByteBros & Enigma Studios)

1.  **Cuidado com a Memória Dinâmica:** Como as salas e pistas são criadas durante o jogo, use `malloc()` para cada novo nó. Não esqueça de criar uma função `limparMansao()` para dar um `free()` em tudo ao final!
2.  **Função Hash Simples:** Para o nível mestre, uma função hash fácil é somar o valor ASCII de todas as letras da palavra e usar o resto da divisão (`%`) pelo tamanho da tabela.
    * *Exemplo:* `hash = (soma_ascii % tamanho_tabela);`
3.  **Ponteiros de Ponteiros:** Ao lidar com a Tabela Hash e colisões, você precisará manipular ponteiros que apontam para o início de listas ligadas. Mantenha a calma e desenhe no papel antes de codar!

---
*Investigue os dados, conecte os pontos e não deixe nenhum ponteiro solto (dangling pointer).*
*Desenvolvido para a trilha de Algoritmos Avançados - Enigma Studios.*
