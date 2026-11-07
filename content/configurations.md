this is page is more on the technical side / 101 of setting up an online garden. fair warning i didn't mean for this to be a tutorial but more of a record of what i did so i can backtrack in case i fork some things up or just forget.

if you're more interested on the *whys* of setting up an online garden, you can read about it [[on setting up an online garden|here]].

see also: my [[cheatsheet]], [[a gardener's diary|my gardener's diary]], and [[back of the notebook|the back of my notebook]].


> [!info] what i'm using
> **machine:** macbook air m1 (2020)\
> **coding tool:** terminal


# initial set-up

- installed [node.js](https://nodejs.org/en) version 26.13.0
- created a new obsidian vault
- installed quartz by running ```npm create quartz@latest``` on terminal
- connected to github for hosting

# obsidian

## configurations

- explored some themes and plug-ins

## themes installed

 - **everforest** - i think this will always be my default, eversince discovering and using it on vscode (i believe this was based on gruvbox? or was it the other way around? don't quote me yet i'm gonna google later)
- **primary** - oh my god ever since i was a child i've always ever wanted a cookie-themed digital notebook. it gives cookie run kingdom vibes!!!!!
- **underwater** - my current !!!!!! i thinks this made me really understand the difference of a theme vs just color palettes. it is a ==theme== - ya get me?
- **wikipidia** - self-explanatory. this is so cool
- **maple** - this is somewhat primary's little sister and is also its minimal version

## community plug-ins i have

- style settings
- calendar

> links to follow!!!

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

***

i don't know how this page turned into a how-to page but that's all the configurations i did so far