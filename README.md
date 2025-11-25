Squad Beta – Logística e Delivery
Este repositório contém as implementações das estruturas de dados solicitadas para o Desafio de Squads – 25/11/2025, conforme o memorando oficial da Diretoria Técnica.
A Squad Beta é responsável por desenvolver soluções para sistemas de gerenciamento de entregas e armazéns, implementando listas, pilhas, filas e outras estruturas usando JavaScript (Node.js).

👥 Composição da Squad e Papéis
🧭 Tech Lead
MAURICIO LIMA
Responsável pela arquitetura geral, organização do repositório, revisão e aprovação dos Pull Requests, garantia de boas práticas e padronização do código.
🧪 QA Engineer / Tester
JHONATAS DAVID
Responsável pela criação dos casos de teste, validações, tentativas de quebra ("break tests"), verificação dos requisitos e garantia da estabilidade do sistema.
🛠️ Software Engineers (Developers)

MARIA CAROLINA
PAULA MIRANDA
JHONATAS DAVID

Responsáveis pela implementação prática das classes, métodos, estruturas de dados e simulações das situações-problema.

📦 Estruturas Desenvolvidas e Situações-Problema
A Squad Beta deve resolver 5 desafios específicos do setor de Logística e Delivery, conforme descrito no documento oficial.
1️⃣ A Rota de Entrega – Lista Simplesmente Encadeada (LinkedList)
Um entregador tem uma sequência de endereços e só pode ir do ponto A para o B, do B para o C, seguindo a ordem da rota.
Implementação

Classe Node

🔧 Como Executar o Projeto
1. Instalar dependências
bashnpm install
2. Executar testes
bashnode test/main.test.js
3. Executar simulações
bashnode LinkedList/deliveryRouteSimulation.js
node Stack/warehouseSimulation.js
node Queue/orderDispatchSimulation.js
node CircularList/vehicleTrackingSimulation.js
node ArrayComparison/routeOptimization.js
```
```
feat: implementa adição de endereços na rota
fix: corrige bug no método listRoute()
test: adiciona casos para fila com alta demanda

🧪 Validação e Testes (QA)
O arquivo main.test.js deve conter testes para:

Adição de endereços em rota vazia
Listagem completa da rota de entrega
Remoção de caixa em pilha vazia
Comportamento da fila com mais de 10 pedidos
Ciclo infinito da lista circular de veículos
Tentativas de acesso inválido em todas as estruturas

O QA é responsável por garantir que:

Todos os requisitos foram atendidos
O sistema não quebra com entradas inválidas
Edge cases foram contemplados
Logs e mensagens de erro são claros


🚀 Conclusão
Este repositório entrega todas as estruturas de dados solicitadas para o setor de Logística e Delivery, simulando desafios reais de sistemas de gerenciamento de entregas e armazéns. A Squad Beta aplicou conceitos fundamentais de Linked Lists, Stacks, Queues, Circular Lists e Arrays para criar soluções funcionais, bem documentadas e testadas.
