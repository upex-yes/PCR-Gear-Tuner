# PCR Gear Tuner

<img width="1312" height="885" alt="Screenshot from 2025-11-07 00-20-20" src="https://github.com/user-attachments/assets/96607994-2ade-4085-a061-a636f05447b0" />


A simple web-based tool for visualizing and creating custom gear tunes in *Pixel Car Racer* (PCR). Easily drag sliders to configure gear ratios, preview RPM drops, and export tunes—eliminating the trial-and-error frustration of traditional tuning.

[Try it here](https://upex-yes.github.io/PCR-Gear-Tuner/)

> **Note:** This tool is best used on a desktop or laptop. It's functional on mobile but not optimized. If there's demand, a mobile version could be developed.

## Why This Tool?
Tuning gears in PCR has always felt like a shot in the dark: endless tweaking, testing, and restarting when one change throws everything off. This tool simplifies it by letting you:
- Drag sliders to adjust ratios and instantly see RPMs after shifts, top speeds per gear, and more.
- Visualize your engine's power band to stay optimal.
- Export tunes as `.txt` files for easy reference.

I built this from an Excel spreadsheet prototype because I love PCR's tuning mechanics but hated the blind adjustments. The game might not have a huge active community anymore (though the subreddit seems somewhat lively), but if you're still playing, this should help.

## Getting Started
Before tuning, dyno your car in-game to get two key values:
- **Rev Limiter RPM**: The static RPM on the dyno when it settles.
- **Peak HP RPM**: Where your horsepower peaks.

### Input Setup
At the top of the page:
- Enter your **Rev Limiter RPM** into the "Shift RPM" box (RPM right before shifting).
- Set the "Target RPM" to your Peak HP RPM minus a few hundred RPM (tweak later; never exceed Peak HP RPM).
- Leave "Tire Diameter" as-is unless customizing MPH estimates.

## Section A: Auto-Progression Tuning
This is for quick, optimized tunes:
- Adjust the **1st Gear Ratio** and **Final Drive Ratio** sliders to hit your target trap speed in top gear.
- Other gears auto-adjust to keep you in the power band based on your Target RPM.
- Moving the 1st gear slider recalculates all ratios for ideal performance.

At the bottom:
- View top speeds per gear.
- See RPM drops and post-shift RPMs—no more guessing!

Use the **Export** button to save as `.txt`.

> **Tip:** Disable "Auto Progression" (top-right checkbox) to manually tweak like Section B.

## Section B: Custom Manual Tuning
For full control:
- Functions like Section A but without auto-adjustments.
- Purely informational: Adjust freely and preview speeds/RPMs.
- Great for refining a Section A tune—copy over and tweak.

## Fine-Tuning Target RPM
To avoid redlining before the finish:
- Lower Target RPM by 200-300 RPM increments if taching out early.
- Aim to just reach the line before redline—keeps you in the power band.
- Avoid tweaking Final Drive alone (makes 1st gear too tall); adjust ratios instead.
- **Reminder:** Target RPM must stay below Peak HP RPM.

## Feedback & Community
If PCR still has fans out there (dev seems to have abandoned it), share your tunes, suggestions, or improvements in the comments or issues. I've been away from the community for 7+ years but still play—tuning is the game's best feature!

Cheers! 🚗💨

# PCR Gear Tuner – Changelog

## [v2.0.0] – November 10, 2025
*Major Release – Multi-Game Support & Full Customization*

### Major Features
- **Compatibility Mode**  
  Adds 7th–10th gears, supports other racing games  
  Increases final drive max to `6.00`, RPM to `15,000`
- **Tire Diameter Calculator**  
  Enter RPM + speed + ratios → auto-calculate tire size  
  Apply with one click
- **Settings Panel**  
  Toggle MPH/KM/H, inches/cm  
  Customize colors, font, size, style

### Enhancements
- Dynamic unit labels (MPH ↔ KM/H, in ↔ cm)
- Smart gear enable/disable in Setup A
- Export includes units and proper gear suffixes
- Auto-progression respects disabled gears

### Code
- Modular gear system with `rebuildGears()`
- Full unit-aware physics engine
- Extended default ratios for 10 gears

---
