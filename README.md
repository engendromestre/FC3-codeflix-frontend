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
- Agora temos o nosso desenvolvimento contínuo pronto (CD)

# Prettier Config

- site do tailwind css / Docs / Editor Setup
- A gente pode fazer uso de intelisense para quando estiver trabalhando com o tailwind
- Essa configuração é essencial para a produtividade
- O tailwind intellisense tem integração do vscode e essa integração permite que a gente veja os nomes das funções
- Digamos que eu queira mudar a cor do fundo para azul. Aqui no JS eu precisaria configurar uma classe css com o background de cor azul. No tailwind é diferente, ele já te dá uma base de cores deixando preparado para o dev todo o esquema de um design system (conjunto de componentes reutilizáveis).
- Para ter acesso ao intellisense (autocomplete, syntax highlighting and linting) é preciso instalar a extensão no VSCode

- Prettier: permite formatar o nosso código de forma automática e alternativa. Isso é muito importante quando se trabalha com times deixando a codificação dos projetos com uma mesma cara e possamos confiar que a estilização do projeto seja igual para que todos os devs estejam no mesmo caminho.
- Prettier and Tailwind: Automatic Class sorting with prettier. Ordena automaticamente as classes de acordo com as recomendações do tailwind.

# Tailwindcss Utility First

- Qual a maior diferença entre usar CssJS ou qualquer outra lib (biblioteca) e o Prettier. Uma das formas de organizar o CSS é utilizando a Metodologia BEM (Block Element Mdifier), uma das abordagens mais utilizadas para nomenclatura das classes CSS que focava o nome do componente e o que ele faz e ia-se quebrando isso em camadas. O maior problema de utilizar essa abordagem é que ela não é escalável, pois a cada página que fosse criada seria necessário criar também mais CSS. Um projeto de mais de 5 anos de produção teria uma quantidade enorme de CSS legado para se desenvolver. Não se consegue ver claramente classes repetidas, colisão entre classes, não se reaproveitando código. O CSS funciona como Folha de Estilo em Cascata, e a melhor maneira de se utilizar um CSS é reutilizando código. Então se tinha um custo muito grande de tempo de desenvolvimento, de processamento e armazenando desses arquivos CSS.

- Aqui temos que pensar as classes como funcões que a gente reutiliza durante a codificação do programa.
- Sabemos ao analisar as classes o que elas estão fazendo extamente e se vão entrar em conflito umas com as outras
- Também faz remoção (dead-code elimination): faz remoção de todo o código que não está sendo utilizado no build
- Te dá uma série de seletores que podem ser usados de forma funcional, e na hora do build ele verifica o que não estão sendo usados e remove do nosso CSS final para a produção.

- page.tsx
- globals.css
- layer base (estretégia para uso global para todas as páginas)
- Responsividade: na documentação já tem breakpoints pré-definidos.
- vh - view hight
- layout que vai servir como wrapper para todas as outras telas

# Header Hook

- todas as páginas são renderizada no servidor, exceto páginas ou componetes que fazem modificação de estado, sendo necessária a sua renderização do lado do cliente.
