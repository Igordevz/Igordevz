### Hello, I'm igor Silva Programmer👋

[![Blog](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/igor-silva-386b09255/) ![blog](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)
[![blog](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/euigor_santoss/)


[![Anurag's GitHub stats-Dark](https://github-readme-stats.vercel.app/api?username=Igordevz&show_icons=true&theme=dark#gh-dark-mode-only)](https://github.com/Igordevz)



###  Some Skills
![blog](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![blog](https://img.shields.io/badge/Express.js-404D59?style=for-the-badge)
![blog](https://img.shields.io/badge/React_Router-CA4245?style=for-the-badge&logo=react-router&logoColor=white)
![blog](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![blog](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![blog](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![blog](https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![blog](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
![blog](https://img.shields.io/badge/styled--components-DB7093?style=for-the-badge&logo=styled-components&logoColor=white)
![blog](https://img.shields.io/badge/Netlify-00C7B7?style=for-the-badge&logo=netlify&logoColor=white)
![blog](https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E)
![blog](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)


### [![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=IgorDevz&layout=compact)](https://github.com/Igordevz/chatgpt-integration)



Nome da Actions:
name: Snake Game

Controlador do tempo que sera feito a atualização dos arquivos.
on:
  schedule:
      # Será atualizado a cada 5 horas.
    
cron: "0 /5 * *"

Permite executar na na lista de Actions (utilizado para testes de build).
  workflow_dispatch:

Regras
jobs:
  build:
    runs-on: ubuntu-latest
    steps:

    # Checks repo under $GITHUB_WORKSHOP, so your job can access it
      
uses: actions/checkout@v2

    # Repositorio que será utilizado para gerar os arquivos.
      
uses: Platane/snk@master
      id: snake-gif
      with:
        github_user_name: Formandodev #Seu usuario
        gif_out_path: dist/github-contribution-grid-snake.gif
        svg_out_path: dist/github-contribution-grid-snake.svg

      
run: git status

      # Para as atualizações.
      
name: Push changes
      uses: ad-m/github-push-action@master
      with:
        github_token: ${{ secrets.GITHUB_TOKEN }}
        branch: master
        force: true

      
uses: crazy-max/ghaction-github-pages@v2.1.3
      with:# the output branch we mentioned above
        target_branch: output
        build_dir: dist
      env:
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
