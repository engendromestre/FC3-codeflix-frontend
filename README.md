# Projeto Inicial

- Create Next App: a aplicação semelhante ao create next app responsável pelo start, pelo boostrap do projeto. Esse pacote torna o processo da criação inicial muito simples. Pode ser usado com o comando npx para fazer o Scaffold do projeto completo. Ajuda também a definir, setar e configurar o tailwind e o eslint.

- npx create-next-app

  - What is your project Name? codeflix-client
  - Typescript? Y
  - ESLint? Y
  - Tailwind CSS? Y
  - 'src' directory? Y
  - 'app/' directory? Y
  - import alias like configured? default

- A partir das depedências instaladas tem-se o projeto rodando.

- cd codeflix-client
- yarn (para instalar as dependências)
- yarn dev (para iniciar um servidor na porta 3000)

- .next (Todas as configurações do NextJS)
- src (usando o app directory que é uma feature do Next3, ou seja, é o esquema de como a aplicação será dividida)
  - se você vem do Rails ou de frameworks parecidos vai se familiarizar pois se tem layout e páginas onde cada diretório funciona como se fosse um divisor para partes da aplicação. Cada diretório terá uma página, também uma API e pode ter um layout.
- Tudo pronto para começar, se for modificada alguma página, por meio do hot-reload, assim que salvar a modificação ela estará disponível para ser visualizada no brownser.
- Também já se tem acesso a todas as configurações do tailwind

## Processo de Build

- yarn build (gera as páginas estáticas da aplicação)
- utilizar a plataforma Vercel para fazer o deploy da aplicação

- rm -rf .git
- git remote add origin git@github.com:engendromestre/FC3-codeflix-frontend.git

- Adicionar projeto no GitHub e depois subir o projeto na Vercel
- A vercel vai escanear todo o repositório, adicionar as configurações necessárias e dar acesso a todo o esquema de deploy do projeto.
- Agora o projeto já está disponível na nuvem da Vercel e toda vez que dermos um push para a branch main as modificações já vão automaticamente estar visíveis no projeto na Vercel.
- O código é buildado novamente e temos algumas URLs para deploy e para preview
