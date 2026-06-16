# Safety Room Roadmap

## Product Target

Make Safety Room feel like a polished playable demo: readable rules, strong dread, smooth input, fast retry, and stable performance on desktop and mobile.

## Current Baseline

- Night 1 is playable with menu, intro, monitor, power, Freddy route pressure, flashlight defense, jumpscare, game over, and 6 A.M. clear.
- Monitor rooms support Room3/4/6/7/8, Freddy-present states, fake signals, random phantom flashes, and a circular monitor flashlight.
- Latest polish pass adds adaptive smoothness, ambient dread pulses, and Game Over retry/menu actions.

## This Iteration

- Added Game Over action buttons so failure has a clear playable loop instead of a dead-end screen.
- Added a runtime smoothness governor that softens continuous animations on mobile or slower frames.
- Added visibility pause handling so hidden/background tabs stop nonessential animation work.
- Added subtle night dread pulses that become more likely under Freddy route or door pressure.
- Added a director layer that turns Freddy route state into subtle map/camera instability, making danger more learnable without direct tutorial text.
- Added a compact 6 A.M. result panel with remaining power, breach count, and Freddy checks so the demo has a stronger completion beat.
- Added a Game Over incident report so failure explains cause, last signal, and remaining power without breaking the horror tone.
- Added a long-monitor-use fatigue layer that makes the feed feel less trustworthy when the player camps the tablet too long.

## Design Notes

- FNAF-style tension works best when the player has partial information, limited power, and enough readable cues to blame their own choices after failure.
- Strong fan-game loops usually add diegetic feedback rather than explicit instructions: camera noise, audio tells, UI instability, and fast retry carry the learning.
- For Safety Room, prioritize atmosphere plus fairness: scares should be surprising, but the route and resource pressure should be understandable after repeat play.
- Good failure design should make the player want to retry immediately: keep the scare sharp, then give just enough evidence to form a better next attempt.

## Next Priorities

- Improve first-night onboarding through diegetic cues instead of tutorial text.
- Tune Freddy route fairness: every loss should feel traceable to monitor/power/flashlight decisions.
- Add stronger room identity for Room4/6/7/8 with unique audio tells and short one-off visual events.
- Continue mobile performance work: reduce filters during tablet-open state and keep touch response instant.
- Add a second-night rules variant only after the failure report proves Night 1 is understandable.
- Add Night 2 scaffolding only after Night 1 fairness and mobile smoothness feel stable.

## Guardrails

- Keep changes small and deployable in one iteration.
- Do not weaken core Night 1 stability or page openability.
- Preserve the black/dark-brown premium horror direction.
- Prefer CSS/JS runtime polish over new heavy assets unless the asset is essential.
- Validate locally and on GitHub Pages before marking an iteration done.