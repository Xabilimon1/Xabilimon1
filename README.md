<div align="center">
  <img src="assets/banner.svg" alt="Xabilimon" width="100%"/>
</div>

---

I'm **Xabi**, 2nd-year AI Systems Engineering at [UFV](https://www.ufv.es) (Madrid). I've spent the last year and a half shipping production agent systems — Salesforce-integrated commercial agents, MCP servers with security review iterations, field-ops trainers on Android, multi-language institutional tools. **Now pivoting toward research output** as the prerequisite for the work I actually want to do.

---

### Now (June 2026)

- **Writing** — empirical ablation study of LLM agent harness components ([harness-ablation](https://github.com/Xabilimon1/harness-ablation))
- **Studying** — [ARENA](https://www.arena.education/) curriculum, chapter 0 fundamentals ([solutions repo](https://github.com/Xabilimon1/xabier-arena-solutions))
- **Contributing** — merged fixes to the [METR/hawk](https://github.com/METR/hawk/pull/627) and [HAL](https://github.com/princeton-pli/hal-harness/pull/182) eval harnesses
- **Reading** — Anthropic engineering posts on eval methodology + infrastructure noise
- **Blog** — in setup; first posts on the journey + paper reading notes

---

### Research

<table>
<tr>
<td width="50%" valign="top">

#### [harness-ablation](https://github.com/Xabilimon1/harness-ablation)

Empirical ablation study of LLM agent harness components — prompt structure, tool selection logic, retry policy, context management, error handling.

Extends Anthropic's *Quantifying infrastructure noise in agentic coding evals* outward: if infra config dominates eval variance, what does the rest of the harness do? Synthetic controlled experiment informed by production deployment experience.

`Python` `Inspect-AI` `Claude` `Gemini` `GPT`

*Status: paper in progress*

</td>
<td width="50%" valign="top">

#### [xabier-arena-solutions](https://github.com/Xabilimon1/xabier-arena-solutions)

Public journey through ARENA — Alignment Research Engineer Accelerator curriculum — plus the original mech interp experiments I run alongside each chapter.

Builder background, weak research foundations, trying to close the gap before applying to alignment/interp work.

`PyTorch` `Transformers` `Mechanistic Interpretability`

*Status: chapter 0 in progress*

</td>
</tr>
</table>

**Merged contributions** — fixes to the eval infrastructure behind frontier-model safety research.

- **[METR/hawk #627](https://github.com/METR/hawk/pull/627)** — [METR](https://github.com/METR) (Model Evaluation & Threat Research). Auth fix in `hawk`, their cloud Inspect-AI eval runner: a passthrough credential header containing only whitespace is now treated as missing (`401` + `anonymous`) instead of surfacing an unactionable `"invalid api key"`. *Merged.*
- **[princeton-pli/hal-harness #182](https://github.com/princeton-pli/hal-harness/pull/182)** — [HAL](https://github.com/princeton-pli), the Holistic Agent Leaderboard (Princeton PLI). Resolved a `wandb`/`weave`/`gql` version conflict that broke every agent-env container at startup; aligned the three runners, the Docker image, packaging, and contributor docs. *Merged.*
- **[affaan-m/ECC #920](https://github.com/affaan-m/ECC/pull/920)** — [everything-claude-code](https://github.com/affaan-m/ECC). Contributed the Token Budget Advisor skill. *Merged.*

---

### Production

<table>
<tr>
<td width="50%" valign="top">

#### [LinceReservations](https://github.com/Xabilimon1/LinceReservations)

Full-stack room booking system deployed at [UFV](https://www.ufv.es)'s DOT space. 12 rooms, 4 user roles (student, professor, PAS, admin), real-time sync via Supabase Realtime, Outlook Calendar integration via Microsoft Graph, institutional email via Office 365, admin dashboard with audit logs, blacklist system, XLSX report exports, and 5-language i18n.

`React 19` `TypeScript` `Supabase` `Azure AD` `Vercel` `Tailwind CSS`

[🌐 reservas-salas-dot.vercel.app](https://reservas-salas-dot.vercel.app)

</td>
<td width="50%" valign="top">

#### [Token Budget Advisor](https://github.com/Xabilimon1/TBA-Token-Budget-Advisor-Claude-Code)

Claude Code skill that intercepts your prompt, estimates token consumption with a zero-dependency heuristic engine (measured ~87.6% accuracy vs `tiktoken` cl100k_base), and lets you choose how deep Claude's answer should be before it responds.

Contributed to [**everything-claude-code**](https://github.com/affaan-m/ECC) (ECC) by affaan-m — the agent harness with 220k+ stars used across the Claude Code ecosystem.

`Python 3.8+` `Claude Code` `zero dependencies`

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### [save-session](https://github.com/Xabilimon1/save-session)

Claude Code skill that saves compressed session summaries to an Obsidian vault, automatically maintaining bidirectional links between project notes, session logs, and technology nodes.

`Claude Code skill` `Obsidian` `Markdown`

</td>
<td width="50%" valign="top">

#### Lince Suite

Portfolio of internal web tools for UFV's DOT space — operational management interfaces built as lightweight applications deployed on Vercel.

`HTML` `CSS` `JavaScript` `Vercel`

</td>
</tr>
</table>

---

### Stack

<div align="center">

**Languages**

![TypeScript](https://img.shields.io/badge/TypeScript-0d1117?style=for-the-badge&logo=typescript&logoColor=f97316)
![JavaScript](https://img.shields.io/badge/JavaScript-0d1117?style=for-the-badge&logo=javascript&logoColor=f97316)
![Python](https://img.shields.io/badge/Python-0d1117?style=for-the-badge&logo=python&logoColor=f97316)
![HTML5](https://img.shields.io/badge/HTML5-0d1117?style=for-the-badge&logo=html5&logoColor=f97316)
![CSS3](https://img.shields.io/badge/CSS3-0d1117?style=for-the-badge&logo=css3&logoColor=f97316)

**Frameworks & Tooling**

![React](https://img.shields.io/badge/React-0d1117?style=for-the-badge&logo=react&logoColor=f97316)
![Vite](https://img.shields.io/badge/Vite-0d1117?style=for-the-badge&logo=vite&logoColor=f97316)
![Node.js](https://img.shields.io/badge/Node.js-0d1117?style=for-the-badge&logo=nodedotjs&logoColor=f97316)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-0d1117?style=for-the-badge&logo=tailwindcss&logoColor=f97316)
![PyTorch](https://img.shields.io/badge/PyTorch-0d1117?style=for-the-badge&logo=pytorch&logoColor=f97316)

**Platform & Data**

![Supabase](https://img.shields.io/badge/Supabase-0d1117?style=for-the-badge&logo=supabase&logoColor=f97316)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-0d1117?style=for-the-badge&logo=postgresql&logoColor=f97316)
![Google Cloud](https://img.shields.io/badge/Google_Cloud-0d1117?style=for-the-badge&logo=googlecloud&logoColor=f97316)
![Vercel](https://img.shields.io/badge/Vercel-0d1117?style=for-the-badge&logo=vercel&logoColor=f97316)
![Git](https://img.shields.io/badge/Git-0d1117?style=for-the-badge&logo=git&logoColor=f97316)

**AI & Agents**

![Anthropic](https://img.shields.io/badge/Claude-0d1117?style=for-the-badge&logo=anthropic&logoColor=f97316)
![Vertex AI](https://img.shields.io/badge/Vertex_AI-0d1117?style=for-the-badge&logo=googlecloud&logoColor=f97316)
![MCP](https://img.shields.io/badge/MCP-0d1117?style=for-the-badge&logo=anthropic&logoColor=f97316)
![Inspect AI](https://img.shields.io/badge/Inspect_AI-0d1117?style=for-the-badge&logo=anthropic&logoColor=f97316)

</div>

---

### Signal

<div align="center">

**Merged into the eval infrastructure behind frontier-model safety research**

[![METR · hawk #627](https://img.shields.io/badge/METR%20%C2%B7%20hawk%20%23627-merged-f97316?style=for-the-badge&logo=github&logoColor=white&labelColor=0d1117)](https://github.com/METR/hawk/pull/627)
[![Princeton HAL · hal-harness #182](https://img.shields.io/badge/Princeton%20HAL%20%23182-merged-f97316?style=for-the-badge&logo=github&logoColor=white&labelColor=0d1117)](https://github.com/princeton-pli/hal-harness/pull/182)
[![everything-claude-code #920](https://img.shields.io/badge/everything--claude--code%20%23920-merged-f97316?style=for-the-badge&logo=github&logoColor=white&labelColor=0d1117)](https://github.com/affaan-m/ECC/pull/920)

<br/>

[![ECC stars](https://img.shields.io/github/stars/affaan-m/ECC?style=flat-square&logo=github&label=ECC+contributor&color=f97316&labelColor=0d1117)](https://github.com/affaan-m/ECC)
[![Inspect AI](https://img.shields.io/badge/eval%20stack-Inspect--AI-f97316?style=flat-square&logo=anthropic&logoColor=white&labelColor=0d1117)](https://inspect.aisi.org.uk/)
[![Views](https://komarev.com/ghpvc/?username=Xabilimon1&style=flat-square&color=f97316&label=profile+views&abbreviated=true)](https://github.com/Xabilimon1)

<br/>

**Focus** — agent evals · Inspect-AI · mechanistic interpretability  
**Working in** — Python · TypeScript · PyTorch

</div>

---

<div align="center">
  <a href="https://github.com/Xabilimon1">
    <img src="https://img.shields.io/badge/GitHub-Xabilimon1-f97316?style=for-the-badge&logo=github&logoColor=white"/>
  </a>
</div>
