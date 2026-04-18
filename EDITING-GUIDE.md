# Lekker Land Website — Editing Guide

A plain-English guide to editing your own website. No coding knowledge required.

---

## How the website works

You have **4 main files**:

1. **`index.html`** — The landing page (language popup + choice between Preschool/Naskool)
2. **`preschool.html`** — The Preschool page
3. **`aftercare.html`** — The Naskool page
4. **`translations.js`** — All text on the site, in both English and Afrikaans

Plus folders:
- **`images/`** — All photos and logos

---

## The Golden Rule

**Almost all text changes happen in `translations.js`, NOT in the HTML files.**

This is because every piece of text has an English and Afrikaans version. The file keeps them paired up so they stay in sync.

---

## How to edit text (most common task)

### Step 1: Open GitHub and find translations.js

1. Go to https://github.com/Spvdwalt/lekkerland-website
2. Click on **`translations.js`**
3. Click the **pencil icon** (top right of the file) to edit

### Step 2: Find what you want to change

Each piece of text looks like this:

```
heroSubtitle: { en: "Quality early childhood education from 3 months to Grade R",
                af: "Kwaliteit vroeë kinderontwikkeling van 3 maande tot Graad R" },
```

- `en:` is the English version
- `af:` is the Afrikaans version
- Change ONLY the text **between the quote marks** `"..."`
- Keep the commas and brackets exactly as they are
- **Always change BOTH the English and Afrikaans**

### Step 3: Save

1. Scroll to the bottom of the page
2. Type a short description like "Updated hero subtitle"
3. Click **Commit changes**

Your live site updates within 1 minute.

---

## How to swap a photo placeholder with a real photo

Every "REPLACE ME" placeholder on the site can be swapped for a real photo.

### Step 1: Prepare your photo

- Use JPG or PNG format
- Resize it before uploading (the placeholder tells you the recommended size)
- Name it something clear like `playground.jpg`

### Step 2: Upload to GitHub

1. Go to https://github.com/Spvdwalt/lekkerland-website
2. Click the **`images`** folder
3. Click **Add file → Upload files**
4. Drag your photo in
5. Click **Commit changes**

### Step 3: Replace the placeholder in HTML

This is the only time you edit HTML files directly. Don't worry, it's simple.

Let's say you want to replace the "Playground photo" placeholder on the preschool page:

1. Open `preschool.html`
2. Click the pencil to edit
3. Press **Ctrl+F** (or Cmd+F on Mac) to search
4. Search for: `Playground photo`
5. You'll find a block like this:

```html
<div class="photo-placeholder">
  <span>📷</span>
  <strong>REPLACE ME</strong>
  <em>Playground photo</em>
</div>
```

6. Replace that entire block with:

```html
<img src="images/playground.jpg" alt="Lekker Land playground" class="content-photo">
```

(Change `playground.jpg` to whatever you named your file)

7. Click **Commit changes**

---

## How to change phone number, email, or address

These appear in all three HTML files (`index.html`, `preschool.html`, `aftercare.html`). You need to update each one.

1. Open the file
2. Press **Ctrl+F** to search for the old value (e.g. "+27 76 957 7959")
3. Change every occurrence
4. Save

Do this for all three HTML files.

---

## How to check your Afrikaans translations

The Afrikaans I wrote was done my best effort. Your wife should review them. To do that:

1. Open `translations.js`
2. Look for `af:` entries — those are Afrikaans
3. If any sound wrong, edit the text between the quote marks
4. Save

---

## Common edits cheat sheet

| What you want to change | File | Search for |
|---|---|---|
| Grade R price (R1500) | `translations.js` | `Lekker Lite` |
| Operating hours Preschool | `translations.js` | `hoursText` |
| Operating hours Naskool | `translations.js` | `hoursText` (in aftercare section) |
| Schools collected from | `aftercare.html` | `school-list` |
| Phone number | All HTML files | `+27 76 957 7959` |
| Email address | All HTML files | `admin@lekker-land.co.za` |
| Street address | All HTML files | `Billingham` |
| A testimonial | `translations.js` | `testimonials` |
| Food bullet points | `translations.js` | `food1`, `food2`, etc. |
| Value descriptions | `translations.js` | `valueIntegrityText` etc. |

---

## Things to ask Claude for help with

- Adding a new section
- Changing colours or fonts
- Adding a new page (e.g. pricing, events)
- Anything structural

Just start a new Claude conversation, paste the file you want to change, and describe what you want. Claude will give you the new version to paste back into GitHub.

---

## Emergency: I broke something!

GitHub keeps every version of every file. If you mess up:

1. Go to the file you broke
2. Click **History** (top right)
3. Find the version from before your mistake
4. Click the `...` menu → **View file at this point**
5. Copy that content and paste it back into the current version

Alternatively, just ask Claude to fix it.

---

## Rules that never change

1. **Always keep the quote marks `"..."` around text.** Never delete them.
2. **Always update both `en:` and `af:`** when changing text.
3. **Don't touch anything in `translations.js` below the line that says "DO NOT EDIT BELOW THIS LINE"**. That's the language-switching code.
4. **Test on mobile too.** Most parents will view the site on their phone.
