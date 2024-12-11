Alterar jnome do arquivo
alterando o username


# Nome da Actions:  
name: Snake Game

# Controlador do tempo que sera feito a atualização dos arquivos.
on:
  schedule:
      # Será atualizado a cada 5 horas.
    - cron: "0 */5 * * *"

# Permite executar na na lista de Actions (utilizado para testes de build).
  workflow_dispatch:

# Regras
jobs:
  build:
    runs-on: ubuntu-latest
    steps:

    # Checks repo under $GITHUB_WORKSHOP, so your job can access it
      - uses: actions/checkout@v2

    # Repositorio que será utilizado para gerar os arquivos.
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: nomeUsuario #Seu usuario
          gif_out_path: dist/github-contribution-grid-snake.gif
          svg_out_path: dist/github-contribution-grid-snake.svg

      - run: git status

      # Para as atualizações.
      - name: Push changes
        uses: ad-m/github-push-action@master
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          branch: master
          force: true

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          # the output branch we mentioned above
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}


Retornando na opção Actions do repositório, clique em “Run workflow”:

Repositorio

Pasta dos arquivos:
Em seu repositorio cliente em main e selecione a branch output:
output

E aqui estão os arquivos gerados que você pode utilizar como bem entender:

Arquivos

Codigo Github para utilização:

![snake gif](https://github.com/SEU_USUARIO/SEU_REPOSITORIO/blob/output/github-contribution-grid-snake.svg)

👋 One new thing before you go

Tired of getting nickel-and-dimed on your side projects? 😒
We have created a membership program that helps cap your costs so you can build and experiment for less. And we currently have early-bird pricing which makes it an even better value! 🐥

The DEV Team 
Introducing DEV++
Ben Halpern for The DEV Team ・ Aug 29
#meta #news #productivity #career
Just one of many great perks of being part of the network ❤️

Top comments (0)
Subscribe
pic
Add to the discussion
Code of Conduct • Report abuse
profile
AWS
Promoted

AWS Security LIVE! Stream

Level up your security knowledge and skills
Join AWS Security LIVE! for expert insights on threat detection, infrastructure protection, and more. Hosted by AWS experts and AWS Partners. No sales pitches, just deep dives!

Learn More

Read next
kannav02 profile image
Testing with Jest
Kannav Sethi - Nov 11

komsenapati profile image
Deploy a bento to GitHub Pages
K Om Senapati - Nov 9

gaundergod profile image
Lucia Auth is getting deprected
Gleb Kotovsky - Oct 21

waradu profile image
How to commit
Waradu - Nov 9


Henrique Lopes
Follow
"Não há razão alguma em usar a palavra “impossível” para descrever algo que claramente pode acontecer."
Joined
5 de set. de 2021
Trending on DEV Community 
Mercy profile image
What is your favorite IDE?
#discuss #webdev #vscode
Ben Halpern profile image
Meme Monday
#discuss #jokes #watercooler
Ravin Rau profile image
8 Type of Load Balancing
#discuss #webdev #cloudcomputing #programming
profile
AWS
Promoted

AWS Security LIVE! Stream

Practical guidance for security practitioners
Don't miss AWS Security LIVE! Whether you're an AWS newbie or a seasoned pro, this show has something for everyone with actionable tips, expert advice, and security knowledge.

Learn More



# Nome da Actions:  
name: Snake Game

# Controlador do tempo que sera feito a atualização dos arquivos.
on:
  schedule:
      # Será atualizado a cada 5 horas.
    - cron: "0 */5 * * *"

# Permite executar na na lista de Actions (utilizado para testes de build).
  workflow_dispatch:

# Regras
jobs:
  build:
    runs-on: ubuntu-latest
    steps:

    # Checks repo under $GITHUB_WORKSHOP, so your job can access it
      - uses: actions/checkout@v2

    # Repositorio que será utilizado para gerar os arquivos.
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: nomeUsuario #Seu usuario
          gif_out_path: dist/github-contribution-grid-snake.gif
          svg_out_path: dist/github-contribution-grid-snake.svg

      - run: git status

      # Para as atualizações.
      - name: Push changes
        uses: ad-m/github-push-action@master
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          branch: master
          force: true

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          # the output branch we mentioned above
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}




# Nome da Actions:  
name: Snake Game

# Controlador do tempo que sera feito a atualização dos arquivos.
on:
  schedule:
      # Será atualizado a cada 5 horas.
    - cron: "0 */5 * * *"

# Permite executar na na lista de Actions (utilizado para testes de build).
  workflow_dispatch:

# Regras
jobs:
  build:
    runs-on: ubuntu-latest
    steps:

    # Checks repo under $GITHUB_WORKSHOP, so your job can access it
      - uses: actions/checkout@v2

    # Repositorio que será utilizado para gerar os arquivos.
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: nomeUsuario #Seu usuario
          gif_out_path: dist/github-contribution-grid-snake.gif
          svg_out_path: dist/github-contribution-grid-snake.svg

      - run: git status

      # Para as atualizações.
      - name: Push changes
        uses: ad-m/github-push-action@master
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          branch: master
          force: true

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          # the output branch we mentioned above
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
