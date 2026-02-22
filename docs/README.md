# SyncScript Pro

**SyncScript Pro** allows you to synchronise Script Keywords with transcribed Captions and generate `FCPXML` Titles for Final Cut Pro.

> [:icon-desktop-download: Click here to **buy** on the **Mac App Store**](/buy/)

---

## Features

### Page 1: Script Parsing
- Parse screenplay/script files (PDF, TXT)
- Extract dialogue keywords with character names
- Support for scene numbers and take information

### Page 2: Autosequence Generation
- Import FCPXML from Final Cut Pro browser
- Generate autosequence timeline from clips
- Audio export for transcription

### Page 3: Transcription
- Transcribe audio using **Parakeet** (v2/v3) or **Apple Speech Pro** (macOS 26+)
- Speaker diarization support
- Generate captions with precise timing

### Page 4: Caption Matching
- Match script keywords to transcribed captions
- Semantic matching using embeddings
- Import FCPXML timeline with captions

### Page 5: Titles to FCP
- Generate titles for matched keywords
- Speaker-specific roles for color coding
- Trigger phrase support (start/end triggers)
- Make "Action-Cut" ranges
- Export to Final Cut Pro

### Page 6: Keywords to FCP
- **Titles to Keywords** - Convert timeline titles to keywords on browser clips (based on CommandPost's approach)
- Convert matched titles back to keywords on the original source clips

---

## Titles to Keywords Feature

Based on CommandPost's **Titles to Keywords** toolbox, this feature:

1. Finds all titles on the timeline with their absolute positions
2. Finds clips in the spine with their timing information
3. Checks which titles intersect with which clips
4. Converts timeline positions to source clip internal timecodes
5. Adds `<keyword>` elements to clips in the EVENT (browser), not the timeline

---

## FCP Event Naming

The app creates consistently named events when exporting to Final Cut Pro:

- **02 Auto Sequence** - Generated autosequence timeline
- **03 Transcribe Captions** - Transcribed captions
- **05 Titles** - Generated titles for matched keywords
- **06 Keywords** - Keywords applied to browser clips

---

## FCPXML Support

- Supports FCPXML versions up to **1.14**
- Uses local FCPXMLKit package for parsing and validation
