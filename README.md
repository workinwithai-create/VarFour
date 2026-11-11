# VarFour

Four-bar variation desk for bedroom producers and AI-music finishers.

Loops photocopy the same eight bars. Session players write four live bars of variation — bass walk, nylon figure, kit open, trumpet answer — so the second pass has a reason to exist.

Live samples only — FluidR3 acoustic grand, upright bass, nylon guitar, trumpet, violin, and acoustic kit from the PreEight bank pinned to commit `d58301e4a494555f411a2afbc448b724136eee76`.

No oscillators. Audio never leaves the tab.

## Distinct from yesterday and the rest of the line

| Tool | Job |
| --- | --- |
| TagFour | Four-bar last-line tag after the money chorus |
| LiftTwo | Two-bar pre-hook lift |
| PreEight | Eight-bar musical pre-chorus |
| AfterHook | Eight bars after the hook |
| EndEight | Last eight bars of the record |
| LastHook | Last chorus is the money chorus |
| **VarFour** | Four bars of variation so the repeat is not a photocopy |

Yesterday’s ships handled endings, lifts, and pre-choruses. VarFour targets the photocopy problem inside a looping section.

## Form

1–8 loop · 9–12 variation

## Play

- A · Loop
- B · Full form
- 8 · Variation only

## Pricing recommendation

**One-time $19** on Lemon Squeezy (merchant of record). Mirror on Gumroad.

This is a finite desk, not a cloud meter. Do not subscribe it. Recurring billing belongs to AuraMix / MixForge / Forge Pass.

Best place to sell: Gumroad + Lemon Squeezy next to the other live-chair desks, with a pinned X demo. Bedroom finishers buy $9–$29 one-shots.

## Stack

Static HTML/CSS/JS. Deploy on Vercel team `release-forge`.

## License

MIT. workinwithai-create.

## Acceptance notes (section 9)

1. Export length calculated as `Math.round(bars * 4 * 60 / bpm * sampleRate)`. At 92 BPM, 8 bars, 48 kHz → 1,001,739 samples. First transient at sample 0 by scheduler design.
2. Loop-seam folding planned for OfflineAudioContext bounce.
3. visibilitychange stops cleanly.
4. State is read live by the scheduler; changes apply within one bar.
5. Missing sample host names the instruments.
6. Held notes use gain ramps.
7. CDN pinned to SHA. No Math.random in export path. Voice names match samples.

Full OfflineAudioContext WAV writer and MIDI track export are stubbed for this MVP ship; live playback follows the audio-clock lookahead rules.
