---
tags:
  - meta
---
this is page is more on the technical side / 101 of setting up an online garden. fair warning that i didn't mean for this to be a tutorial but more of a record of what i did so i can backtrack in case i fork some things up or just plainly forget.

if you're more interested on the *whys* of setting up an online garden, you can read about it [[on setting up an online garden|here]].

> [!attention] re: links
> to be updated teka lang

# initial set-up

- installed [node.js](https://nodejs.org/en) version 26.13.0
- created a new obsidian vault
- installed quartz by running ```npm create quartz@latest``` on terminal
- connected to github for hosting

# obsidian

## configurations

- explored some themes and plug-ins

## themes installed

 - **everforest** - i think this will always be my default, ever since discovering and using it on vscode (i believe this was based on gruvbox? or was it the other way around? don't quote me yet i'm gonna google later)
- **primary** - i've always ever wanted a cookie-themed digital notebook. it gives cookie run kingdom vibes!!!!!
- **underwater** - my current !!!!!! i thinks this made me really understand the difference of a theme vs just color palettes. it is a ***theme*** theme
- **wikipidia** - self-explanatory. this is so cool
- **maple** - this is somewhat primary's little sister and is also its minimal version

## frankensteined themes

### underwater with primary colors

```
{
  "underwater-theme@@underwater-colors-light": "uw-aqua",
  "underwater-theme@@underwater-colors-dark": "uw-deep",
  "underwater-theme@@foam-rgb@@light": "#BF3F35",
  "underwater-theme@@gold-rgb@@light": "#D6971A",
  "underwater-theme@@love-rgb@@light": "#593E21",
  "underwater-theme@@rose-rgb@@light": "#23739B",
  "underwater-theme@@pine-rgb@@light": "#339562",
  "underwater-theme@@iris-rgb@@light": "#D9746E",
  "underwater-theme@@text@@light": "#593E21",
  "underwater-theme@@bold-color": "var(--rose)",
  "underwater-theme@@italic-color": "var(--rose)",
  "underwater-theme@@underline-color": "var(--rose)",
  "underwater-theme@@strikethrough-color": "var(--rose)",
  "underwater-theme@@callout": "callout-outlined",
  "underwater-theme@@list-marker-color": "var(--text)",
  "underwater-theme@@subtle@@light": "#339562",
  "underwater-theme@@h2-color": "var(--love)",
  "underwater-theme@@h3-color": "var(--love)",
  "underwater-theme@@h4-color": "var(--love)",
  "underwater-theme@@h5-color": "var(--love)",
  "underwater-theme@@h6-color": "var(--love)",
  "underwater-theme@@text-highlight-bg": "rgba(var(--gold-rgb), 0.2)",
  "underwater-theme@@links-styling": "normal",
  "underwater-theme@@vault-icon": "vault-dev",
  "underwater-theme@@no-bases": false,
  "underwater-theme@@overlay@@light": "#F1EBE3",
  "underwater-theme@@base@@light": "#F1EBE3",
  "underwater-theme@@muted@@light": "#9D8E7D",
  "underwater-theme@@checkbox": "checkbox-circle"
}
```

## community plug-ins i have

- better properties
- brat
- calendar
- commander
- dataview
- hider
- importer
- kanban
- style settings
- templater

# quartz

## configurations

### installing a theme

you can find a looooong list of theme options [here](https://github.com/saberzero1/quartz-themes).

once you've picked a theme:

- [ ] run `npm install @quartz-themes/core @quartz-themes/[YOUR CHOSEN THEME]`
	- for example: `npm install @quartz-themes/core @quartz-themes/everforest`
- [ ] open config.yaml →  `open -e quartz.config.yaml`
- [ ] find `source: "@quartz-themes/core"` (cmd + f if  you must)
	- you will see something like this by default:
		```
		- source: "@quartz-themes/core"
		  enabled: false
		  options:
		    theme: tokyo-night
		    mode: both
		```

- [ ] change it to `enabled: true`, `theme: [YOUR CHOSEN THEME]`, and `mode: both` can  be `light` or `dark` too
- [ ] to check if plug-ins are working cleanly → `npx quartz plugin install --from-config`
- [ ] then run preview (or not) and publish
### script short-cuts

#### npm run preview

a shortcut to running `npx quartz build --serve` or `npx quartz build -d \"[YOUR PATH HERE]" --serve"` everytime

- [ ] run `npm pkg set scripts.preview="npx quartz build -d \"[YOUR PATH HERE]" --serve"`

#### npm run publish

a shortcut to running `npx quartz sync --no-pull` everytime

- [ ] run `npm pkg set scripts.publish="npx quartz sync --no-pull"`

### in case you fork up

- [ ] reset → `git checkout package.json`

# other gardens to visit

- [olu](https://notes.olu.online/)
- [eilleen](https://quartz.eilleeenz.com/)