# API de Gestão de Alunos

Uma API REST simples para gerenciamento de registros de alunos construída com Node.js e Express.js.

## Funcionalidades

- Criar novos alunos
- Listar todos os alunos
- Atualizar informações dos alunos
- Excluir alunos
- Geração de ID único para cada aluno

## Pré-requisitos

- Node.js (v12 ou superior)
- npm (Gerenciador de Pacotes do Node)

## Instalação

1. Clone o repositório:
```bash
git clone [url-do-seu-repositorio]
```

2. Instale as dependências:
```bash
npm install
```

3. Inicie o servidor:
```bash
node index.js
```

O servidor iniciará em `http://localhost:3000`.

## Dependências

- express: Framework web para Node.js
- uuid: Para geração de IDs únicos

## Endpoints da API

### Criar um Aluno
- **POST** `/alunos`
- **Corpo da requisição:**
```json
{
    "nome": "João Silva",
    "email": "joao@exemplo.com",
    "nome_curso": "Ciência da Computação"
}
```
- **Resposta:** Retorna o objeto do aluno criado com ID gerado

### Listar Todos os Alunos
- **GET** `/alunos`
- **Resposta:** Retorna um array com todos os alunos

### Atualizar um Aluno
- **PUT** `/alunos/:id`
- **Corpo da requisição:**
```json
{
    "nome": "João Silva Atualizado",
    "email": "joao.atualizado@exemplo.com",
    "nome_curso": "Ciência de Dados"
}
```
- **Resposta:** Retorna o objeto do aluno atualizado

### Excluir um Aluno
- **DELETE** `/alunos/:id`
- **Resposta:** Status 204 (Sem Conteúdo)

## Estrutura dos Dados

Cada objeto de aluno possui a seguinte estrutura:
```json
{
    "id": "uuid-gerado",
    "nome": "Nome do Aluno",
    "email": "aluno@email.com",
    "nome_curso": "Nome do Curso"
}
```

## Armazenamento

A API utiliza um array em memória para armazenar os dados dos alunos. Os dados serão perdidos quando o servidor for reiniciado.

## Como Contribuir

1. Faça um fork do repositório
2. Crie sua branch de feature (`git checkout -b feature/nova-funcionalidade`)
3. Faça commit das suas alterações (`git commit -m 'Adiciona nova funcionalidade'`)
4. Faça push para a branch (`git push origin feature/nova-funcionalidade`)
5. Abra um Pull Request
