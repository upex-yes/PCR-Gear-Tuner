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
