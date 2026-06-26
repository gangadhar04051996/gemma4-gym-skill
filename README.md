# 🏋️ Gym Coach — Edge Gallery Agent Skill

A personal gym coach skill for Google AI Edge Gallery with Gemma 4 E2B.  
Logs daily workouts, reads your history, plans tomorrow's session, and accepts photos/video for form analysis.

---

## Your Goals
- 🏃 **Faster running** — pace improvement, endurance, 5K and beyond
- 💪 **Abs** — core strength, visible definition, planks, crunches, leg raises
- 🔥 **Toned body** — lean muscle, resistance training, no bulk

---

## Files in this skill

```
gym-skill/
├── SKILL.md                  ← Load this into Edge Gallery (required)
├── scripts/
│   └── index.html            ← JavaScript workout logger (auto-loaded)
├── gym-log.md                ← Copy to your Obsidian vault
├── daily-note-template.md    ← Obsidian Templater daily note template
└── README.md                 ← This file
```

---

## Setup — Edge Gallery (5 min)

### Step 1: Load the skill

**Option A — From local file (recommended):**
1. Copy the entire `gym-skill/` folder to your phone's internal storage  
   e.g. `Downloads/gym-skill/`
2. Open **Google AI Edge Gallery** → tap **Agent Skills**
3. Tap **+** → **Import from local file**
4. Navigate to `gym-skill/SKILL.md` and select it
5. The skill loads — you'll see "gym-coach" in your skills list ✅

**Option B — From GitHub URL:**
1. Push this folder to a public GitHub repo
2. In Edge Gallery → Agent Skills → **+** → **Load from URL**
3. Paste the raw URL to your `SKILL.md`

### Step 2: Select Gemma 4 E2B

- In Agent Skills, confirm **Gemma 4 E2B** is the active model
- E2B supports multimodal — you can attach photos directly in the chat

### Step 3: Set up the log file path

The skill saves your workout log to `gym-log.md` in the Edge Gallery sandbox.  
To sync it with Obsidian:

- **Android:** Enable Obsidian's local folder vault → point to a folder Edge Gallery can also access, or use the manual copy workflow below
- **Manual sync:** After each week, export `gym-log.md` from Edge Gallery and paste into your Obsidian vault

---

## Setup — Obsidian (optional, for bookkeeping)

### Daily note template

If you use the **Templater** plugin:
1. Copy `daily-note-template.md` to your Obsidian templates folder
2. In Templater settings, set it as your daily note template
3. Every day you get a pre-built gym log section in your daily note

### Gym log note

1. Copy `gym-log.md` into your Obsidian vault root (or a `Fitness/` folder)
2. This is your permanent record — the skill appends to it over time
3. Use the **Smart Connections** plugin to let Gemma 4 query it for history

---

## How to Use

### Log a workout
Open Edge Gallery → Agent Skills → type:

> "I just finished my workout. I did 3 sets of push-ups (15 reps), 3 sets of dumbbell rows (12 reps, 10kg), and a 20-minute run at a moderate pace. Energy was 4/5."

The skill will:
- Format and save the entry to `gym-log.md`
- Tell you what muscle groups need rest
- Recommend tomorrow's session

### Ask for tomorrow's plan
> "What should I do tomorrow at the gym?"

The skill reads your last 7 days and builds a balanced plan avoiding overtraining.

### Upload a photo or video
Attach a photo directly in the Edge Gallery chat:
> "Check my plank form" *(+ attach photo)*

or:
> "Here's my running video, is my posture right?" *(+ attach video)*

Gemma 4 E2B will analyze it and give specific feedback.

### Weekly review
> "How was my week? Give me a summary."

---

## Example Prompts

| What you want | What to type |
|---|---|
| Log today's session | "Log my workout: [describe what you did]" |
| Get tomorrow's plan | "What should I do tomorrow?" |
| Check form | "Is my squat form correct?" + photo |
| See progress | "How am I doing this week?" |
| Running focus | "I want to improve my pace — what's my running plan?" |
| Core focus | "Give me a 15-minute abs finisher" |
| Light day | "I'm tired today, what's a good active recovery?" |

---

## Workflow: Obsidian ↔ Edge Gallery

```
Morning:
  Open Obsidian daily note → See gym section template
  Copy yesterday's log summary from Obsidian → paste into Edge Gallery
  Ask: "Based on this, what should I do today?"

After gym:
  Type your session into Edge Gallery
  Skill logs it + gives tomorrow's recommendation
  Copy the log entry → paste back into Obsidian daily note

Weekly:
  Ask Edge Gallery: "Weekly summary"
  Copy to Obsidian "summaries/2026-W26.md"
```

---

## Tips for Gemma 4 E2B

- **Context is king:** The more detail you log, the better tomorrow's plan
- **Be consistent with format:** "3 sets × 12 reps @ 10kg" is easier for the model to parse than "did some rows"
- **Use photos:** E2B is multimodal — a 5-second form check photo is faster than describing your posture
- **Log mood:** Even just "energy 3/5" helps the skill avoid pushing you on low days
- **Don't skip rest days:** Log them too — the skill tracks recovery as part of planning

---

## License
Apache 2.0 — free to use and modify