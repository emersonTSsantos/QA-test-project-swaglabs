# Análise de Sistemas - SwagLabs

## 1. Visão Geral da Aplicação

O SwagLabs é uma aplicação web de comércio eletrônico de demonstração, utilizada para praticar atividades de teste de software.

O sistema permite que os usuários se autentiquem, naveguem pelos produtos disponíveis, adicionem itens ao carrinho de compras e concluam o processo de finalização da compra.

URL do aplicativo:
https://www.saucedemo.com/

## Credenciais de teste:

Nome de usuário: standard_user

Senha: secret_sauce

---

## 2. Principais funcionalidades identificadas

Durante a análise exploratória, as seguintes funcionalidades principais foram identificadas:

1. Autenticação do usuário (Login/Logout)
2. Página de inventário de produtos
3. Classificação de produtos
4. Detalhes do produto
5. Adicionar produto ao carrinho
6. Remover produto do carrinho
7. Página do carrinho de compras
8. Processo de finalização da compra
9. Confirmação do pedido

---

## 3. Escopo do teste

O foco deste projeto será o **teste manual funcional** utilizando a **técnica de teste de caixa preta**.

Níveis de teste:
- Teste de sistema
- Teste de aceitação

Tipo de teste:
- Teste funcional

---

## 4. Riscos potenciais de teste

Os seguintes riscos potenciais foram identificados durante a análise do sistema:

- Validação de login inválida
- Exibição incorreta do preço do produto
- Quantidade no carrinho não atualizada
- Problemas de validação do formulário de finalização da compra
- Problemas de expiração da sessão
- Erros de navegação entre páginas