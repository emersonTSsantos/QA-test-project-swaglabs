# Bug Reports
Projeto: SwagLabs  
Autor: Emerson Teixeira  
Data: 2026  

Este documento registra defeitos encontrados durante a execução de testes manuais no sistema SwagLabs.

---

# BUG 01 - Ordenação alfabética incorreta na versão traduzida da página

ID: BUG-01  
Severidade: Média  
Prioridade: Média  
Módulo: Inventário / Filtro de Ordenação  

## Descrição
Ao selecionar o filtro de ordenação "Nome (A a Z)" na versão traduzida da página, os produtos não são exibidos em ordem alfabética correta.

Por exemplo, o primeiro produto exibido começa com a letra **"M" (Mochila)** enquanto um produto com a letra **"C" (Camiseta)** deveria aparecer antes.

Foi observado que a ordenação funciona corretamente quando a página está em inglês, mas deixa de funcionar após a tradução da interface.

## Passos para reproduzir

1. Acessar a página de login do SwagLabs
2. Realizar login com um usuário válido
3. Acessar a página de inventário
4. Traduzir a página para português utilizando o tradutor do navegador
5. Selecionar o filtro **"Nome (A a Z)"**

## Resultado esperado

Os produtos devem ser exibidos em ordem alfabética crescente considerando os nomes traduzidos.

Exemplo esperado:

- Camiseta
- Jaqueta
- Macacão
- Mochila

## Resultado atual

Os produtos não são ordenados corretamente após a tradução da página.

---

# BUG 02 - Exibição de código na descrição do produto Mochila

ID: BUG-02  
Severidade: Baixa  
Prioridade: Média  
Módulo: Inventário / Descrição do Produto

## Descrição

A descrição do produto **Mochila Sauce Labs** exibe um trecho de código dentro do texto descritivo:

carry.allTheThings()

Isso indica possível erro de integração ou conteúdo não tratado corretamente no frontend.

## Passos para reproduzir

1. Realizar login no sistema
2. Acessar a página de inventário
3. Localizar o produto **Mochila Sauce Labs**
4. Observar a descrição do produto

## Resultado esperado

A descrição do produto deve conter apenas texto descritivo do item.

## Resultado atual

A descrição exibe um trecho de código:

carry.allTheThings()

---

# BUG 03 - Título do produto exibindo nome técnico em vez de nome amigável

ID: BUG-03  
Severidade: Baixa  
Prioridade: Média  
Módulo: Inventário / Nome do Produto

## Descrição

O produto **Test.allTheThings() Camiseta (Vermelha)** apresenta um nome técnico contendo código dentro do título.

Esse formato não é adequado para usuários finais e aparenta ser um identificador interno do sistema.

## Passos para reproduzir

1. Realizar login no sistema
2. Acessar a página de inventário
3. Localizar o produto **Test.allTheThings() Camiseta (Vermelha)**

## Resultado esperado

O nome do produto deveria ser exibido de forma amigável ao usuário, por exemplo:

Camiseta (Vermelha)

## Resultado atual

O sistema exibe:

Test.allTheThings() Camiseta (Vermelha)

---

# Resumo dos Bugs

| ID | Módulo | Severidade | Prioridade |
|----|------|------------|-----------|
BUG-01 | Inventário / Ordenação | Média | Média |
BUG-02 | Inventário / Descrição | Baixa | Média |
BUG-03 | Inventário / Nome do Produto | Baixa | Média |