# Documentação de Requisitos - Sistema de E-commerce (Swag Labs)

Este documento descreve as principais **Histórias de Usuário**, **Regras de Negócio** e **Critérios de Aceite** para funcionalidades principais do sistema.

---

# História de Usuário 1 - Login do Usuário

## Épico
Autenticação do Usuário

---

## História de Usuário

Como usuário registrado,  
desejo fazer login na plataforma  
para acessar o inventário de produtos.

---

## Descrição

O sistema deve permitir que usuários registrados se autentiquem usando um nome de usuário e senha válidos.

Após a autenticação bem-sucedida, o usuário deve ser redirecionado para a página de inventário, onde a lista de produtos disponíveis é exibida.

---

## Regras de Negócio

- O campo de nome de usuário deve aceitar nomes de usuário válidos e registrados.
- A senha deve estar associada corretamente ao nome de usuário.
- Ambos os campos são obrigatórios.
- Se as credenciais forem inválidas, o sistema deve exibir uma mensagem de erro.
- O botão de login deve autenticar apenas credenciais válidas.

---

## Critérios de Aceitação

### Cenário: Login bem-sucedido

Dado que o usuário está na página de login,  
Quando o usuário insere um nome de usuário e senha válidos,  
E clica no botão de login,  
Então o usuário deve ser redirecionado para a página de inventário.

### Cenário: Login inválido

Dado que o usuário está na página de login,  
Quando o usuário insere credenciais inválidas,  
E clica no botão de login,  
Então uma mensagem de erro deve ser exibida.

---

# História de Usuário 2 - Adicionar Produto ao Carrinho

## Épico
Shopping Cart

---

## História de Usuário

Como cliente autenticado,  
quero adicionar produtos ao carrinho de compras  
para que eu possa comprá-los mais tarde.

---

## Descrição

O sistema deve permitir que usuários autenticados adicionem produtos ao carrinho de compras diretamente da página de inventário.

Após adicionar um produto ao carrinho, o sistema deve atualizar o estado do carrinho e refletir visualmente que o item foi adicionado com sucesso.

---

## Regras de Negócio

- Apenas usuários autenticados podem adicionar produtos ao carrinho.
- Cada produto possui um botão **"Add to Cart"**.
- Ao clicar no botão, o produto deve ser incluído no carrinho do usuário.
- O carrinho deve atualizar automaticamente a quantidade de itens.
- O usuário pode adicionar múltiplos produtos ao carrinho.
- O sistema deve permitir remover o produto do carrinho após adicioná-lo.

---

## Critérios de Aceitação

### Cenário: Adicionar produto ao carrinho

Dado que o usuário está autenticado na plataforma,  
E está visualizando a lista de produtos no inventário,  
Quando o usuário clicar no botão **"Add to Cart"**,  
Então o produto deve ser adicionado ao carrinho.

### Cenário: Atualização do carrinho

Dado que o usuário adicionou um produto ao carrinho,  
Quando o produto for adicionado com sucesso,  
Então o número de itens no carrinho deve ser atualizado.

### Cenário: Remover produto do carrinho

Dado que um produto foi adicionado ao carrinho,  
Quando o usuário clicar no botão **"Remove"**,  
Então o produto deve ser removido do carrinho.

---

# História de Usuário 3 - Processo de Finalização da Compra

## Épico
Checkout

---

## História de Usuário

Como cliente autenticado,  
quero finalizar a compra dos produtos adicionados ao carrinho  
para concluir meu pedido.

---

## Descrição

O sistema deve permitir que usuários autenticados iniciem o processo de checkout a partir do carrinho de compras.

Durante o processo de finalização, o usuário deverá fornecer informações de entrega e pagamento para concluir o pedido.

Após a finalização com sucesso, o sistema deve confirmar que o pedido foi realizado.

---

## Regras de Negócio

- O usuário deve possuir pelo menos um produto no carrinho para iniciar o checkout.
- O usuário deve informar dados de entrega válidos.
- O usuário deve informar dados de pagamento válidos.
- O sistema deve validar todos os campos obrigatórios antes de permitir a finalização.
- Após a finalização da compra, o carrinho deve ser esvaziado.
- O sistema deve exibir uma mensagem de confirmação do pedido.

---

## Critérios de Aceitação

### Cenário: Iniciar checkout

Dado que o usuário possui produtos no carrinho,  
Quando o usuário clicar no botão **"Checkout"**,  
Então o sistema deve redirecionar para a página de finalização da compra.

### Cenário: Finalização da compra com sucesso

Dado que o usuário está na página de checkout,  
Quando o usuário preencher corretamente os dados de entrega e pagamento,  
E confirmar o pedido,  
Então o sistema deve exibir uma mensagem de confirmação da compra.

### Cenário: Falha na finalização

Dado que o usuário está na página de checkout,  
Quando os dados obrigatórios não forem preenchidos corretamente,  
Então o sistema deve impedir a finalização da compra  
E exibir mensagens de erro apropriadas.