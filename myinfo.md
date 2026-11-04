**OmniRoute: Free AI Gateway**
Step by Step Installation Guide

**OmniRoute is a free**, open-source AI gateway. It connects many AI providers, including free ones, behind a single endpoint. Your coding tool (Cursor, Cline, Claude Code and others) talks to that one endpoint, OmniRoute picks a provider for you, and if one provider hits its limit it switches to another automatically.

Official Links
Website: https://omniroute.online
GitHub: https://github.com/diegosouzapw/OmniRoute

Be careful: There are many mirror sites and hosting pages for OmniRoute. Download and install commands only from the two official links above, and stay away from fake sites.

Before You Start
A computer running Windows, Mac or Linux.
Node.js 22 LTS (recommended). Check the GitHub README for the latest requirement.
An internet connection and about 10 minutes. No credit card needed.
**Step 1** : Install Node.js
Open nodejs.org in your browser.
Download the LTS version and install it.
Open a terminal and check:
bash
node -v

If it prints a version number (for example v22.x.x), Node is installed correctly.

**Step 2**: Open a Terminal
Windows: search for "PowerShell" in the Start menu.
Mac: press Cmd + Space, type "Terminal".
Linux: press Ctrl + Alt + T.

**Step 3**: Install OmniRoute

Paste this into the terminal and press Enter:

bash
npm install -g omniroute

It can take about a minute. If it finishes without errors, the install worked.

**Step 4**: Start OmniRoute
bash
omniroute

The server starts on port 20128.

Important: Do not close this terminal window. Closing it stops OmniRoute.

**Step 5**: Open the Dashboard

Open this address in your browser:

http://localhost:20128

The dashboard appears. On first run a password or setup screen may show up. Follow it.

**Step 6**: Connect a Free Provider
Go to the Providers page and click Add Provider.
Choose a free option, for example Kiro AI (for Claude models) or OpenCode Free.
Click Connect and follow the instructions on screen.

Free providers and models change over time. What you see in your own dashboard is the final word.

**Step 7**: Get Your API Key
Open Settings, then the API Keys section.
Create a new key or copy an existing one.

Never share your API key with anyone, and blur it in screenshots.

**Step 8**: Use It in Your Tool

Open the settings of Cursor, Cline, Claude Code or any OpenAI-compatible tool and enter:

Base URL : http://localhost:20128/v1
API Key  : (the key from Step 7)
Model    : auto   (or pick one from the dashboard list)

Send a prompt. If a response comes back, your setup is complete!

Optional: Test From the Terminal (Mac / Linux)
bash
curl http://localhost:20128/v1/chat/completions \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -d '{"model":"auto","messages":[{"role":"user","content":"Hello!"}]}'
Alternative: Install With Docker

If Node gives you trouble and you have Docker installed:

bash
docker run -d --name omniroute --restart unless-stopped \
  -p 20128:20128 -v omniroute-data:/app/data \
  -e DATA_DIR=/app/data diegosouzapw/omniroute:latest

Then open http://localhost:20128.

**Common Problems and Solutions**
| Problem | Solution |
|---|---|
| "npm" is not recognized | Node.js did not install properly. Reinstall it, then close and reopen the terminal. |
| Node version error | Install Node 22 LTS and check the GitHub README for the latest requirement. |
| EACCES / permission error (Mac, Linux) | Put `sudo` before the command, or fix your npm global folder permissions. |
| localhost:20128 does not open | Check that `omniroute` is still running in the terminal. If you closed it, start it again. |
| Port 20128 already in use | Close the other app using that port, or check whether OmniRoute is already running. |
| No response from the model | Check that your provider is connected on the Providers page. You may have hit a free limit, so connect another provider. |

Official website: omniroute.online · Official GitHub: github.com/diegosouzapw/OmniRoute

join my biggest community to get more info like this became expert using Ai

**https://chat.whatsapp.com/FFpCBlrGWXyJLnlVOgzbGW**

@growwithwenky
