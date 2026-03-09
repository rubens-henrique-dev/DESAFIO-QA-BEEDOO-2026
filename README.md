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
