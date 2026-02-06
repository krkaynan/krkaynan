# 👨🏻‍💻 Kaynan Raikkonen

**`FullStack developer`**

My name is Kaynan Raikkonen, I'm 18 years old, and I'm from São Paulo, Brazil. I graduated from high school at ETEC, with a technical degree in Administration. I'm currently studying Systems Development at SENAI and Software Engineering at UMC.
<p align="left">
    <a href="mailto:raikkonenkaynan@gmail.com">
    <img
        alt="Gmail"
        src="https://img.shields.io/badge/GMAIL-cc4b4b?style=for-the-badge&logo=gmail&logoColor=white&labelColor=a83232"
    />
    </a>
    <a href="https://wa.me/5511945553352" target="_blank">
    <img
        alt="WhatsApp"
        src="https://img.shields.io/badge/WHATSAPP-25D366?style=for-the-badge&logo=whatsapp&logoColor=white&labelColor=1DA85D"
    />
    </a>
</p>

---

name: Update README cards

on:
  schedule:
    - cron: "0 3 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - name: Generate stats card
        uses: readme-tools/github-readme-stats-action@v1
        with:
          card: stats
          options: username=${{ github.repository_owner }}&show_icons=true
          path: profile/stats.svg
          token: ${{ secrets.GITHUB_TOKEN }}

      - name: Commit cards
        run: |
          git config user.name "github-actions"
          git config user.email "github-actions@users.noreply.github.com"
          git add profile/*.svg
          git commit -m "Update README cards" || exit 0
          git push


---
<div align="center">

### Languages

[![My Skills](https://skillicons.dev/icons?i=html,css,js,python,java)](https://skillicons.dev)

### Frameworks & Tools

[![My Skills](https://skillicons.dev/icons?i=fastapi,django,git,vue,nodejs,react,flask,postgres,mysql,figma,azure,gcp,aws)](https://skillicons.dev)

</div>
