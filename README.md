# DESAFIO-QA-BEEDOO-2026

Objetivo da aplicação:

A aplicação tem como objetivo permitir o gerenciamento de cursos, possibilitando que o usuário visualize, cadastre e exclua cursos em uma base de dados.
Cada curso possui informações que descrevem suas características. As informações são as seguintes:
- Nome do Curso
- Descrição do curso
- Instrutor
- Url da imagem de capa
- Data de início
- Data de fim
- Número de vagas
- Tipo de curso

Principais fluxos disponíveis:

1. Listagem de cursos: Ao acessar a aplicação, o usuário deve visualizar na tela inicial uma lista contendo todos os cursos cadastrados. Cada curso deve apresentar as principais informações.
2. Navegação entre telas: A aplicação deve possuir uma barra fixa na parte superior com as opções de: "Listar cursos" e "Cadastrar cursos", permitindo que o usuário navegue entre as funcionalidades principais a qualquer momento.
3. Cadastro de cursos: Ao clicar em "Cadastrar cursos" a aplicação deve ir para a tela de cadastro, onde o usuário poderá preencher os dados do curso para salvá-los.
4. Exclusão de cursos: Na listagem de cursos, cada curso deve possuir uma opção para exclusão individual.

Pontos do sistema mais críticos para teste:

- Cadastro de curso: Verificar se após adicionar um curso, ele é corretamente salvo e adicionado na lista de cursos.
- Exclusão de curso: Verificar se a exclusão de cursos ocorre corretamente e remove o curso da lista.
- Campos obrigatórios: Verificar se é possível cadastrar cursos sem informações essenciais.
- Regras de negócio: Verificar se o usuário consegue colocar número negativo em quantidade de vagas.
- Validação de datas: Verificar se usuário consegue adicionar curso com data início inferior a data atual. Ou se consegue colocar data de fim inferior a data de início.

---

Casos de teste: 

Tela inicial da aplicação:

1: Verificar se a lista de cursos está sendo exibida.
2: Verificar se  se possui uma barra superior fixa com as opções de "Listar cursos" e "Cadastrar cursos".
3: Verificar se a visualização dos cursos está visível da melhor forma para o usuário. 
4: Sugerir um ordenador na lista de cursos, permitindo ordenar por "Nome" ou "Data de início".
5: Sugerir um campo de busca na lista de cursos, permitindo o usuário buscar por nome do curso. 
6: Sugerir criar uma paginação na tela para melhorar a otimização. Criar uma opção no fim dessa paginação para usuário selecionar quantos registros ele quer visualizar(10/20/50/100...).

Cadastro de curso:

7: Tela inicial >> Cadastrar Curso >> Nessa tela deverá possuir um formulário de cadastro com os campos a seguir(Caso algum dos campos não obedecer as regras, deve impossibilitar o cadastro e informar o usuário o que está incorreto, mantendo as informações que ele já preencheu no formulário para ele editar):
- Nome do Curso: Deve aceitar apenas texto, ser obrigatório e deve possuir um limitador de 100 caracteres.
- Descrição do curso: Deve aceitar apenas texto, ser obrigatório e deve possuir uma caixa de texto maior que do 'Nome do Curso' para facilitar o detalhamento do usuário. Deve ter limitador de 1500 caracteres.
- Instrutor: Deve aceitar apenas texto, ser obrigatório e deve possuir um limitador de 100 caracteres.
- Url da imagem de capa: Deve aceitar apenas texto, não precisa ser obrigatório e deve possuir um limitador de 1000 caracteres.
- Data de início: Deve ser obrigatório, ser do tipo date, com mascará de data permitindo a digitação do usuário, mas também permitindo o usuário selecionar a data pela funcionalidade do calendário. A data de início não pode ser inferior a data atual.
- Data de fim: Deve ser obrigatório,  ser do tipo date, com mascará de data permitindo a digitação do usuário, mas também permitindo o usuário selecionar a data pela funcionalidade do calendário. A data de fim não pode ser inferior a data de início.

Observação: Segue abaixo um exemplo de como o usuário poderia adicionar uma data:
![Date1](https://github.com/user-attachments/assets/7dc3dd00-9e30-4e94-ab37-212e7f427101)
- Número de vagas: Deve ser obrigatório, ser do tipo texto e com seta para adicionar ou diminuir a quantidade. Não deve permitir quantidade negativa
- Tipo de curso: Deve ser obrigatório e ser um combo box, permitindo selecionar as opções "Presencial" ou "Online".
- Caso selecionar a opção "Presencial", deve aparecer um novo campo obrigatório na tela com nome "Endereço", que deve permitir apenas texto e ter um limitador de 500 caracteres.
- Caso selecionar a opção Online, deve aparecer um novo campo obrigatório na tela com nome "Link da inscrição", que deve permitir apenas texto e um limitador de 500 caracteres.

8: Ao finalizar o cadastro de um curso deve exibir uma mensagem em verde na tela informando que o cadastro foi realizado com sucesso e voltar para a lista de cursos.
9: Verificar se após o cadastro de um curso, ele foi adicionado corretamente na lista.
10: Ao estar na tela de "Cadastro de curso", quando clicar no botão "Listar cursos", a aplicação deve ir para a tela de lista de cursos.

Exclusão de cursos:

11: Na tela de lista de cursos, ao clicar em "Excluir curso", deve remover o curso da lista e exibir uma mensagem em verde na tela informando que o curso foi removido. Também deve atualizar automaticamente a tela para os cursos ficarem visíveis corretamente.
