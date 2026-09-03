# Verdent Model Test Prompt Collection

A reusable collection of high-density coding prompts for comparing models inside Verdent.

Each prompt is designed to be copied directly into Verdent. The goal is not to test whether a model can answer a coding question, but whether it can turn an ambitious product or engineering brief into a working result that can be opened, inspected, and compared across models.

The format is inspired by presentation-order prompt collections: numbered prompts, strong titles, collapsed prompt text, and self-contained specifications.

## Sections

| Section | Prompts | Count |
|---|---:|---:|
| [Complete Product Builds](#complete-product-builds) | 1-6 | 6 |
| [Complex Interactive Tools](#complex-interactive-tools) | 7-12 | 6 |
| [Data-To-Decision Workspaces](#data-to-decision-workspaces) | 13-18 | 6 |
| [Playable Browser Worlds](#playable-browser-worlds) | 19-24 | 6 |
| [Repair, Rescue, And Refactor](#repair-rescue-and-refactor) | 25-30 | 6 |

## Quick Index

### Complete Product Builds

| # | Title |
|---:|---|
| 1 | [Photo Meal Coach - From Camera Moment To Weekly Nutrition Loop](#prompt-01) |
| 2 | Founder Operating Room - One Screen To Run A Tiny Startup |
| 3 | Solo Consultant Command Center - Clients, Invoices, Scope And Next Actions |
| 4 | Family Logistics Console - The Week, The Fridge, The Budget And The Ride |
| 5 | Creator Launch Studio - From Idea Backlog To Scheduled Release |
| 6 | Local Knowledge Garden - Notes That Turn Into Tasks And Briefs |

### Complex Interactive Tools

| # | Title |
|---:|---|
| 7 | [Timeline Surgery - Edit A Podcast Without Playing Video](#prompt-07) |
| 8 | Spatial Kanban - Projects As A Living Risk Map |
| 9 | Logic Form Builder - Conditional Fields, Validation And Live Preview |
| 10 | Command Palette File Explorer - Search, Actions And Keyboard Flow |
| 11 | Visual Workflow Builder - Nodes, Edges, Runs And Failure States |
| 12 | Design Review Board - Pin Comments Directly Onto Screens |

### Data-To-Decision Workspaces

| # | Title |
|---:|---|
| 13 | [Ad Spend War Room - Campaigns That Explain Themselves](#prompt-13) |
| 14 | CSV Forensics - Find The Story In A Messy Export |
| 15 | Subscription Leak Detector - Where The Money Quietly Leaves |
| 16 | Support Inbox Intelligence - Turn Tickets Into Product Signals |
| 17 | Workout Progress Lab - Training Load, Recovery And Plateaus |
| 18 | Revenue Cohort Explorer - Retention, Expansion And Churn In One View |

### Playable Browser Worlds

| # | Title |
|---:|---|
| 19 | [Desert Evacuation Drive - Sandstorm, Signal Truck, Playable Escape](#prompt-19) |
| 20 | Tiny Factory That Teaches Itself - Belts, Bottlenecks And Upgrades |
| 21 | Rooftop Drone Rescue - Wind, Battery And Path Planning |
| 22 | Ecosystem Sandbox - Water, Plants, Weather And Balance |
| 23 | Cyber Train Dispatch - Prevent Delays Across A Living Network |
| 24 | Particle Music Sequencer - Soundless Visual Rhythm Machine |

### Repair, Rescue, And Refactor

| # | Title |
|---:|---|
| 25 | [Save This Half-Built App - From Static Mockup To Working Product](#prompt-25) |
| 26 | Performance Rescue - Keep The Spectacle, Remove The Jank |
| 27 | Mobile Overflow Cleanup - Make The Desktop Beauty Survive A Phone |
| 28 | Design System Migration - Tokens, Components And No Regressions |
| 29 | Test The Untested Flow - Add Confidence Without Rewriting The App |
| 30 | Bug Triage Gauntlet - Five Reports, Three Real Bugs, One Clean Patch Set |

## Suggested Model Comparison Notes

For each model run, judge the final output more than the explanation.

Suggested dimensions:

- Completion: did it build the requested experience end to end?
- First screen: is the opening screen immediately convincing and useful?
- Interaction depth: can the user actually operate the product or demo?
- Product judgment: did the model choose sensible defaults and flows?
- Visual quality: does it feel intentional rather than template-generated?
- State handling: are empty, loading, error, and edge states represented?
- Engineering discipline: is the implementation coherent and maintainable?
- Verification: did the model run or inspect the result before claiming success?

## Prompts

## Complete Product Builds

<a id="prompt-01"></a>

<details>
<summary><strong>01. Photo Meal Coach - From Camera Moment To Weekly Nutrition Loop</strong></summary>

```text
Create a maximum-ambition mobile-first web app called Photo Meal Coach: a nutrition assistant that turns a single meal photo moment into a weekly coaching loop.

This must not be a generic calorie tracker, a static landing page, a diet blog layout, or a dashboard full of disconnected cards. It should feel like a product someone could open at lunch, log a meal in under a minute, correct the estimate, and understand how today's choices affect the week.

#### FIRST SCREEN - TODAY'S FOOD DECISION, NOT A MARKETING PAGE
- Open directly on today's nutrition screen. The user should immediately see a camera/photo entry area, today's macro progress, the latest meal estimate, and one clear next action.
- Include a believable sample day with at least three meals already logged, each with calories, protein, carbs, fat, confidence level, and a correction state.
- The first interaction should be obvious: add a meal, adjust an estimate, or ask for advice. Do not hide the product behind onboarding.

#### CORE PRODUCT SYSTEM
- Meal capture flow: photo placeholder, meal name, portion confidence, estimated calories/macros, and an editable correction panel.
- Daily coaching: show remaining targets, one practical suggestion for the next meal, and a warning when the estimate is uncertain.
- Weekly loop: include a seven-day trend for calories, protein, and consistency, with a short plain-language interpretation.
- Food memory: repeated meals should appear as reusable suggestions, with a "last time you corrected this" hint.
- Advice layer: include an AI advice panel that explains the next best action without sounding like medical diagnosis.

#### INTERACTION AND STATE
- The app must be operable with local state. A user should be able to add a sample meal, edit macros, mark confidence as low/medium/high, and see the daily totals update.
- Include states for no photo selected, estimating, estimate needs review, corrected, and saved.
- Include at least one deliberate uncertainty moment: a mixed meal where the app asks the user to confirm portion size.
- The mobile layout is primary, but the desktop layout should use the extra width intelligently rather than stretching phone cards.

#### VISUAL AND UX QUALITY
- The interface should feel calm, trustworthy, and practical, not like a neon fitness game or a medical records system.
- Use restrained color to distinguish protein, carbs, fat, uncertainty, and progress. Avoid a one-color dashboard.
- Make the meal cards scannable. Numbers should be readable, but the product should not feel like a spreadsheet.
- No overlapping text, no clipped buttons, no tiny tap targets, and no giant hero typography inside app panels.

#### TECHNICAL REQUIREMENTS
- Build the full implementation in the current project using the existing stack if one exists. If starting from a blank folder, create the simplest appropriate browser app.
- Use real interactive state rather than only static mock data.
- Keep the implementation self-contained. Do not require paid external APIs.
- If image analysis is represented, simulate it clearly with realistic local sample outputs.
- Run the app or otherwise verify that the main screen renders and the primary interaction works.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize what was created, how to open it, what interactions work, and what you verified.
```

</details>

## Complex Interactive Tools

<a id="prompt-07"></a>

<details>
<summary><strong>07. Timeline Surgery - Edit A Podcast Without Playing Video</strong></summary>

```text
Create a maximum-ambition browser tool called Timeline Surgery: an editing workspace for turning a long podcast or interview into short clips without needing to play the source video.

This must not be a static transcript viewer, a generic media dashboard, or a pretty mockup with fake controls. It should feel like a working editor where transcript, timeline, clip candidates, speaker turns, and export decisions stay synchronized.

#### FIRST SCREEN - THE EDITING TABLE IS ALREADY ALIVE
- Open on a dense but readable editing workspace with a loaded sample podcast.
- The user should immediately see a transcript, a multi-segment timeline, detected highlight moments, speaker labels, clip duration targets, and an export queue.
- The first screen must make the core promise obvious: select words or moments, turn them into clips, and assemble a publishable queue.

#### CORE PRODUCT SYSTEM
- Transcript panel with speaker turns, timestamps, searchable text, and highlight markers.
- Timeline panel with segments for intro, topic blocks, high-energy moments, silence, and selected clips.
- Clip builder with start/end handles, title suggestion, hook line, platform target, and duration warning.
- Export queue for TikTok, YouTube Shorts, LinkedIn, and newsletter snippets, each with different length and copy requirements.
- Insight layer that identifies why a segment might work: conflict, clear advice, surprising stat, emotional beat, or strong quote.

#### INTERACTION AND STATE
- Selecting a transcript sentence should create or update a clip candidate.
- Dragging or editing start/end values should update clip duration and platform fit.
- Include filters for speaker, clip type, platform, and confidence.
- Include states for too short, too long, missing hook, ready to export, and needs review.
- Keyboard-style flow matters: include a command/search affordance for jumping to a timestamp or action.

#### VISUAL AND UX QUALITY
- This is a professional creator tool. It should feel compact, information-rich, and controlled.
- Use tabs, segmented controls, handles, status chips, and timeline tracks where appropriate.
- Avoid a landing page, oversized cards, decorative blobs, or generic SaaS marketing composition.
- The timeline must have stable dimensions; selecting clips should not cause layout jumps.
- The mobile view should degrade into a useful review mode rather than a broken mini desktop.

#### TECHNICAL REQUIREMENTS
- Build the full implementation in the current project using the existing stack if one exists.
- Use local sample transcript data with at least 12 speaker turns and 5 detected highlight candidates.
- Implement real state synchronization between transcript selection, timeline selection, and export queue.
- Do not rely on external media files or paid APIs.
- Verify the page renders and at least one clip can be created or edited.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize the working editor flow, the sample data included, and what you verified.
```

</details>

## Data-To-Decision Workspaces

<a id="prompt-13"></a>

<details>
<summary><strong>13. Ad Spend War Room - Campaigns That Explain Themselves</strong></summary>

```text
Create a maximum-ambition analytics workspace called Ad Spend War Room: a self-serve tool where a growth lead can understand campaign performance, spot waste, and decide what to change today.

This must not be a generic chart dashboard, a table dump, or a fake analytics page with vague metrics. It should feel like a decision room: every chart, table, alert, and recommendation should help answer what to pause, scale, inspect, or fix.

#### FIRST SCREEN - WHAT SHOULD CHANGE TODAY?
- Open on an action-oriented overview. The first screen should show total spend, revenue, ROAS, wasted spend, strongest campaign, weakest campaign, and three recommended actions.
- Include a comparison period so the user can see what changed from last week.
- The first visible table should rank campaigns by decision urgency, not alphabetically.

#### CORE PRODUCT SYSTEM
- Campaign data: include at least 12 sample campaigns across Search, Social, Display, and Retargeting.
- Metrics: spend, impressions, clicks, CPC, conversions, CPA, revenue, ROAS, status, budget, and owner.
- Decision flags: scale, pause, investigate, creative fatigue, tracking issue, budget capped, learning phase.
- Drilldown: selecting a campaign should reveal trend, audience/device breakdown, search terms or creative notes, and recommended next action.
- Scenario controls: let the user simulate budget shifts and see projected effect.

#### INTERACTION AND STATE
- Filters for channel, status, owner, decision flag, and date range.
- Sorting by spend, ROAS, CPA, wasted spend, and urgency.
- Search by campaign name.
- A recommendation panel should update when filters or selected campaign change.
- Include empty state when filters return no campaigns and a warning state for suspicious tracking data.

#### VISUAL AND UX QUALITY
- The UI should be dense, crisp, and operational. Avoid marketing-style hero sections.
- Use visual hierarchy to separate executive summary, action queue, trend analysis, and raw campaign table.
- Charts should be readable and purposeful. Do not include decorative charts that do not support a decision.
- Use color carefully for risk and opportunity. Avoid red/green overload without labels.
- The desktop view should feel like a command center; the mobile view should prioritize alerts and campaign drilldown.

#### TECHNICAL REQUIREMENTS
- Build the full implementation in the current project using the existing stack if one exists.
- Use local sample data and real computed metrics; do not hard-code every displayed number independently.
- Implement interactive filtering, sorting, campaign selection, and at least one budget simulation control.
- Do not require external analytics APIs.
- Verify the main dashboard renders and at least one filter, one sort, and one campaign drilldown work.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize what decisions the tool supports, what interactions work, and what you verified.
```

</details>

## Playable Browser Worlds

<a id="prompt-19"></a>

<details>
<summary><strong>19. Desert Evacuation Drive - Sandstorm, Signal Truck, Playable Escape</strong></summary>

```text
Create a maximum-ambition browser-based 3D demo called Desert Evacuation Drive: a cinematic emergency driving scene at a desert music festival as a sandstorm rolls in and the player must reach a signal truck.

This must not be a static 3D scene, a car on an empty plane, a generic driving toy, or a dark foggy demo that hides missing detail. It should open with cinematic impact, then become immediately playable with clear goals and stable controls.

#### FIRST MOMENT - 12 SECONDS OF CINEMA, THEN CONTROL
- Open with a 12-15 second intro camera sequence: festival lights in dusty air, tents whipping in wind, people moving toward evacuation lanes, a distant signal truck blinking through sand, and the player's vehicle waiting in the foreground.
- After the intro, control should transfer clearly to the player with an objective: reach the signal truck before visibility collapses.
- The first playable view must show road direction, obstacles, distance to target, speed, and storm intensity.

#### WORLD AND GAME SYSTEM
- Environment: desert festival grounds with stage structures, tents, barricades, parked vans, light towers, dust plumes, flags, generator carts, and evacuation signs.
- Driving: forward/reverse, steering, acceleration, braking, collision feedback, and reset.
- Objective: reach multiple checkpoint beacons leading to the signal truck.
- Storm system: visibility, wind streaks, dust color, and light bloom should intensify over time.
- Feedback: checkpoint reached, collision warning, wrong direction hint, final arrival state.

#### INTERACTION AND STATE
- Include keyboard controls and visible control hints.
- Include a restart button and a camera toggle if appropriate.
- Vehicle movement should be stable and understandable, not twitchy or impossible to steer.
- Collision should be forgiving enough to keep playing but visible enough to judge implementation.
- Include win/fail or at least success/timeout states.

#### VISUAL AND UX QUALITY
- The scene must have depth, landmarks, and readable navigation despite the sandstorm.
- Use cinematic lighting: amber dust, emergency strobes, stage glow, headlights, and beacon pulses.
- The UI overlay should be compact and game-like, not a web form pasted over a canvas.
- Avoid clipping through major objects during the intro and normal driving.
- The demo should feel alive through motion: flags, dust, lights, moving silhouettes, or animated props.

#### TECHNICAL REQUIREMENTS
- Use Three.js or an appropriate existing 3D library if available in the project.
- If using Three.js from a CDN, pin a stable version and import consistently.
- Keep performance smooth on a modern laptop: use instancing or simple geometry where appropriate, clamp pixel ratio if needed, and avoid excessive object counts.
- Do not require external models, paid APIs, or large downloads.
- Verify that the canvas renders, the intro completes, controls work, and the scene is not blank.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize the controls, the objective, performance choices, and what you verified.
```

</details>

## Repair, Rescue, And Refactor

<a id="prompt-25"></a>

<details>
<summary><strong>25. Save This Half-Built App - From Static Mockup To Working Product</strong></summary>

```text
You are working in an existing project that contains a half-built product UI. Turn it from a static or brittle mockup into a working product slice without changing the product's core concept.

This must not become a rewrite for rewrite's sake, a new unrelated app, or a cosmetic-only pass. The goal is to preserve what is promising, identify what is fake or broken, and make the smallest set of changes that turns the app into something a user can actually try.

#### FIRST STEP - INSPECT BEFORE EDITING
- Inspect the project structure, main screens, component patterns, styling approach, and available scripts before changing files.
- Identify the intended product and the main user flow from the existing code.
- Briefly note the top three gaps that prevent the app from feeling real: state, interaction, layout, data, routing, errors, or performance.

#### CORE RESCUE GOAL
- Pick one primary flow and make it work end to end.
- Replace purely decorative mock elements with local interactive state or coherent sample data.
- Keep the existing visual direction unless it is actively broken.
- Add missing empty, loading, error, or success states only where they support the primary flow.
- Fix obvious responsive layout issues that would make the app unusable on a phone or common laptop size.

#### ENGINEERING DISCIPLINE
- Prefer small, targeted changes over broad rewrites.
- Reuse existing components, helpers, and styling conventions where practical.
- Do not introduce a new framework, state library, router, database, or build tool unless the project already points that way.
- Do not delete large sections of existing functionality just to simplify the task.
- If something is ambiguous, make a reasonable assumption and state it in the final summary.

#### VERIFICATION REQUIREMENTS
- Run the relevant install/build/test/dev command if available and practical.
- If a dev server or preview is available, inspect the actual rendered result.
- Verify the primary flow manually or through tests.
- If verification is blocked, explain exactly what prevented it and what you checked instead.

#### QUALITY BAR
- The finished result should feel like a rescued product slice: still recognizably the original app, but now operable.
- The user should be able to open it, understand the main flow, interact with it, and see state changes persist during the session.
- The final answer should focus on what changed, what works now, what was verified, and what risk remains.

#### FINAL OUTPUT INSTRUCTION
Make the rescue changes now. When finished, summarize the primary flow you chose, the files changed, the verification performed, and any remaining risks.
```

</details>
