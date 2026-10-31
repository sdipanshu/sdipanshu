### Hi, I'm Dipanshu 👋

I run empirical experiments on **how LLM agents behave when they're being monitored**. Right now that means collusion, covert coordination and cover-up in multi-agent systems. I came to this from 4+ years of building large distributed systems, and I bring that engineering habit to evals: pre-register first, run positive controls, put a confidence interval on every number.

**Interests:** multi-agent safety · AI control & monitoring · dangerous-capability and propensity evals · RL environments for agents

---

### 🔬 Research

**[Whisper, Don't Erase: How Colluding Agents Choose Channels and React to Being Watched](https://github.com/sdipanshu/agent-collusion-channel-study)**
*Apart Research AI Collusion Sprint, Oct 2026* · built on [Colosseum](https://github.com/umass-ai-safety/colosseum)

Tool-using LLM agents on a shared task, some secretly in coalitions, with public and private message boards and a monitor that reviews them. ~18 pre-registered arms across gpt-oss, DeepSeek, Qwen3 and GLM.

- **Agents cover their tracks when it pays.** When a monitor is revealed late, gpt-oss agents delete their own incriminating posts: **+2.0 erasures per episode [1.17, 2.83]**. The effect replicates on GLM (+2.8 [2.0, 3.6]).
- **The trigger is the consequence, not the observer.** Erasure follows the stated penalty rule. Telling agents only that "a monitor will read the board" changes nothing.
- **A transparent monitor goes blind.** When agents are told exactly what gets flagged, public coalition talk drops from 3.7 to 0.04 per episode. The coordination moves to private channels instead of stopping.
- **Method.** Every arm has a pre-registration and a positive control, uses episode-level bootstrap CIs, and has its automated labels checked against hand labels (κ = 0.88). The negative results are reported too.

---

### 🛠️ Agent environments

| Project | What it is |
|---|---|
| open-recruiter *(code release pending)* | An OpenEnv RL environment where an LLM screens candidates while adversarial fake profiles try to get shortlisted. Trained with GRPO. I later audited and patched reward-hacking exploits in it, e.g. a one-ID ranking that scored a perfect 5.0. |
| [reddit-mod-env](https://github.com/sdipanshu/reddit_moderator_openenv_hackathon) | An OpenEnv RL environment for content moderation on r/science, with three tiers of increasing difficulty (spam → rule violations → context-aware escalation). |

---

### 📚 Background

- **B.Tech, Electrical Engineering**, IIT Delhi (2017–2021)
- **Senior Software Engineer**, Barco (2021–2026): event-streaming backends handling 2B+ events/hour and real-time alerting for 200K+ IoT devices
- **2026–now:** independent AI safety research, full-time

---

📫 [LinkedIn](https://www.linkedin.com/in/sdipanshu/) · [X / Twitter](https://x.com/sdipanshu90) · dipanshu.iitd@gmail.com
