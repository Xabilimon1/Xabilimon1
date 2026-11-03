# Xabier Ariznabarreta

<p align="center">
  <img width="300" alt="Xabier Ariznabarreta" src="assets/xabier-2010.jpg" />
</p>

<p align="center"><sub><em>
AI Engineering student in Madrid, turning from shipping production systems toward research.<br />
Over the last year and a half I've built production systems: LLM agents over Salesforce taking real traffic, institutional department tooling in real use, a university booking platform built to spec and pending rollout, and a local-first desktop stats app. On my own, I took apart an undocumented binary format and wrote a decompiler for it.<br />
The bugs were the teacher. The bottleneck isn't the engineering, it's the science underneath.<br />
So I'm working my way in from the applied side, with merged fixes to the eval infrastructure behind frontier-model safety and the lessons written down in public.<br />
Builder in the concrete, learner in the deep.
</em></sub></p>

<p align="center"><b><a href="https://xabier.me">xabier.me →</a></b></p>

---

## Merged contributions

Small fixes, real repos — the eval infrastructure behind frontier-model safety research, and the tools around my own work.

- **[METR/hawk #627](https://github.com/METR/hawk/pull/627)** — [METR](https://github.com/METR) (Model Evaluation & Threat Research). Auth fix in `hawk`, their cloud Inspect-AI eval runner: a passthrough credential header containing only whitespace is now treated as missing (`401` + `anonymous`) instead of surfacing an unactionable `"invalid api key"`. *Merged.*
- **[princeton-pli/hal-harness #182](https://github.com/princeton-pli/hal-harness/pull/182)** — [HAL](https://github.com/princeton-pli), the Holistic Agent Leaderboard (Princeton PLI). Resolved a `wandb`/`weave`/`gql` version conflict that broke every agent-env container at startup; aligned the three runners, the Docker image, packaging, and contributor docs. *Merged.*
- **[boykopovar/AnyPS5 #4555](https://github.com/boykopovar/AnyPS5/pull/4555)** — [AnyPS5](https://github.com/boykopovar/AnyPS5) (50k stars), a relinker that ports PS5 executables to Linux and Windows. Made `libkernel` build on macOS: `O_DIRECT` is now guarded (the macOS SDK doesn't define it) and the `getrlimit` test gets its missing header. Built and tested on an M3. *Merged.*
- **[affaan-m/ECC #920](https://github.com/affaan-m/ECC/pull/920)** — [everything-claude-code](https://github.com/affaan-m/ECC), the most-starred agent toolkit on GitHub. Contributed the Token Budget Advisor skill. *Merged.*
- **[karanb192/awesome-claude-code-mods #254](https://github.com/karanb192/awesome-claude-code-mods/pull/254)** — [awesome-claude-code-mods](https://github.com/karanb192/awesome-claude-code-mods), a catalogue of 6,000+ Claude Code mods. Added the five [EMCC](https://github.com/Xabilimon1/emcc-claude-code-mods) mods to its scanner seeds, after fixing what its scanner and the maintainer's review flagged. *Merged.*

---

## Production work

Real systems built for clients and institutions, some live and taking traffic, some built to spec and pending rollout. Code is private; the writeups on SAM and LinceReservations are on [xabier.me](https://xabier.me).

<table>
  <tr>
    <td width="50%" valign="top">
      <b>SAM — production LLM agent</b><br />
      <sub>Commercial + field-ops orchestrator built for a Spanish firm that maintains the exteriors of 2,500+ buildings. A declarative profile-pipeline over Salesforce + Vertex AI / Gemini — adding a new agent is one declarative entry, no core changes. Serves Salesforce Apex (sync) and an Android app (SSE streaming). FastAPI · Cloud Run.</sub><br />
      <img src="https://img.shields.io/static/v1?style=for-the-badge&label=focus&message=llm%20agents%20%7C%20fastapi%20%7C%20vertex%20ai&labelColor=4338ca&color=0f172a" alt="focus llm agents" />
    </td>
    <td width="50%" valign="top">
      <b>LinceReservations</b><br />
      <sub>A study-room booking platform I built for a private university in Madrid, designed to their institutional requirements and pending adoption (not yet deployed). Five languages, institutional SSO (Azure AD / MSAL), row-level security, calendar sync. React 19 · TypeScript · Supabase.</sub><br />
      <img src="https://img.shields.io/static/v1?style=for-the-badge&label=focus&message=full-stack%20%7C%20react%20%7C%20supabase&labelColor=4338ca&color=0f172a" alt="focus full-stack" />
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <b>Numo</b><br />
      <sub>A local-first desktop statistics app, in development — a real stats engine (pandas / scipy / statsmodels) bundled with the app, so your data never leaves your machine. Tauri v2.</sub><br />
      <img src="https://img.shields.io/static/v1?style=for-the-badge&label=focus&message=desktop%20%7C%20tauri%20%7C%20local-first&labelColor=4338ca&color=0f172a" alt="focus desktop" />
    </td>
    <td width="50%" valign="top">
      <b>Institutional tooling</b><br />
      <sub>Evaluation and automation tools built for a university department — project-review interfaces used by ~30–40 professors a year, room-booking automation, an annual reporting pipeline. Production institutional software, not proofs of concept.</sub><br />
      <img src="https://img.shields.io/static/v1?style=for-the-badge&label=focus&message=production%20%7C%20institutional&labelColor=4338ca&color=0f172a" alt="focus institutional" />
    </td>
  </tr>
</table>

---

## Open Source

<table>
  <tr>
    <td width="50%" valign="top">
      <a href="https://github.com/Xabilimon1/hubble-cosmos"><b>Hubble</b></a><br />
      <sub>Decompiler for MultiBase Cosmos: compiled <code>.omd</code> modules back to COOL source that recompiles to the same bytes. The format had no public documentation; it was worked out from the binaries, with an ImHex pattern to read it field by field.</sub><br />
      <img src="https://img.shields.io/static/v1?style=for-the-badge&label=focus&message=reverse%20engineering%20%7C%20python&labelColor=4338ca&color=0f172a" alt="focus reverse engineering python" /><br />
      <img src="https://img.shields.io/github/stars/Xabilimon1/hubble-cosmos?style=flat-square&label=stars&color=f59e0b" alt="Hubble stars" />
      <img src="https://img.shields.io/github/forks/Xabilimon1/hubble-cosmos?style=flat-square&label=forks&color=818cf8" alt="Hubble forks" />
    </td>
    <td width="50%" valign="top">
      <a href="https://github.com/Xabilimon1/emcc-claude-code-mods"><b>EMCC</b></a><br />
      <sub>Five tested Claude Code mods (453 tests): a live panel of what Claude is doing, a context bar, and a guard against moved goalposts. Listed in <a href="https://github.com/karanb192/awesome-claude-code-mods">awesome-claude-code-mods</a></sub><br />
      <img src="https://img.shields.io/static/v1?style=for-the-badge&label=focus&message=claude%20code%20%7C%20mods&labelColor=4338ca&color=0f172a" alt="focus claude code mods" /><br />
      <img src="https://img.shields.io/github/stars/Xabilimon1/emcc-claude-code-mods?style=flat-square&label=stars&color=f59e0b" alt="EMCC stars" />
      <img src="https://img.shields.io/github/forks/Xabilimon1/emcc-claude-code-mods?style=flat-square&label=forks&color=818cf8" alt="EMCC forks" />
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <a href="https://github.com/Xabilimon1/TBA-Token-Budget-Advisor-Claude-Code"><b>TBA — Token Budget Advisor</b></a><br />
      <sub>Depth/cost choice before Claude answers · merged into <a href="https://github.com/affaan-m/ECC/pull/920">ECC</a></sub><br />
      <img src="https://img.shields.io/static/v1?style=for-the-badge&label=focus&message=claude%20code%20%7C%20token%20budget&labelColor=4338ca&color=0f172a" alt="focus claude code token budget" /><br />
      <img src="https://img.shields.io/github/stars/Xabilimon1/TBA-Token-Budget-Advisor-Claude-Code?style=flat-square&label=stars&color=f59e0b" alt="TBA stars" />
      <img src="https://img.shields.io/github/forks/Xabilimon1/TBA-Token-Budget-Advisor-Claude-Code?style=flat-square&label=forks&color=818cf8" alt="TBA forks" />
    </td>
    <td width="50%" valign="top">
      <a href="https://github.com/Xabilimon1/save-session"><b>save-session</b></a><br />
      <sub>Claude Code skill — compressed session summaries to a vault</sub><br />
      <img src="https://img.shields.io/static/v1?style=for-the-badge&label=focus&message=claude%20code%20%7C%20skill&labelColor=4338ca&color=0f172a" alt="focus claude code skill" /><br />
      <img src="https://img.shields.io/github/stars/Xabilimon1/save-session?style=flat-square&label=stars&color=f59e0b" alt="save-session stars" />
      <img src="https://img.shields.io/github/forks/Xabilimon1/save-session?style=flat-square&label=forks&color=818cf8" alt="save-session forks" />
    </td>
  </tr>
</table>

<sub>Also: <a href="https://github.com/Xabilimon1/xabier-blog">xabier-blog</a> (this research notebook, Astro, <a href="https://xabier.me">xabier.me</a>) and <a href="https://github.com/Xabilimon1/reeljet">reeljet</a> (a short-form video ad generator, as a Claude Code skill). Early / idea-stage: <a href="https://github.com/Xabilimon1/harness-ablation">harness-ablation</a> (an agent-harness ablation study I sketched out) and <a href="https://github.com/Xabilimon1/xabier-arena-solutions">xabier-arena-solutions</a> (placeholder for the ARENA curriculum, starting soon).</sub>

---

## Currently

- **Writing up** the lessons as case studies on [xabier.me](https://xabier.me): SAM's agent architecture and the LinceReservations build are up, Hubble's teardown is next.
- **Contributing** to eval-framework open source — more PRs in the pipeline after the five above.
- **Next** — the [ARENA](https://www.arena.education/) alignment curriculum, to build the research foundations under the applied experience.

---

## Highlights

| Highlight | Detail |
|---|---|
| **Merged contributions** | 5 PRs into [METR/hawk](https://github.com/METR/hawk/pull/627), [Princeton HAL](https://github.com/princeton-pli/hal-harness/pull/182), [AnyPS5](https://github.com/boykopovar/AnyPS5/pull/4555), [ECC](https://github.com/affaan-m/ECC/pull/920), and [awesome-claude-code-mods](https://github.com/karanb192/awesome-claude-code-mods/pull/254) — the eval stack behind frontier-model safety research, and the tools around it |
| **Production work** | LLM agents over Salesforce taking real traffic, department tooling for ~30–40 professors in real use, a university booking platform built to spec (pending adoption), a local-first desktop stats app |
| **Open source** | [Hubble](https://github.com/Xabilimon1/hubble-cosmos) (a decompiler for an undocumented format), [EMCC](https://github.com/Xabilimon1/emcc-claude-code-mods) (five Claude Code mods), [TBA](https://github.com/Xabilimon1/TBA-Token-Budget-Advisor-Claude-Code) (merged into ECC), [save-session](https://github.com/Xabilimon1/save-session), and [this blog](https://xabier.me) |
| **Writing in public** | [xabier.me](https://xabier.me) — a research notebook, bilingual (ES/EN) |
| **Studying** | 3rd-year AI Systems Engineering at [UFV](https://www.ufv.es), Madrid |

---

<div align="center">

**Focus** — agent evals · Inspect-AI · production LLM systems &nbsp;·&nbsp; **Stack** — Python · TypeScript · FastAPI · React · Astro

</div>

---

<p align="center">
  <a href="https://github.com/Xabilimon1?tab=repositories"><img src="https://img.shields.io/badge/repositories-9+-4338ca?style=flat-square&labelColor=0f172a" alt="repositories" /></a>
  <a href="https://xabier.me"><img src="https://img.shields.io/badge/blog-xabier.me-4338ca?style=flat-square&labelColor=0f172a" alt="blog" /></a>
  <img src="https://komarev.com/ghpvc/?username=Xabilimon1&style=flat-square&color=4338ca&labelColor=0f172a&label=profile+views&abbreviated=true" alt="profile views" />
</p>

---

<p align="center">
  <a href="https://xabier.me">Blog</a> ·
  <a href="https://github.com/Xabilimon1">GitHub</a> ·
  <a href="mailto:xabier.ariznabarreta@gmail.com">Email</a> ·
  <a href="https://xabier.me/rss.xml">RSS</a>
</p>
