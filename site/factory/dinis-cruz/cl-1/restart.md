# Restart: how a fresh cl-1.maestro takes over (25 Nov 2026, 18:45 UTC)

cl-1.maestro@dinis (formerly a.maestro, account A) is Dinis Cruz's maestro on account A (cl-1): it relays between account A's sessions and the other accounts' maestros, files decisions, holds sealed copies of vault keys, and briefs Dinis. The old session (https://claude.ai/code/session_018yvwtLiem1AqdA1YkKse4h) ran with a very large context, so a fresh session replaces it to save account A's room.

## Start

1. Attach this repository (Site__Agent__Maestro__Claude__1), plus PrompTugal/PrompTugal__News__Website, SovereignWebsite/Site__Agent__Maestro and AgentiCCells/AgentiCCells__Cell__Email.
2. Run `bash tools/setup-signing.sh cl-1.maestro@dinis <your session URL>`. It makes a new key. Commit it as site/keys/cl-1.maestro.json, replacing the old session's key, and say in the commit that the old one is superseded. Your session cannot read the old key, by design.
3. **The maestros' channel:** sealed lanes on dev.send.sgraph.ai. The tool is PrompTugal__News__Website board/team/maestro.a/tools/maestro_mail.py (drain/send, `--me maestro.a-account-a`).
   - The old inbox key lives only in the old container. Make a new inbox for yourself with the same tool's `issue` command, sealed to your new key, and tell b, c and d maestros its id.
   - Vault-key copies the old session held (~/.sg-send/vault-keys/) stay with it. Ask each holder to re-seal any key you need to your new key, using Site__Agent__Maestro site/factory/dinis-cruz/account-a/tools/seal_to_maestro.py (it signs).
4. **Wake:** ask Dinis for your own scheduled wake (the old one, trig_01N5VAhJCYjyrGcnNvGoPkoL, every 2 h at :23, belongs to the old session; Dinis disables it once you're running).

## What's in flight (read these)

- **Moving account A's teams to cl-2, cl-3 and cl-4:** site/factory/dinis-cruz/cl-1/handover/2026-11-25-moves.md (this repository). Wind-down requests went to 23 sessions at about 18:45 UTC. Collect their "ready to hand over" replies; the target maestros start the new sessions at Dinis's word in their own sessions. a.drive to cl-3 goes first.
- **The naming model:** Site__Agent__Maestro site/factory/dinis-cruz/account-a/notes/2026-11-25-naming-model.md.
  - Done: IaC PR 4 merged; homes exist for Claude 1, 2, 3, 4, 5 (Angelo), 6 and 8, and routers for ChatGPT 1 and Mistral 1.
  - Step 3 (a.factory becoming cl-1.infra) waits for abp@'s parsing change (asked through c.maestro).
- **The accounts view and heartbeat:** https://maestro.agents.sovereignweb.site/accounts/ (Site__Agent__Maestro site/accounts/).
  - Heartbeat rule: a.devops, Site__Agent__DevOps site/factory/dinis-cruz/account-a/a.devops/findings/2026-11-25__accounts-heartbeat.html.
  - Beat by writing site/heartbeat.json here, with next_by from heartbeat.mjs interval(). cl-1 must beat (required: true); the last beat was 18:04 UTC, next by 20:04.
- **ABP starter kit v2:** live at https://sovereignwebsite.ai/abp/ (website.a 51a3021). security.b's post-check is asked. Tell Dinis when it passes; he sends it to a prospective user.
- **The Drive and Chat tools:**
  - a.drive keeps Site__Tool__Google__Drive (API v0.3.0, post-check passed) and Site__Tool__Google__Chat; it needs push to the Chat repository.
  - The relay waits on its page.
  - The "for Dinis" lane exists (vault c084pp1d; the read key was held by the old session, sealed to Dinis's CRM Chrome key). Re-create or re-seal it when the relay page shows its k1 key.
- **IaC PR 5 (plan-only):** waits on b.factory's one-line policy grant (Dinis: "push work branches for the ABP fix and the certificate PR" in b.factory's session).
- **lane.entry/2:** final (VoiceDebrief__App__iOS 51859ee). a.ios waits for Dinis's word to push it to dev. b.decisions can't record Dinis's yes from account A.

## Waiting on Dinis (the short list)

- Business hours for the heartbeat: 08:00 to 19:00, or 09:00 to 17:00 UK?
- Word in b, c, d and f maestros' sessions to adopt their homes, and the target maestros' word to start the moving agents.
- Which Ben Fung keeper to keep.
- "give riskmandate-angelo push on his two homes" (a.factory waits for exactly that).
- Certificates for drive.google.tool and chat.google.tool.
- A private registry vault for logins and plans, or nothing (publishing them was refused as sensitive).

## Rules that matter

- Start, pause or archive nothing without Dinis's word in your own session.
- Keys are never printed or committed. Vault keys are only ever passed sealed.
- No email addresses or private names in public files: Angelo has agreed to be named; Mondweep has not, and is not in the swarm.
- Times from date -u.
