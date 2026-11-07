---
tags:
  - meta
---
# common terminal commands
- open config → `open -e quartz.config.yaml`
- open css → `open -e quartz/styles/custom.scss` 
- run preview on localhost → `npx quartz build --serve` 
- upload changes online → `npx quartz sync`

# in case of reverting config to default

- [ ] change page title and base url
	```
	sed -i '' 's|baseUrl: quartz.jzhao.xyz|baseUrl: vuoyez.github.io/fieldnotes|g' quartz.config.yaml
	sed -i '' "s|pageTitle: Quartz 5|pageTitle: ch's fieldnotes|g" quartz.config.yaml
	```
- [ ] validate
	```
	grep -E "pageTitle:|baseUrl:" quartz.config.yaml
	```