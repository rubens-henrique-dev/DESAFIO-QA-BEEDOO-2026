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
