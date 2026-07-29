<div align="center">

<img src="./banner.svg" alt="Mayur Vijayvargiya - QA & Delivery Lead" width="100%" />

### QA &amp; Delivery Lead &nbsp;·&nbsp; AI-Agent QA Skills &nbsp;·&nbsp; Playwright / pytest &nbsp;·&nbsp; Scrum

<em>I lead QA &amp; delivery for product teams and build AI-agent "skills" that do real testing work — generating senior-reviewed test cases and driving suites to an honest green. 9+ years across product &amp; enterprise: banking, insurance, media, and industrial AI.</em>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mayur-vijayvargiya-5907a5b9)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mayur.vijay.99@gmail.com)
![Location](https://img.shields.io/badge/Indore%2C%20India-4B5563?style=for-the-badge&logo=googlemaps&logoColor=white)
![Remote](https://img.shields.io/badge/Open%20to%20100%25%20Remote-2EA44F?style=for-the-badge)

</div>

---

## 🚀 AI-agent QA system — skills I built

I designed a **complete, agent-driven QA pipeline**: one command takes a software feature from *nothing* to a **merged, CI-verified feature** — it writes senior-QA-reviewed test cases, drives a real ≥95%-green suite, runs code review, opens the PR, and handles the post-merge CI cleanup — pausing only at the two points where a human must decide.

### ⭐ The flagship — Full-Flow Orchestrator

An **orchestrator**, not another engine: each phase either does lightweight "glue" work (ticket, live-UI read, PR) or **calls one of the specialized skills below**. Every phase reads/writes a **durable run manifest**, so a crash, a long CI wait, or a brand-new session all resume exactly where the run left off. **Two human stops only** — approve the cases, and merge.

```mermaid
flowchart TD
    A["0 · Context & preflight"] --> B["1 · Ticket + isolated branch"]
    B --> C["2 · Read the live feature<br/><i>observe real DOM/API — never guess</i>"]
    C --> D["3 · Generate + senior-QA review<br/><i>reviewed cases → report</i>"]
    D --> S1{{"✋ 4 · STOP 1 — Human approves the cases<br/>Slack posts &amp; waits — no auto-advance"}}
    S1 -- edits --> D
    S1 -- approved --> E["5 · Push to test management"]
    E --> F["6 · Drive suite to ≥95% green<br/><i>honest run, evidence-triaged</i>"]
    F --> G["7 · Independent code review"]
    G --> H["8 · Known-issue repro doc"]
    H --> I["9 · Open PR + link the ticket"]
    I --> S2{{"✋ STOP 2 — Human merges<br/>the agent never merges itself"}}
    S2 --> J["10 · Post-merge CI loop<br/><i>trigger CI · pull only failing traces · fix</i>"]
    J -- "on red: fix & re-PR (≤3×)" --> I
    J -- green --> DONE(["✅ Merged & CI-verified"])

    classDef glue fill:#E8F0FE,stroke:#1A73E8,color:#174EA6;
    classDef engine fill:#F3E8FD,stroke:#7C3AED,color:#5B21B6;
    classDef stop fill:#FEF3C7,stroke:#D97706,color:#92400E;
    classDef done fill:#DCFCE7,stroke:#16A34A,color:#166534;
    class A,B,C,G,H,I glue;
    class D,E,F,J engine;
    class S1,S2 stop;
    class DONE done;
```

- **Two human stops, and they're the right two** — everything else, including post-merge CI cleanup, runs unattended.
- **Resumable & crash-safe** — the run manifest survives crashes, long CI waits, and session restarts.
- **It never merges itself** — a deliberate, non-negotiable boundary.

### The building blocks

Each stands on its own; the orchestrator conducts them.

| Skill | What it does | Impact |
|-------|--------------|--------|
| [**QA Test Case Generator**](https://github.com/mvijayvargiya/qa-testcase-generator-skill) | Generates **and senior-QA-reviews** cases → Zephyr Scale | 30–80 reviewed cases / feature |
| [**Test Suite → Green**](https://github.com/mvijayvargiya/test-suite-to-green-skill) | Drives cases to an **honest ≥95%-green** pytest + Playwright suite | suite build ≈ 2 weeks → ≈ 1 day |
| **Jenkins CI Runner** | Triggers CI headlessly; on red, pulls back **only failing traces** — not the bulk archive | fast, evidence-first triage |
| **Slack Notifier** | The human-in-the-loop backbone: **blocking** approval gates vs. **non-blocking** FYIs | keeps a human in control, never blocks the run |

> **Honesty gate:** the green number comes from a real run — skips can't hide failures, every verdict cites evidence (trace / DOM / API), and nothing merges without a human.

### How the pieces fit together

```mermaid
flowchart LR
    O["⭐ Full-Flow Orchestrator"] --> G["Test Case Generator"]
    O --> S["Suite → Green"]
    O --> J["Jenkins CI Runner"]
    O --> N["💬 Slack Notifier"]
    J --> N
    G -. reviewed cases .-> S
    S -. merged feature .-> J
    N -. "gates & FYIs" .-> R(["👤 Reviewer"])

    classDef o fill:#FEF3C7,stroke:#D97706,color:#92400E;
    classDef c fill:#E8F0FE,stroke:#1A73E8,color:#174EA6;
    classDef n fill:#F0FDF4,stroke:#16A34A,color:#166534;
    class O o; class G,S,J c; class N,R n;
```

---

## 🛠️ Delivery & process — how I run QA + delivery

- [**Agile Delivery Playbook**](https://github.com/mvijayvargiya/agile-delivery-playbook) — POD-based delivery + a monthly release train
- [**Jira POD Delivery**](https://github.com/mvijayvargiya/jira-pod-delivery) — Components-as-POD, boards, release versions, dashboards
- [**QA Test Plan &amp; Framework**](https://github.com/mvijayvargiya/qa-test-plan-templates) — manual QA plan + Playwright/pytest framework
- [**QA Onboarding Guide**](https://github.com/mvijayvargiya/qa-onboarding-guide) — ramp new QA hires fast

## 🧰 Tech &amp; tools

![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge&logo=playwright&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)

![Jira](https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=jira&logoColor=white)
![Confluence](https://img.shields.io/badge/Confluence-172B4D?style=for-the-badge&logo=confluence&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Scrum](https://img.shields.io/badge/Scrum-6DB33F?style=for-the-badge)
![Agile](https://img.shields.io/badge/Agile-FF6F00?style=for-the-badge)
![AI/LLM Testing](https://img.shields.io/badge/AI%2FLLM%20Testing-8A2BE2?style=for-the-badge)

## 🎓 Certifications &amp; recognition
`ISTQB Foundation (CTFL)` &nbsp; `Agile Testing (ATA)` &nbsp; `Selenium Automation (ATA)` &nbsp; `PSM I — in progress` &nbsp; `Best Service & High-Performance awards`

---

<div align="center"><sub>Portfolio note: these are generalized versions of skills and systems I built for a proprietary platform — employer-specific identifiers, infrastructure, and workflows removed.</sub></div>
