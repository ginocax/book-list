# 📚 Book List

Aplicação simples de gerenciamento de livros, desenvolvida com [Vite](https://vitejs.dev/) e Vue.js.  
Permite visualizar, adicionar e acompanhar o progresso de leitura de livros.

---

## 🚀 Tecnologias

- [Vite](https://vitejs.dev/) – ferramenta de build rápida para projetos frontend modernos.
- [Vue 3](https://vuejs.org/) – framework progressivo para construção de interfaces de usuário.

---

## ⚙️ Pré-requisitos

- **Node.js** versão 18 ou superior. Verifique com:
  ```bash
  node -v
- **Vite** instalado globalmente (opcional, mas recomendado):
  ```bash
  npm install -g vite
  ```
  
## 🛠️ Instalação e execução

1. Clone o repositório:
   ```bash
   git clone https://github.com/ginocax/book-list.git
   cd book-list

2. Instale as dependências:
   ```bash
   npm install
   ````

3. Inicie o servidor de desenvolvimento:
   ```bash
   npm run dev
   ```
   
O projeto estará disponível em http://localhost:5173/
(ou na porta indicada no terminal).

## 📦 Scripts disponíveis

npm run dev: inicia o servidor de desenvolvimento.

npm run build: compila o projeto para produção.

npm run preview: pré-visualiza a versão de produção localmente.

## 📝 Observações
- Este é um projeto pessoal com foco em aprendizado e prática de Vue e Vite.
- O gerenciamento de estado é feito localmente, sem backend.
- IDs únicos para os livros são gerados no frontend utilizando:

  ```bash
  newBook.id = Math.max(...books.map(el => el.id)) + 1;
