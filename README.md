# DESAFIO-QA-BEEDOO-2026

## 1. Objetivo da aplicação

Com base na análise inicial da aplicação, entende-se que o objetivo do sistema é permitir o cadastro e a visualização de cursos em uma plataforma simples de gerenciamento.

A aplicação oferece um formulário para cadastro de novos cursos e uma página para listagem dos cursos cadastrados.

---

## 2. Principais fluxos disponíveis

Durante a exploração da aplicação foram identificados dois fluxos principais:

### Listagem de cursos
Permite visualizar os cursos cadastrados no sistema.

### Cadastro de curso
Permite cadastrar um novo curso através de um formulário contendo diversas informações.

---

## 3. Campos identificados no formulário

Durante a análise da tela de cadastro foram identificados os seguintes campos:

- Nome do curso
- Descrição do curso
- Instrutor
- URL da imagem de capa
- Data de início
- Data de fim
- Número de vagas
- Tipo de curso

Além disso, existe o botão:

- Cadastrar curso

---

## 4. Pontos críticos para teste

Os pontos considerados mais críticos durante a análise foram:

- Validação dos campos obrigatórios
- Cadastro de curso com dados válidos
- Comportamento da aplicação ao inserir dados inválidos
- Consistência das datas (data de início e data de fim)
- Comportamento do campo número de vagas
- Exibição correta dos cursos cadastrados na listagem
- Tratamento de campos vazios
- Validação do campo URL da imagem

---

## 5. Estratégia de testes

A estratégia de testes adotada foi baseada em:

- Fluxos principais da aplicação
- Cenários positivos
- Cenários negativos
- Validação de campos
- Testes exploratórios para identificar comportamentos inesperados

## Comportamento condicional identificado

Durante a exploração do formulário foi identificado um comportamento condicional no campo "Tipo de curso".

Quando o tipo de curso selecionado é **Online**, o sistema exibe o campo:

- Link de inscrição

Quando o tipo de curso selecionado é **Presencial**, o sistema exibe o campo:

- Endereço

Esse comportamento indica que o sistema possui lógica dinâmica baseada no tipo de curso selecionado, sendo um ponto importante para validação durante os testes.

## Bugs encontrados

Durante a execução dos testes foram identificados bugs na aplicação.

O relatório completo pode ser acessado em:

relatorio-de-bugs.md

## Casos de teste

Planilha com os cenários e casos de teste executados:

https://docs.google.com/spreadsheets/d/1muy70_0OjjlEijbqZmdo530yEtq5_sTOIsrhLn2vkzc/edit?usp=sharing

## Evidências dos testes

As evidências da execução dos testes podem ser acessadas no link abaixo:

https://drive.google.com/drive/folders/13snNzVYUu0VCYUSTn9xsJiLZOFJGCrOS?usp=sharing

## Melhorias sugeridas

Durante a execução dos testes, foram identificadas algumas oportunidades de melhoria na aplicação:

- Implementar validação obrigatória para campos essenciais como nome do curso.
- Validar regras de negócio para datas (data de fim não pode ser anterior à data de início).
- Garantir que o número de vagas seja um valor positivo maior que zero.
- Implementar validação de campos condicionais (link de inscrição para cursos online e endereço para cursos presenciais).
- Ajustar o comportamento da mensagem de sucesso para que permaneça visível por tempo suficiente.
- Corrigir a funcionalidade de exclusão de cursos.
- Garantir que rotas da aplicação possam ser acessadas diretamente pela URL.
