# Muscle Lab

A 3D muscle lab that runs in the browser. You watch about 60 muscles on each side work in slow motion, in 31 activities, with 67 muscles.

### ▶ [Open Muscle Lab](https://stevenwsharp-ctrl.github.io/muscle-lab/)

**Live site:** [stevenwsharp-ctrl.github.io/muscle-lab](https://stevenwsharp-ctrl.github.io/muscle-lab/)

## What it does

- **Activities:**
  - Arm raises, pull-up, push-up, squat
  - Running on asphalt, trail or track, jump rope, boxing, and a slam dunk (approach, penultimate step, plant, takeoff, dunk, landing)
  - Skiing on groomers, moguls and powder, ski jumping, and a freeride cliff drop (approach, load, pop, compact air, extend, absorb, ride away)
  - Piloting a boat in rough seas
  - Daily life and work: desk life (sitting and typing) and nursing (bedside care)
- **Breath, neck, hand and foot:** 4 lessons (breath mechanics, neck deep vs superficial, hand grip and fine control, foot arches and the windlass) and 8 new muscles: diaphragm, intercostals, transversus abdominis, pelvic floor, suboccipitals, thumb pad, little-finger pad and hand intrinsics. The breathing muscles follow the breath in every activity; the hand muscles light up when you grip. Each coach card has a "Breath link".
- **Animal mode:** 7 movements the body already knows but chairs and overuse let fade: koala climb (hug a tree, diagonal hand-foot pairs), vine swing (hang and pump a swing), monkey hang (passive and active hang, scapular pulls, knee raise, side swing), bear crawl, crab walk, ape squat and lizard crawl. Each explains which muscles work and why the pattern matters.
- **Yoga mode:** 26 poses and a sun salutation, with Sanskrit names. Pick up to three focus areas (hips, hamstrings, shoulders, spine, core, legs, balance, neck, feet, calm, or the muscle you picked in the coach). The flow follows a class arc: arrive, warm up, sun salutation, standing poses, balance, backbend, seated poses, cool down and rest. One-sided poses play on the left side, then on the right side. Short flows are free; full flows are Pro. Share a flow with a link.
- **Bath yoga:** 11 gentle poses in a bathtub (floating arms, neck release, shoulder circles, seated cat and cow, tub twist, knee to chest, figure four, foot waves, water forward fold, float and rest). Water and buoyancy are drawn on screen, and the gravity layer counts only about 10% of the weight below the waterline.
- **Muscle action focus:** pick Isometric, Concentric, Eccentric or Stretch in the coach or yoga panel, or click a row in the color legend. Only muscles doing that action light up, the panel explains the difference, and the plan tempo changes: holds for isometric, a pause then lift for concentric, a slow 3-count lowering for eccentric, long relaxed holds for stretch.
- **Breath option:** a breath circle and lungs and a diaphragm that move on the body. Paces: calm 4–6, even 5–5, box 4–4–4–4 and relax 4–7–8. In yoga, the breath follows the poses: inhale to lift or open, exhale to fold, twist or lower.
- **Activities button:** the bright ▦ Activities button at the top left opens a grid of every activity, the muscle coach, yoga and bath yoga.
- **Fast on phones:** muscle fibers draw in batches, colors are cached, and the coach reuses its movement samples. Phones start at a lower pixel ratio. If frames get slow, the app steps quality down by itself (sharpness, glows, fiber detail).
- **Easy to read:** 📖 Read pace (on by default) slows the motion when an instruction needs more time to read (about 200 words a minute), and each caption stays on screen long enough to read. Tap the caption to pause.
- **Recenter and color key:** ⌖ Recenter (or double-tap the body) brings the whole body back to the center. 🎨 Key explains every color: working, lengthening, holding, stretching, resting, the picked muscle, start and attach dots, gravity line and bones.
- **Share anything:** the 🔗 Share button copies a link to what you see now, with your settings: speed, view angle, sweep, layer, anatomy, labels, body, gravity, zoom panel, breath and pace, running surface, and (when paused) the exact frame: an activity (`#act-desk`), its counter moves (`#counter-desk`), a muscle in the coach (`#muscle-soleus`), a plan, one exercise, a yoga flow or one yoga pose (`#pose-tree`).
- **Find the muscle:** when you pick a muscle, the body turns to show it (front, back or side) and zooms in. A spotlight, a pulsing pink fill and a label show where it is. Green dots show where it starts (origin) and blue dots where it attaches (insertion). The coach card names both bones.
- **Countdowns:** in the slam dunk, cliff drop and ski jumping, a ring counts down to the takeoff, the dunk and the landing impact, then flashes JUMP!, POP!, SLAM! or IMPACT!.
- **Proper vs avoid:** in lessons that show a wrong form (back seat, slumping, stooping), a large red "✕ AVOID" badge and a red screen edge show the wrong part. A green "✓ PROPER" badge shows the correct part.
- **Counter moves:** each activity has a "↺ Counter it" row. It plays moves that undo the load of that activity, for example a chest opener and a neck reset after desk life.
- **Both sides and all angles:** every one-sided exercise and activity plays on the left side, then on the right side (boxing, slam dunk, ski jumping landing, desk mouse hand and nursing included). A large LEFT SIDE / RIGHT SIDE badge shows the side, and the camera mirrors to face it. The ↔↕ Sweep view swings the camera left-right and up-down.
  - Two gravity lessons: stacked vs slumped posture, and centered vs back-seat ski stance
- **Muscle colors:**
  - Red: shortening under load
  - Orange: lengthening under load
  - Yellow: holding
  - Blue: being stretched
- **Zoom:** close-up anatomy of one region at a time, with the sarcomere, length-tension curve, pennation angle, ground reaction force and ski vibration.
- **Muscle coach:** pick a muscle to see its synergists, antagonists, stabilizers and fascial chain from the feet to the head. Then play a generated plan from martial arts, sports, yoga, ballet and qigong.
- **Gravity and ease:**
  - center of mass and line of gravity
  - base of support
  - gravity load on each joint, in N·m
  - an Ease score
- **Sharing:** links open a plan or one exercise directly. For example, `#plan-deltLat-wake` or `#move-soleus-kick`.
- **Phone mode:** the page detects a phone and changes its layout automatically.

## Plans

> **Now:** every feature is free. `CONFIG.allFree` is `true` in `index.html`. To turn on the paid plans, set it to `false`.


| Plan | What it includes |
|---|---|
| **Free** | 9 activities, the Muscle coach with plans for every muscle, the Gravity and Ease layer, sharing, and Zoom anatomy |
| **Pro** | All 18 activities, the physiology views, saved plans, and printing plans or saving them as PDF |
| **Coach** | Everything in Pro, plus your name, title and booking link on every plan you share, and branded printed plans |

### How to set up payment

1. In Stripe, make a Payment Link for each plan.
2. In each Payment Link, set **After payment → Redirect** to:
   - Pro: `https://stevenwsharp-ctrl.github.io/muscle-lab/?unlock=pro-7Q4K9X`
   - Coach: `https://stevenwsharp-ctrl.github.io/muscle-lab/?unlock=coach-3M8T2V`
3. In `index.html`, find `const CONFIG=`. Paste the Payment Link URLs into `pay`, and set the prices, your booking link and your email.

The unlock runs in the browser and is saved on the buyer's device. It is simple to set up, but a person who reads the page code can find the codes. To make the unlock secure, move the check to a small server, such as a Cloudflare Worker that verifies Stripe payments.

## Files

| File | Description |
|---|---|
| `index.html` | The complete app in one file. Open it in Chrome, or use the live site. |
| `README.md` | This file. |
| `LICENSE` | Copyright and terms: all rights reserved. |
| `icon.svg`, `favicon-32.png`, `apple-touch-icon.png` | Tab icon and phone home-screen icon. |

## Notes

This is a teaching model, not medical advice. Joint loads are static gravity loads for a 70 kg body. Fascial chains follow Myers' Anatomy Trains, and the app shows the evidence level for each chain (Wilke et al. 2016).

### 🌱 → ⚡ Wake to strong (activation ladder)
Every muscle page has 4 stages, based on the size principle (small motor units switch on first, big units last):
1. **🌱 Wake (~15% effort):** 3 gentle 3 s pulses with full relax. Rebuilds the brain-to-muscle link.
2. **🌿 Control (~35%):** slow full-range reps, about 3 s each way.
3. **🔥 Strength (~70%):** more load, 6–10 reps, slow 3 s lowering.
4. **⚡ Max (100%, short):** 5 s full-effort holds or 3–5 heavy reps, long rests.

An effort meter shows the stage. Muscles glow more as effort goes up. Share a stage with `#stage-<muscle>-<1-4>`.
New low-load moves: wall angel, dead bug, side-lying leg lift, clamshell.

### 🎯 Muscle ID view
Choose a muscle (tap it, or pick it from the full list) and the body shows it clearly:
- The muscle glows pink. Unrelated muscles fade.
- Green and blue dots show where it starts and where it attaches.
- Tags with lines show its **helpers**, **opposers** and **steadiers**.
- The label shows what the muscle does **now** (shortening, lengthening, holding, stretching or resting).
- "How it works" buttons (Shorten, Lengthen under load, Hold, Stretch, Rest) play a short demo of each way it works, with an example.

### 🦶 Feet close-up
When foot position matters (squats, ski stance, jumps, running, foot work, or captions about the feet), a small front view of the feet opens. It shows:
- the foot tripod (heel, big toe, little toe)
- the arch
- whether the knee tracks over the 2nd toe
- where the weight falls

Use the 🦶 Feet button to set it to auto, on or off.

### ◎ Modes and Simple view
A mode picker opens at the start: Train a muscle, Activities, Yoga, Bath yoga, Mudras, Breath and channels, Musician relief, Tai chi and qigong, Animal mode.
- **Simple view** (default) hides the lab panels (zoom, gravity data, layers).
- **Full lab** shows everything.
- Reopen the picker any time with ◎ Modes.

### 🙏 Mudras
16 hand seals (Gyan, Prana, Apana, Prithvi, Shuni, Varuna, Vayu, Shunya, Surya, Heart, Vishnu, Adi, Abhaya, Anjali, Hakini, Dhyana). Each one has:
- a hand close-up that forms the seal, with element colors on the fingers
- the hand muscles that hold the seal
- breath-paced holds

The meanings shown are traditional, not medical claims.

### 🔆 Front and rear channels
Shows the Daoist microcosmic orbit on the body:
- The rear channel (Governing Vessel) rises up the spine on the inhale.
- The front channel (Conception Vessel) descends down the front on the exhale.

A meter shows whether the front body or the back body is lengthening.

### 🎸 Musician relief (guitar)
- Right-handed playing, tense vs balanced: the strumming shoulder lifts, the fretting shoulder rolls in, the head turns, and the fretting hand squeezes too hard.
- A left–right balance meter.
- 10 relief moves, including the least-pressure ladder and thumb-to-finger taps.

### Easier viewing
- The camera keeps the whole body (head to feet) in view.
- A head-and-neck side close-up opens for neck work.
- The left panel shows **Now playing**: the current move, the muscles it works and steadies, and its steps.

### ⚖ Front and back power
Trains the back line and the front line for 4 jobs:
- **Back line** (calves, hamstrings, glutes, erectors): drives you forward and holds you upright.
- **Front line** (shin, quads, hip flexors, abs): pulls the leg through, braces the trunk and brakes.

The 4 jobs:
- 🪑 sit tall
- 🧍 stand up and sit down
- 🏃 move forward with power
- ↩ move backward and brake

Each job has 4 stages: 🌱 Wake → 🌿 Control → 🔥 Strength → ⚡ Power.
- 12 new moves: seated rock, bird dog, hip hinge, hip swing, calf raise, toe lift, hollow hold, plank, knee drive, sit to stand, reverse lunge, wall drive.
- Back-line muscles have a gold edge and front-line muscles a blue edge.
- A live meter shows which line does the work.
- Share a program with `#fb-<sit|stand|fwd|back>-<1-4>`.
