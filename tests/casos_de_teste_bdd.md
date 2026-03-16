# Casos de Teste - BDD
Projeto: SwagLabs  
Autor: Emerson Teixeira  
Tipo de teste: BDD (Behavior Driven Development)

---

## CT01 - Login com credenciais válidas

Cenário: Login com sucesso

Dado que o usuário está na página de login  
Quando ele informar um usuário válido  
E informar uma senha válida  
E clicar no botão "Login"  
Então o sistema deve redirecionar o usuário para a página de inventário

---

## CT02 - Login com senha incorreta

Cenário: Senha inválida

Dado que o usuário está na página de login  
Quando ele informar um usuário válido  
E informar uma senha incorreta  
E clicar no botão "Login"  
Então o sistema deve exibir uma mensagem de erro informando que a senha é inválida

---

## CT03 - Login com usuário inexistente

Cenário: Usuário inválido

Dado que o usuário está na página de login  
Quando ele informar um usuário inexistente  
E informar uma senha qualquer  
E clicar no botão "Login"  
Então o sistema deve exibir uma mensagem de erro de autenticação

---

## CT04 - Login com campos vazios

Cenário: Campos obrigatórios

Dado que o usuário está na página de login  
Quando ele deixar os campos de usuário e senha vazios  
E clicar no botão "Login"  
Então o sistema deve impedir o login e exibir mensagem de erro

---

## CT05 - Usuário bloqueado

Cenário: Login com usuário bloqueado

Dado que o usuário está na página de login  
Quando ele informar um usuário bloqueado  
E informar a senha correta  
E clicar no botão "Login"  
Então o sistema deve exibir uma mensagem informando que o usuário está bloqueado

---

## CT06 - Visualização da lista de produtos

Cenário: Exibir produtos

Dado que o usuário está autenticado no sistema  
Quando acessar a página de inventário  
Então o sistema deve exibir a lista de produtos disponíveis

---

## CT07 - Ordenação de produtos A-Z

Cenário: Ordenar produtos alfabeticamente

Dado que o usuário está na página de inventário  
Quando selecionar a opção de ordenação "A-Z"  
Então os produtos devem ser exibidos em ordem alfabética crescente

---

## CT08 - Ordenação de produtos Z-A

Cenário: Ordenar produtos inversamente

Dado que o usuário está na página de inventário  
Quando selecionar a opção de ordenação "Z-A"  
Então os produtos devem ser exibidos em ordem alfabética decrescente

---

## CT09 - Adicionar produto ao carrinho

Cenário: Adicionar item ao carrinho

Dado que o usuário está na página de inventário  
Quando clicar no botão "Adicionar ao carrinho" de um produto  
Então o produto deve ser adicionado ao carrinho

---

## CT10 - Remover produto do carrinho

Cenário: Remover item do carrinho

Dado que o usuário possui um produto no carrinho  
Quando clicar no botão "Remover"  
Então o produto deve ser removido do carrinho