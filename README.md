![Profile Views](https://komarev.com/ghpvc/?username=Saaatsuki)

![GitHub Followers](https://img.shields.io/github/followers/Saaatsuki?label=follow&logo=github&style=flat)
[![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/platane/platane/main.yml?label=action&style=flat-square)](https://github.com/Platane/Platane/actions/workflows/main.yml)
[![GitHub release](https://img.shields.io/github/release/Saaatsuki/Saaatsuki.svg?style=flat-square)](https://github.com/Saaatsuki/Saaatsuki/releases/latest)
[![GitHub marketplace](https://img.shields.io/badge/marketplace-snake-blue?logo=github&style=flat-square)](https://github.com/marketplace/actions/generate-snake-game-from-github-contribution-grid)
![type definitions](https://img.shields.io/npm/types/typescript?style=flat-square)
![code style](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square)






  <picture>
  <source media="(prefers-color-scheme: dark)" srcset="github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="github-snake.svg" />
  <img alt="github-snake" src="github-snake.svg" />
</picture>

## Stats
![Profile Details](http://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=Saaatsuki&theme=gruvbox)
![Repos per Language](http://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=Saaatsuki&theme=gruvbox)
![Most Commit Language](http://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=Saaatsuki&theme=gruvbox)
![Stats](http://github-profile-summary-cards.vercel.app/api/cards/stats?username=Saaatsuki&theme=gruvbox)
![Productive Time](http://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=Saaatsuki&theme=gruvbox&utcOffset=9)

## Trophy
![Trophy](https://github-profile-trophy.vercel.app/?username=Saaatsuki&theme=gruvbox)

name: generate animation

on:
  schedule:
    - cron: "0 */24 * * *"
  workflow_dispatch:
  push:
    branches:
    - main

jobs:
  generate:
    permissions: 
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5
    steps:
      - name: generate github-contribution-grid-snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
        env:
          GITHUB_TOKEN: ${{ secrets.SAMPLE_SECRETS }}
      - name: push github-contribution-grid-snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.SAMPLE_SECRETS }}


![Snake animation](https://raw.githubusercontent.com/Saaatsuki/PythonPractice/output/github-contribution-grid-snake.svg)




<!--
**Saaatsuki/Saaatsuki** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
