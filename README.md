# Olá, Bem vindo(a)


Me chamo Diogo, sou estudante de análise e desenvolvimento de sistemas (3 semestre), e atualmente estou estudando sobre Front-End. Meu objetivo é unir um design intuitivo e elegante, com código eficiente para entregar projetos de alta qualidade.

## Habilidades em estudo no momento

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/61/HTML5_logo_and_wordmark.svg/120px-HTML5_logo_and_wordmark.svg.png" alt="HTML5" width="80"> <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d5/CSS3_logo_and_wordmark.svg/120px-CSS3_logo_and_wordmark.svg.png" alt="CSS3" width="80"> <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Unofficial_JavaScript_logo_2.svg/120px-Unofficial_JavaScript_logo_2.svg.png" alt="JavaScript" width="80">


## Ferramentas

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e0/Git-logo.svg/120px-Git-logo.svg.png" alt="Git" width="80"> <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9a/Visual_Studio_Code_1.35_icon.svg/120px-Visual_Studio_Code_1.35_icon.svg.png" alt="VS Code" width="80">


Linkedin : https://shre.ink/QLm0


name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: rafaballerini
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
