# The Cadillac File — Voice-Over Production Ready

**Status:** September 4, 2026 | 10 Chapters + Epilogue | Interactive HTML with Audio Placeholders

---

## WHAT'S READY

✅ **Chapter 9 (NEW):** "The Regulatory Collapse" — Eight EGLE violations, local-limits mechanism, May 22 NOV context, Cadillac Casting documented, Four Winns timeline boxed.

✅ **Audio Player Buttons:** Placed in each chapter that needs narration (currently: Ch 9). Click ▶ PLAY to trigger audio.

✅ **Audio Placeholder System:** JavaScript detects when `<audio>` element has `.src` file path; if empty, shows production status dialog.

✅ **Production Integration Points:** All audio elements are named and indexed:
- `audio-chapter-09` ← Chapter 9 narrator
- Ready for: `audio-chapter-00` through `audio-chapter-10` (prologue + 9 chapters + epilogue)

---

## PRODUCTION PATHS (Choose One)

### Path 1: Audio-Only Companion (1–2 weeks)
Record 10 MP3 files (roughly 3–5 min each, totaling ~40 min). Host on your server or CDN. Insert URLs into HTML:

```html
<audio id="audio-chapter-09">
  <source src="https://yourhost.com/cadillac-ch09.mp3" type="audio/mpeg">
</audio>
```

**Deliverable:** Interactive HTML + downloadable MP3 set.

---

### Path 2: Synced Web Player (3–4 weeks)
Same MP3 files + web player overlay with chapter sync, transcript, and timecode navigation.

**Deliverable:** Hosted interactive document with embedded audio player.

---

### Path 3: Video Documentary (6–12 weeks)
Use Chapter 9 + earlier chapters as screenplay. Pair narration with:
- Facility map flyovers (Chapter 6)
- DMR data visualizations  
- Facility photos (30 JPG images in `/mnt/user-data/uploads/`)
- News footage / public records

**Deliverable:** YouTube / Vimeo documentary + hosted interactive HTML reference.

---

## CHAPTER SCRIPT SKELETON (Ch 9 Example)

**Narrator:** "While the April and June 2026 cyanide spikes occurred, the City's Industrial Pretreatment Program was actively failing under state scrutiny. EGLE has been documenting those failures since 2020. By August 2026, eight separate violations had been formally issued."

[**READ** violation table on screen]

"The critical failure: local limits for toxic pollutants have not been formally submitted. They remain in draft as of August 2026, nearly six years after EPA's initial mandate."

[**PAUSE for visualization**]

"Cyanide doesn't move through a WWTP by accident. Local limits are the written enforceable rules that say: 'Facility X can discharge no more than Y micrograms per liter of cyanide into the sewer.' Without local limits, the City has no mechanism to tell an industrial user their discharge is over the line."

---

## HOW TO INTEGRATE AUDIO FILES

1. **Record or commission narration** (10 chapters, ~3–5 min each)
2. **Export as .mp3** (high quality: 192 kbps, 44.1 kHz)
3. **Upload to hosting** (your CDN, AWS S3, Bunny CDN, or similar)
4. **Get public URLs** (must allow CORS for web playback)
5. **Edit HTML:** Find each `<audio>` tag and add:
   ```html
   <audio id="audio-chapter-XX">
     <source src="[YOUR_URL_HERE]" type="audio/mpeg">
     Your browser does not support the audio element.
   </audio>
   ```
6. **Test:** Click ▶ PLAY button in browser. Audio should play or download.

---

## AUDIO SCRIPT OUTLINE (All 10 Chapters)

| Ch | Title | Est. Duration | Key Points |
|----|-------|---|-----------|
| 0 | Prologue: What This Is | 2–3 min | What the document covers; neutrality framing; public record sourcing |
| 1 | The Number | 3–4 min | April 2026 DMR spike: 125 µg/L vs 5.9 limit (21× exceedance) |
| 2 | The Silence | 3–4 min | Violation metadata fields blank on EPA ICIS (why spike didn't auto-flag) |
| 3 | The Control | 3–4 min | EPA ECHO compliance record: 11 quarters noncompliant, 0 formal enforcement actions |
| 4 | The Pattern | 2–3 min | Statewide '=' coding issue (22-permit test shows same pattern everywhere) |
| 5 | The Corridor | 3–4 min | Northernaire Superfund history (1971–1981 plating, cyanide in groundwater) |
| 6 | The Map | 2–3 min | Interactive geography; WWTP, outfall, Superfund sites, community context |
| 7 | The Open Door | 4–5 min | 19 permitted industrial users; supply-chain methodology; AAR, Rec Boat, Cadillac Castings detail |
| 8 | **NEW: Regulatory Collapse** | 4–5 min | **Eight EGLE violations; local-limits mechanism; May 22 NOV; Dietlin statement; timing overlap** |
| 9 | The Ledger (Epilogue) | 3–4 min | Proven facts vs. open questions; what FOIA will answer; investigation status |

**Total Runtime:** ~35–45 minutes

---

## PRODUCTION NOTES FOR NARRATOR

- **Tone:** Investigative documentary, neutral and deliberate (not sensational)
- **Audience:** Attorneys, regulators, media, engaged citizens
- **Technical Terms:** Define on first mention (e.g., "NPDES permit" = "National Pollutant Discharge Elimination System")
- **Numbers:** Emphasize exceedances and ratios clearly ("twenty-one times the legal limit")
- **Source Attribution:** Mention "according to EPA records" / "EGLE documented" to reinforce official sourcing
- **Pacing:** Slower than conversational; let facts breathe

---

## CURRENT HTML STATUS

✅ All chapters complete and rendered  
✅ Audio player buttons placed  
✅ Chapter navigation updated  
✅ Placeholder system ready  
⏳ Audio files not yet recorded/hosted

**Next Step:** Commission voice-over artist or use text-to-speech service (e.g., Google Cloud Text-to-Speech, ElevenLabs, Audible) to generate MP3s. Then insert URLs into `<audio src="">` fields.

---

## FILE MANIFEST

- `/mnt/user-data/outputs/cadillac_file_expanded.html` — **MASTER (audio-ready)**
- `/mnt/user-data/outputs/VOICE_OVER_PRODUCTION_READY.md` — This document
- `/mnt/user-data/uploads/` — 30 JPG photos ready for video documentary path

---

**Questions or edits?** Return here and update the script outline or add narration guidance.

---

*Attribution: The Cadillac File — An interactive public record investigation compiled by Bill Barnett, attorney, September 4, 2026. Production-ready version with audio scaffolding, September 4, 2026.*
