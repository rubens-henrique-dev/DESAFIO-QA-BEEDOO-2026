# Relatório de Bugs

## BUG 001 - Mensagem de sucesso desaparece rapidamente após cadastro

### Passos para reproduzir
1. Acessar a página de cadastro de curso
2. Preencher todos os campos corretamente
3. Clicar em "Cadastrar curso"

### Resultado atual
Uma mensagem de sucesso aparece, mas desaparece muito rapidamente, impossibilitando a leitura completa pelo usuário.

### Resultado esperado
A mensagem de sucesso deveria permanecer visível por tempo suficiente ou exigir interação do usuário para desaparecer.

### Severidade
Baixa (problema de usabilidade)

---

## BUG 002 - Curso não é removido da lista após clicar em excluir

### Passos para reproduzir
1. Acessar a lista de cursos
2. Localizar um curso cadastrado
3. Clicar no botão "Excluir curso"

### Resultado atual
O curso permanece visível na lista mesmo após clicar no botão de exclusão.

### Resultado esperado
O curso deveria ser removido da lista após a exclusão.

### Severidade
Alta (funcionalidade principal não funciona corretamente)

### Observação:
A imagem do curso muda após recarregar a página devido ao uso de URL dinâmica (picsum.photos).

## BUG 003 - Sistema informa exclusão de curso, mas curso continua na listagem

### Passos para reproduzir
1. Acessar a lista de cursos
2. Localizar um curso cadastrado
3. Clicar no botão "Excluir curso"
4. Observar a mensagem exibida pelo sistema
5. Atualizar a página (F5)

### Resultado atual
O sistema exibe uma mensagem informando que o curso foi excluído com sucesso, porém o curso continua visível na listagem mesmo após atualizar a página.

### Resultado esperado
Após a exclusão, o curso deveria ser removido da listagem e não deveria aparecer novamente ao atualizar a página.

### Severidade
Alta (inconsistência entre a ação executada e o estado real do sistema)

### Evidência
Print da tela mostrando o curso ainda presente após a mensagem de exclusão.

## BUG 004 - Sistema permite cadastrar curso com data final anterior à data inicial

### Passos para reproduzir
1. Acessar a página de cadastro de curso
2. Preencher os campos obrigatórios
3. Inserir uma data de início posterior à data de fim (exemplo: início 10/03/2026 e fim 09/03/2026)
4. Clicar em "Cadastrar curso"

### Resultado atual
O sistema aceita o cadastro e cria o curso mesmo com a data final anterior à data inicial.

### Resultado esperado
O sistema deveria impedir o cadastro e exibir uma mensagem informando que a data de fim não pode ser anterior à data de início.

### Severidade
Alta (violação de regra de negócio)

## BUG 005 - Página de cadastro retorna "Page not found" ao acessar diretamente pela URL

### Passos para reproduzir
1. Acessar a aplicação
2. Copiar a URL da página de cadastro de cursos
3. Abrir uma nova aba no navegador
4. Colar a URL diretamente e pressionar Enter

### Resultado atual
A aplicação exibe a mensagem "Page not found".

### Resultado esperado
A página de cadastro deveria carregar normalmente ao acessar diretamente pela URL.

### Severidade
Média (problema de navegação/roteamento)

## BUG 006 - Sistema permite cadastrar curso sem preencher o título do curso

### Passos para reproduzir
1. Acessar a página de cadastro de curso
2. Deixar o campo "Nome do curso" em branco
3. Preencher os demais campos obrigatórios
4. Clicar em "Cadastrar curso"

### Resultado atual
O sistema aceita o cadastro e cria o curso mesmo sem o preenchimento do título.

### Resultado esperado
O sistema deveria impedir o cadastro e exibir uma mensagem informando que o campo "Nome do curso" é obrigatório.

### Severidade
Alta (falha de validação de campo obrigatório)

## BUG 007 - Sistema permite cadastrar curso com número de vagas negativo

### Passos para reproduzir
1. Acessar a página de cadastro de curso
2. Preencher os campos obrigatórios
3. Inserir um número negativo no campo "Número de vagas" (exemplo: -5)
4. Clicar em "Cadastrar curso"

### Resultado atual
O sistema aceita o cadastro e cria o curso com número de vagas negativo.

### Resultado esperado
O sistema deveria impedir o cadastro e informar que o número de vagas deve ser um valor positivo.

### Severidade
Alta (falha de validação de regra de negócio)

## BUG 008 - Sistema permite cadastrar curso online sem preencher o link de inscrição

### Passos para reproduzir
1. Acessar a página de cadastro de curso
2. Selecionar o tipo de curso "Online"
3. Não preencher o campo "Link de inscrição"
4. Clicar em "Cadastrar curso"

### Resultado atual
O sistema permite o cadastro do curso mesmo sem o link de inscrição.

### Resultado esperado
O sistema deveria impedir o cadastro e exigir o preenchimento do link de inscrição para cursos online.

### Severidade
Alta (falha de validação de campo obrigatório)

## BUG 009 - Sistema permite cadastrar curso presencial sem preencher o endereço

### Passos para reproduzir
1. Acessar a página de cadastro de curso
2. Selecionar o tipo de curso "Presencial"
3. Não preencher o campo "Endereço"
4. Clicar em "Cadastrar curso"

### Resultado atual
O sistema permite o cadastro do curso mesmo sem o preenchimento do endereço.

### Resultado esperado
O sistema deveria impedir o cadastro e exigir o preenchimento do endereço para cursos presenciais.

### Severidade
Alta (falha de validação de campo obrigatório)

## BUG 010 - Sistema permite cadastrar curso com número de vagas igual a zero

### Passos para reproduzir
1. Acessar a página de cadastro de curso
2. Preencher os campos obrigatórios
3. Inserir "0" no campo "Número de vagas"
4. Clicar em "Cadastrar curso"

### Resultado atual
O sistema permite o cadastro do curso com número de vagas igual a zero.

### Resultado esperado
O sistema deveria impedir o cadastro e exigir que o número de vagas seja maior que zero.

### Severidade
Média (falha de validação de regra de negócio)
