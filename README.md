🌱 My name is G
💬 SAN - 2998483320
😄 编程白总
⚡ 哪有人会喜欢孤独，不过是不喜欢失望罢了。  --村上春树
⚡ 记得你的温柔多富有，我不愿改变这境遇当王侯。  --莎士比亚
⚡ 这个世界太假，我们唯一能做的就是减少一切情绪。  --《请回答1918》


<!--
**Ggy-king/Ggy-king** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

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
# Visit https://github.com/lowlighter/metrics/blob/master/action.yml for full reference
name: Metrics
on:
  # Schedule updates (each hour)
  schedule: [{cron: "0 * * * *"}]
  # Lines below let you run workflow manually and on each commit
  workflow_dispatch:
  push: {branches: ["master", "main"]}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    steps:
      - uses: lowlighter/metrics@latest
        with:
          # Your GitHub token
          # The following scopes are required:
          #  - public_access (default scope)
          # The following additional scopes may be required:
          #  - read:org  (for organization related metrics)
          #  - read:user (for user related data)
          #  - repo      (optional, if you want to include private repositories)
          token: ${{ secrets.METRICS_TOKEN }}

          # Options
          user: Ggy-king
          template: classic
          base: header, activity, community, repositories, metadata
          config_timezone: Asia/Shanghai
          plugin_achievements: yes
          plugin_achievements_display: detailed
          plugin_achievements_ignored: 财富者，编程机器，思路清奇
          plugin_achievements_limit: 6
          plugin_achievements_threshold: C
          plugin_fortune: yes
          plugin_habits: yes
          plugin_habits_charts: yes
          plugin_habits_charts_type: chartist
          plugin_habits_days: 20
          plugin_habits_facts: yes
          plugin_habits_from: 200
          plugin_languages: yes
          plugin_languages_aliases: javascript,html,css,python,c++,c
          plugin_languages_analysis_timeout: 18
          plugin_languages_categories: markup, programming
          plugin_languages_colors: github
          plugin_languages_ignored: java
          plugin_languages_indepth: yes
          plugin_languages_limit: 8
          plugin_languages_recent_categories: markup, programming
          plugin_languages_recent_days: 14
          plugin_languages_recent_load: 300
          plugin_languages_sections: most-used
          plugin_languages_threshold: 0%
          plugin_music: yes
          plugin_music_limit: 6
          plugin_music_time_range: short
          plugin_music_top_type: artists
          plugin_music_user: .user.login
          plugin_nightscout: yes
          plugin_nightscout_datapoints: 12
          plugin_nightscout_highalert: 180
          plugin_nightscout_lowalert: 80
          plugin_nightscout_urgenthighalert: 250
          plugin_nightscout_urgentlowalert: 50
          plugin_nightscout_url: https://example.herokuapp.com
          plugin_notable: yes
          plugin_notable_from: organization
          plugin_notable_types: commit
          plugin_people: yes
          plugin_people_limit: 24
          plugin_people_size: 28
          plugin_people_types: followers, following
          plugin_repositories: 100
          plugin_repositories: yes
          plugin_repositories_affiliations: owner
          plugin_repositories_batch: 100
          plugin_rss: yes
          plugin_rss_limit: 4
          plugin_screenshot: yes
          plugin_screenshot_background: yes
          plugin_screenshot_selector: body
          plugin_screenshot_title: Screenshot
          plugin_skyline: yes
          plugin_skyline_frames: 60
          plugin_skyline_quality: 0.5
          plugin_skyline_year: current-year
          plugin_stackoverflow: yes
          plugin_stackoverflow_limit: 2
          plugin_stackoverflow_lines: 4
          plugin_stackoverflow_lines_snippet: 2
          plugin_stackoverflow_sections: answers-top, questions-recent
          plugin_stock: yes
          plugin_stock_duration: 1d
          plugin_stock_interval: 5m
          plugin_topics: yes
          plugin_topics_limit: 15
          plugin_topics_mode: starred
          plugin_topics_sort: stars
          plugin_wakatime: yes
          plugin_wakatime_days: 7
          plugin_wakatime_limit: 5
          plugin_wakatime_sections: time, projects, projects-graphs, languages, languages-graphs, editors, os
          plugin_wakatime_url: https://wakatime.com
          plugin_wakatime_user: current
