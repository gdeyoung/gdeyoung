# Greg DeYoung

Building AI agent fleets on self-hosted hardware since before it was cool.

## The project: an AI agent fleet that runs itself

My public repos are the visible edge of a homelab AI fleet — multiple servers, dozens of agent profiles, local LLM serving, and memory systems that learn while I sleep. The philosophy: own your inference, measure everything, automate the maintenance, and publish what it teaches you.

The fleet's daily-driver machines run Omarchy (Arch + Hyprland), and when the desktop is missing something, I build the plugin and publish it.

## Where to start

| Repo | What it is |
|---|---|
| **[praxis](https://github.com/gdeyoung/praxis)** | ⭐ The hub — hard-won lessons from running the fleet: serving recipes with verification gates, agent memory architecture, benchmark methodology, curated links |
| **[mnemograph](https://github.com/gdeyoung/mnemograph)** | The in-process knowledge graph for AI agents — no external databases, no network calls, zero infrastructure |
| **[focus](https://github.com/gdeyoung/focus)** | Self-hosted web launchpad — Flask + vanilla JS, the start page every browser in the fleet calls home. Inspired by Bonjourr. |
| **[Clearvoice](https://github.com/gdeyoung/Clearvoice)** | Privacy-first meeting assistant for Linux — record, transcribe, diarize, and summarize meetings with local AI. The fleet's meeting-intelligence frontend. |

## Omarchy desktop plugins

Four open plugins that grew out of running Omarchy on the fleet's laptops:

| Repo | What it does |
|---|---|
| **[omarchy-appdock](https://github.com/gdeyoung/omarchy-appdock)** | KDE-style task manager and minimize engine for Omarchy (Hyprland 0.56) — dock widget, per-workspace window icons, hyprbars titlebar buttons |
| **[omarchy-tailfin](https://github.com/gdeyoung/omarchy-tailfin)** | The stock Tailscale bar widget rebuilt as a tabbed panel — health warnings, preference toggles, exit-node and Mullvad tabs, searchable peer list |
| **[omarchy-sysmon](https://github.com/gdeyoung/omarchy-sysmon)** | Live RAM, CPU, network rate, and whole-disk stats in the Omarchy bar — four groups, one widget |
| **[omarchy-displayplus](https://github.com/gdeyoung/omarchy-displayplus)** | One panel for every display setting — brightness, text size, and universal scale on the front page, full hyprmoncfg layout editor underneath |

## How the pieces fit

- **praxis** — the operating education: what deploying all of this taught us
- **mnemograph** — knowledge-graph memory as an embeddable library
- **Clearvoice** — meetings in, structured notes out, without the audio leaving the machine
- **Omarchy plugins** — the desktop layer the agents and I both work from
- Everything else (startpages, tooling, forks I track) keeps the fleet running

## Forks with real work in them

- **[Qwen3.8-Flash-Next-NVFP4-DGX-Spark](https://github.com/gdeyoung/Qwen3.8-Flash-Next-NVFP4-DGX-Spark)** — vLLM serving of Qwen3.8-Flash-Next (NVFP4) on DGX Spark: disk-backed n-gram table patch, staged gather, reduced-vocab MTP draft. 43.9 tok/s on one Spark, 53.7 tok/s TP2, 9M-token KV pool at TP4. Launchers, patch, and a 40-prompt harness included.
- **[hermes-agent](https://github.com/gdeyoung/hermes-agent)** — the agent framework the whole fleet runs on
- **[BonjourrNue](https://github.com/gdeyoung/BonjourrNue)** — minimalist startpage (upstream fork I track)

## Elsewhere

- [build.nvidia.com](https://build.nvidia.com) — where the DGX Spark practitioner community trades notes (find my verification posts there)
