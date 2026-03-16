# Casos de Teste - Step by Step
Projeto: SwagLabs  
Autor: Emerson Teixeira  
Tipo de teste: Teste manual detalhado

---

## CT11 - Verificar exibição das informações do produto

Passos:
1. Realizar login no sistema
2. Acessar a página de inventário
3. Observar os produtos listados

Resultado esperado:
Cada produto deve apresentar imagem, título, descrição e preço.

---

## CT12 - Verificar funcionamento do botão "Adicionar ao carrinho"

Passos:
1. Realizar login no sistema
2. Acessar a página de inventário
3. Clicar no botão "Adicionar ao carrinho" de um produto

Resultado esperado:
O produto deve ser adicionado ao carrinho e o contador do carrinho deve aumentar.

---

## CT13 - Verificar ordenação de produtos de A a Z

Passos:
1. Realizar login
2. Acessar a página de inventário
3. Selecionar o filtro de ordenação "A-Z"

Resultado esperado:
Os produtos devem ser exibidos em ordem alfabética crescente.

---

## CT14 - Verificar ordenação de produtos de Z a A

Passos:
1. Realizar login
2. Acessar a página de inventário
3. Selecionar o filtro de ordenação "Z-A"

Resultado esperado:
Os produtos devem ser exibidos em ordem alfabética decrescente.

---

## CT15 - Verificar ordenação de produtos por menor preço

Passos:
1. Realizar login
2. Acessar a página de inventário
3. Selecionar o filtro "Menor para maior preço"

Resultado esperado:
Os produtos devem ser exibidos do menor preço para o maior.

---

## CT16 - Verificar ordenação de produtos por maior preço

Passos:
1. Realizar login
2. Acessar a página de inventário
3. Selecionar o filtro "Maior para menor preço"

Resultado esperado:
Os produtos devem ser exibidos do maior preço para o menor.

---

## CT17 - Verificar exibição de produtos no carrinho

Passos:
1. Realizar login
2. Adicionar dois produtos ao carrinho
3. Acessar a página do carrinho

Resultado esperado:
Os produtos adicionados devem ser exibidos com nome, descrição e preço.

---

## CT18 - Verificar remoção de produto no carrinho

Passos:
1. Realizar login
2. Adicionar um produto ao carrinho
3. Acessar o carrinho
4. Clicar no botão "Remover produto"

Resultado esperado:
O produto deve ser removido da lista do carrinho.

---

## CT19 - Verificar validação de campos obrigatórios no checkout

Passos:
1. Realizar login
2. Adicionar um produto ao carrinho
3. Acessar o carrinho
4. Clicar em "Checkout"
5. Deixar os campos de dados pessoais vazios
6. Clicar em "Continuar"

Resultado esperado:
O sistema deve impedir o avanço e exibir mensagens de validação dos campos obrigatórios.

---

## CT20 - Verificar finalização do pedido com dados válidos

Passos:
1. Realizar login
2. Adicionar um produto ao carrinho
3. Acessar o carrinho
4. Clicar em "Checkout"
5. Preencher os campos:
   - Primeiro Nome
   - Sobrenome
   - CEP
6. Clicar em "Continuar"
7. Clicar em "Finalizar Pedido"

Resultado esperado:
O sistema deve concluir a compra e exibir a mensagem de confirmação do pedido.