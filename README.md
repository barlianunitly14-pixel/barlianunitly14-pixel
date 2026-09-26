Add a gh-ascii ASCII profile card to my GitHub profile README.

Context:
- My GitHub handle: barlianunitly14-pixel
- My profile README lives in the repo barlianunitly14-pixel/barlianunitly14-pixel. If it doesn't exist, create it as a public repo with a README.
- Card generator: https://gh.crafter.run/barlianunitly14-pixel?theme=dark|light returns an SVG.

Steps:
1. Clone github.com/barlianunitly14-pixel/barlianunitly14-pixel and download both themes into its root:
   curl -fL "https://gh.crafter.run/barlianunitly14-pixel?theme=dark&cols=140" -o dark_mode.svg
   curl -fL "https://gh.crafter.run/barlianunitly14-pixel?theme=light&cols=140" -o light_mode.svg
2. Render or open both SVGs and look at them before committing.
3. Insert this at the top of README.md, keeping all existing content:
   <picture>
     <source media="(prefers-color-scheme: dark)" srcset="dark_mode.svg" />
     <source media="(prefers-color-scheme: light)" srcset="light_mode.svg" />
     <img alt="barlianunitly14-pixel's GitHub profile" src="dark_mode.svg" />
   </picture>
   If the light card reads poorly against white, use a plain <img src="dark_mode.svg" width="100%" /> instead of <picture> — the dark card carries its own background.
4. Commit both SVGs + the README change ("feat: add gh-ascii profile card") and push.
5. Confirm it renders at github.com/barlianunitly14-pixel.
