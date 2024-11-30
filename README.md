# Insta-Bytes - Back-End

Este repositório contém o código do back-end para o projeto **Insta-Bytes**, desenvolvido durante a **Imersão Alura Back-End**.

## Tecnologias utilizadas:
- **Node.js**: Ambiente de execução JavaScript utilizado para desenvolver a aplicação.
- **MongoDB**: Banco de dados NoSQL utilizado para armazenamento dos dados do projeto.
- **Gemini Generative AI**: Utilizado para criar automaticamente as descrições das imagens enviadas.

## Passos para rodar o projeto:

### 1. Instale as dependências

Certifique-se de que o [Node.js](https://nodejs.org/) está instalado em sua máquina (recomenda-se a versão v20.x.x). Após isso, instale as dependências do projeto executando o comando abaixo no diretório raiz do projeto:

```bash
npm install
```

### 2. Configure o banco de dados

Você precisará de uma instância do **MongoDB** para armazenar os dados. Você pode usar o MongoDB localmente ou configurar um serviço na nuvem, como o [MongoDB Atlas](https://www.mongodb.com/cloud/atlas).

- Crie um banco de dados e obtenha a **string de conexão** para conectá-lo ao seu aplicativo.
- Configure a variável de ambiente `MONGODB_URI` com a string de conexão.

### 3. Variáveis de ambiente

Crie um arquivo `.env` na raiz do projeto e adicione as seguintes variáveis:

```
MONGODB_URI=<sua_string_de_conexao_do_mongodb>
GEMINI_API_KEY=<sua_chave_da_API_Gemini>
```

### 4. Execute o projeto

Após configurar as variáveis de ambiente, inicie o servidor com o comando:

```bash
npm run dev
```

O servidor estará rodando localmente na URL `http://localhost:5000`.

### 5. Integrando com o Front-End

O back-end foi projetado para funcionar em conjunto com o front-end, permitindo uma experiência interativa para o usuário. Após rodar o servidor back-end, você pode rodar o front-end (na branch `frontend`) para acessar a interface gráfica que interage diretamente com o back-end. O front-end pode ser encontrado na branch `frontend` do repositório.

Para acessar o front-end, faça o checkout para a branch `frontend`:

```bash
git checkout frontend
```

E então, siga as instruções específicas do front-end para rodá-lo.

### 6. Endpoints disponíveis

- `POST /upload`: Endpoint para envio de imagens. O sistema irá gerar automaticamente a descrição da imagem utilizando a IA do Gemini.
- `GET /images`: Endpoint para buscar todas as imagens enviadas, com suas respectivas descrições.
