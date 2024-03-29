### Hello i'm Julia Araujo 👋
- 🌱 Estudante de Sistemas de Informação (SPtech)
- 📫 Contate-me no email: julia.oliveira@sptech.school
-  😄 Pronouns: She/her

[![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=JuliaAraujoOliveira&show_icons=true&theme=material-palenight)](https://github.com/anuraghazra/github-readme-stats)<br>
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=JuliaAraujoOliveira&show_icons=true&theme=material-palenight)](https://github.com/anuraghazra/github-readme-stats)

  <div>
     <img align="center" src="https://icongr.am/devicon/css3-original.svg?size=50&color=60307e">
     <img align="center" src="https://icongr.am/devicon/html5-original.svg?size=50&color=60307e">
     <img  align="center" src="https://icongr.am/devicon/javascript-plain.svg?size=50&color=60307e">
     <img  align="center" src="https://icongr.am/devicon/java-original.svg?size=50&color=60307e">
     <img  align="center" src="https://icongr.am/devicon/mysql-original.svg?size=50&color=60307e">
     <img  align="center"src="https://icongr.am/devicon/git-original.svg?size=50&color=60307e">
 </div>
<div>
 # GitHub Action for generating a contribution graph with a snake eating your contributions.

# ![snake gif](https://github.com/your-user-name/your-user-name/blob/output/github-contribution-grid-snake.gif)

name: Generate Snake

# Controls when the action will run.
on:
  schedule:
      # every 12 hours
    - cron: "0 */12 * * *"

  # This command allows us to run the Action automatically from the Actions tab.
  workflow_dispatch:
  
  # Also run on every push on the master branch
  push:
    branches:
    - main

# The sequence of runs in this workflow:
jobs:
  # This workflow contains a single job called "build"
  build:
    # The type of runner that the job will run on
    runs-on: ubuntu-latest

    # Steps represent a sequence of tasks that will be executed as part of the job
    steps:
      - name: Clone repo
        uses: actions/checkout@v3
    
      - name: Generate the snake files in './dist/'
        uses: Platane/snk@v3
        id: snake-gif
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |     
            dist/github-contribution-grid-snake.gif
            dist/github-contribution-grid-snake.svg
        env:
           GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

      - name: Show build status
        run: git status

      - name: Push new files to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
          commit_message: Update snake animations
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
</div>

<!--
**JuliaAraujoOliveira/JuliaAraujoOliveira** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 Contate-me no email: julia.oliveira@sptech.school
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
