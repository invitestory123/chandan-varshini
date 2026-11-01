# Editing Guide — Lantern Madurai

Fast customer customization guide for `lantern-madurai` (Madurai lanterns & temple theme with GSAP parallax and intro video).

## Primary Customer Data

All text, dates, events, venue, scratch-card info, and media paths live in:
- `editable/wedding-data.js`

### What to edit in `editable/wedding-data.js`:
- **Couple Details**:
  - `couple.groom`: Groom's name (e.g. `"Aarav"`)
  - `couple.bride`: Bride's name (e.g. `"Ananya"`)
  - `couple.dateDisplay`: Date formatted text (e.g. `"14 · 02 · 2027"`)
  - `couple.city`: City & state (e.g. `"Madurai, Tamil Nadu"`)
- **Countdown**:
  - `countdown.targetISO`: Target ISO date string (e.g. `"2027-02-14T07:30:00+05:30"`)
- **Scratch-to-reveal Date Card**:
  - `scratchCard.day`: Day of week (e.g. `"Sunday"`)
  - `scratchCard.date`: Day number (e.g. `"14"`)
  - `scratchCard.monthYear`: Month and year (e.g. `"February · 2027"`)
  - `scratchCard.city`: Location (e.g. `"Madurai"`)
- **Story & Pre-Wedding Moment**:
  - `story.title`, `story.text`: Story heading and paragraph
  - `ceremonyMoment.captionTitle`, `ceremonyMoment.captionText`: Haldi/Mehendi caption
- **Events**:
  - `events[]`: Array of events with `name`, `date`, `time`, `venue`, `note`, `icon`
- **Venue**:
  - `venue.title`, `venue.address`, `venue.mapQuery`
- **Gallery**:
  - `gallery[]`: Array of photo objects with `src`, `caption`, `alt`
- **Footer**:
  - `footer.dateLine`: Footer date string (e.g. `"14 February 2027 · Madurai"`)
- **Assets**:
  - `assets.video`: Intro MP4 path
  - `assets.videoPoster`: First frame image
  - `assets.heroArt`: Hero illustration
  - `assets.ceremonyImage`: Ceremony photo
  - `assets.footerImage`: Footer art / OG image
  - `assets.bgMusic`: Background music MP3 path

## Replacing Assets

Place customer replacement files in `editable/assets/`:
- `editable/assets/aarav-ananya-opening.mp4` — Opening video gate
- `editable/assets/entrance-first-frame.png` — First frame poster for video
- `editable/assets/invitation-reference.png` — Hero illustrated scene
- `editable/assets/haldi-mehendi.png` — Ceremony photo
- `editable/assets/og-aarav-ananya.png` — Footer art & social share image
- `editable/assets/bg-music.mp3` — Background soundtrack
- `editable/assets/gallery-1.jpg` to `gallery-5.jpg` — Wedding photoshoot gallery photos

## Testing

```bash
node --check editable/wedding-data.js
```
Open `http://localhost:9014/` in browser.
