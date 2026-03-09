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
