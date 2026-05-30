# Ohio SNAP & Medicaid Assistant
### `ohio-benefits-chatbot-gemini.html`

A single, self-contained HTML file that helps Ohio residents understand the 2025–2026 changes to **SNAP** (food assistance) and **Medicaid** benefits. Powered by Google Gemini. No installation, no server, no dependencies — just open the file in a browser.

---

## Requirements

- A **Google Gemini API key** (free tier available)
- An internet connection
- **Chrome** or **Edge** browser (required for voice input; other browsers support text only)

---

## Quick Start

1. Get a free API key at [aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey)
2. Open `ohio-benefits-chatbot-gemini.html` in Chrome or Edge
3. Click **Settings** in the top-right of the chat panel
4. Paste your API key and click **Test Key** — the status dot turns green when connected
5. Start asking questions by typing or using the microphone

> Your API key is held in browser memory only for the current session. It is never saved to disk and is only sent to Google's API.

---

## Features

### Chat
- Ask questions about Ohio SNAP and Medicaid rule changes in plain language
- Full conversation memory — the assistant remembers what was said earlier in the session
- **Quick-question chips** for the six most common topics (disappear after first use)
- Typing indicator while the response is being generated
- Handles Gemini safety filter blocks gracefully with a helpful redirect message

### Voice Input
- Click the **microphone button** to speak instead of type
- Speech is transcribed in real time and shown in the voice bar as you talk
- Auto-sends the message when you stop speaking
- Click the microphone again or hit **Cancel** to stop at any time
- Supports multiple languages (configurable in Settings)

### Resources Sidebar
Direct links to 11 official Ohio resources, organized by category:

| Category | Links |
|----------|-------|
| Apply & Manage | Ohio Benefits portal, Self-service portal, County JFS office finder |
| SNAP | ODJFS SNAP overview, SNAP work requirement changes, OhioMeansJobs |
| Medicaid | Ohio Dept. of Medicaid, Ohio Medicaid coverage groups |
| Legal & Advocacy | Legal Aid Society of Cleveland, Ohio Legal Help, Health Policy Institute of Ohio |

### Status Indicator
A color-coded dot in the chat header shows connection state at a glance:

| Color | Meaning |
|-------|---------|
| 🟡 Amber | No API key entered yet |
| 🟢 Green | Gemini connected and responding |
| 🔴 Red | API key error or connection problem |

---

## Settings Panel

Click the **Settings** button (gear icon) in the chat header to configure the tool.

### 🔑 Gemini API Key

| Field | Description |
|-------|-------------|
| API Key | Your `AIza…` key from Google AI Studio. Use **Show/Hide** to toggle visibility. |
| Model | Which Gemini model to use (see table below) |
| Test Key button | Sends a test request to verify the key is valid and the model is accessible |

**Available models:**

| Model | Notes |
|-------|-------|
| `gemini-3.1-flash-lite` | Fastest responses, basic tier |
| `gemini-2.5-flash` | Default — reliable and stable, recommended for most use |
| `gemini-2.5-flash-lite` | Lightweight legacy option |

### 🎙 Voice — Recognition Language

| Language | Setting |
|----------|---------|
| English (US) | `en-US` — default |
| English (UK) | `en-GB` |
| Spanish (US) | `es-US` |
| Spanish (Spain) | `es-ES` |
| Arabic | `ar-US` |
| Somali | `so-SO` |
| French | `fr-FR` |

Voice uses the browser's built-in Web Speech API. **Chrome and Edge only.** No microphone software or additional setup is required.

---

## What the Chatbot Knows

The assistant's knowledge is embedded directly in the file as a system prompt, covering Ohio-specific information current as of **May 2026**.

### SNAP (effective February 1, 2026)
- Work requirement exemptions **eliminated** for veterans, homeless individuals, former foster youth, and adults over 54 (change took effect November 2025)
- Able-bodied adults without dependents (ABAWDs) ages 18–64 must work or participate in an approved activity for **80+ hours per month**
- Adults with children age 14 or older must now also meet work requirements
- **March 1, 2026** deadline to submit proof of employment or a verification form
- **May 1, 2026** — recipients who have not met requirements or proven an exemption for 3+ months lose benefits
- How to submit proof: online at ssp.benefits.ohio.gov, by mail, or in person at a local JFS office

**Still exempt from SNAP work requirements:**
- Pregnant individuals
- People physically or mentally unable to work (with medical certification)
- People caring for a child under age 14
- Adults age 65 and older
- Adults age 60–64 who are pregnant, live with a child under 14, or cannot work
- People receiving unemployment compensation
- Native Americans, Urban Indians, and California Indians

**Other SNAP changes:** Refugees are no longer eligible. Income limits updated October 1, 2025.

### Medicaid (work requirements begin January 1, 2027 — not yet in effect)
- Affects **Group VIII / ACA expansion** adults ages 19–64 at or below 138% of the federal poverty level
- Must complete 80 hours/month of qualifying activities (work, community service, job training, education)
- Exemptions: pregnant, disabled, age 65+, physically or mentally unable to work
- Estimates range from 62,000 to 200,000+ Ohioans losing coverage
- Special Income Level for long-term care: $2,982/month
- Some members now face six-month eligibility reviews instead of annual renewals

---

## Updating the Knowledge Base

Rules change. To keep the chatbot current:

1. Open the file in any text editor
2. Find the `const SYS = \`...\`` block near the top of the `<script>` section
3. Edit the relevant facts
4. Save the file and reload the browser tab

No build tools, packages, or server restarts are needed.

---

## Troubleshooting

**Blue "API key required" banner is showing**
Click **Enter API Key**, paste your key from [aistudio.google.com](https://aistudio.google.com/app/apikey), and click **Test Key**.

**Status dot is red after testing**
- Double-check the key was copied completely (starts with `AIza`)
- Make sure the key has not been revoked in Google AI Studio
- Check that your free-tier quota has not been exceeded

**Microphone button does nothing or shows an error**
- Confirm you are using Chrome or Edge — Firefox and Safari do not support Web Speech
- Allow microphone access when the browser prompts; check the address bar for a blocked microphone icon
- On a kiosk or locked-down device, microphone permissions may be restricted by policy

**Responses seem cut off or incomplete**
The model is limited to 1,000 output tokens per response. For detailed questions, try asking follow-ups or requesting a specific section.

---

## Disclaimer

This tool provides **general information only** and is not legal advice. Eligibility rules vary by individual circumstance and are subject to change. Always confirm your specific situation with:

- Your **local county Job and Family Services (JFS) office** — [find yours](https://jfs.ohio.gov/county/countydirectory.stm)
- **Legal Aid Society of Cleveland** — [lasclev.org](https://lasclev.org)
- **Ohio Legal Help** — [ohiolegalhelp.org](https://www.ohiolegalhelp.org)

---

## Sources

- Ohio Department of Job and Family Services — jfs.ohio.gov
- Ohio Department of Medicaid — medicaid.ohio.gov
- One Big Beautiful Bill Act (HR 1, signed July 4, 2025)
- Summit County DJFS SNAP work requirement guidance
- Health Policy Institute of Ohio

*Information current as of May 2026.*
