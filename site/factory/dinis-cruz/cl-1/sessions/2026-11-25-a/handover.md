# Handover: the first cl-1.maestro session (formerly a.maestro), 25 Nov 2026

The first run of the [session handover protocol v1](https://github.com/SovereignWebsite/Site__Agent__Maestro/blob/dev/site/factory/dinis-cruz/account-a/notes/2026-11-25-session-handover-protocol.md). This session ran from 22 Nov. Its context reached about 670K tokens, because it carried a strategy conversation that belongs in a strategy agent's session. Start with [restart.md](../../restart.md) and the [moves tracker](../../handover/moves.json).

## Strategy decided today (25 Nov), and where each is written

| Decision | Record |
|---|---|
| Agent ids `<account>.<role>[.<speciality>]@[<project>.]<owner>`; account ids cl-1 to cl-8, mi-1, gpt-1, gem-1 | Site__Agent__Maestro notes/2026-11-25-naming-model.md |
| One home per role per account, `Site__Agent__<Role>__<Provider>__<Number>`, no Pages; IaC PR 4 merged | the same note; IaC requests |
| factory becomes infra (cl-1.infra, Site__Agent__Infrastructure); the IaC repository keeps its name | the same note; a.factory's plan in Site__Agent__Factory proposals/2026-11-25-naming-model-steps.md |
| Which account is which: public page, no logins or emails | https://maestro.agents.sovereignweb.site/accounts/ |
| Heartbeat by business hours, work in hand and room | a.devops: Site__Agent__DevOps findings/2026-11-25__accounts-heartbeat.html |
| Move account A's teams to cl-2, cl-3 and cl-4 | handover/2026-11-25-moves.md and moves.json in this repository |
| Session handover protocol v1; Dinis starts only maestro, decisions and infra sessions | Site__Agent__Maestro notes/2026-11-25-session-handover-protocol.md |
| Drive and Chat as importable APIs (any site, its own client id), browser only, no Claude needed | Site__Tool__Google__Drive docs and START; a.drive's start prompt in Site__Agent__Maestro account-a/start-prompts/a.drive.md |
| ABP starter kit for outside teams | https://sovereignwebsite.ai/abp/ (v2, security.b's post-check asked) |
| Angelo's account is cl-5 (named with his consent); Mondweep is not in the swarm | accounts page; IaC c223d9a |
| lane.entry/2 is the one envelope (CRM, mail, iOS, Drive/Chat relay) | VoiceDebrief__App__iOS website/lanes/entry-v2 (51859ee) |

## Secrets this session holds (ids only), to re-seal to the new session's key before archive

- **Vault keys** in ~/.sg-send/vault-keys/: sub3og9j, z9jbp8wb, kqsq3vof, sygecq6z, zxehwe8t (+ enum), 5zrg7jjk, ttei3vjb, yiy6okw9, kg37tfil, c084pp1d (the for-dinis lane: vault key, read key, append token).
- **The maestros' inbox key** (maestro.a-account-a): it can't move, so the new session makes its own inbox.
- **The maestros' shared vault key:** it can't move either, so the new session asks b.maestro to re-seal it.

## What the new session does first (protocol step 5)

1. Run START.md: make your key, publish it, write a heartbeat.
2. Tell this session your key (send_message to session_018yvwtLiem1AqdA1YkKse4h) so it can re-seal the keys above.
3. Answer the checklist:
   - signed push works;
   - key published;
   - each sealed key received;
   - wake set;
   - questions.
4. Pick up the moves tracker: every wave is ready, and the target maestros wait on Dinis's word.
