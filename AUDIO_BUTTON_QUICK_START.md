# Audio Button: Quick Start Guide

🎙️ **The Cadillac File now has audio narration placeholders.**

---

## WHAT YOU'LL SEE

When you open `cadillac_file_expanded.html` and scroll to **Chapter 9: The Regulatory Collapse**, you'll see:

```
Audio narration available:  [▶ PLAY]
```

Click the button. It will either:
1. **Play audio** (if narration .mp3 has been linked)
2. **Show a production status message** (if the file hasn't been added yet)

---

## WHAT TO DO NOW

### If You Want to Listen Right Away
The audio button is ready but **no .mp3 files are linked yet**. Clicking it will show:
```
🎙️ Audio narration in production

Chapter 09 will be available as an .mp3 file or via hosted audio URL.
```

### If You Want to Add Narration

**Three easy steps:**

1. **Record or commission narration** for Chapter 9 (estimate 4–5 minutes)
   - Read the Chapter 9 text aloud
   - Export as .mp3 (high quality recommended: 192 kbps, 44.1 kHz)
   
2. **Upload to hosting** (any of these work):
   - AWS S3
   - Google Cloud Storage
   - Bunny CDN
   - Your own web server
   - Get a public URL that ends in `.mp3`

3. **Insert the URL into the HTML**
   - Open `cadillac_file_expanded.html` in a text editor
   - Find: `<audio id="audio-chapter-09">`
   - Add this line inside the `<audio>` tag:
   ```html
   <source src="https://your-domain.com/cadillac-ch09.mp3" type="audio/mpeg">
   ```
   - Save the file
   - Reload in browser
   - Click ▶ PLAY — it should now play your audio

---

## EXAMPLE HTML (Before and After)

**Before (production-ready, no audio linked):**
```html
<audio id="audio-chapter-09">
  <!-- No source yet -->
</audio>
```

**After (with .mp3 URL inserted):**
```html
<audio id="audio-chapter-09">
  <source src="https://cadillac-investigation.s3.amazonaws.com/ch09.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>
```

---

## FULL PRODUCTION WORKFLOW

Want to do all 10 chapters? See: `/mnt/user-data/outputs/VOICE_OVER_PRODUCTION_READY.md`

That document covers:
- Script outlines for each chapter
- Narrator tone & pacing
- Full production timeline
- Video documentary path (optional)

---

## BROWSER COMPATIBILITY

The audio player works in all modern browsers:
- ✅ Chrome / Edge (Windows & Mac)
- ✅ Firefox (Windows, Mac, Linux)
- ✅ Safari (Mac & iOS)
- ✅ Chrome Mobile (Android)

Audio will either stream or download depending on your server configuration.

---

## TESTING THE BUTTON

1. Open `cadillac_file_expanded.html` in your browser
2. Scroll down through the chapters using navigation buttons or arrow buttons
3. When you reach **Chapter 9**, you'll see the play button
4. Click ▶ PLAY
5. If no audio is linked, you'll see the production status
6. Once audio .mp3 is added, click ▶ PLAY to hear narration

---

## TECHNICAL DETAILS (For Developers)

The audio system uses:
- HTML5 `<audio>` element (standard browser API)
- JavaScript `playAudio()` function for button interaction
- CORS-enabled hosting (required for web playback)
- .mp3 codec (widely supported)

No external libraries required. Works offline after files are cached.

---

## HELP & TROUBLESHOOTING

**"Click ▶ PLAY but nothing happens"**
→ The .mp3 file URL hasn't been added yet. Follow the "Add Narration" steps above.

**"Audio plays in one browser but not another"**
→ Check that your hosting allows CORS headers. Most CDNs (AWS S3, Bunny, Cloudflare) handle this automatically.

**"I recorded narration but the file is too large"**
→ Compress to .mp3 format at 128–192 kbps. Most audio editors can do this. Aim for <50 MB per chapter.

**"I want to use a different format (WAV, FLAC, etc.)"**
→ Possible but .mp3 is most compatible. If you prefer another format, let me know and I can update the HTML.

---

## NEXT STEPS

- [ ] Record Chapter 9 narration (or all 10 chapters)
- [ ] Upload .mp3 to hosting
- [ ] Paste URL into HTML audio tag
- [ ] Test play button
- [ ] Ready to present to Bill / media / EGLE

---

**Questions?** Check `/mnt/user-data/outputs/VOICE_OVER_PRODUCTION_READY.md` for the full production guide.

---

*Audio Infrastructure Ready | September 4, 2026*
