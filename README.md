# video-manager-api

Esta é uma API simples para gerenciar vídeos, permitindo a criação, edição, exibição e exclusão de informações sobre vídeos. A API utiliza o PostgreSQL como banco de dados e é desenvolvida em Node.js.

## Pré-requisitos

Antes de começar, certifique-se de ter instalado o seguinte:

- Node.js: [Baixe e instale o Node.js](https://nodejs.org/)
- PostgreSQL: [instale a dependencia do PostgreSQL](https://github.com/porsager/postgres)
- fastify: [instale a dependencia fastify ](https://fastify.dev/)

## Configuração do Banco de Dados

1. Crie um banco de dados PostgreSQL para a aplicação.

## Instalação

1. Clone este repositório:

   ```bash
   git clone https://github.com/seu-usuario/api-gerenciamento-videos.git
   ```

2. Navegue até a pasta do projeto:

   ```bash
   cd video-manager-api
   ```

3. Instale as dependências:

   ```bash
   npm install
   ```

4. Inicie o servidor:

   ```bash
   npm run dev

A API estará disponível em `http://localhost:3333`.

## Endpoints da API

### 1. Criar um vídeo

- **URL**: `/videos`
- **Método**: `POST`
- **Corpo da solicitação**:

  ```json
  {
    "title": "Título do Vídeo",
    "description": "Descrição do Vídeo",
    "duration": 180
  }
  ```

- **Resposta de Exemplo**:

  ```json
  {
    "id": "UUID aleatorio",
    "title": "Título do Vídeo",
    "description": "Descrição do Vídeo",
    "duration": "180"
  }
  ```

### 2. Obter todos os vídeos

- **URL**: `/videos`
- **Método**: `GET`
- **Resposta de Exemplo**:

  ```json
  [
    {
    "id": "8d44b2f9-be27-4d7a-bddc-a4e0d4018cb4",
    "title": "Título do Vídeo",
    "description": "Descrição do Vídeo",
    "duration": 180
    },
    {
      "id": "8d44b2f9-b987-4d7a-bddc-a4e0d4018cb4",
      "title": "Outro Vídeo",
      "description": "Descrição do Outro Vídeo",
      "duration": "360"
    }
  ]
  ```

### 3. Obter um vídeo por ID

- **URL**: `/videos/:id`
- **Método**: `GET`
- **Resposta de Exemplo**:

  ```json
  {
    "id": "8d44b2f9-be27-4d7a-bddc-a4e0d4018cb4",
    "title": "Título do Vídeo",
    "description": "Descrição do Vídeo",
    "duration": "180"
  }
  ```

### 4. Atualizar um vídeo por ID

- **URL**: `/videos/:id`
- **Método**: `PUT`
- **Corpo da solicitação**:

  ```json
  {
    "title": "Novo Título",
    "description": "Nova Descrição",
    "durstion": "380"
  }
  ```

- **Resposta de Exemplo**:

  ```json
  {
    "id": "8d44b2f9-be27-4d7a-bddc-a4e0d4018cb4",
    "title": "Novo Título",
    "description": "Nova Descrição",
    "duration": 180
  }
  ```

### 5. Excluir um vídeo por ID

- **URL**: `/videos/:id`
- **Método**: `DELETE`
- **Resposta de Exemplo**:

  ```json
  {
    "HTTP/1.1 204 No Content",
    "Date: Fri, 08 Sep 2023 08:58:23 GMT",
    "Connection: close"
  }
  ```

## Contribuindo

Sinta-se à vontade para contribuir com este projeto. Basta fazer um fork do repositório, fazer suas alterações e criar um pull request.

## Licença

Este projeto está licenciado sob a Licença MIT. Consulte o arquivo [LICENSE](LICENSE) para obter detalhes.
