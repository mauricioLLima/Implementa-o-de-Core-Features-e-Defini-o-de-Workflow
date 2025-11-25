# Squad Beta – Logística e Delivery

Este repositório contém as implementações das estruturas de dados solicitadas para o **Desafio de Squads – 25/11/2025**, conforme o memorando oficial da Diretoria Técnica.

A **Squad Beta** é responsável por desenvolver soluções para sistemas de gerenciamento de entregas e armazéns, implementando listas, pilhas, filas e outras estruturas usando **JavaScript (Node.js)**.

---

## 👥 Composição da Squad e Papéis

### 🧭 Tech Lead
**MAURICIO LIMA**  
Responsável pela arquitetura geral, organização do repositório, revisão e aprovação dos Pull Requests, garantia de boas práticas e padronização do código.

### 🧪 QA Engineer / Tester
**JHONATAS DAVID**  
Responsável pela criação dos casos de teste, validações, tentativas de quebra ("break tests"), verificação dos requisitos e garantia da estabilidade do sistema.

### 🛠️ Software Engineers (Developers)
- **MARIA CAROLINA**
- **PAULA MIRANDA**
- **JHONATAS DAVID**

Responsáveis pela implementação prática das classes, métodos, estruturas de dados e simulações das situações-problema.

---

## 📦 Estruturas Desenvolvidas e Situações-Problema

A Squad Beta deve resolver **5 desafios específicos** do setor de Logística e Delivery, conforme descrito no documento oficial.

### 1️⃣ A Rota de Entrega – Lista Simplesmente Encadeada (LinkedList)

Um entregador tem uma sequência de endereços e só pode ir do ponto A para o B, do B para o C, seguindo a ordem da rota.

#### Implementação
- **Classe Node**
  ```javascript
  constructor(data) // endereço
  next // ponteiro para próximo endereço
  ```
- **Classe LinkedList:**
  - `append(endereco)` → adiciona endereço no final da rota
  - `listRoute()` → exibe a rota completa

#### Objetivo
Simular uma rota de entrega sequencial com navegação unidirecional entre os pontos.

---

### 2️⃣ Gerenciamento de Armazém – Pilha (Stack)

Caixas são empilhadas no armazém, e apenas a caixa do topo pode ser acessada (LIFO - Last In, First Out).

#### Implementação
- **Classe Stack:**
  - `push(caixa)` → empilha uma caixa
  - `pop()` → remove a caixa do topo
  - `peek()` → visualiza a caixa do topo sem remover

#### Objetivo
Simular o gerenciamento de estoque com acesso restrito ao último item empilhado.

---

### 3️⃣ Fila de Pedidos para Despacho – Fila (Queue)

Pedidos chegam ao centro de distribuição e devem ser processados na ordem de chegada (FIFO - First In, First Out).

#### Implementação
- **Classe Queue:**
  - `enqueue(pedido)` → adiciona pedido à fila
  - `dequeue()` → processa e remove o primeiro pedido
  - `size()` → retorna quantidade de pedidos na fila
  - `peek()` → visualiza o próximo pedido sem remover

#### Regras
- Se `size() > 10` → exibir **"Alta demanda no centro de distribuição"**
- Processar (remover) os **3 primeiros pedidos**

---

### 4️⃣ Rastreamento de Veículos – Lista Circular

Os veículos de entrega circulam entre pontos de distribuição em um ciclo contínuo.

#### Implementação
- Lista circular com nós representando veículos
- **Método:**
  - `next()` → retorna o próximo veículo na rota

#### Teste obrigatório
Chamadas sucessivas devem ciclar infinitamente:
```
next() → Veículo 1
next() → Veículo 2
next() → Veículo 3
next() → Veículo 1
```

---

### 5️⃣ Otimização de Rotas – Comparação Array vs Lista Encadeada

O sistema precisa armazenar dados de rotas fixas que são consultadas frequentemente.

#### Entrega
Arquivo explicando por que usar **Array (Vetor)** ao invés de **LinkedList** para rotas fixas.

#### Pontos-chave
- Acesso direto por índice → **O(1)**
- Lista Encadeada tem acesso sequencial → **O(n)**
- Rotas fixas raramente mudam → inserções não são o foco
- Arrays ocupam menos memória (sem ponteiros)

---

## 📁 Estrutura Sugerida do Repositório

```
Estruturas-Squad-Beta/
│
├── LinkedList/
│   ├── Node.js
│   ├── LinkedList.js
│   └── deliveryRouteSimulation.js
│
├── Stack/
│   ├── Stack.js
│   └── warehouseSimulation.js
│
├── Queue/
│   ├── Queue.js
│   └── orderDispatchSimulation.js
│
├── CircularList/
│   ├── CircularNode.js
│   ├── CircularList.js
│   └── vehicleTrackingSimulation.js
│
├── ArrayComparison/
│   └── routeOptimization.js
│
├── test/
│   └── main.test.js
│
└── README.md
```

---

## 🔧 Como Executar o Projeto

### 1. Instalar dependências
```bash
npm install
```

### 2. Executar testes
```bash
node test/main.test.js
```

### 3. Executar simulações
```bash
node LinkedList/deliveryRouteSimulation.js
node Stack/warehouseSimulation.js
node Queue/orderDispatchSimulation.js
node CircularList/vehicleTrackingSimulation.js
node ArrayComparison/routeOptimization.js
```

---

## 🌐 Fluxo de Trabalho (GitHub)

### ✔️ Branches por funcionalidade
- `feature/linkedlist`
- `feature/stack`
- `feature/queue`
- `feature/circular-list`
- `feature/array-comparison`

### ✔️ Pull Requests revisados pelo Tech Lead
- Código deve seguir padrão definido
- Revisão obrigatória antes do merge

### ✔️ Commits padronizados
```bash
feat: implementa adição de endereços na rota
fix: corrige bug no método listRoute()
test: adiciona casos para fila com alta demanda
```

---

## 🧪 Validação e Testes (QA)

O arquivo `main.test.js` deve conter testes para:

- ✅ Adição de endereços em rota vazia
- ✅ Listagem completa da rota de entrega
- ✅ Remoção de caixa em pilha vazia
- ✅ Comportamento da fila com mais de 10 pedidos
- ✅ Ciclo infinito da lista circular de veículos
- ✅ Tentativas de acesso inválido em todas as estruturas

### O QA é responsável por garantir que:
- Todos os requisitos foram atendidos
- O sistema não quebra com entradas inválidas
- Edge cases foram contemplados
- Logs e mensagens de erro são claros

---

## 🚀 Conclusão

Este repositório entrega todas as estruturas de dados solicitadas para o setor de **Logística e Delivery**, simulando desafios reais de sistemas de gerenciamento de entregas e armazéns. 

A **Squad Beta** aplicou conceitos fundamentais de **Linked Lists**, **Stacks**, **Queues**, **Circular Lists** e **Arrays** para criar soluções funcionais, bem documentadas e testadas.

---

## 📄 Licença

Este projeto foi desenvolvido para fins educacionais como parte do Desafio de Squads – 25/11/2025.

---

## 👨‍💻 Desenvolvido por

**Squad Beta** - Logística e Delivery  
Diretoria Técnica - 2025
