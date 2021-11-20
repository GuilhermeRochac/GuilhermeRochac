📫 How to reach me guiolirocha2017@gmail.com

💻 I'm Developer!

📚 I’m currently learning everything from front-end and back-end.

📤 2021 Goals: take more programmer courses and find a new job

![programador](https://user-images.githubusercontent.com/89705029/142737718-b3bca479-7f50-4399-97da-ad9e8be1163a.gif)

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
  
