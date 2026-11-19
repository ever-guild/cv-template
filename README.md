# CV PDF Template

A minimal template for generating a CV PDF from a single Markdown file

## Goal

- edit `cv.md` and optionally add `cv.png` or `cv.jpg` to override the generated identicon
- run `make pdf`
- get `cv-xp-<mode>.pdf`

## Local build

```bash
make doctor
make pdf xp=4       # show 4 full experience entries
make pdf xp=full    # show all experience entries in full format
```

## Example coverage

`cv.md` demonstrates contact links, a Booking button, service icons, skill
categories, languages, full-time and part-time roles, project metadata, and
education details. The Booking URL is Ilyar's real scheduling link; replace it
when adapting the sample. Other sample profile and project URLs are illustrative.

Public highlights from all roles appear in Key Achievements. Links can be inline
Markdown or nested `Submission`, `Demo`, and `Reddit demo` bullets. Known services
get their own icons; other URLs use the external-link icon.

The default `xp=4` layout shows the first three bullets for each of the first four
roles and summarizes earlier roles. Use `xp=full` to display all experience
bullets, including delivery, responsibilities, tooling, and constraints.
Project subsection details are parsed but are not expanded in the PDF; project
names and technology lists serve as fallbacks for roles without their own bullets.

`Calendly` is an alias for `Booking`. A single `## Basics` section can replace
`## Contact` and `## Profile`; do not combine these two formats. Telegram also
accepts an `@username`. Skill category names are free-form; `Languages` gets its
own section. A local `cv.png` or `cv.jpg` replaces the generated avatar.

## Dev Container CLI

Docker is required for this workflow

```bash
npm install -g @devcontainers/cli
devcontainer up
devcontainer exec make pdf
```

Or use [deco](https://github.com/ilyar/deco) alternatively for `@devcontainers/cli` 

```bash
curl -fsSL https://raw.githubusercontent.com/ilyar/deco/refs/heads/main/install.sh | bash
deco exec make pdf
```
