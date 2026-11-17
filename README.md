# Muscle Lab

A 3D muscle lab that runs in the browser. You watch about 60 muscles on each side work in slow motion, in 18 activities.

### ▶ [Open Muscle Lab](https://stevenwsharp-ctrl.github.io/muscle-lab/)

**Live site:** [stevenwsharp-ctrl.github.io/muscle-lab](https://stevenwsharp-ctrl.github.io/muscle-lab/)

## What it does

- **Activities:**
  - Arm raises, pull-up, push-up, squat
  - Running on asphalt, trail or track, jump rope, boxing
  - Skiing on groomers, moguls and powder, and ski jumping
  - Piloting a boat in rough seas
  - Daily life and work: desk life (sitting and typing) and nursing (bedside care)
- **Yoga mode:** 26 poses and a sun salutation, with Sanskrit names. Pick up to three focus areas (hips, hamstrings, shoulders, spine, core, legs, balance, neck, feet, calm, or the muscle you picked in the coach). The flow follows a class arc: arrive, warm up, sun salutation, standing poses, balance, backbend, seated poses, cool down and rest. One-sided poses play on the left side, then on the right side. Short flows are free; full flows are Pro. Share a flow with a link.
- **Breath option:** a breath circle and lungs and a diaphragm that move on the body. Paces: calm 4–6, even 5–5, box 4–4–4–4 and relax 4–7–8. In yoga, the breath follows the poses: inhale to lift or open, exhale to fold, twist or lower.
- **Share anything:** the 🔗 Share button copies a link to what you see now: an activity (`#act-desk`), its counter moves (`#counter-desk`), a muscle in the coach (`#muscle-soleus`), a plan, one exercise, a yoga flow or one yoga pose (`#pose-tree`).
- **Counter moves:** each activity has a "↺ Counter it" row. It plays moves that undo the load of that activity, for example a chest opener and a neck reset after desk life.
- **Both sides and all angles:** one-sided exercises play on the left side, then on the right side. The ↔↕ Sweep view swings the camera left-right and up-down.
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

## Notes

This is a teaching model, not medical advice. Joint loads are static gravity loads for a 70 kg body. Fascial chains follow Myers' Anatomy Trains, and the app shows the evidence level for each chain (Wilke et al. 2016).
