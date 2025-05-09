## Reunião

> Somos uma biblioteca pequena e gostariámos de controlar a nossa entrada e saída de livros. Queremos cadastrar o usuário que irá pegar o livro emprestado, cadastrar os livros da nossa biblioteca e poder emprestar os livros para qualquer usuário, além de buscar os registros de empréstimos.

## Dados
- Usuário: [nome_completo, CPF, telefone, endereco, email]
- Livro: [nome, quantidade, autor, genero, ISBN]
- Emprésitmo: [usuario_id, livro_id, data_retorno, data_devolucao, data_saida]

## UseCases (Regras de negócio)
[] Cadastrar um novo usuário
[] = CPF ou email devem ser únicos

[] Buscar um cadastro de usuário por CPF
[] - Retornar um usuário ou vazio (null)

[] Cadastrar um novo livro
[] - ISBN deve ser único

[] Buscar livro por nome ou ISBN
[] - Retornar os livro ou vazio

[] Emprestar um livro ao usuário
[] - A data de retorno não pode ser menor que a data de saída
[] - Um usuário não pode estar com mais de um livro com o mesmo ISBN ao mesmo tempo
[] - Um usuário pode estar com mais de um livro com ISBN diferentes ao mesmo tempo
[] - Ao cadastrar um empréstimo, será enviado um email automaticamente informando o nome do livro, nome do usuário, CPF, a data de saída e a data de retorno

[] Devolver o livro emprestado
[] - Caso o usuário tenha atrasado, será gerada uma multa fixa de R$ 10,00

[] Mostrar todos os emprésitmos pendentes, com o nome do livro, nome do usuário, CPF, data de saída e data de retorno. Ordenados pela data de retorno mais antiga