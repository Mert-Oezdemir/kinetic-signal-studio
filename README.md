# Kinetic Signal Studio

A visual editor for cubic Bézier timing curves. Open `index.html` in a current browser. The app runs offline and uses no dependencies.

- Try one of four presets or adjust the two control points with the sliders.
- Scrub to see a position without playback, or use Play motion to preview a full run.
- Select the CSS easing field and copy its value to a stylesheet.

The interface, math, text, and drawing code were created independently. The motion demo that prompted the project is linked for context. [Concept reference](https://github.com/YildizDikme/Framer-Motion)

## Local server and agent connection

Install Node 22 or newer and Git. From this repository run:

```sh
npm ci
npm start
```

Open the loopback URL printed by the command. The runtime is pinned to a specific revision of [Project Agent Bridge](https://github.com/Mert-Oezdemir/project-agent-bridge).

To connect an MCP-compatible agent, run `npm run mcp:config --silent` and add its `mcpServers` entry to your host. Run `npm run doctor` to see local project and account configuration.

Chrome or Edge is needed for agent browser controls. You can set `CHROME` in `.env`, or run `npx playwright install chromium` to install a browser.

Copy `.env.example` to `.env` before adding account settings. Keep `.env` local. Restart the runtime after changing it.
