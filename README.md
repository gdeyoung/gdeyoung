# Greg DeYoung

Building AI agent fleets on self-hosted hardware since before it was cool.

## The project: an AI agent fleet that runs itself

My public repos are the visible edge of a homelab AI fleet — multiple servers, dozens of agent profiles, local LLM serving, and memory systems that learn while I sleep. The philosophy: own your inference, measure everything, automate the maintenance, and publish what it teaches you.

The fleet's daily-driver machines run Omarchy (Arch + Hyprland), and when the desktop is missing something, I build the plugin and publish it. The KDE/Bazzite machines get the same treatment.

## Where to start

| Repo | What it is |
|---|---|
| **[praxis](https://github.com/gdeyoung/praxis)** | ⭐ The hub — hard-won lessons from running the fleet: serving recipes with verification gates, agent memory architecture, benchmark methodology, curated links |
| **[mnemograph](https://github.com/gdeyoung/mnemograph)** | The in-process knowledge graph for AI agents — no external databases, no network calls, zero infrastructure |
| **[Clearvoice](https://github.com/gdeyoung/Clearvoice)** | Privacy-first meeting assistant for Linux — record, transcribe, diarize, and summarize meetings with local AI; the audio never leaves the machine |
| **[focus](https://github.com/gdeyoung/focus)** | Self-hosted web launchpad — Flask + vanilla JS, the start page every browser in the fleet calls home. Inspired by Bonjourr. |

## The Omarchy suite

Sixteen repos for running heavily customized Omarchy (Arch + Hyprland) machines — two runbooks and fourteen open plugins, every one born from daily use:

| Repo | What it does |
|---|---|
| **[omarchy-recipes](https://github.com/gdeyoung/omarchy-recipes)** | How to run a heavily customized Omarchy machine as code — recipe-repo discipline, measured update-overwrite model, plugin hygiene. Sibling of praxis. |
| **[omarchy-skills](https://github.com/gdeyoung/omarchy-skills)** | Agent skills for Omarchy: triage + reporting, plugin development, shell-plugin debugging |
| **[omarchy-appdock](https://github.com/gdeyoung/omarchy-appdock)** | KDE-style task manager and minimize engine — dock widget, per-workspace window icons, hyprbars titlebar buttons |
| **[omarchy-sysmon](https://github.com/gdeyoung/omarchy-sysmon)** | Live RAM, CPU, network rate, and whole-disk stats in the bar — four groups, one widget |
| **[omarchy-tailfin](https://github.com/gdeyoung/omarchy-tailfin)** | Tailscale status in the bar — device list, connection state, subnet routes, self-IPs, themed panel |
| **[omarchy-powercore](https://github.com/gdeyoung/omarchy-powercore)** | Battery and power strategy — per-source profiles, charge protection, clamshell inhibitor, keyboard backlight, live watts |
| **[omarchy-displayplus](https://github.com/gdeyoung/omarchy-displayplus)** | One panel for every display setting — brightness, text size, universal scale up front, full layout editor underneath |
| **[omarchy-audiofx](https://github.com/gdeyoung/omarchy-audiofx)** | Audio panel with system-wide effects (3D/bass/night/movie), per-app routing and pins, device disabling |
| **[omarchy-driveway](https://github.com/gdeyoung/omarchy-driveway)** | Every drive one click from the bar — USB/disks, SMB/NFS/sshfs shares, rclone cloud mounts |
| **[omarchy-foyer](https://github.com/gdeyoung/omarchy-foyer)** | The front door — full menu tree on open, live all-source search, one-row AI answers, custom handoffs, timers |
| **[omarchy-ready-room](https://github.com/gdeyoung/omarchy-ready-room)** | The gaming panel — game-mode session toggles, controller battery and test, instant replay recorder, MangoHud-linked FPS overlay |
| **[omarchy-timepiece](https://github.com/gdeyoung/omarchy-timepiece)** | The bar clock, rebuilt — date in the label, color-coded world clocks, countdown timer, self-running pomodoro |
| **[omarchy-timemachine](https://github.com/gdeyoung/omarchy-timemachine)** | Unencrypted rsync time machine — status chip, five-tab popup (Status/Snapshots/Health/Recovery/Settings), bundled engine |
| **[omarchy-weather](https://github.com/gdeyoung/omarchy-weather)** | WeatherX — tabbed panel, pinned places, live keyless radar (Esri + RainViewer), Open-Meteo. No API keys. |
| **[omarchy-armoury](https://github.com/gdeyoung/omarchy-armoury)** | ASUS laptop control for the bar — temps, fan, battery care mode, firmware attributes (asus-armoury kernel module) |
| **[omarchy-ultrawide-bar](https://github.com/gdeyoung/omarchy-ultrawide-bar)** | The stock bar, rebuilt — opt-in partial width for ultrawide monitors, fullscreen auto-hide, window-mode helper |

## Desktop & system tools

| Repo | What it does |
|---|---|
| **[bazzite-customizations](https://github.com/gdeyoung/bazzite-customizations)** | KDE Plasma customizations, tweaks, and plugins for Bazzite (immutable Fedora) — sudo-free, reversible, verified with measured numbers |
| **[audiofx-engine](https://github.com/gdeyoung/audiofx-engine)** | System-wide audio effects for PipeWire — 3D binaural, bass, night, movie modes as a filter-chain virtual sink. The engine behind omarchy-audiofx. |
| **[ghosttype](https://github.com/gdeyoung/ghosttype)** | Offline voice typing for Windows — press a hotkey, speak, words land in whatever app has focus. Local Whisper, no API key, no account. |
| **[galaxybook5-pro-platform](https://github.com/gdeyoung/galaxybook5-pro-platform)** | Out-of-tree DKMS driver that makes the internal speakers work on a Samsung Galaxy Book5 Pro (Lunar Lake) under Linux/Bazzite |

## Local AI serving & media

| Repo | What it does |
|---|---|
| **[qfn-abl-exl3](https://github.com/gdeyoung/qfn-abl-exl3)** | Abliterated Qwen3.8-Flash-Next at the stock 3.05bpw EXL3 allocation — integer-pinned recipe for DGX Spark (GB10). 65 tok/s, MTP2, 226k ctx verified. |
| **[Qwen3.8-Flash-Next-NVFP4-DGX-Spark](https://github.com/gdeyoung/Qwen3.8-Flash-Next-NVFP4-DGX-Spark)** | vLLM serving of Qwen3.8-Flash-Next (NVFP4) on DGX Spark with our disk-backed n-gram table patch, staged gather, and reduced-vocab MTP draft — 43.9 tok/s on one Spark, 53.7 TP2, 9M-token KV pool at TP4. Launchers, patch, 40-prompt harness. |
| **[localgen](https://github.com/gdeyoung/localgen)** | Local media generation — images and video (OpenVINO GenAI), neural upscale + frame interpolation (ncnn/Vulkan), cloned-voice TTS, transcription. Device-adaptive. |

## How the pieces fit

- **praxis** — the operating education: what deploying all of this taught us
- **omarchy-recipes / bazzite-customizations** — the desktops, run as code
- **The Omarchy suite** — fourteen plugins that make those desktops complete
- **mnemograph** — knowledge-graph memory as an embeddable library
- **Clearvoice** — meetings in, structured notes out, without the audio leaving the machine
- **DGX Spark repos** — local LLM serving recipes with measured numbers and harnesses
- **localgen / audiofx-engine / ghosttype** — the media, audio, and voice utilities the fleet uses daily
- Everything else (startpages, tooling, forks I track) keeps the fleet running

## Forks I track

Upstream projects the fleet runs or watches — theirs, not mine to reorganize:

- **[hermes-agent](https://github.com/gdeyoung/hermes-agent)** — the agent framework the whole fleet runs on
- **[flea](https://github.com/gdeyoung/flea)** — fast, keyboard-first file manager for Omarchy
- **[BonjourrNue](https://github.com/gdeyoung/BonjourrNue)** / **[portal](https://github.com/gdeyoung/portal)** — the startpages that inspired focus
- **[agent-zero](https://github.com/gdeyoung/agent-zero)** / **[a0-plugins](https://github.com/gdeyoung/a0-plugins)** — agent framework and plugin index
- **[awesome](https://github.com/gdeyoung/awesome)** / **[ai-agents-for-beginners](https://github.com/gdeyoung/ai-agents-for-beginners)** / **[bolt_prompts](https://github.com/gdeyoung/bolt_prompts)** — reference shelves

## Elsewhere

- [build.nvidia.com](https://build.nvidia.com) — where the DGX Spark practitioner community trades notes (find my verification posts there)
