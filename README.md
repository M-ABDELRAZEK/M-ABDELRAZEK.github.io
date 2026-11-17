# Mohamed Abdelrazek | Portfolio

Personal engineering portfolio of **Mohamed Abdelrazek Abou-Shahin**, an Electrical Engineering student and Electrical Head of Menofia Racing Team, focused on EV powertrains, battery systems and Model-Based Design.

**Live site:** [m-abdelrazek.github.io](https://m-abdelrazek.github.io)

## What's inside

- **EV powertrain and battery design:** Formula Student 2025 (FSUK), Shell Eco-marathon 2025 and 2026, EVER Egypt 2024
- **Model-Based Design (MATLAB/Simulink):** passive cell balancing, accelerator pedal sensor (APPS) fault detection, automatic headlights, vehicle indicators with MIL/SIL/HIL testing, ADAS direction detection
- **Skills, resume and contact links**

## Built with

- [Jekyll](https://jekyllrb.com/) and GitHub Pages
- Based on the free-to-engineer portfolio template from [Lowinertia](https://lowinertia.com)

## Project structure

| Path | Purpose |
|---|---|
| `_config.yml` | Name, headline, links, skills and theme colors |
| `_projects/` | One folder per project, each with an `index.md` |
| `_layouts/`, `_includes/` | Page layouts and reusable components |
| `assets/` | Images, resume and scripts |
| `css/` | Styles |

## Run locally

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000`.

## Add a project

Create `_projects/<project-name>/index.md` with this front matter, then write the content below it in Markdown:

```yaml
---
layout: post
title: "Project title"
description: "Short description of the project"
skills:
  - MATLAB/Simulink
  - Stateflow
main-image: /project.webp
---
```

## Contact

- [LinkedIn](https://www.linkedin.com/in/mohamed-abdelrazek-a8aa98246/)
- [GitHub](https://github.com/M-ABDELRAZEK)
- [Digital portfolio on Lowinertia](https://lowinertia.com/portfolio/m-abdelrazek)

## License

Released under the CC0-1.0 license (see [LICENSE](LICENSE)).
