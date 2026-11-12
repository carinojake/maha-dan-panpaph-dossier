# Bai Yueling: Jade Veil — Game Design Proposal v0.1

**Status:** PROPOSED / UNAPPROVED | **Date:** 2026-11-12
**Genre:** 2D Boss Rush Action RPG | **Preferred concept:** Hybrid Sword Duel
**Engine candidate:** Godot | **First target:** macOS Apple Silicon M1, reference 1280×720, goal 60 FPS (unmeasured)
**Universe:** 《มหาแดนพันภพ: ผนึกกระบี่สะบั้นสวรรค์》

## Creative vision

A playable Bai Yueling emphasizes precise sword combat, agile movement and tactical flying-sword timing. Each boss attack should be learnable, clearly telegraphed and fairly counterable. The game's identity is elegant technical dueling, not repetitive attack-button input.

## Evidence boundary

**CANON (to be verified against originals before approval):** Bai Yueling exists in the main universe; world rules are controlled by World Bible v1.2 and Canon C-001–C-022. The owner-supplied image depicts a white/silver-robed sword-bearing woman with teal/jade accents. A picture is visual reference, not proof of powers or lore.

**PROPOSED:** Working title; independently playable character; 3-hit melee combo; one flying-sword mechanic; guard/dodge/timed parry/counterattack; one noncanonical trial arena and one training boss; 2-phase battle.

**UNRESOLVED:** Bai Yueling's canonical power ceiling; true number and origin of swords; frost powers; chronology relative to the main story; whether a premium hand-painted treatment is compatible with the established art canon; rights to the reference image.

## Four design pillars

1. **Elegant Precision:** timing, spacing and earned counterattack windows.
2. **Flying Sword Identity:** launch, travel, return and recovery, without making melee obsolete.
3. **Fair Bosses:** readable telegraphs, accurate hitboxes, learnable attack responses.
4. **Chinese Fantasy Legibility:** refined motion, restrained ink/cloth/mist effects that never hide danger cues.

## Proposed moment-to-moment loop

Enter arena → observe boss → dodge/guard/parry → punish opening with melee → time flying sword → adapt to phase change → win/lose → review result/restart.

**Hypothesis:** one encounter loop takes roughly 5–8 minutes; requires real playtesting.

## Player controls and combat

- Movement: left/right, jump, dodge; keyboard first with gamepad planning.
- Basic attack: three-hit sword combo. Final hit has meaningful recovery risk.
- Flying sword proposed states: READY → LAUNCH → RETURN → RECOVERY → READY.
- Defense: dodge, guard, timed parry and a counter window; exact priority/cancel rules remain to be specified.
- Early test-tuning hypotheses: dodge duration ~0.18s; parry window 0.12–0.18s; boss phase change around 50% HP. **Not final frame data or Canon powers.**
- Keep combat-state interruptions, invulnerability, hitstop and error cases explicitly in the technical review.

## First boss proposal

**Working name:** หุ่นกระบี่หยกพิทักษ์ม่าน (Jade Veil Training Construct).
A noncanonical training encounter to avoid inventing history.

- **Phase 1:** horizontal slash, ranged blade strike, heavy telegraphed strike. Emphasize readable cues and deliberate recovery windows.
- **Phase 2:** changed timings/attack combinations rather than only higher damage; test how players adapt.
- **Fairness rules:** at least one viable answer per attack; consistent hitbox; no unavoidable attacks; attack telegraph readable in silhouette and audio; no confusing effects over important cues.

## Art / animation proposal

The owner's image suggests silver-white layered robes, jade/teal detail, translucent flowing fabric, long dark hair and luminous sword imagery. Consider Chinese Xianxia + restrained ink-wash. Snow motifs are **not proof** of canonical elemental abilities.

Required initial animation design list: idle, run, jump, dodge, basic attacks 1–3, flying-sword launch/return, parry, hurt, defeat, victory. Compare frame animation, skeletal/cutout and hybrid before choosing an asset pipeline.

Any move toward Premium Hand-Painted styling must undergo art-canon review. No image is uploaded as an asset in this documentation pack.

## HUD and accessibility

Player HP, boss HP/name, flying sword state, phase change indicator, pause, victory/defeat/restart. Provide remappable controls, proposed one-handed layout, training assistance for precise timing, reduced flashing/motion, visual + audio tells, and legible 1280×720 presentation.

## Vertical slice — proposed in-scope

One player; one arena; one two-phase boss; movement and dodge; 3-hit combo; one flying sword mechanic; guard/parry; HP/HUD; victory, defeat and restart; basic input configuration.

**Out-of-scope:** open world, multiplayer, store/gacha, skill-tree expansion, quest campaign, multiple bosses, canon-changing story, networking, production asset pipeline.

## Technical concept only

Proposed design boundaries: Game Flow, Player Controller, Combat State Machine, Flying Sword component, Hitbox/Hurtbox, Boss State Machine, Camera, HUD/Accessibility, Audio/VFX, Telemetry/Test plan. No implementation or code is authorized.

## Acceptance hypotheses (for future validation)

- Boots on target macOS; supports start/fight/win/lose/restart.
- Player and sword never lock in invalid states during normal and interrupted combat.
- Boss phase 1/2 and all cues work; damaging hitboxes match visible attacks.
- No crashes over at least 10 repeated sessions.
- Performance **measured** on M1 against the 60 FPS goal; goals are not test results.
- Canon compliance and parent-game integrity verified.
- Attack readability and accessibility checked through actual use.

## Major risks

Combat complexity/scope creep; animation–hitbox mismatch; visual effects obscuring telegraphs; flying-sword state bugs; unfamiliar player controls; Mac M1 performance; unverified Canon; mistaken public rights to image; accidental parent-game change.

Mitigation: graybox one-boss concept only **after** a separate production gate; independent AI review, scoped acceptance criteria, explicit Canon matrix, isolated workspaces, immutable parent-game controls.

## Planned stages, all subject to approval

D0 Concept → D1 Design → D2 Technical/Production Authorization → D3 Vertical Slice Acceptance.

**This document does not grant D1 or D2, does not unlock Gate G1 of the parent game, and does not request code generation.**
