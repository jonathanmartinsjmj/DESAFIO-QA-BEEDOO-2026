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
2. Navegação entre telas: A aplicação deve possuir uma barra fixa na parte superior com as opções de: "Listar cursos" e "Cadastrar curso", permitindo que o usuário navegue entre as funcionalidades principais a qualquer momento.
3. Cadastro de cursos: Ao clicar em "Cadastrar cursos" a aplicação deve ir para a tela de cadastro, onde o usuário poderá preencher os dados do curso para salvá-los.
4. Exclusão de cursos: Na listagem de cursos, cada curso deve possuir uma opção para exclusão individual.

Pontos do sistema mais críticos para teste:

- Cadastro de curso: Verificar se após adicionar um curso, ele é corretamente salvo e adicionado na lista de cursos.
- Exclusão de curso: Verificar se a exclusão de cursos ocorre corretamente e remove o curso da lista.
- Campos obrigatórios: Verificar se é possível cadastrar cursos sem informações essenciais.
- Regras de negócio: Verificar se o usuário consegue colocar número negativo em quantidade de vagas.
- Validação de datas: Verificar se usuário consegue adicionar curso com data início inferior a data atual. Ou se consegue colocar data de fim inferior a data de início.

---

Casos de teste: https://docs.google.com/spreadsheets/d/12gSKbxluqMT_s7wPdaj8X4UkYETeqRVEK7fyFkleFxk/edit?usp=sharing


